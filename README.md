# unityProject

## Coding Style

### 1.1 變數命名
- 全域變數: PascalCase 第一個字母要大寫
- 區域變數: camelCase 第一個字母小寫
- 成員變數: _CamelCase 小寫字母前加底線
```
public void Foo()
{
  public string PublicName = "James"; 
}
```
```
public void Foo()
{
  private string privateName = "Joe";
}
```
```
public class Foo
{
  private string _memberName = "Owen";
}
```

### 1.2 變數修飾子
- 全域: 一定要加 public
- 私有: 一定要加 private

### 1.3 封裝變數
```
public class Foo
{
  
   private int bar;
 
   public int Bar
   {
     get { return bar; }
     set { bar = value; }
   }
 
}
```
```
public class Foo
{
   private int bar;
   
   public int Bar { get { return bar; } set { bar = value; } }
}
```

### 1.4 變數排列
請依照以下順序

1. static public
2. static private
3. public
4. private

```
public class NicCage
{
    //static public
    static public Vector3 point1 = Vector3.zero;
    static public Vector3 point2 = Vector3.zero;

    //static private
    static private float Thickness = 1f;
    static private float ScaleMod = .95f;

    //public
    public float OffsetMod = .01f;
    public bool DecayTrigger = false;

    //private
    private Vector3 offset;
    private Vector3 lastP1;
    private Vector3 lastP2;
    private GameObject texture;
    private bool decay = false;
    private float decayDrop = 1f;
    
}
```

### 2 class與function命名
- 方法: PascalCase 第一個字母要大寫
- class: PascalCase 第一個字母要大寫
```
public void AddThisFunction()
{
}
```
```
public class NicCage
{
  public void SlapTheGuyNotFollowingCodingStandards()
  {
    //I'll show you a SOLID design principle
  }
}
```

### 3 區塊
- 大括號在 if(判斷式) 的下一行
```
public void AddThisFunction()
{
  public class NicCage
  {
    // some code
  }
}
```

### 4 縮排
```
switch (someExpression) 
{
   case 0:
      DoSomething();
      break;
 
   case 1:
      DoSomethingElse();
      break;
 
   case 2: 
      {
         int n = 1;
         DoAnotherThing(n);
      }
      break;
}
```

### 5 空格
- 逗號後方一定要空一格
- 小括號後方不用空格
- function後方小括號不用空格
- 中括號不用空格
- 運算子前後要空格
```
// 正確
Console.In.Read(myChar, 0, 1);

// 錯誤
Console.In.Read(myChar,0,1);
```
```
// 正確
CreateFoo(myChar, 0, 1);

// 錯誤
CreateFoo( myChar, 0, 1 );
```
```
// 正確
CreateFoo();

// 錯誤
CreateFoo ();
```
```
// 正確
x = dataArray[index];

// 錯誤
x = dataArray[ index ];
```
```
// 正確
while (x == y)

// 錯誤
while(x==y)
```
```
// 正確
if (x == y)

// 錯誤
if (x==y)
```

### 6 註解
- 註解盡量放在function前方
```
// This is required for Controller access for hit detection
FPSController controller = hit.GetComponent<FPSController>();
 
 
// Creare a new ray against the ground
//
Ray ray = new Ray(hit.transform.position, -Vector3.up);
```

參考

1. https://github.com/Hitcents/unity3d-standards/blob/master/coding.md
2. http://wiki.unity3d.com/index.php/Csharp_Coding_Guidelines
3. http://programmers.stackexchange.com/questions/209532/name-convention-for-variables-in-c

Markdown Cheatsheet

1. https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
2. https://help.github.com/articles/basic-writing-and-formatting-syntax/
