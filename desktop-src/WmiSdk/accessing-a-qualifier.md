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
# <a name="accessing-a-wmi-qualifier"></a><span data-ttu-id="df032-103">Aufrufen eines WMI-Qualifizierers</span><span class="sxs-lookup"><span data-stu-id="df032-103">Accessing a WMI Qualifier</span></span>

<span data-ttu-id="df032-104">Ein Qualifizierer ist ein Tag, das weitere Informationen zu einem WMI-Objekt, einer Methode oder einer Eigenschaft bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="df032-104">A qualifier is a tag that provides more information about a WMI object, method, or property.</span></span> <span data-ttu-id="df032-105">Manchmal müssen Sie möglicherweise auf die in einem Qualifizierer gespeicherten Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="df032-105">At times, you may need to access the data stored in a qualifier.</span></span> <span data-ttu-id="df032-106">Beispielsweise besteht eine häufige Aufgabe darin, zu bestimmen, ob ein Anbieter eine Methode implementiert, indem versucht wird, den **implementierten** Qualifizierer für diese Methode abzurufen.</span><span class="sxs-lookup"><span data-stu-id="df032-106">For example, a common task is to determine if a provider implements a method by attempting to retrieve the **Implemented** qualifier for that method.</span></span> <span data-ttu-id="df032-107">Weitere Informationen finden Sie unter [WMI-Qualifizierer](wmi-qualifiers.md) und [Hinzufügen eines Qualifizierers](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="df032-107">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

<span data-ttu-id="df032-108">Sie können die Qualifizierer für ein WMI-Objekt in PowerShell abrufen, indem Sie zuerst das Objekt abrufen und dann die Qualifizierer wie jede andere Eigenschaft untersuchen.</span><span class="sxs-lookup"><span data-stu-id="df032-108">You can retrieve the qualifiers on a WMI object in PowerShell by first retrieving the object, and then examining the qualifiers as you would any other property.</span></span>

<span data-ttu-id="df032-109">**So rufen Sie einen Qualifizierer mithilfe von PowerShell ab**</span><span class="sxs-lookup"><span data-stu-id="df032-109">**To retrieve a qualifier using PowerShell**</span></span>

-   <span data-ttu-id="df032-110">Rufen Sie mit [Get-WMIObject](https://technet.microsoft.com/library/dd315379.aspx)das Objekt ab, dessen Qualifizierer Sie anzeigen möchten, und greifen Sie dann über die **qualifizierereigenschaft** auf die Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="df032-110">Retrieve the object whose qualifiers you want to view using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), and then access the qualifiers through the **Qualifiers** property:</span></span>

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

    

    <span data-ttu-id="df032-111">Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="df032-111">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="df032-112">Sie können die Qualifizierer für eine WMI-Instanz in c# abrufen, indem Sie zuerst das Objekt abrufen und dann die Qualifizierer als Auflistung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="df032-112">You can retrieve the qualifiers on a WMI instance in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

<span data-ttu-id="df032-113">**Zum Abrufen eines Qualifizierers mit c# (Microsoft.System. Personal**</span><span class="sxs-lookup"><span data-stu-id="df032-113">**To retrieve a qualifier using C# (Microsoft.System.Management)**</span></span>

1.  <span data-ttu-id="df032-114">Rufen Sie die Klasse ab, deren Qualifizierer Sie anzeigen möchten, indem Sie ein ciminstance-Objekt mit dem angegebenen Klassennamen und Namespace erstellen.</span><span class="sxs-lookup"><span data-stu-id="df032-114">Retrieve the class whose qualifiers you want to view by creating a CimInstance object, using the specified class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    <span data-ttu-id="df032-115">Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="df032-115">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="df032-116">Sie können die Klassen Qualifizierer aus den Klassen " [ciminstance. cimclass. cimclassqualifizierer](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85))", den Eigenschaften [Qualifizierern aus "ciminstance. cimclass. cimclassproperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))" und den Methoden [Qualifizierern aus "ciminstance. cimclass. cimclassmethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85))" abrufen</span><span class="sxs-lookup"><span data-stu-id="df032-116">You can retrieve the class qualifiers from the [CimInstance.CimClass.CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), the property qualifiers from [CimInstance.CimClass.CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85)), and the method qualifiers from [CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span></span>

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

    

    <span data-ttu-id="df032-117">Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="df032-117">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="df032-118">Sie können die Qualifizierer für ein WMI-Objekt in c# abrufen, indem Sie zuerst das Objekt abrufen und dann die Qualifizierer als Auflistung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="df032-118">You can retrieve the qualifiers on a WMI object in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

> [!Note]  
> <span data-ttu-id="df032-119">**System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.</span><span class="sxs-lookup"><span data-stu-id="df032-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="df032-120">**So rufen Sie einen Qualifizierer mit c# ab (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="df032-120">**To retrieve a qualifier using C# (System.Management)**</span></span>

1.  <span data-ttu-id="df032-121">Rufen Sie das Objekt, dessen Qualifizierer Sie anzeigen möchten, mithilfe von [ManagementObject](/dotnet/api/system.management.managementobject)ab.</span><span class="sxs-lookup"><span data-stu-id="df032-121">Retrieve the object whose qualifiers you want to view using [ManagementObject](/dotnet/api/system.management.managementobject).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    <span data-ttu-id="df032-122">Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="df032-122">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="df032-123">Platzieren Sie die Qualifizierer in einem [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)-Element, und durchlaufen Sie die [QualifierData](/dotnet/api/system.management.qualifierdata) -Werte.</span><span class="sxs-lookup"><span data-stu-id="df032-123">Place the qualifiers into a [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection), and enumerate through the [QualifierData](/dotnet/api/system.management.qualifierdata) values.</span></span>

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    <span data-ttu-id="df032-124">Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="df032-124">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="df032-125">Im folgenden Verfahren wird beschrieben, wie ein Qualifizierer mithilfe von VBScript abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="df032-125">The following procedure describes how to retrieve a qualifier using VBScript.</span></span>

<span data-ttu-id="df032-126">**So rufen Sie einen Qualifizierer mit VBScript ab**</span><span class="sxs-lookup"><span data-stu-id="df032-126">**To retrieve a qualifier using VBScript**</span></span>

1.  <span data-ttu-id="df032-127">Rufen Sie das Objekt ab, dessen Qualifizierer Sie anzeigen möchten, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="df032-127">Retrieve the object whose qualifiers you want to view, as shown in the following example:</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    <span data-ttu-id="df032-128">Die gängigste Methode zum Abrufen eines Objekts ist die Verwendung der [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode.</span><span class="sxs-lookup"><span data-stu-id="df032-128">The most common way to retrieve an object is by using the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method.</span></span> <span data-ttu-id="df032-129">Weitere Informationen finden Sie unter [Abrufen einer WMI-Instanz](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="df032-129">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="df032-130">Greifen Sie über die Eigenschaft " [**errbemubject. Qualifizierer \_**](swbemobject-qualifiers-.md) " auf die Qualifizierer des Objekts zu, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="df032-130">Access the qualifiers of the object through the [**SWbemObject.Qualifiers\_**](swbemobject-qualifiers-.md) property, as shown in the following example:</span></span>

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

<span data-ttu-id="df032-131">Im folgenden Codebeispiel wird beschrieben, wie auf alle Qualifizierer eines [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Objekts zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="df032-131">The following code example describes how to access all the qualifiers on a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object.</span></span>


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



<span data-ttu-id="df032-132">Im folgenden Verfahren wird beschrieben, wie ein Qualifizierer mit C++ abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="df032-132">The following procedure describes how to retrieve a qualifier using C++.</span></span>

<span data-ttu-id="df032-133">**So rufen Sie einen Qualifizierer mit C++ ab**</span><span class="sxs-lookup"><span data-stu-id="df032-133">**To retrieve a qualifier using C++**</span></span>

1.  <span data-ttu-id="df032-134">Rufen Sie das Objekt ab, dessen Qualifizierer Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="df032-134">Retrieve the object whose qualifiers you want to view.</span></span>

    <span data-ttu-id="df032-135">Die gängigste Methode zum Abrufen eines Objekts ist das Aufrufen von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) oder [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="df032-135">The most common way to retrieve an object is by using a call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="df032-136">Weitere Informationen finden Sie unter [Abrufen von WMI-Klassen-oder Instanzdaten](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="df032-136">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="df032-137">Rufen Sie den Qualifizierer Satz für eine angegebene Eigenschaft mit einem Aufruf von [**IWbemClassObject:: getpropertyqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) -oder [**IWbemClassObject:: getmethodqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) -Methoden ab.</span><span class="sxs-lookup"><span data-stu-id="df032-137">Retrieve the qualifier set for a given property with a call to [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) or [**IWbemClassObject::GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) methods.</span></span>

3.  <span data-ttu-id="df032-138">Greifen Sie über die zurückgegebene [**iwbemqualifierset**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) -Schnittstelle auf die Qualifizierer des Objekts zu.</span><span class="sxs-lookup"><span data-stu-id="df032-138">Access the qualifiers of the object through the returned [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="df032-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df032-139">Examples</span></span>

<span data-ttu-id="df032-140">Weitere Informationen zum Abrufen von Qualifizierern finden Sie im PowerShell-Codebeispiel [Get-wmiclassmethodsandwrite](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) in der TechNet Gallery.</span><span class="sxs-lookup"><span data-stu-id="df032-140">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

 

 
