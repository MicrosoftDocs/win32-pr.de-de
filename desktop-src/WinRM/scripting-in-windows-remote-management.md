---
title: Skripterstellung in Windows Remoteverwaltung
description: Die Skript-API in WinRM und die zugehörige COM-API für C++ sind so konzipiert, dass sie die Vorgänge des WS-Management Protokolls genau widerspiegeln.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Skripterstellung in Windows Remoteverwaltung
- Windows Remoteverwaltung, Skripterstellung in
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c10d36420b2826162a6ed5e3fb6bf69408a74032faafac75c84c25a754cf534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795430"
---
# <a name="scripting-in-windows-remote-management"></a>Skripterstellung in Windows Remoteverwaltung

Die [Skript-API in WinRM](winrm-scripting-api.md) und die zugehörige COM-API für C++ sind so konzipiert, dass sie die Vorgänge des WS-Management Protokolls genau widerspiegeln.

Die WinRM-Skripterstellungs-API in Windows Remoteverwaltung unterstützt alle WS-Management-Protokollvorgänge mit Ausnahme eines. Abonnements für Ereignisse sind nicht zulässig. Um Ereignisse aus dem BMC-Systemereignisprotokoll zu abonnieren, müssen Sie die Befehlszeilentools Wecutil oder Wevtutil verwenden. Weitere Informationen finden Sie unter [Ereignisse](events.md).

Die WinRM Scripting-API wird von Winrm.vbs aufgerufen, einem Befehlszeilentool, das in Visual Basic Scripting Edition (VBScript) geschrieben ist. Winrm.vbs enthält Beispiele für die Verwendung der [WinRM-Skript-API.](winrm-scripting-api.md)

## <a name="using-wsman-compared-to-using-wmi-scripting"></a>Verwenden von WSman im Vergleich zur Verwendung von WMI-Skripts

WMI stellt über DCOM eine Verbindung mit Remotecomputern her. Hierfür ist die konfiguration erforderlich, die unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer)beschrieben ist. WinRM verwendet DCOM nicht, um eine Verbindung mit einem Remotecomputer herzustellen. Stattdessen sendet das WS-Management-Protokoll SOAP-Nachrichten, und der Dienst verwendet einen einzelnen Port für HTTP und einen Port für den HTTPS-Transport.

Im Gegensatz zum **Befehlszeilentool winrm** müssen Skripts den XML-Code bereitstellen, der für die Übergabe an die WS-Management Protokollmeldungen erforderlich ist. Sie müssen auch URIs bereitstellen. Weitere Informationen finden Sie unter [Ressourcen-URIs](resource-uris.md) und [Windows Remoteverwaltung und WMI.](windows-remote-management-and-wmi.md)

Die WMI-Skripterstellungs-API funktioniert mit -Objekten, z. B. Instanzen von [**Win32 \_ LogicalDisk,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)die Ressourcen auf einem Computer darstellen. Diese WMI-Klasse wird in [*mof-Dateien (Managed Object Format)*](/windows/desktop/WmiSdk/gloss-m) definiert, die im WMI-Repository in binärer Form gespeichert werden. In WMI gibt ein Get-Vorgang für eine einzelne Ressource oder eine Abfrage für mehrere Instanzen WMI-Objekte zurück.

Ein WinRM-Skript gibt keine Objekte zurück, sondern xml-Textstreams. Weitere Informationen finden Sie unter [Windows Remoteverwaltung und WMI.](windows-remote-management-and-wmi.md)

## <a name="displaying-xml-output-from-winrm-scripts"></a>Anzeigen der XML-Ausgabe von WinRM-Skripts

Die WinRM-Skript-API ruft XML-Zeichenfolgen ab, die Ressourcen beschreiben, und empfängt sie. Das resultierende XML hat die Form eines Textstreams und erfordert, dass eine XML-Transformation auf andere Weise angezeigt wird.

Das folgende WinRM-Skript erzeugt eine unformatierte XML-Ausgabe.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



Der folgende Textblock zeigt die XML-Ausgabe des WinRM-Skripts.


```XML
<p:Win32_Service xmlns:xsi="https://www.w3.org/2001/XMLSchema-
instance" xmlns:p="http://schemas.microsoft.com/wbem/wsman/1
/wmi/root/cimv2/Win32_Service" xmlns:cim="https://schemas.dmtf
.org/wbem/wsman/1/base" cim:Class="Win32_Service"><p:AcceptP
ause>false</p:AcceptPause><p:AcceptStop>true</p:AcceptStop>
<p:Caption>Print Spooler</p:Caption><p:CheckPoint>0</p:CheckP
oint><p:CreationClassName>Win32_Service</p:CreationClassName>
<p:Description>Loads files to memory for later printing</p:De
scription><p:DesktopInteract>true</p:DesktopInteract><p:Displ
ayName>Print Spooler</p:DisplayName><p:ErrorControl>Normal</p
:ErrorControl><p:ExitCode>0</p:ExitCode><p:InstallDate xsi:ni
l="true"/><p:Name>spooler</p:Name><p:PathName>C:\Windows\Syst
em32\spoolsv.exe</p:PathName><p:ProcessId>1720</p:ProcessId><
p:ServiceSpecificExitCode>0</p:ServiceSpecificExitCode><p:Ser
viceType>Own Process</p:ServiceType><p:Started>true</p:Starte
d><p:StartMode>Auto</p:StartMode><p:StartName>LocalSystem</p:
StartName><p:State>Running</p:State><p:Status>OK</p:Status><p
:SystemCreationClassName>Win32_ComputerSystem</p:SystemCreati
onClassName><p:SystemName>wsplab6-4</p:SystemName><p:TagId>0<
/p:TagId><p:WaitHint>0</p:WaitHint><cim:Location xmlns:cim="h
ttp://schemas.dmtf.org/wbem/wsman/1/base" xmlns:a="https://sc
hemas.xmlsoap.org/ws/2004/08/addressing" xmlns:w="https://sche
mas.dmtf.org/wbem/wsman/1/wsman"><a:Address>https://schemas.xm
lsoap.org/ws/2004/08/addressing/role/anonymous</a:Address><a:
ReferenceParameters><w:ResourceURI>https://schemas.microsoft.c
om/wbem/wsman/1/wmi/root/cimv2/Win32_Service</w:ResourceURI><
w:SelectorSet><w:Selector Name="Name">spooler</w:Selector></w
:SelectorSet></a:ReferenceParameters></cim:Location></p:Win32
_Service>
```



Ihre Skripts können eine XML-Transformation verwenden, um diese Ausgabe lesbarer zu machen. Weitere Informationen finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts.](displaying-xml-output-from-winrm-scripts.md)

Die folgende Version des Skripts formatiert den XML-Code in eine für Menschen lesbare Ausgabe.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xslFile.Load( "WsmTxt.xsl" )
Wscript.Echo xmlFile.TransformNode( xslFile )
```



Die XSL-Transformation erstellt die folgende Ausgabe.


```XML
Win32_Service
    AcceptPause = false
    AcceptStop = true
    Caption = Print Spooler
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = Loads files to memory for later printing
    DesktopInteract = true
    DisplayName = Print Spooler
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = Spooler
    PathName = C:\Windows\System32\spoolsv.exe
    ProcessId = 1720
    ServiceSpecificExitCode = 0
    ServiceType = Own Process
    Started = true
    StartMode = Auto
    StartName = LocalSystem
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = wsplab6-4
    TagId = 0
    WaitHint = 0
```



## <a name="winrm-script-and-winrmcmd-output"></a>WinRM-Skript und Winrm.cmd-Ausgabe

Die Ausgabe eines WinRM-Skripts wird in Unicode codiert. Wenn Sie ein [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) erstellen und eine Datei aus dem Skript schreiben, ist die resultierende Datei Unicode. Wenn Sie die Ausgabe jedoch an eine Datei umleiten, ist die Codierung ANSI. Wenn Sie die Ausgabe an eine XML-Datei umleiten und die Ausgabe Unicode-Zeichen enthält, ist der XML-Code ungültig. Beachten Sie,  dass das Winrm-Befehlszeilentool ANSI ausgibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden der Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Msxsl](/previous-versions/windows/desktop/ms763742(v=vs.85))
</dt> <dt>

[DOM-Referenz](/previous-versions/windows/desktop/ms764730(v=vs.85))
</dt> </dl>

 

 