---
description: Ein Qualifizierer ist ein Tag, das weitere Informationen zu einem WMI-Objekt, einer -Methode oder einer -Eigenschaft bereitstellt.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Zugreifen auf einen WMI-Qualifizierer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45601de8e7b3f8ef7054742812c24f9a81dcedf5417f7b7ba501f2471adedc58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820618"
---
# <a name="accessing-a-wmi-qualifier"></a>Zugreifen auf einen WMI-Qualifizierer

Ein Qualifizierer ist ein Tag, das weitere Informationen zu einem WMI-Objekt, einer -Methode oder einer -Eigenschaft bereitstellt. Manchmal müssen Sie möglicherweise auf die in einem Qualifizierer gespeicherten Daten zugreifen. Eine häufige Aufgabe besteht beispielsweise darin, zu bestimmen, ob ein Anbieter eine Methode implementiert, indem versucht wird, den **Implementierten** Qualifizierer für diese Methode abzurufen. Weitere Informationen finden Sie unter [WMI-Qualifizierer](wmi-qualifiers.md) und [Hinzufügen eines Qualifizierers.](adding-a-qualifier.md)

Sie können die Qualifizierer für ein WMI-Objekt in PowerShell abrufen, indem Sie zuerst das -Objekt abrufen und dann die Qualifizierer wie jede andere Eigenschaft untersuchen.

**So rufen Sie einen Qualifizierer mithilfe von PowerShell ab**

-   Rufen Sie das Objekt ab, dessen Qualifizierer Sie mit [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx)anzeigen möchten, und greifen Sie dann über die Qualifiers-Eigenschaft auf die **Qualifizierer** zu:

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz.](retrieving-an-instance.md)

Sie können die Qualifizierer für eine WMI-Instanz in C# abrufen, indem Sie zuerst das -Objekt abrufen und dann die Qualifizierer als Auflistung untersuchen.

**So rufen Sie einen Qualifizierer mit C# (Microsoft.System ab. Verwaltung)**

1.  Rufen Sie die Klasse ab, deren Qualifizierer Sie anzeigen möchten, indem Sie unter Verwendung des angegebenen Klassennamens und Namespaces ein CimInstance-Objekt erstellen.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz.](retrieving-an-instance.md)

2.  Sie können die Klassenqualifizierer aus [CimInstance.CimClass.CimClassQualifiers,](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85))die Eigenschaftsqualifizierer aus [CimInstance.CimClass.CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))und die Methodenqualifizierer aus [CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85))abrufen.

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz.](retrieving-an-instance.md)

Sie können die Qualifizierer für ein WMI-Objekt in C# abrufen, indem Sie zuerst das -Objekt abrufen und dann die Qualifizierer als Auflistung untersuchen.

> [!Note]  
> **System.Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch im Allgemeinen langsamer und werden nicht so gut skaliert, relativ zu ihren moderneren **Microsoft.Management.Infrastructure-Entsprechungen.**

 

**So rufen Sie einen Qualifizierer mit C# ab (System.Management)**

1.  Rufen Sie das Objekt ab, dessen Qualifizierer Sie mit [ManagementObject](/dotnet/api/system.management.managementobject)anzeigen möchten.

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz.](retrieving-an-instance.md)

2.  Platzieren Sie die Qualifizierer in eine [QualifierDataCollection,](/dotnet/api/system.management.qualifierdatacollection)und durchlaufen Sie die [QualifierData-Werte.](/dotnet/api/system.management.qualifierdata)

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz.](retrieving-an-instance.md)

Im folgenden Verfahren wird beschrieben, wie Sie einen Qualifizierer mit VBScript abrufen.

**So rufen Sie einen Qualifizierer mit VBScript ab**

1.  Rufen Sie das Objekt ab, dessen Qualifizierer Sie anzeigen möchten, wie im folgenden Beispiel gezeigt:

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    Die gängigste Methode zum Abrufen eines Objekts ist die Verwendung der [**GetObject-Methode.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz.](retrieving-an-instance.md)

2.  Greifen Sie wie im folgenden Beispiel gezeigt über die [**\_ SWbemObject.Qualifiers-Eigenschaft**](swbemobject-qualifiers-.md) auf die Qualifizierer des Objekts zu:

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

Im folgenden Codebeispiel wird beschrieben, wie auf alle Qualifizierer für ein [**Win32 \_ Process-Objekt**](/windows/desktop/CIMWin32Prov/win32-process) zugegriffen wird.


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



Im folgenden Verfahren wird beschrieben, wie Sie einen Qualifizierer mit C++ abrufen.

**So rufen Sie einen Qualifizierer mit C++ ab**

1.  Rufen Sie das Objekt ab, dessen Qualifizierer Sie anzeigen möchten.

    Die gängigste Methode zum Abrufen eines Objekts ist die Verwendung eines Aufrufs von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) Weitere Informationen finden Sie unter [Abrufen der WMI-Klasse oder Instanzdaten.](retrieving-class-or-instance-data.md)

2.  Rufen Sie den Qualifizierersatz für eine bestimmte Eigenschaft mit einem Aufruf der [**Methoden IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) oder [**IWbemClassObject::GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) ab.

3.  Greifen Sie über die zurückgegebene [**IWbemQualifierSet-Schnittstelle**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) auf die Qualifizierer des Objekts zu.

## <a name="examples"></a>Beispiele

Weitere Informationen zum Abrufen von Qualifizierern finden Sie im [PowerShell-Codebeispiel Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) im TechNet-Katalog.

 

 
