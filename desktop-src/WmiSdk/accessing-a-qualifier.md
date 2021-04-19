---
description: Ein Qualifizierer ist ein Tag, das weitere Informationen zu einem WMI-Objekt, einer Methode oder einer Eigenschaft bereitstellt.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Aufrufen eines WMI-Qualifizierers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352695"
---
# <a name="accessing-a-wmi-qualifier"></a>Aufrufen eines WMI-Qualifizierers

Ein Qualifizierer ist ein Tag, das weitere Informationen zu einem WMI-Objekt, einer Methode oder einer Eigenschaft bereitstellt. Manchmal müssen Sie möglicherweise auf die in einem Qualifizierer gespeicherten Daten zugreifen. Beispielsweise besteht eine häufige Aufgabe darin, zu bestimmen, ob ein Anbieter eine Methode implementiert, indem versucht wird, den **implementierten** Qualifizierer für diese Methode abzurufen. Weitere Informationen finden Sie unter [WMI-Qualifizierer](wmi-qualifiers.md) und [Hinzufügen eines Qualifizierers](adding-a-qualifier.md).

Sie können die Qualifizierer für ein WMI-Objekt in PowerShell abrufen, indem Sie zuerst das Objekt abrufen und dann die Qualifizierer wie jede andere Eigenschaft untersuchen.

**So rufen Sie einen Qualifizierer mithilfe von PowerShell ab**

-   Rufen Sie mit [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx)das Objekt ab, dessen Qualifizierer Sie anzeigen möchten, und greifen Sie dann über die **qualifizierereigenschaft** auf die Qualifizierer

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

    

    Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).

Sie können die Qualifizierer für eine WMI-Instanz in c# abrufen, indem Sie zuerst das Objekt abrufen und dann die Qualifizierer als Auflistung überprüfen.

**Zum Abrufen eines Qualifizierers mit c# (Microsoft.System. Personal**

1.  Rufen Sie die Klasse ab, deren Qualifizierer Sie anzeigen möchten, indem Sie ein ciminstance-Objekt mit dem angegebenen Klassennamen und Namespace erstellen.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).

2.  Sie können die Klassen Qualifizierer aus den Klassen " [ciminstance. cimclass. cimclassqualifizierer](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85))", den Eigenschaften [Qualifizierern aus "ciminstance. cimclass. cimclassproperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))" und den Methoden [Qualifizierern aus "ciminstance. cimclass. cimclassmethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85))" abrufen

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

    

    Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).

Sie können die Qualifizierer für ein WMI-Objekt in c# abrufen, indem Sie zuerst das Objekt abrufen und dann die Qualifizierer als Auflistung überprüfen.

> [!Note]  
> **System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.

 

**So rufen Sie einen Qualifizierer mit c# ab (System. Management)**

1.  Rufen Sie das Objekt, dessen Qualifizierer Sie anzeigen möchten, mithilfe von [ManagementObject](/dotnet/api/system.management.managementobject)ab.

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).

2.  Platzieren Sie die Qualifizierer in einem [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)-Element, und durchlaufen Sie die [QualifierData](/dotnet/api/system.management.qualifierdata) -Werte.

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).

Im folgenden Verfahren wird beschrieben, wie ein Qualifizierer mithilfe von VBScript abgerufen wird.

**So rufen Sie einen Qualifizierer mit VBScript ab**

1.  Rufen Sie das Objekt ab, dessen Qualifizierer Sie anzeigen möchten, wie im folgenden Beispiel gezeigt:

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    Die gängigste Methode zum Abrufen eines Objekts ist die Verwendung der [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode. Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).

2.  Greifen Sie über die Eigenschaft " [**errbemubject. Qualifizierer \_**](swbemobject-qualifiers-.md) " auf die Qualifizierer des Objekts zu, wie im folgenden Beispiel gezeigt:

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

Im folgenden Codebeispiel wird beschrieben, wie auf alle Qualifizierer eines [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Objekts zugegriffen wird.


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



Im folgenden Verfahren wird beschrieben, wie ein Qualifizierer mit C++ abgerufen wird.

**So rufen Sie einen Qualifizierer mit C++ ab**

1.  Rufen Sie das Objekt ab, dessen Qualifizierer Sie anzeigen möchten.

    Die gängigste Methode zum Abrufen eines Objekts ist das Aufrufen von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync). Weitere Informationen finden Sie unter [Abrufen von WMI-Klassen-oder Instanzdaten](retrieving-class-or-instance-data.md).

2.  Rufen Sie den Qualifizierer Satz für eine angegebene Eigenschaft mit einem Aufruf von [**IWbemClassObject:: getpropertyqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) -oder [**IWbemClassObject:: getmethodqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) -Methoden ab.

3.  Greifen Sie über die zurückgegebene [**iwbemqualifierset**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) -Schnittstelle auf die Qualifizierer des Objekts zu.

## <a name="examples"></a>Beispiele

Weitere Informationen zum Abrufen von Qualifizierern finden Sie im PowerShell-Codebeispiel [Get-wmiclassmethodsandwrite](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) in der TechNet Gallery.

 

 
