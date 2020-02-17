# 字面量 Literals

Crystal提供了一些字面量用于创建某些基本类型的值。

| Literal                                                     | Sample values                                           |
| ----------------------------------------------------------- | ------------------------------------------------------- |
| [空值（Nil）](./literals/nil.html)                          | `nil`                                                   |
| [布尔值（Bool）](./literals/bool.html)                      | `true`, `false`                                         |
| [整数（Integers）](./literals/integers.html)                | `18`, `-12`, `19_i64`, `14_u32`,`64_u8`                 |
| [浮点数（Floats）](./literals/floats.html)                  | `1.0`, `1.0_f32`, `1e10`, `-0.5`                        |
| [字符型（Char）](./literals/char.html)                      | `'a'`, `'\n'`, `'あ'`                                   |
| [字符串（String）](./literals/string.html)                  | `"foo\tbar"`, `%("あ")`, `%q(foo #{foo})`               |
| [符号（Symbol）](./literals/symbol.html)                    | `:symbol`, `:"foo bar"`                                 |
| [数组（Array）](./literals/array.html)                      | `[1, 2, 3]`, `[1, 2, 3] of Int32`, `%w(one two three)`  |
| [Array-like](./literals/array.html#array-like-type-literal) | `Set{1, 2, 3}`                                          |
| [哈希表（Hash）](./literals/hash.html)                      | `{"foo" => 2}`, `{} of String => Int32`                 |
| [Hash-like](./literals/hash.html#hash-like-type-literal)    | `MyType{"foo" => "bar"}`                                |
| [范围（Range）](./literals/range.html)                      | `1..9`, `1...10`, `0..var`                              |
| [正则表达式（Regex）](./literals/regex.html)                | `/(foo)?bar/`, `/foo #{foo}/imx`, `%r(foo/)`            |
| [元组（Tuple）](./literals/tuple.html)                      | `{1, "hello", 'x'}`                                     |
| [命名元组（NamedTuple）](./literals/named_tuple.html)       | `{name: "Crystal", year: 2011}`, `{"this is a key": 1}` |
| [指针（Proc）](./literals/proc.html)                        | `->(x : Int32, y : Int32) { x + y }`                    |
| [shell命令（Command）](./literals/command.html)             | `` `echo foo` ``, `%x(echo foo)`                        |

