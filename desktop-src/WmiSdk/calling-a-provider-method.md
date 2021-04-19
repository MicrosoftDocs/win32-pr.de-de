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
# <a name="calling-a-provider-method"></a>Aufrufen einer Anbieter Methode

Eine Anbieter Methode ist eine Methode, die von einem Windows-Verwaltungsinstrumentation (WMI)-Anbieter implementiert wird. Die-Methode befindet sich in einer Klasse, die von einem Anbieter definiert wird, um Daten von Software oder Hardware darzustellen. Die [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse verfügt z. b. über Methoden zum Starten, anhalten, fortsetzen, anhalten und Ändern von Diensten.

Anbieter Methoden sollten nicht mit den folgenden Methoden Typen verwechselt werden:

-   Methoden für [WMI-System Klassen](wmi-system-classes.md), wie z. b. die [**gezd-**](--systemsecurity-getsd.md) Methode für [**\_ \_ SystemSecurity**](--systemsecurity.md).
-   Methoden für Objekte in der [Skript-API für WMI](scripting-api-for-wmi.md), z. b. " [**Swap Services. InstancesOf**](swbemservices-instancesof.md)".
-   Methoden in der [com-API für WMI](com-api-for-wmi.md), z. b. [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

## <a name="calling-a-provider-method-using-scripting"></a>Aufrufen einer Anbieter Methode mithilfe der Skripterstellung

Jede Automatisierungs Sprache, wie z. b. VBScript, PowerShell oder perl, kann eine WMI-Methode aufzurufen. Einige Sprachen können den [direkten Zugriff](/windows)verwenden, andere müssen jedoch [**SWbemServices.Execmethod**](swbemservices-execmethod.md) verwenden, um die Anbieter Methode indirekt auszuführen.

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

Im folgenden Verfahren wird beschrieben, wie Sie eine Anbieter Methode mithilfe der Skript-API aufrufen und direkt Zugriff verwenden.

**So wenden Sie eine Anbieter Methode mithilfe der Skript-API und des direkten Zugriffs an**

1.  Verwenden Sie diesen Ansatz für VBScript oder PowerShell.
2.  Bestimmen Sie, ob die auszuführende Methode implementiert ist.

    Für einige Klassen sind Methoden definiert, die von einem Anbieter nicht unterstützt werden. Wenn eine Methode nicht implementiert ist, kann Sie nicht ausgeführt werden. Sie können bestimmen, ob eine Methode implementiert ist, indem Sie überprüfen, ob die Methode den [**implementierten**](standard-wmi-qualifiers.md) Qualifizierer aufweist Weitere Informationen finden Sie unter [WMI-Qualifizierer](wmi-qualifiers.md) und [zugreifen auf einen WMI-Qualifizierer](accessing-a-qualifier.md). Sie können auch bestimmen, ob eine Anbieter Klassenmethode den **implementierten** Qualifizierer festgelegt hat, indem Sie das nicht unterstützte Wbemtest.exe Hilfsprogramm ausführen, das auf einem beliebigen Betriebssystem mit installiertem WMI

3.  Stellen Sie fest, ob die Methode, die Sie ausführen möchten, eine [*statische Methode*](gloss-s.md) oder eine nicht statische Methode ist.

    Statische Methoden gelten nur für WMI-Klassen und nicht für bestimmte Instanzen einer Klasse. Beispielsweise ist die [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) -Methode der [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse eine statische Methode, da Sie verwendet wird, um einen neuen Prozess ohne eine Instanz dieser Klasse zu erstellen. Nicht statische Methoden gelten nur für Instanzen einer Klasse. Beispielsweise ist die [**Beendigungs Methode**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) der **Win32- \_ Prozess** Klasse eine nicht statische Methode, da es nur sinnvoll ist, einen Prozess zu beenden, wenn eine Instanz dieses Prozesses vorhanden ist. Sie können ermitteln, ob eine Methode statisch ist, indem Sie überprüfen, ob der [**statische**](standard-wmi-qualifiers.md) Qualifizierer der Methode zugeordnet ist.

4.  Rufen Sie die Klasse oder Instanz ab, die die Methode enthält, die Sie ausführen möchten.

    Weitere Informationen finden Sie unter [Abrufen von WMI-Klassen-oder Instanzdaten](retrieving-class-or-instance-data.md).

5.  Richten Sie Sicherheitseinstellungen ein, die von der Methode möglicherweise benötigt werden.

    Sie können häufig die Berechtigungen bestimmen, die eine Methode erfordert, indem [**Sie die Werte**](swbemsecurity-privileges.md) im Berechtigungs Qualifizierer der Methode überprüfen. Zum Beispiel erfordert die Methode zum [**herunter**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) fahren der [**Win32- \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) -Klasse, dass Sie die Berechtigung "SeShutdownPrivilege" festlegen. Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).

6.  Ruft die-Methode auf und untersucht den Rückgabewert, um zu bestimmen, ob die Methode erfolgreich war.

Im folgenden Codebeispiel wird ein Notepad-Prozess erstellt und die Prozess-ID mithilfe des direkten Zugriffs abgerufen.


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

Im folgenden Verfahren wird beschrieben, wie eine Anbieter Methode mithilfe der Skript-API und der [**SWbemServices.Execmethod**](swbemservices-execmethod.md)aufgerufen wird.

**So wenden Sie eine Anbieter Methode mithilfe der Skript-API und SWbemServices.Execmethod an**

1.  Rufen Sie die WMI-Klassendefinition ab, um eine statische Methode auszuführen. Rufen Sie die WMI-Klasseninstanz ab, um eine nicht statische Methode auszuführen.
2.  Rufen Sie die Methode ab, die Sie mithilfe der Methode " [**errbemubjectset. Item**](swbemobjectset-item.md) " aus der " [**errbemubject. Methods \_**](swbemobject-methods-.md) "-Auflistung Ihrer Klasse oder Instanz ausführen möchten.
3.  Rufen Sie ein [**InParameters**](swbemmethod-inparameters.md) -Objekt für die Methode ab, und richten Sie die Parameter wie unter [Erstellen von inparameter-Objekten](constructing-inparameters-objects.md)beschrieben ein.
4.  Führen Sie die **SWbemServices.Execmethod** -Methode aus, um auszuführen, und weisen Sie den Rückgabe [**Wert einem-**](swbemobject.md) Objekt mit dem-Objekt zu, um die Ausgabeparameter zu speichern.
5.  Überprüfen Sie die Werte im Ausgabeparameter-Objekt, um sicherzustellen, dass die Methode ordnungsgemäß ausgeführt wurde.

Im folgenden VBScript-Codebeispiel wird der gleiche Vorgang wie das vorherige Skript ausgeführt, indem der indirekte Ansatz durch Aufrufen von [**SWBemServices.Execmethod**](swbemservices-execmethod.md)aufgerufen wird.


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




Im folgenden Verfahren wird beschrieben, wie eine Anbieter Methode mithilfe von C++ aufgerufen wird.

**So wenden Sie eine Anbieter Methode mithilfe von C++ an**

1.  Verbindung mit WMI herstellen.

    Um eine Methode in WMI aufzurufen, müssen Sie zunächst über eine funktionierende Verbindung mit einem WMI-Namespace verfügen. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md) und [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).

    Im folgenden Beispiel wird gezeigt, wie eine Verbindung mit WMI hergestellt wird. Weitere Informationen zu Sicherheitsproblemen bei WMI-Anbieter aufrufen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).

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

    

2.  Rufen Sie [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) auf, um die Definition der Klasse der Methode abzurufen, die Sie aufrufen möchten.

    Die [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) -Methode gibt einen [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Zeiger zurück, der auf die Klassendefinition zeigt.

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  Für Methoden, für die Eingabeparameter erforderlich sind, müssen Sie die [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) -Methode aufrufen, um das Input Parameter Class-Objekt abzurufen.

    [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) gibt einen [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Zeiger zurück, der auf die Eingabeparameter Klasse zeigt.

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  Generieren Sie eine Instanz der Eingabeparameter Klasse, indem Sie die [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) -Methode aufrufen.

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  Legen Sie die Eigenschaften der Eingabeparameter Klasse mit einem-Befehl für die [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) -Methode fest.

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  Rufen Sie die Methode mit einem Aufruf von [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) oder [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)auf.

    Bei [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)gibt WMI alle Ausgabeparameter im-Befehl zurück. Bei [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)gibt WMI alle Ausgabeparameter durch einen Aufruf von [**iwbemubjectsink**](iwbemobjectsink.md)zurück. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

Der folgende Code ist ein umfassendes Beispiel zum Aufrufen einer Anbieter Methode.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 
