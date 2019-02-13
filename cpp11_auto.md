# auto

A fordító (compiler) a változó inicializálásából kitalálja a változó típusát.

```cpp
auto a = 3.14; // double
auto b = 1; // int
auto& c = b; // int&
auto d = { 0 }; // std::initializer_list<int>
auto g = new auto(123); // int*
const auto h = 1; // const int
auto i = 1, j = 2, k = 3; // int, int, int
```

Iniciaizálás nélkül nem működik, hiszen nem tudja kitalálni automatikusan a típust, ha nincs változó.

```cpp
auto l = 1, m = true, n = 1.61; // error -- `l` deduced to be int, `m` is bool
auto o; // error -- `o` requires initializer
```

Bonyolult típusoknál segíti a kódolást:

```cpp
std::vector<int> v = ...;
std::vector<int>::const_iterator cit = v.cbegin();
// vs.
auto cit = v.cbegin();
```
