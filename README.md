# HttpPostSerializer

## Installation

Install as [NuGet package](https://www.nuget.org/packages/HttpPostSerializer/):

```powershell
Install-Package HttpPostSerializer
```

.NET CLI:

```shell
dotnet add package HttpPostSerializer
```

## Basic Usage
```C#
class POCO {
  [HttpProperty("id")]
  public int Id { get; set; }
  
  [HttpProperty("firstname")]
  public string FirstName { get; set; }
    
  [HttpProperty("lastname")]
  public string lastName { get; set; }
}

static void Main(string[] args) {
  var poco = new POCO() {
    Id = 1,
    FirstName = "John",
    LatName = "Doe"
  };
  
  FormUrlEncodedContent content = HttpPostConverter.SerializeObject(poco);
}
```
