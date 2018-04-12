# 设计模式-装饰者(结构)

## 释义
不改动原类结构情况下，对原类进行功能扩展。
![image](./pattern_decorator_uml.png)
## ruby实现

```ruby
class Person
  attr_accessor :first_name, :last_name

  def initialize(first_name, last_name)
    @first_name = first_name
    @last_name = last_name
  end
end

class PersonDecorator < SimpleDelegator
  def full_name
    "#{first_name} #{last_name}"
  end
end
```
![image](./pattern_decorator.png)
