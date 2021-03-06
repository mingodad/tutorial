# Classes as Record Types

Sometimes you just need to group a few values together.
This is called a "record" in Pascal,
and a "struct" in C.
You can use Pike's **class** mechanism for this too.
Just create a class with the data you are interested in:

```pike
class customer
{
  int number;
  string name;
  array(string) phone_numbers;
}
```

Then use it:

```pike
array(customer) all_customers = ({ });
customer c = customer();
c->number = 18;
c->name = "Ellen Ripley";
c->phone_numbers = ({ "555-8767", "555-4001" });
all_customers += ({ c });
```
