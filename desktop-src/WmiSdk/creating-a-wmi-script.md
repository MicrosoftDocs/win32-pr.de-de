---
description: Sie können alle über WMI verfügbaren Informationen mithilfe von Skripts anzeigen oder bearbeiten.
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: Erstellen eines WMI-Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a56eca450757086b3d334d8f64fa41c4cf297f903963498afe958bee802705eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464190"
---
# <a name="creating-a-wmi-script"></a>Erstellen eines WMI-Skripts

Sie können alle über WMI verfügbaren Informationen mithilfe von Skripts anzeigen oder bearbeiten. Skripts können in jeder Skriptsprache geschrieben werden, die Microsoft ActiveX-Skripthosting unterstützt, einschließlich Visual Basic Scripting Edition (VBScript), PowerShell und Perl. Windows Skripthost (WSH), Active Server Pages und Internet Explorer können alle WMI-Skripts hosten.

> [!Note]
>
> Die primäre Skriptsprache, die derzeit von WMI unterstützt wird, ist PowerShell. WMI enthält jedoch auch eine stabile Unterstützung für Skripts für VBScript und andere Sprachen, die auf die [Skripterstellungs-API für WMI zugreifen.](scripting-api-for-wmi.md)

 

## <a name="wmi-scripting-languages"></a>WMI-Skriptsprachen

Die beiden Hauptsprachen, die von WMI unterstützt werden, sind PowerShell und VBScript (über Windows Script Host oder WSH).

-   **PowerShell** wurde mit einer engen Integration in WMI entwickelt. Daher sind viele der zugrunde liegenden Elemente von WMI in die WMI-Cmdlets integriert: [Get-WmiObject,](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1) [Set-WmiInstance,](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1) [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)und [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1). In der folgenden Tabelle werden die allgemeinen Prozesse beschrieben, die für den Zugriff auf WMI-Informationen verwendet werden. Beachten Sie, dass während die meisten dieser Beispiele Get-WMIObject verwenden, viele der PowerShell-WMI-Cmdlets dieselben Parameter haben, z. B. *-Class* oder *-Credentials*. Daher funktionieren viele dieser Prozesse auch für andere Objekte. Eine detailliertere Erörterung von PowerShell und WMI finden Sie unter [Using the Get-WMiObject Cmdlet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) and Windows PowerShell - the [WMI Connection](/previous-versions/technet-magazine/cc162365(v=msdn.10)).

-   **VBScript** hingegen ruft explizit die Skripterstellungs-API für [WMI](scripting-api-for-wmi.md)auf, wie oben erwähnt. Andere Sprachen wie Perl können auch die Skript-API für WMI verwenden. Im Rahmen dieser Dokumentation verwenden die meisten Beispiele, die die Skripterstellungs-API für WMI veranschaulichen, jedoch VBScript. Wenn eine Programmiertechnik für VBScript spezifisch ist, wird sie jedoch aufgerufen.

    VBScript verfügt im Wesentlichen über zwei separate Möglichkeiten für den Zugriff auf WMI. Die erste besteht in der Verwendung [**eines SWbemLocator-Objekts**](swbemlocator.md) zum Herstellen einer Verbindung mit WMI. Alternativ können Sie [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) und einen Moniker verwenden. Ein Moniker ist eine Zeichenfolge, die eine Reihe von Elementen beschreiben kann: Ihre Anmeldeinformationen, [](gloss-n.md) Identitätswechseleinstellungen, den Computer, mit dem Sie eine Verbindung herstellen möchten, den WMI-Namespace (d. h. den allgemeinen Speicherort, an dem WMI Objektgruppen speichert) und das WMI-Objekt, das Sie abrufen möchten. In vielen der folgenden Beispiele werden beide Techniken beschrieben. Weitere Informationen finden Sie unter [Erstellen einer Monikerzeichenfolge](constructing-a-moniker-string.md) und [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)

    Unabhängig davon, welche Technik Sie zum Herstellen einer Verbindung mit WMI verwenden, werden Sie wahrscheinlich mindestens ein Objekt aus der Skripterstellungs-API abrufen. Am häufigsten wird [**SWbemObject verwendet,**](swbemobject.md)mit dem WMI ein WMI-Objekt beschreibt. Alternativ können Sie ein [**SWbemServices-Objekt**](swbemservices.md) verwenden, um den WMI-Dienst selbst zu beschreiben, oder ein [**SWbemObjectPath-Objekt,**](swbemobjectpath.md) um den Speicherort eines WMI-Objekts zu beschreiben. Weitere Informationen finden Sie unter [Scripting with SWbemObject (Skripterstellung mit SWbemObject)](scripting-with-swbemobject.md) und [Scripting Helper Objects (Skripterstellung für Hilfsobjekte).](scripting-helper-objects.md)

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a>Verwenden von WMI und einer Skriptsprache, How Do I...

<dl> <dt>

<span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... Stellen Sie eine Verbindung mit WMI her?
</dt> <dd>

Rufen Sie für VBScript und die Skripterstellungs-API für WMI ein [**SWbemServices-Objekt**](swbemservices.md) mit einem Moniker und einem Aufruf von [**GetObject ab.**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) Alternativ können Sie mit einem Aufruf von [**SWbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)eine Verbindung mit dem Server herstellen. Anschließend können Sie das -Objekt verwenden, um auf einen bestimmten WMI-Namespace oder eine WMI-Klasseninstanz zuzugreifen.

Für PowerShell erfolgt die Verbindung mit WMI in der Regel direkt im Cmdlet-Aufruf. Daher sind keine zusätzlichen Schritte erforderlich.

Weitere Informationen finden Sie unter Beschreiben des Speicherorts eines [WMI-Objekts,](describing-the-location-of-a-wmi-object.md)Erstellen einer [Monikerzeichenfolge](constructing-a-moniker-string.md)und Herstellen einer Verbindung [mit WMI mit VBScript.](connecting-to-wmi-with-vbscript.md)


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... Informationen aus WMI abrufen?
</dt> <dd>

Verwenden Sie für VBScript und die Skripterstellungs-API für WMI eine Abruffunktion wie [**WbemServices.Get**](swbemservices-get.md) oder [**WbemServices.InstancesOf.**](swbemservices-instancesof.md) Sie können auch den Klassennamen des abzurufenden Objekts in einem Moniker platzieren, was effizienter sein kann.

Verwenden Sie für PowerShell den *Parameter -Class.* Beachten Sie, dass -Class der Standardparameter ist. Daher müssen Sie dies nicht explizit besingen.

Weitere Informationen finden Sie unter [Abrufen von WMI-Klassen- oder Instanzdaten.](retrieving-class-or-instance-data.md)


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... Eine WMI-Abfrage erstellen?
</dt> <dd>

Verwenden Sie für VBScript und die Skripterstellungs-API für WMI die [**SWbemServices.ExecQuery-Methode.**](swbemservices-execquery.md)

Verwenden Sie für PowerShell den *Parameter -Query.* Sie können auch mit dem *Parameter -Filter* filtern.

Weitere Informationen finden Sie unter [Abfragen von WMI.](querying-wmi.md)


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... Eine Liste von WMI-Objekten auflisten?
</dt> <dd>

Verwenden Sie für VBScript und die Skripterstellungs-API für WMI das [**Containerobjekt SWbemObjectSet,**](swbemobjectset.md) das im Skript als Auflistung behandelt wird, die aufzählt werden kann. Sie können ein **SWbemObjectSet** aus einem Aufruf von [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) oderSWbemServices.Exe [**cQuery abrufen.**](swbemservices-execquery.md)

PowerShell kann Enumerationen wie jedes andere Objekt abrufen und verarbeiten. es gibt nichts Besonderes für WMI.

Weitere Informationen finden Sie unter [Zugreifen auf eine Auflistung.](accessing-a-collection.md)


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... auf einen anderen WMI-Namespace zugreifen?
</dt> <dd>

Geben Sie für VBScript und die Skript-API für WMI den Namespace im Moniker an, oder sie können den Namespace im Aufruf von [**SwbemLocator.ConnectServer explizit angeben.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)

Verwenden Sie für PowerShell den *Parameter -Namespace.* Der Standardnamespace ist "root cimV2". Viele ältere Klassen werden jedoch \\ in "root \\ default" gespeichert.

Um den Speicherort einer bestimmten WMI-Klasse zu finden, sehen Sie sich die Referenzseite an. Alternativ können Sie einen Namespace mit get-WmiObject manuell untersuchen.


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... alle untergeordneten Instanzen einer Klasse abrufen?
</dt> <dd>

Für Sprachen, die direkt die Skripterstellungs-API für WMI und PowerShell verwenden, unterstützt WMI das Abrufen der untergeordneten Klassen einer Basisklasse. Daher müssen Sie nur nach der übergeordneten Klasse suchen, um die untergeordneten Instanzen abzurufen. Im folgenden Beispiel wird nach [**CIM \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk)gesucht. Dabei handelt es sich um eine vorinstallierte WMI-Klasse, die logische Datenträger auf einem Windows-basierten Computersystem darstellt. Daher gibt die Suche nach dieser übergeordneten Klasse auch Instanzen von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)zurück, die Windows verwendet, um Festplatten zu beschreiben. Weitere Informationen finden Sie unter [Common Information Model](common-information-model.md). WMI stellt ein vollständiges Schema solcher vorinstallierten Klassen zur Steuerung verwalteter Objekte und für den Zugriff darauf zur Überwachung von verwalteten Objekten. Weitere Informationen finden Sie unter [Win32-Klassen](/windows/desktop/CIMWin32Prov/win32-provider) und [WMI-Klassen](wmi-classes.md).


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... WMI-Objekt suchen?
</dt> <dd>

Sowohl für die Skripterstellungs-API für WMI als auch für PowerShell verwendet WMI eine Kombination aus Namespace-, Klassennamen- und Schlüsseleigenschaften, um eine bestimmte WMI-Instanz eindeutig zu identifizieren. Zusammen wird dies als WMI-Objektpfad bezeichnet. Für VBScript beschreibt die [**\_ SWbemObject.Path-Eigenschaft**](swbemobject-path-.md) den Pfad für jedes objekt, das von der Skripterstellungs-API zurückgegeben wird. Für PowerShell hat jedes WMI-Objekt eine \_ \_ PATH-Eigenschaft. Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)

Zusätzlich zum Namespace- und Klassennamen verfügt ein WMI-Objekt auch über eine Schlüsseleigenschaft, die diese Instanz im Vergleich zu anderen Instanzen auf Ihrem Computer eindeutig identifiziert. Beispielsweise ist die **DeviceID-Eigenschaft** die Schlüsseleigenschaft für die [**Win32 \_ LogicalDisk-Klasse.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) Weitere Informationen finden Sie unter [Managed Object Format (MOF).](managed-object-format--mof-.md)

Schließlich ist der relative Pfad einfach eine verkürzte Form des Pfads und enthält den Klassennamen und den Schlüsselwert. In den folgenden Beispielen kann der Pfad \\ \\ "computerName \\ root \\ cimv2:Win32 \_ LogicalDisk.DeviceID="D:"" sein, während der relative Pfad "Win32LogicalDisk.DeviceID="D"" wäre.


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... Informationen in WMI festlegen?
</dt> <dd>

Verwenden Sie für VBScript und die Skripterstellungs-API für WMI die [**\_ SWbemObject.Put-Methode.**](swbemobject-put-.md)

Für PowerShell können Sie entweder die Put-Methode oder sonst [Set-WmiInstance verwenden.](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true)

Weitere Informationen finden Sie unter [Ändern einer Instanzeigenschaft.](modifying-an-instance-property.md)


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... Andere Anmeldeinformationen verwenden?
</dt> <dd>

Verwenden Sie für VBScript und die Skripterstellungs-API für WMI die *Parameter UserName* und *Password* in der [**SWbemLocator.ConnectServer-Methode.**](swbemlocator-connectserver.md)

Verwenden Sie für PowerShell den *Parameter -Credential.*

Beachten Sie, dass Sie nur alternative Anmeldeinformationen auf einem Remotesystem verwenden können. Weitere Informationen finden Sie unter [Schützen von Skriptclients.](securing-scripting-clients.md)


```VB
strComputer = "remoteComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... Auf einen Remotecomputer zugreifen?
</dt> <dd>

Geben Sie für VBScript und die Skript-API für WMI explizit den Namen des Computers entweder im Moniker oder andernorts im Aufruf von [**SWbemLocator.ConnectServer an.**](swbemlocator-connectserver.md) Weitere Informationen finden Sie unter [Herstellen einer Remoteverbindung mit WMI mit VBScript.](connecting-to-wmi-remotely-with-vbscript.md)

Verwenden Sie für PowerShell den *Parameter -ComputerName.* Weitere Informationen finden Sie unter [Herstellen einer Remoteverbindung mit WMI mitHilfe von PowerShell.](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... Legen Sie die Ebenen Authentifizierung und Identitätswechsel fest?
</dt> <dd>

Verwenden Sie für VBScript und die Skripterstellungs-API für WMI die [**\_ SWbemServices.Security-Eigenschaft**](swbemlocator-security-.md) für das zurückgegebene Serverobjekt, oder legen Sie die relevanten Werte im Moniker fest.

Verwenden Sie für PowerShell die Parameter *-Authentication* bzw. *-Impersonation.* Weitere Informationen finden Sie unter [Schützen von Skriptclients.](securing-scripting-clients.md)

Weitere Informationen finden Sie unter [Schützen von Skriptclients.](securing-scripting-clients.md)


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... Fehler in WMI behandeln?
</dt> <dd>

Für die Skripterstellungs-API für WMI kann der Anbieter ein [**SWbemLastError-Objekt**](swbemlasterror.md) zur Verfügung stellen, um weitere Informationen zu einem Fehler zu erhalten.

Insbesondere in VBScript wird die Fehlerbehandlung auch mithilfe des nativen **Err-Objekts** unterstützt. Sie können auch auf das [**SWbemLastError-Objekt**](swbemlasterror.md)zugreifen, wie oben beschrieben. Weitere Informationen finden Sie unter [Abrufen eines Fehlercodes.](retrieving-an-error-code.md)

Für PowerShell können Sie die standardmäßigen PowerShell-Fehlerbehandlungstechniken verwenden. Weitere Informationen finden Sie unter [Einführung in die Fehlerbehandlung in PowerShell.](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell)


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 
