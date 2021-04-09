---
title: Skripterstellung in Windows-Remoteverwaltung
description: Die Skript-API in WinRM und die dazugehörige com-API für C++ sind so konzipiert, dass Sie die Vorgänge des WS-Management Protokolls genau widerspiegeln.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Skripterstellung in Windows-Remoteverwaltung
- Windows-Remoteverwaltung, Skripterstellung in
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 75af10fea03853de99c884eda0a74ce340683b49
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101675"
---
# <a name="scripting-in-windows-remote-management"></a><span data-ttu-id="995fa-105">Skripterstellung in Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="995fa-105">Scripting in Windows Remote Management</span></span>

<span data-ttu-id="995fa-106">Die [Skript-API in WinRM](winrm-scripting-api.md) und die dazugehörige com-API für C++ sind so konzipiert, dass Sie die Vorgänge des WS-Management Protokolls genau widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="995fa-106">The [Scripting API in WinRM](winrm-scripting-api.md) and the accompanying COM API for C++ are designed to closely reflect the operations of the WS-Management protocol.</span></span>

<span data-ttu-id="995fa-107">Die WinRM-Skript-API in Windows-Remoteverwaltung unterstützt alle WS-Management Protokoll Vorgänge mit Ausnahme von 1.</span><span class="sxs-lookup"><span data-stu-id="995fa-107">The WinRM Scripting API in Windows Remote Management supports all the WS-Management protocol operations except one.</span></span> <span data-ttu-id="995fa-108">Abonnements für Ereignisse können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="995fa-108">It does not allow subscriptions to events.</span></span> <span data-ttu-id="995fa-109">Zum Abonnieren von Ereignissen aus dem BMC-System Ereignisprotokoll müssen Sie die Befehlszeilen Tools "wecutil" oder "wevtutil" verwenden.</span><span class="sxs-lookup"><span data-stu-id="995fa-109">To subscribe to events from the BMC System Event Log, you must use the Wecutil or Wevtutil command-line tools.</span></span> <span data-ttu-id="995fa-110">Weitere Informationen finden Sie unter [Ereignisse](events.md).</span><span class="sxs-lookup"><span data-stu-id="995fa-110">For more information, see [Events](events.md).</span></span>

<span data-ttu-id="995fa-111">Die WinRM-Skript-API wird von Winrm.vbs, einem Befehlszeilen Tool, das in Visual Basic Scripting Edition (VBScript) geschrieben ist, aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="995fa-111">The WinRM Scripting API is called by Winrm.vbs, a command-line tool, which is written in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="995fa-112">Winrm.vbs enthält Beispiele für die Verwendung der [WinRM-Skript-API](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="995fa-112">Winrm.vbs provides examples of how to use the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

## <a name="using-wsman-compared-to-using-wmi-scripting"></a><span data-ttu-id="995fa-113">Verwenden von WSMAN im Vergleich zur Verwendung von WMI-Skripting</span><span class="sxs-lookup"><span data-stu-id="995fa-113">Using WSman Compared to Using WMI Scripting</span></span>

<span data-ttu-id="995fa-114">WMI stellt über DCOM eine Verbindung mit Remote Computern her. hierfür ist die Konfiguration erforderlich, die unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="995fa-114">WMI connects to remote computers through DCOM, which requires the configuration described in [Connecting to WMI on a Remote Computer](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span></span> <span data-ttu-id="995fa-115">WinRM verwendet nicht DCOM, um eine Verbindung mit einem Remote Computer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="995fa-115">WinRM does not use DCOM to connect to a remote computer.</span></span> <span data-ttu-id="995fa-116">Stattdessen sendet das WS-Management Protokoll SOAP-Nachrichten, und der Dienst verwendet einen einzelnen Port für http und einen Port für den HTTPS-Transport.</span><span class="sxs-lookup"><span data-stu-id="995fa-116">Instead, the WS-Management protocol sends SOAP messages and the service uses a single port for HTTP and a port for HTTPS transport.</span></span>

<span data-ttu-id="995fa-117">Im Gegensatz zum **WinRM** -Befehlszeilen Tool müssen Skripts das XML bereitstellen, das für die Übergabe an die WS-Management-Protokollnachrichten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="995fa-117">Unlike the **winrm** command-line tool, scripts must provide the XML required to pass to the WS-Management protocol messages.</span></span> <span data-ttu-id="995fa-118">Sie müssen auch URIs bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="995fa-118">They must also provide URIs.</span></span> <span data-ttu-id="995fa-119">Weitere Informationen finden Sie unter [Ressourcen-URIs](resource-uris.md) und [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="995fa-119">For more information, see [Resource URIs](resource-uris.md) and [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="995fa-120">Die WMI-Skript-API funktioniert mit Objekten, wie z. b. Instanzen von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), die Ressourcen auf einem Computer darstellen.</span><span class="sxs-lookup"><span data-stu-id="995fa-120">The WMI Scripting API works with objects, such as instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which represent resources on a computer.</span></span> <span data-ttu-id="995fa-121">Diese WMI-Klasse wird in [*Managed Object Format Dateien (MOF*](/windows/desktop/WmiSdk/gloss-m) -Dateien) definiert, die im WMI-Repository im Binärformat gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="995fa-121">This WMI class is defined in [*Managed Object Format (MOF)*](/windows/desktop/WmiSdk/gloss-m) files, which are stored in binary form in the WMI repository.</span></span> <span data-ttu-id="995fa-122">In WMI gibt ein Get-Vorgang für eine einzelne Ressource oder eine Abfrage für mehrere Instanzen WMI-Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="995fa-122">In WMI, a Get operation for a single resource or a query for multiple instances returns WMI objects.</span></span>

<span data-ttu-id="995fa-123">Ein WinRM-Skript gibt keine Objekte zurück, sondern stattdessen XML-Text Ströme.</span><span class="sxs-lookup"><span data-stu-id="995fa-123">A WinRM script does not return objects, but rather streams of XML text.</span></span> <span data-ttu-id="995fa-124">Weitere Informationen finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="995fa-124">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="995fa-125">Anzeigen der XML-Ausgabe von WinRM-Skripts</span><span class="sxs-lookup"><span data-stu-id="995fa-125">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="995fa-126">Die WinRM-Skript-API ruft XML-Zeichen folgen ab, die Ressourcen beschreiben und empfängt.</span><span class="sxs-lookup"><span data-stu-id="995fa-126">The WinRM Scripting API gets and receives XML strings that describe resources.</span></span> <span data-ttu-id="995fa-127">Das resultierende XML-Format ist in Form eines Textstreams und erfordert, dass eine XML-Transformation auf andere Weise angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="995fa-127">The resultant XML is in the form of a text stream and requires an XML transform to be displayed in some other way.</span></span>

<span data-ttu-id="995fa-128">Das folgende WinRM-Skript erzeugt eine unformatierte XML-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="995fa-128">The following WinRM script produces raw XML output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



<span data-ttu-id="995fa-129">Der folgende TextBlock zeigt die XML-Ausgabe des WinRM-Skripts.</span><span class="sxs-lookup"><span data-stu-id="995fa-129">The following block of text shows the XML output from the WinRM script.</span></span>


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



<span data-ttu-id="995fa-130">Ihre Skripts können eine XML-Transformation verwenden, um diese Ausgabe lesbarer zu machen.</span><span class="sxs-lookup"><span data-stu-id="995fa-130">Your scripts can use an XML transform to make this output more readable.</span></span> <span data-ttu-id="995fa-131">Weitere Informationen finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="995fa-131">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="995fa-132">Die folgende Version des Skripts formatiert den XML-Code in eine lesbare Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="995fa-132">The following version of the script formats the XML into human-readable output.</span></span>


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



<span data-ttu-id="995fa-133">Die XSL-Transformation erstellt die folgende Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="995fa-133">The XSL transform creates the following output.</span></span>


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



## <a name="winrm-script-and-winrmcmd-output"></a><span data-ttu-id="995fa-134">WinRM-Skript und WinRM. cmd-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="995fa-134">WinRM Script and Winrm.cmd Output</span></span>

<span data-ttu-id="995fa-135">Die Ausgabe eines WinRM-Skripts wird in Unicode codiert.</span><span class="sxs-lookup"><span data-stu-id="995fa-135">The output from a WinRM script is encoded in Unicode.</span></span> <span data-ttu-id="995fa-136">Wenn Sie ein [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) erstellen und eine Datei aus dem Skript schreiben, ist die resultierende Datei Unicode.</span><span class="sxs-lookup"><span data-stu-id="995fa-136">If you create a [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) and write a file from the script, the resulting file is Unicode.</span></span> <span data-ttu-id="995fa-137">Wenn Sie die Ausgabe jedoch in eine Datei umleiten, ist die Codierung ANSI.</span><span class="sxs-lookup"><span data-stu-id="995fa-137">However, if you redirect the output to a file, the encoding is ANSI.</span></span> <span data-ttu-id="995fa-138">Wenn Sie die Ausgabe an eine XML-Datei umleiten und Unicode-Zeichen in der Ausgabe vorhanden sind, ist die XML ungültig.</span><span class="sxs-lookup"><span data-stu-id="995fa-138">If you redirect the output to an XML file and there are Unicode characters in the output, the XML will be invalid.</span></span> <span data-ttu-id="995fa-139">Beachten Sie, dass das **WinRM** -Befehlszeilen Tool ANSI ausgibt.</span><span class="sxs-lookup"><span data-stu-id="995fa-139">Be aware that the **Winrm** command-line tool outputs ANSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="995fa-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="995fa-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="995fa-141">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="995fa-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="995fa-142">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="995fa-142">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

<span data-ttu-id="995fa-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="995fa-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="995fa-144">[DOM-Referenz](/previous-versions/windows/desktop/ms764730(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="995fa-144">[DOM Reference](/previous-versions/windows/desktop/ms764730(v=vs.85))</span></span>
</dt> </dl>

 

 