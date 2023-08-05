# TypeScript

//类型注解
let helloWorld: string = "Hello World";

let numArr = [1, 2, 3];
// 类型断言
const ret = numArr.find(item => item > 2) as number
console.log(ret * 5);

// 数组、元组、枚举等
let v1TS: 1 | 2 | 3 = 4;  // Error，必须是1/2/3之一
let arr = [1, 2, 3, 'a'];
let arrTS: number[] = [1, 2, 3, 'a'];  // Error，数据元素必须是number
let strTS: Array<string> = ['a', 'b', 'c', 4];  // Error，数据元素必须是string
let tuple1: [number, string, number] = [1, 'abc'];  // Error，元组必须包含3个数
let tuple2: [number, string, number?] = [1, 'abc'];

// 函数
function myFunc(a: number = 10, b: string, c: boolean, ...rest: number[]): number{
    return 100;
}
myFunc(5,'abc',true,1,2,3)

// 接口类型
interface Obj {
    name: string,
    age: number
}
const obj: Obj = {
    name: 'miros',
    age: 12
}

// 类型别名
type MyUsrName = number | string;
const myName: MyUsrName = 123;

// 泛型
function myFuncGene<T, G>(a: T, b: G): [T, G] {
    return [a, b];
}
myFuncGene<number, string>(12, '34');
