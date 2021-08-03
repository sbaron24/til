

## Scope
Add a method to a class instance like this:

```
greeting = 'hello'

def greeting.broaden
  self + ', world!'
end

greeting.broaden # returns "Hello, world!"
```

This is a _singleton method_ since it's defined on just one object.

Add a method to a class like this:

```
def String.hello
  'Hello world!'
end
```

this is effectively the same as:

```
class String
  def self.my_method
    # ...
  end
end
```

since `self` refers to the "current object under construction by the compiler"

## Overriding

If a method already exists, it is not considered an error.  The method overrides any previous definition:

```
"43".to_i # returns 43

class String
  def to_i
    123
  end
end

"43".to_i # returns 123
```

## Default Values

Default arguments to a method must be grouped together, otherwise a Syntax Error is raised:

```
def my_method(a=1, b, c=3) # raises SyntaxError
```