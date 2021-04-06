---
description: Mithilfe von Skripts können Sie alle Informationen anzeigen oder bearbeiten, die über WMI verfügbar gemacht werden.
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
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960894"
---
# <a name="creating-a-wmi-script"></a>Erstellen eines WMI-Skripts

Mithilfe von Skripts können Sie alle Informationen anzeigen oder bearbeiten, die über WMI verfügbar gemacht werden. Skripts können in jeder Skriptsprache geschrieben werden, die das Hosting von Microsoft-ActiveX-Skripts unterstützt, einschließlich Visual Basic Scripting Edition (VBScript), PowerShell und perl. WMI-Skripts können von Windows Script Host (WSH), Active Server Seiten und Internet Explorer gehostet werden.

> [!Note]
>
> Die primäre Skriptsprache, die derzeit von WMI unterstützt wird, ist PowerShell. WMI enthält jedoch auch einen robusten Text der Skriptunterstützung für VBScript und andere Sprachen, die auf die [Skript-API für WMI](scripting-api-for-wmi.md)zugreifen.

 

## <a name="wmi-scripting-languages"></a>WMI-Skriptsprachen

Die zwei Hauptsprachen, die von WMI unterstützt werden, sind PowerShell und VBScript (über den Windows Script Host oder WSH).

-   **PowerShell** wurde mit einer engen Integration in WMI entworfen. Daher sind viele der zugrunde liegenden Elemente von WMI in die WMI-Cmdlets integriert: [Get-WMIObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Aufruf-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)und [Remove-WMIObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1). In der folgenden Tabelle werden die allgemeinen Prozesse für den Zugriff auf WMI-Informationen beschrieben. Beachten Sie, dass zwar die meisten dieser Beispiele Get-WMIObject verwenden, aber viele der PowerShell-WMI-Cmdlets dieselben Parameter haben, wie z. b. *-Class* oder *--Anmelde* Informationen. Daher funktionieren viele dieser Prozesse auch für andere Objekte. Eine ausführlichere Erläuterung von PowerShell und WMI finden [Sie unter Verwenden des Get-WMiObject Cmdlets](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) und [Windows PowerShell-der WMI-Verbindung](/previous-versions/technet-magazine/cc162365(v=msdn.10)).

-   **VBScript** führt dagegen explizit Aufrufe an die [Skript-API für WMI aus](scripting-api-for-wmi.md), wie oben erwähnt. Andere Sprachen, wie z. b. perl, können auch die Skript-API für WMI verwenden. Im Rahmen dieser Dokumentation wird jedoch in den meisten Beispielen, die die Skript-API für WMI veranschaulichen, VBScript verwendet. Wenn ein Programmierverfahren für VBScript spezifisch ist, wird es jedoch als "out" bezeichnet.

    VBScript bietet im Wesentlichen zwei separate Möglichkeiten für den Zugriff auf WMI. Der erste verwendet zum Herstellen einer Verbindung mit WMI ein "WS- [**Locator**](swbemlocator.md) "-Objekt. Alternativ können Sie [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) und einen Moniker verwenden. Ein Moniker ist eine Zeichenfolge, die eine Reihe von Elementen beschreiben kann: Ihre Anmelde Informationen, die Identitätswechsel Einstellungen, den Computer, mit dem Sie eine Verbindung herstellen möchten, den WMI- [*Namespace*](gloss-n.md) (d.h. den allgemeinen Speicherort, an dem WMI Gruppen von Objekten speichert) und das WMI-Objekt, das Sie abrufen möchten. Viele der Beispiele unten beschreiben beide Techniken. Weitere Informationen finden Sie unter [Erstellen einer Monikerzeichenfolge](constructing-a-moniker-string.md) und [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).

    Unabhängig von der Methode, die Sie zum Herstellen einer Verbindung mit WMI verwenden, werden Sie wahrscheinlich ein oder mehrere Objekte aus der Skript-API abrufen. Der häufigste Wert ist " [**errbewbject**](swbemobject.md)", der von WMI zum Beschreiben eines WMI-Objekts verwendet wird. Alternativ dazu können Sie ein " [**errbemservices**](swbemservices.md) "-Objekt verwenden, um den WMI-Dienst selbst zu beschreiben, oder ein " [**errbewbjectpath**](swbemobjectpath.md) "-Objekt, um den Speicherort eines WMI-Objekts zu beschreiben. Weitere Informationen finden Sie unter [Skripterstellung mit "Swap](scripting-with-swbemobject.md) Helper"- [Objekten](scripting-helper-objects.md).

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a>Gewusst wie: Verwenden von WMI und einer Skriptsprache

<dl> <dt>

<span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... Verbindung mit WMI herstellen?
</dt> <dd>

Rufen Sie für VBScript und die Skript-API für WMI ein [**-Objekt mit einem**](swbemservices.md) Moniker und einem Aufruf von [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))ab. Alternativ können Sie eine Verbindung mit dem Server herstellen, indem Sie den [**Befehl "Swap-Server. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)" aufzurufen. Anschließend können Sie das-Objekt verwenden, um auf einen bestimmten WMI-Namespace oder eine bestimmte WMI-Klasseninstanz zuzugreifen.

Für PowerShell erfolgt die Verbindung mit WMI in der Regel direkt im Cmdlet-Befehl. Daher sind keine weiteren Schritte erforderlich.

Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md), [Erstellen einer Monikerzeichenfolge](constructing-a-moniker-string.md)und [Herstellen einer Verbindung mit WMI mit VBScript](connecting-to-wmi-with-vbscript.md).


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

<span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... Abrufen von Informationen aus WMI
</dt> <dd>

Verwenden Sie für VBScript und die Skript-API für WMI eine Abruf Funktion, z. b. [**wbemServices. Get**](swbemservices-get.md) oder [**wbemServices. InstancesOf**](swbemservices-instancesof.md). Sie können auch den Klassennamen des Objekts platzieren, das in einem Moniker abgerufen werden kann. Dies kann effizienter sein.

Verwenden Sie für PowerShell den *-Class-* Parameter. Beachten Sie, dass-Class der Standardparameter ist. Daher müssen Sie ihn nicht explizit angeben.

Weitere Informationen finden Sie unter [Abrufen von WMI-Klassen-oder Instanzdaten](retrieving-class-or-instance-data.md).


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

<span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... Erstellen Sie eine WMI-Abfrage?
</dt> <dd>

Verwenden Sie für VBScript und die Skript-API für WMI die [**SWbemServices.Execquery**](swbemservices-execquery.md) -Methode.

Verwenden Sie für PowerShell den *-Query-* Parameter. Sie können auch mit dem *-Filter-* Parameter filtern.

Weitere Informationen finden Sie unter [WMI-Abfrage](querying-wmi.md).


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

<span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... durchlaufen Sie eine Liste von WMI-Objekten?
</dt> <dd>

Verwenden Sie für VBScript und die Skript-API für WMI das in einem Skript behandelte Objekt " [**errbewbjectset**](swbemobjectset.md) " als eine Auflistung, die aufgelistet werden kann. Sie können ein " **errbemubjectset** " aus einem- [**Befehl von "errbemservices. InstancesOf**](swbemservices-instancesof.md) " oder [**SWbemServices.Execquery**](swbemservices-execquery.md)abrufen.

PowerShell kann Enumerationen wie jedes andere Objekt abrufen und verarbeiten. Es gibt keine besonderen Besonderheiten bei WMI.

Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).


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

<span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... greifen Sie auf einen anderen WMI-Namespace zu?
</dt> <dd>

Geben Sie für VBScript und die Skript-API für WMI den Namespace im Moniker an. andernfalls können Sie den Namespace im Aufruf von "WS. [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)" explizit angeben.

Verwenden Sie für PowerShell den Parameter *-Namespace* . Der Standard Namespace ist "root \\ cimV2", aber viele ältere Klassen werden in "root \\ default" gespeichert.

Wenn Sie den Speicherort einer bestimmten WMI-Klasse ermitteln möchten, sehen Sie sich die Referenzseite an. Alternativ können Sie einen Namespace mithilfe von Get-WMIObject manuell durchsuchen.


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

Für Sprachen, die die Skript-API für WMI und PowerShell direkt verwenden, unterstützt WMI das Abrufen der untergeordneten Klassen einer Basisklasse. Um die untergeordneten Instanzen abzurufen, müssen Sie daher nur nach der übergeordneten Klasse suchen. Im folgenden Beispiel wird nach [**CIM \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk)gesucht. Hierbei handelt es sich um eine vorinstallierte WMI-Klasse, die logische Datenträger auf einem Windows-basierten Computersystem darstellt. Daher gibt die Suche nach dieser übergeordneten Klasse auch Instanzen von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)zurück. Dies ist das, was von Windows verwendet wird, um Festplatten zu beschreiben. Weitere Informationen finden Sie unter [Common Information Model](common-information-model.md). WMI stellt ein gesamtes Schema mit vorinstallierten Klassen bereit, mit denen Sie auf verwaltete Objekte zugreifen und diese steuern können. Weitere Informationen finden Sie unter [Win32-Klassen](/windows/desktop/CIMWin32Prov/win32-provider) und [WMI-Klassen](wmi-classes.md).


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... Suchen Sie ein WMI-Objekt?
</dt> <dd>

Bei der Skript-API für WMI und PowerShell verwendet WMI eine Kombination aus Namespace, Klassenname und Schlüsseleigenschaften, um eine bestimmte WMI-Instanz eindeutig zu identifizieren. Dies wird auch als WMI-Objekt Pfad bezeichnet. Für VBScript beschreibt die Eigenschaft " [**Swap. Path \_**](swbemobject-path-.md) " den Pfad für ein beliebiges Objekt, das von der Skript-API zurückgegeben wird. Für PowerShell verfügt jedes WMI-Objekt über eine \_ \_ Path-Eigenschaft. Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md) .

Neben dem Namespace-und Klassennamen verfügt ein WMI-Objekt auch über eine Schlüsseleigenschaft, die diese Instanz im Vergleich zu anderen Instanzen auf dem Computer eindeutig identifiziert. Die **DeviceID** -Eigenschaft ist z. b. die Schlüsseleigenschaft für die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse. Weitere Informationen finden Sie unter [Managed Object Format (MOF)](managed-object-format--mof-.md).

Schließlich ist der relative Pfad einfach eine verkürzte Form des Pfads und enthält den Klassennamen und den Schlüsselwert. In den folgenden Beispielen lautet der Pfad möglicherweise " \\ \\ Computername \\ root \\ CIMV2: Win32 \_ LogicalDisk. toviceid =" D: "", während der relative Pfad "" Win32LogicalDisk. Geräte-ID = "d" "" lauten würde.


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

<span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... Legen Sie Informationen in WMI fest?
</dt> <dd>

Verwenden Sie für VBScript und die Skript-API für WMI die Methode " [**errbemubject. Put \_**](swbemobject-put-.md) ".

Für PowerShell können Sie entweder die Put-Methode oder Else [Set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true)verwenden.

Weitere Informationen finden Sie unter [Ändern einer Instanzeigenschaft](modifying-an-instance-property.md).


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

<span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... Andere Anmelde Informationen verwenden?
</dt> <dd>

Verwenden Sie für VBScript und die Skript-API für WMI die Parameter " *username* " und " *Password* " in der Methode " [**waybemlocator. ConnectServer**](swbemlocator-connectserver.md) ".

Verwenden Sie für PowerShell den *-Credential-* Parameter.

Beachten Sie, dass Sie nur Alternative Anmelde Informationen auf einem Remote System verwenden können. Weitere Informationen finden Sie unter [Sichern von Skript Clients](securing-scripting-clients.md).


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

<span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... auf einen Remote Computer zugreifen?
</dt> <dd>

Geben Sie für VBScript und die Skript-API für WMI explizit den Namen des Computers entweder im Moniker oder andernfalls im Aufruf von "WS. [**ConnectServer**](swbemlocator-connectserver.md)" an. Weitere Informationen finden Sie unter [Herstellen einer Remote Verbindung mit WMI mit VBScript](connecting-to-wmi-remotely-with-vbscript.md).

Verwenden Sie für PowerShell den Parameter " *-Computername* ". Weitere Informationen finden Sie unter [Herstellen einer Remote Verbindung mit WMI mit PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).


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

<span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... Legen Sie die Authentifizierungs-und Identitätswechsel Ebenen fest?
</dt> <dd>

Verwenden Sie für VBScript und die Skript-API für WMI die Eigenschaft " [**Swap Services \_ . Security**](swbemlocator-security-.md) " für das zurückgegebene Server Objekt, oder legen Sie die relevanten Werte im Moniker fest.

Verwenden Sie für PowerShell die Parameter *-Authentication* bzw. *-* Identitätswechsel. Weitere Informationen finden Sie unter [Sichern von Skript Clients](securing-scripting-clients.md).

Weitere Informationen finden Sie unter [Sichern von Skript Clients](securing-scripting-clients.md).


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

<span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... Behandeln von Fehlern in WMI
</dt> <dd>

Der Anbieter kann für die Skript-API für WMI ein " [**taubemlasterror**](swbemlasterror.md) "-Objekt bereitstellen, um weitere Informationen zu einem Fehler zu erhalten.

In VBScript wird die Fehlerbehandlung auch unter Verwendung des nativen **Err** -Objekts unterstützt. Sie können auch wie oben beschrieben auf das Objekt " [**taubemlasterror**](swbemlasterror.md)" zugreifen. Weitere Informationen finden Sie unter [Abrufen eines Fehlercodes](retrieving-an-error-code.md).

Für PowerShell können Sie die Standardverfahren für die PowerShell-Fehlerbehandlung verwenden. Weitere Informationen finden Sie unter [Einführung in die Fehlerbehandlung in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).


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

 

 
