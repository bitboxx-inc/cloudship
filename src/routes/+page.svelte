""<script lang="ts">
	import Button from '@smui/button';
	import Card, { Content as CardContent } from '@smui/card';

	let servers = 1;
	let databases = 1;
	let screens = 1;

	const computePrice = 5000;
	const databasePrice = 7500;
	const screenPrice = 500;

	const getTotal = () => {
		return (servers * computePrice) + (databases * databasePrice) + (screens * screenPrice);
	};
</script>

<div class="mt-10 mx-auto max-w-2xl text-center">
	<h1 class="text-5xl font-bold mb-8 text-gray-800">Cloudship</h1>
	<p class="text-lg mb-8 text-gray-600">
		シンプルで拡張性の高いクラウド管理を、驚くほど簡単に。
	</p>

	<div class="grid grid-cols-3 gap-6 mb-10">
		<div>
			<label class="block mb-2 text-gray-700 font-semibold">サーバー台数</label>
			<input type="number" bind:value={servers} min="1" class="px-4 py-2 border rounded-md text-center w-20">
		</div>
		<div>
			<label class="block mb-2 text-gray-700 font-semibold">DB台数</label>
			<input type="number" bind:value={databases} min="1" class="px-4 py-2 border rounded-md text-center w-20">
		</div>
		<div>
			<label class="block mb-2 text-gray-700 font-semibold">画面数</label>
			<input type="number" bind:value={screens} min="1" class="px-4 py-2 border rounded-md text-center w-20">
		</div>
	</div>

	<Card class="mb-10 p-6 border border-gray-200 rounded-lg shadow-lg">
		<CardContent class="mdc-typography--body2">
			<h2 class="text-2xl font-bold mb-4 text-gray-800">料金明細</h2>
			<div class="text-xl mb-2 text-gray-700">サーバー台数: {servers} × ¥5,000 = ¥{servers * computePrice}</div>
			<div class="text-xl mb-2 text-gray-700">DB台数: {databases} × ¥7,500 = ¥{databases * databasePrice}</div>
			<div class="text-xl mb-2 text-gray-700">画面数: {screens} × ¥500 = ¥{screens * screenPrice}</div>
			<hr class="my-4 border-gray-300"/>
			<div class="text-3xl font-bold text-gray-800">合計: ¥{getTotal()}</div>
		</CardContent>
	</Card>

<!--	<Button variant="raised" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 text-lg font-semibold">-->
<!--		決済に進む-->
<!--	</Button>-->

	<div class="mt-16 border-t pt-8 text-left max-w-2xl mx-auto">
		<h2 class="text-2xl font-bold mb-4 text-gray-800">特定商取引法に基づく表記</h2>
		<p class="mb-2 text-gray-700"><strong>販売業者:</strong> bitboxx Inc.</p>
		<p class="mb-2 text-gray-700"><strong>所在地:</strong> 東京都中央区日本橋箱崎町１６番１１ルミネ日本橋６０１</p>
		<p class="mb-2 text-gray-700"><strong>販売価格:</strong> 各プランに記載された価格に準じます。</p>
		<p class="mb-2 text-gray-700"><strong>お支払い方法:</strong> クレジットカード、Stripe決済</p>
		<p class="mb-2 text-gray-700"><strong>商品引き渡し時期:</strong> 決済完了後、約１か月程度でご利用可能。</p>
		<p class="mb-2 text-gray-700"><strong>返品・キャンセルについて:</strong> サービスの性質上、返品・キャンセルはできません。</p>
		<p class="mb-2 text-gray-700"><strong>不良品・破損時の対応:</strong> サービスに問題がある場合、サポートまでご連絡ください。</p>
	</div>
</div>

<style lang="postcss">
    :global(html) {
        background-color: theme(colors.gray.50);
    }
</style>""
