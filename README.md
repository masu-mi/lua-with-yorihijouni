add events(:ls, rs) to Lua
===========================

sample code

```lua
x = {5}
function test_ls(a, b)
  print("in test_ls function")
  print(a)
  print(b)
  return a[1] < b[1]
end
setmetatable(x, {__ls = test_ls})

print (x << {1})
-- false
print (x << {10})
-- true
```
