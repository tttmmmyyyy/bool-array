# BoolArray

Defined in bool-array@0.2.0

## Values

### namespace BoolArray::BoolArray

#### @

Type: `Std::I64 -> BoolArray::BoolArray -> Std::Bool`

Gets the element at the specified index.

##### Parameters

- `index` : The index of the element to get. If out of range, the program aborts.
- `self` : The target BoolArray

#### @size

Type: `BoolArray::BoolArray -> Std::I64`

Gets the number of elements of the BoolArray.

##### Parameters

- `self` : The target BoolArray

#### fill

Type: `Std::I64 -> Std::Bool -> BoolArray::BoolArray`

Creates a BoolArray of the specified size, every element of which is the specified value.

##### Parameters

- `size` : The number of elements. If negative, the program aborts.
- `value` : The value of every element

#### set

Type: `Std::I64 -> Std::Bool -> BoolArray::BoolArray -> BoolArray::BoolArray`

Sets the element at the specified index.

##### Parameters

- `index` : The index of the element to set. If out of range, the program aborts.
- `value` : The value to set
- `self` : The target BoolArray

## Types and aliases

### namespace BoolArray

#### BoolArray

Defined as: `type BoolArray = unbox struct { ...fields... }`

BoolArray is a structure that represents a sequence of boolean values, storing each value in 1 bit.

`BoolArray` implements `Indexable`, so an element can also be read and written by the index syntax.

##### Examples

```fix
let bits = BoolArray::fill(100, false).set(3, true);
assert(|_|"", bits.@(3));;
assert(|_|"", !bits[3].imod(not).@(3));;
assert_eq(|_|"", bits.@size, 100)
```

## Traits and aliases

## Trait implementations

### impl `BoolArray::BoolArray : Std::Indexable`