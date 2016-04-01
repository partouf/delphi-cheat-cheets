# Freeing objects

* TObject.Free - Checks for nil and calls Destroy (and subsequently de-allocates the memory)
* FreeAndNil(ptr) - Calls TObject.Free and sets given pointer to nil in the caller's scope (in reversed order)

*Note: do not use with reference counted objects like TInterfacedObject*


#### References

Unit System

```
procedure TObject.Free;
begin
  if Self <> nil then
    Destroy;
end;
```

Unit System.SysUtils

```
procedure FreeAndNil(var Obj);
var
  Temp: TObject;
begin
  Temp := TObject(Obj);
  Pointer(Obj) := nil;
  Temp.Free;
end;
```
