---
description: Eine Anbieter Methode ist eine Methode, die von einem Windows-Verwaltungsinstrumentation (WMI)-Anbieter implementiert wird.
ms.assetid: 9c692bc7-246b-4619-a371-cc9e0e2d5a6e
ms.tgt_platform: multiple
title: Aufrufen einer Anbieter Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ed8d05a1105c15f06b3df5f47006c5dafcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362363"
---
# <a name="calling-a-provider-method"></a><span data-ttu-id="59aa0-103">Aufrufen einer Anbieter Methode</span><span class="sxs-lookup"><span data-stu-id="59aa0-103">Calling a Provider Method</span></span>

<span data-ttu-id="59aa0-104">Eine Anbieter Methode ist eine Methode, die von einem Windows-Verwaltungsinstrumentation (WMI)-Anbieter implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="59aa0-104">A provider method is a method that is implemented by a Windows Management Instrumentation (WMI) provider.</span></span> <span data-ttu-id="59aa0-105">Die-Methode befindet sich in einer Klasse, die von einem Anbieter definiert wird, um Daten von Software oder Hardware darzustellen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-105">The method is found in a class defined by a provider to represent data from software or hardware.</span></span> <span data-ttu-id="59aa0-106">Die [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse verfügt z. b. über Methoden zum Starten, anhalten, fortsetzen, anhalten und Ändern von Diensten.</span><span class="sxs-lookup"><span data-stu-id="59aa0-106">For example, the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class has methods to start, stop, resume, pause, and change services.</span></span>

<span data-ttu-id="59aa0-107">Anbieter Methoden sollten nicht mit den folgenden Methoden Typen verwechselt werden:</span><span class="sxs-lookup"><span data-stu-id="59aa0-107">Provider methods should not be confused with the following types of methods:</span></span>

-   <span data-ttu-id="59aa0-108">Methoden für [WMI-System Klassen](wmi-system-classes.md), wie z. b. die [**gezd-**](--systemsecurity-getsd.md) Methode für [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="59aa0-108">Methods on [WMI system classes](wmi-system-classes.md), such as the [**GetSD**](--systemsecurity-getsd.md) method on [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>
-   <span data-ttu-id="59aa0-109">Methoden für Objekte in der [Skript-API für WMI](scripting-api-for-wmi.md), z. b. " [**Swap Services. InstancesOf**](swbemservices-instancesof.md)".</span><span class="sxs-lookup"><span data-stu-id="59aa0-109">Methods on objects in the [Scripting API for WMI](scripting-api-for-wmi.md), such as [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>
-   <span data-ttu-id="59aa0-110">Methoden in der [com-API für WMI](com-api-for-wmi.md), z. b. [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="59aa0-110">Methods in the [COM API for WMI](com-api-for-wmi.md), such as [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

## <a name="calling-a-provider-method-using-scripting"></a><span data-ttu-id="59aa0-111">Aufrufen einer Anbieter Methode mithilfe der Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="59aa0-111">Calling a Provider Method Using Scripting</span></span>

<span data-ttu-id="59aa0-112">Jede Automatisierungs Sprache, wie z. b. VBScript, PowerShell oder perl, kann eine WMI-Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-112">Any automation language, such as VBScript, PowerShell, or Perl, can call a WMI method.</span></span> <span data-ttu-id="59aa0-113">Einige Sprachen können den [direkten Zugriff](/windows)verwenden, andere müssen jedoch [**SWbemServices.Execmethod**](swbemservices-execmethod.md) verwenden, um die Anbieter Methode indirekt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-113">Some languages can use [direct access](/windows), but others must use [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to execute the provider method indirectly.</span></span>

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

<span data-ttu-id="59aa0-114">Im folgenden Verfahren wird beschrieben, wie Sie eine Anbieter Methode mithilfe der Skript-API aufrufen und direkt Zugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="59aa0-114">The following procedure describes how to call a provider method using the Scripting API and using direct access.</span></span>

<span data-ttu-id="59aa0-115">**So wenden Sie eine Anbieter Methode mithilfe der Skript-API und des direkten Zugriffs an**</span><span class="sxs-lookup"><span data-stu-id="59aa0-115">**To call a provider method using the Scripting API and direct access**</span></span>

1.  <span data-ttu-id="59aa0-116">Verwenden Sie diesen Ansatz für VBScript oder PowerShell.</span><span class="sxs-lookup"><span data-stu-id="59aa0-116">Use this approach for VBScript or PowerShell.</span></span>
2.  <span data-ttu-id="59aa0-117">Bestimmen Sie, ob die auszuführende Methode implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="59aa0-117">Determine if the method you want to execute is implemented.</span></span>

    <span data-ttu-id="59aa0-118">Für einige Klassen sind Methoden definiert, die von einem Anbieter nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="59aa0-118">Some classes have methods defined that are not supported by a provider.</span></span> <span data-ttu-id="59aa0-119">Wenn eine Methode nicht implementiert ist, kann Sie nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="59aa0-119">If a method is not implemented, you cannot execute it.</span></span> <span data-ttu-id="59aa0-120">Sie können bestimmen, ob eine Methode implementiert ist, indem Sie überprüfen, ob die Methode den [**implementierten**](standard-wmi-qualifiers.md) Qualifizierer aufweist</span><span class="sxs-lookup"><span data-stu-id="59aa0-120">You can determine if a method is implemented by checking if the method has the [**Implemented**](standard-wmi-qualifiers.md) qualifier.</span></span> <span data-ttu-id="59aa0-121">Weitere Informationen finden Sie unter [WMI-Qualifizierer](wmi-qualifiers.md) und [zugreifen auf einen WMI-Qualifizierer](accessing-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="59aa0-121">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Accessing a WMI Qualifier](accessing-a-qualifier.md).</span></span> <span data-ttu-id="59aa0-122">Sie können auch bestimmen, ob eine Anbieter Klassenmethode den **implementierten** Qualifizierer festgelegt hat, indem Sie das nicht unterstützte Wbemtest.exe Hilfsprogramm ausführen, das auf einem beliebigen Betriebssystem mit installiertem WMI</span><span class="sxs-lookup"><span data-stu-id="59aa0-122">You can also determine if a provider class method has the **Implemented** qualifier set by running the unsupported Wbemtest.exe utility, available on any operating system with WMI installed.</span></span>

3.  <span data-ttu-id="59aa0-123">Stellen Sie fest, ob die Methode, die Sie ausführen möchten, eine [*statische Methode*](gloss-s.md) oder eine nicht statische Methode ist.</span><span class="sxs-lookup"><span data-stu-id="59aa0-123">Determine if the method you want to execute is a [*static method*](gloss-s.md) or a nonstatic method.</span></span>

    <span data-ttu-id="59aa0-124">Statische Methoden gelten nur für WMI-Klassen und nicht für bestimmte Instanzen einer Klasse.</span><span class="sxs-lookup"><span data-stu-id="59aa0-124">Static methods apply only to WMI classes and not to specific instances of a class.</span></span> <span data-ttu-id="59aa0-125">Beispielsweise ist die [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) -Methode der [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse eine statische Methode, da Sie verwendet wird, um einen neuen Prozess ohne eine Instanz dieser Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-125">For example, the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is a static method because use it to create a new process without an instance of this class.</span></span> <span data-ttu-id="59aa0-126">Nicht statische Methoden gelten nur für Instanzen einer Klasse.</span><span class="sxs-lookup"><span data-stu-id="59aa0-126">Nonstatic methods apply only to instances of a class.</span></span> <span data-ttu-id="59aa0-127">Beispielsweise ist die [**Beendigungs Methode**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) der **Win32- \_ Prozess** Klasse eine nicht statische Methode, da es nur sinnvoll ist, einen Prozess zu beenden, wenn eine Instanz dieses Prozesses vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="59aa0-127">For example, the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method of the **Win32\_Process** class is a nonstatic method because it only makes sense to terminate a process if an instance of that process exists.</span></span> <span data-ttu-id="59aa0-128">Sie können ermitteln, ob eine Methode statisch ist, indem Sie überprüfen, ob der [**statische**](standard-wmi-qualifiers.md) Qualifizierer der Methode zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="59aa0-128">You can determine if a method is static by checking if the [**Static**](standard-wmi-qualifiers.md) qualifier is associated with the method.</span></span>

4.  <span data-ttu-id="59aa0-129">Rufen Sie die Klasse oder Instanz ab, die die Methode enthält, die Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="59aa0-129">Retrieve the class or instance that contains the method you want to execute.</span></span>

    <span data-ttu-id="59aa0-130">Weitere Informationen finden Sie unter [Abrufen von WMI-Klassen-oder Instanzdaten](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="59aa0-130">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

5.  <span data-ttu-id="59aa0-131">Richten Sie Sicherheitseinstellungen ein, die von der Methode möglicherweise benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="59aa0-131">Set up any security settings that the method may require.</span></span>

    <span data-ttu-id="59aa0-132">Sie können häufig die Berechtigungen bestimmen, die eine Methode erfordert, indem [**Sie die Werte**](swbemsecurity-privileges.md) im Berechtigungs Qualifizierer der Methode überprüfen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-132">You can often determine the privileges that a method requires by examining the values in the [**Privileges**](swbemsecurity-privileges.md) qualifier of the method.</span></span> <span data-ttu-id="59aa0-133">Zum Beispiel erfordert die Methode zum [**herunter**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) fahren der [**Win32- \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) -Klasse, dass Sie die Berechtigung "SeShutdownPrivilege" festlegen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-133">For example, the [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) method requires you to set the "SeShutdownPrivilege" privilege.</span></span> <span data-ttu-id="59aa0-134">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="59aa0-134">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

6.  <span data-ttu-id="59aa0-135">Ruft die-Methode auf und untersucht den Rückgabewert, um zu bestimmen, ob die Methode erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="59aa0-135">Call the method and examine the return value to determine if the method was successful.</span></span>

<span data-ttu-id="59aa0-136">Im folgenden Codebeispiel wird ein Notepad-Prozess erstellt und die Prozess-ID mithilfe des direkten Zugriffs abgerufen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-136">The following code example creates a Notepad process and gets the process ID using direct access.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_Process")

Error = objWMIService.Create("notepad.exe", null, _
    null, intProcessID)
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & intProcessID & "."
Else
    Wscript.Echo "Notepad could not be started due to error " _
       & Error & "."
End If  
```


```PowerShell

try
{ 
    $myProcess = ([wmiclass]&quot;win32_process&quot;).create(&quot;notepad.exe&quot;, $null, $null) 
}
catch 
{
    &quot;Notepad could not be started due to the following error:&quot; 
    $error[0]
    return 
}
#else
&quot;Notepad was started with a process ID of &quot; + $myProcess.ProcessID
```





<span id="indirect_access"></span><span id="INDIRECT_ACCESS"></span>

<span data-ttu-id="59aa0-137">Im folgenden Verfahren wird beschrieben, wie eine Anbieter Methode mithilfe der Skript-API und der [**SWbemServices.Execmethod**](swbemservices-execmethod.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="59aa0-137">The following procedure describes how to call a provider method using the Scripting API and the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>

<span data-ttu-id="59aa0-138">**So wenden Sie eine Anbieter Methode mithilfe der Skript-API und SWbemServices.Execmethod an**</span><span class="sxs-lookup"><span data-stu-id="59aa0-138">**To call a provider method using the Scripting API and SWbemServices.ExecMethod**</span></span>

1.  <span data-ttu-id="59aa0-139">Rufen Sie die WMI-Klassendefinition ab, um eine statische Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-139">Retrieve the WMI class definition to execute a static method.</span></span> <span data-ttu-id="59aa0-140">Rufen Sie die WMI-Klasseninstanz ab, um eine nicht statische Methode auszuführen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-140">Retrieve the WMI class instance to execute a nonstatic method.</span></span>
2.  <span data-ttu-id="59aa0-141">Rufen Sie die Methode ab, die Sie mithilfe der Methode " [**errbemubjectset. Item**](swbemobjectset-item.md) " aus der " [**errbemubject. Methods \_**](swbemobject-methods-.md) "-Auflistung Ihrer Klasse oder Instanz ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="59aa0-141">Retrieve the method to execute from the [**SWbemObject.Methods\_**](swbemobject-methods-.md) collection of your class or instance by using the [**SWbemObjectSet.Item**](swbemobjectset-item.md) method.</span></span>
3.  <span data-ttu-id="59aa0-142">Rufen Sie ein [**InParameters**](swbemmethod-inparameters.md) -Objekt für die Methode ab, und richten Sie die Parameter wie unter [Erstellen von inparameter-Objekten](constructing-inparameters-objects.md)beschrieben ein.</span><span class="sxs-lookup"><span data-stu-id="59aa0-142">Obtain an [**InParameters**](swbemmethod-inparameters.md) object for the method and set up the parameters as described in [Constructing InParameters Objects](constructing-inparameters-objects.md).</span></span>
4.  <span data-ttu-id="59aa0-143">Führen Sie die **SWbemServices.Execmethod** -Methode aus, um auszuführen, und weisen Sie den Rückgabe [**Wert einem-**](swbemobject.md) Objekt mit dem-Objekt zu, um die Ausgabeparameter zu speichern.</span><span class="sxs-lookup"><span data-stu-id="59aa0-143">Call the **SWbemServices.ExecMethod** method to execute and assign the return value to an [**SWbemObject**](swbemobject.md) object to store the output parameters.</span></span>
5.  <span data-ttu-id="59aa0-144">Überprüfen Sie die Werte im Ausgabeparameter-Objekt, um sicherzustellen, dass die Methode ordnungsgemäß ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="59aa0-144">Check the values in the output parameters object to verify that the method executed correctly.</span></span>

<span data-ttu-id="59aa0-145">Im folgenden VBScript-Codebeispiel wird der gleiche Vorgang wie das vorherige Skript ausgeführt, indem der indirekte Ansatz durch Aufrufen von [**SWBemServices.Execmethod**](swbemservices-execmethod.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="59aa0-145">The following VBScript code example performs the same operation as the previous script by the indirect approach through calling [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")

Set objProcess = objWMIService.Get("Win32_Process")

' Obtain an InParameters object specific to 
'   the Win32_Process.Create method.
Set objInParam = _
    objProcess.Methods_("Create").inParameters.SpawnInstance_()

' Add the input parameters. 
objInParam.Properties_.item("CommandLine") = "Notepad"
objInParam.Properties_.item("CurrentDirectory") = NULL
objInParam.Properties_.item("ProcessStartupInformation") = NULL


Set objOutParams = objProcess.ExecMethod_("Create", objInParam) 
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & objOutParams.ProcessId 
Else
    Wscript.Echo "Notepad could not be started due to error " & _
       objOutParams.ReturnValue
End If
```




<span data-ttu-id="59aa0-146">Im folgenden Verfahren wird beschrieben, wie eine Anbieter Methode mithilfe von C++ aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="59aa0-146">The following procedure describes how to call a provider method using C++.</span></span>

<span data-ttu-id="59aa0-147">**So wenden Sie eine Anbieter Methode mithilfe von C++ an**</span><span class="sxs-lookup"><span data-stu-id="59aa0-147">**To call a provider method using C++**</span></span>

1.  <span data-ttu-id="59aa0-148">Verbindung mit WMI herstellen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-148">Connect to WMI.</span></span>

    <span data-ttu-id="59aa0-149">Um eine Methode in WMI aufzurufen, müssen Sie zunächst über eine funktionierende Verbindung mit einem WMI-Namespace verfügen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-149">To call a method in WMI, first you must have a working connection to a WMI namespace.</span></span> <span data-ttu-id="59aa0-150">Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md) und [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="59aa0-150">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md) and [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="59aa0-151">Im folgenden Beispiel wird gezeigt, wie eine Verbindung mit WMI hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="59aa0-151">The following example shows how to connect to WMI.</span></span> <span data-ttu-id="59aa0-152">Weitere Informationen zu Sicherheitsproblemen bei WMI-Anbieter aufrufen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="59aa0-152">For more information about security issues in WMI provider calls, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

```C++
    HRESULT hr = CoInitialize(0);
        hr  =  CoInitializeSecurity(
                NULL, 
                -1, 
                NULL, 
                NULL,
                RPC_C_AUTHN_LEVEL_DEFAULT, 
                RPC_C_IMP_LEVEL_IMPERSONATE, 
                NULL, 
                EOAC_NONE, 
                NULL); 
        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
                CLSCTX_INPROC_SERVER,
                IID_IWbemLocator, (LPVOID *) &pLocator);
        hr = pLocator->ConnectServer(path, NULL, NULL, 
                NULL, 0, NULL, NULL, &pNamespace);
```

    

2.  <span data-ttu-id="59aa0-153">Rufen Sie [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) auf, um die Definition der Klasse der Methode abzurufen, die Sie aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="59aa0-153">Call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve the definition of the class of the method you want to call.</span></span>

    <span data-ttu-id="59aa0-154">Die [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode gibt einen [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Zeiger zurück, der auf die Klassendefinition zeigt.</span><span class="sxs-lookup"><span data-stu-id="59aa0-154">The [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the class definition.</span></span>

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  <span data-ttu-id="59aa0-155">Für Methoden, für die Eingabeparameter erforderlich sind, müssen Sie die [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) -Methode aufrufen, um das Input Parameter Class-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-155">For methods that require input parameters, call the [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method to get the input parameter class object.</span></span>

    <span data-ttu-id="59aa0-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) gibt einen [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Zeiger zurück, der auf die Eingabeparameter Klasse zeigt.</span><span class="sxs-lookup"><span data-stu-id="59aa0-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the input parameter class.</span></span>

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  <span data-ttu-id="59aa0-157">Generieren Sie eine Instanz der Eingabeparameter Klasse, indem Sie die [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="59aa0-157">Generate an instance of the input parameter class with a call to the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  <span data-ttu-id="59aa0-158">Legen Sie die Eigenschaften der Eingabeparameter Klasse mit einem-Befehl für die [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) -Methode fest.</span><span class="sxs-lookup"><span data-stu-id="59aa0-158">Set the properties of the input parameter class with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  <span data-ttu-id="59aa0-159">Rufen Sie die Methode mit einem Aufruf von [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) oder [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)auf.</span><span class="sxs-lookup"><span data-stu-id="59aa0-159">Invoke the method with a call to [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span>

    <span data-ttu-id="59aa0-160">Bei [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)gibt WMI alle Ausgabeparameter im-Befehl zurück.</span><span class="sxs-lookup"><span data-stu-id="59aa0-160">For [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI returns any output parameters in the call.</span></span> <span data-ttu-id="59aa0-161">Bei [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)gibt WMI alle Ausgabeparameter durch einen Aufruf von [**iwbemubjectsink**](iwbemobjectsink.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="59aa0-161">For [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI returns any output parameters through a call to [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="59aa0-162">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="59aa0-162">For more information, see [Calling a Method](calling-a-method.md).</span></span>

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

<span data-ttu-id="59aa0-163">Der folgende Code ist ein umfassendes Beispiel zum Aufrufen einer Anbieter Methode.</span><span class="sxs-lookup"><span data-stu-id="59aa0-163">The following code is a complete example for calling a provider method.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    IWbemLocator *pLocator = NULL;
    IWbemServices *pNamespace = 0;
    IWbemClassObject * pClass = NULL;
    IWbemClassObject * pOutInst = NULL;
    IWbemClassObject * pInClass = NULL;
    IWbemClassObject * pInInst = NULL;
  
    BSTR path = SysAllocString(L"root\\default");
    BSTR ClassPath = SysAllocString(L"TestMeth");
    BSTR MethodName = SysAllocString(L"Echo");
    BSTR ArgName = SysAllocString(L"sInArg");
    BSTR Text;

    // Initialize COM and connect to WMI.

    HRESULT hr = CoInitialize(0);
    hr  =  CoInitializeSecurity(NULL, -1, NULL, NULL,RPC_C_AUTHN_LEVEL_DEFAULT, 
                                RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE, NULL); 
    hr = CoCreateInstance(CLSID_WbemLocator, 0, CLSCTX_INPROC_SERVER,
                          IID_IWbemLocator, (LPVOID *) &pLocator);
    hr = pLocator->ConnectServer(path, NULL, NULL, NULL, 0, NULL, NULL, &pNamespace);

    // Get the class object for the method definition.

    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);

    // Get the input-argument class object and 
    // create an instance.

    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL); 
    hr = pInClass->SpawnInstance(0, &pInInst);

    // Set the property.

    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);

    // Call the method.

    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
    
    // Display the results. Note that the return 
    // value is in the property "ReturnValue"
    // and the returned string is in the 
    // property "sOutArg".

    hr = pOutInst->GetObjectText(0, &Text);
    printf("\nThe object text is:\n%S", Text);

    // Free up resources.

    SysFreeString(path);
    SysFreeString(ClassPath);
    SysFreeString(MethodName);
    SysFreeString(ArgName);
    SysFreeString(Text);
    pClass->Release();
    pInInst->Release();
    pInClass->Release();
    pOutInst->Release();
    pLocator->Release();
    pNamespace->Release();
    CoUninitialize();
    printf("Terminating normally\n");
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="59aa0-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59aa0-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59aa0-165">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="59aa0-165">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
