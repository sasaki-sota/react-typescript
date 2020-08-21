# TypeScript + Reactについて

## React.FC
関数コンポーネントの宣言

## void型
何も返さないという意味

## any型
なんでもいいという意味
**基本的にあまり使わない**  
`const hoge = (a: number, b: boolean) : number => {`というふうになる  
**ab仮引数**であり**そのあとの型は返り値で欲しい型**

## array型
配列の型  
##### 文字列の配列が欲しい場合
`const aa: string[] = ["aa", "b"]`と後ろに大括弧をつけるだけ  

## object
オブジェクトの型を作るとき -> **Interfaceを使用する**  
	interface Hoge {
	a: number,
	b: number,
	...
	}
↓
`let v: Hoge = {a: 10, b: 20}`となる
**interfaceは多用する**

## undefined 
入ってくるかもしれない時に使う  
interfaceの部分のb: number -> b?: numberと**?を記述することが必要になる**

## null 
何もないかもしれない時に使う
interfaceの部分のb: number -> b: number | null と**nullを記述することが必要になる**  
### undefinedはキーがなくてもいいがnullは必要

## 分割代入
`const { message } = props;` -> このように書くことによって**オブジェクトのメッセージのみを取り出せる**  

