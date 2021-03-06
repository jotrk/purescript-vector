## Module Data.Vector

#### `Vec`

``` purescript
newtype Vec s a
  = Vec (Array a)
```

##### Instances
``` purescript
instance eqVec :: (Eq a) => Eq (Vec s a)
instance showVec :: (Show a) => Show (Vec s a)
instance functorVec :: Functor (Vec s)
instance applyVec :: Apply (Vec s)
instance foldableVector :: Foldable (Vec s)
instance semiringVector :: (Sized s) => Semiring (Vec s Number)
```

#### `fill`

``` purescript
fill :: forall s a. (Num a, Sized s) => a -> Vec s a
```

#### `fromArray`

``` purescript
fromArray :: forall s a. (Sized s) => Array a -> Vec s a
```

#### `toArray`

``` purescript
toArray :: forall s a. Vec s a -> Array a
```

#### `vAdd`

``` purescript
vAdd :: forall a s. (Num a) => Vec s a -> Vec s a -> Vec s a
```

#### `vSub`

``` purescript
vSub :: forall a s. (Num a) => Vec s a -> Vec s a -> Vec s a
```

#### `vMul`

``` purescript
vMul :: forall a s. (Num a) => Vec s a -> Vec s a -> Vec s a
```

#### `vNegate`

``` purescript
vNegate :: forall a s. (Num a) => Vec s a -> Vec s a
```

#### `direction`

``` purescript
direction :: forall s. Vec s Number -> Vec s Number -> Vec s Number
```

The normalized direction from a to b: (a - b) / |a - b|

#### `vlengthSquared`

``` purescript
vlengthSquared :: forall s. Vec s Number -> Number
```

The length of the given vector: |a|

#### `vlength`

``` purescript
vlength :: forall s. Vec s Number -> Number
```

The length of the given vector: |a|

#### `normalize`

``` purescript
normalize :: forall s. Vec s Number -> Vec s Number
```

#### `distanceSquared`

``` purescript
distanceSquared :: forall s. Vec s Number -> Vec s Number -> Number
```

The distance between two vectors.

#### `distance`

``` purescript
distance :: forall s. Vec s Number -> Vec s Number -> Number
```

The distance between two vectors.

#### `scale`

``` purescript
scale :: forall a s. (Num a) => a -> Vec s a -> Vec s a
```

Multiply the vector by a scalar: s * v

#### `dot`

``` purescript
dot :: forall s. Vec s Number -> Vec s Number -> Number
```

The dot product of a and b


