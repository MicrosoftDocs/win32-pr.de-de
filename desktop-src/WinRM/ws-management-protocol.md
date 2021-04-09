---
title: WS-Verwaltungsprotokoll
description: Ein öffentlicher Standard für den Remote Austausch von Verwaltungsdaten mit jedem Computer Gerät, das das Protokoll implementiert.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e01fdc860eeb5510dd78a4127fdc22b30d711a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102306"
---
# <a name="ws-management-protocol"></a><span data-ttu-id="487bd-103">WS-Verwaltungsprotokoll</span><span class="sxs-lookup"><span data-stu-id="487bd-103">WS-Management Protocol</span></span>

<span data-ttu-id="487bd-104">Das WS-Verwaltungsprotokoll wurde von einer Gruppe von Hardware- und Softwareherstellern als öffentlicher Standard für den Remoteaustausch von Verwaltungsdaten mit beliebigen Geräten entwickelt, die das Protokoll implementieren.</span><span class="sxs-lookup"><span data-stu-id="487bd-104">The WS-Management protocol was developed by a group of hardware and software manufacturers as a public standard for remotely exchanging management data with any computer device that implements the protocol.</span></span>

## <a name="standards"></a><span data-ttu-id="487bd-105">Standards</span><span class="sxs-lookup"><span data-stu-id="487bd-105">Standards</span></span>

<span data-ttu-id="487bd-106">Weitere Informationen zum WS-Management-Protokoll finden Sie unter [Spezifikation der Web Services for Management (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span><span class="sxs-lookup"><span data-stu-id="487bd-106">For more information about WS-Management protocol, see [Web Services for Management (WS-Management) Specification](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span></span>

<span data-ttu-id="487bd-107">Der Zweck des Protokolls besteht darin, Konsistenz und Interoperabilität für Verwaltungsvorgänge auf vielen Arten von Geräten (einschließlich Firmware) und Betriebssystemen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="487bd-107">The intent of the protocol is to provide consistency and interoperability for management operations across many types of devices (including firmware) and operating systems.</span></span> <span data-ttu-id="487bd-108">WS-Management Protokoll kann erweitert werden, wenn neue Vorgänge von der IT-Branche identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="487bd-108">WS-Management protocol can be extended as new operations are identified by the IT industry.</span></span>

<span data-ttu-id="487bd-109">Die aktuelle Implementierung des WS-Management Protokolls basiert auf den folgenden Standardspezifikationen: https, SOAP über HTTP (WS-I Profile), SOAP 1,2, WS-Adressierung, WS-Transfer, WS-Enumeration und WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="487bd-109">The current implementation of the WS-Management protocol is based on the following standard specifications: HTTPS, SOAP over HTTP (WS-I profile), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration, and WS-Eventing.</span></span> <span data-ttu-id="487bd-110">Weitere Informationen zu den WS-Management Standards und XML-Schemas finden Sie unter. <https://dmtf.org/standards/wsman></span><span class="sxs-lookup"><span data-stu-id="487bd-110">For more information about the WS-Management standards and XML schemas see <https://dmtf.org/standards/wsman></span></span>

## <a name="messages"></a><span data-ttu-id="487bd-111">Meldungen</span><span class="sxs-lookup"><span data-stu-id="487bd-111">Messages</span></span>

<span data-ttu-id="487bd-112">Das WS-Management-Protokoll stellt einen Standard zum Erstellen von XML- [*Nachrichten*](windows-remote-management-glossary.md) mithilfe verschiedener Webdienst Standards wie [*WS-Adressierung*](windows-remote-management-glossary.md) und [*WS-Transfer*](windows-remote-management-glossary.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="487bd-112">The WS-Management protocol provides a standard for constructing XML [*messages*](windows-remote-management-glossary.md) using various web service standards such as [*WS-Addressing*](windows-remote-management-glossary.md) and [*WS-Transfer*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="487bd-113">Diese Standards definieren XML-Schemas für Webdienst Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="487bd-113">These standards define XML schemas for web service messages.</span></span> <span data-ttu-id="487bd-114">Die Nachrichten verweisen auf eine [*Ressource*](windows-remote-management-glossary.md) , die einen [*Ressourcen-URI*](windows-remote-management-glossary.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="487bd-114">The messages refer to a [*resource*](windows-remote-management-glossary.md) using a [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="487bd-115">Das WS-Management-Protokoll fügt einen Satz von Definitionen für Verwaltungsvorgänge und Werte hinzu.</span><span class="sxs-lookup"><span data-stu-id="487bd-115">The WS-Management protocol adds a set of definitions for management operations and values.</span></span> <span data-ttu-id="487bd-116">Beispielsweise definiert WS-Transfer die Vorgänge "Get", "Put", "Create" und "Delete" für eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="487bd-116">For example, WS-Transfer defines the Get, Put, Create, and Delete operations for a resource.</span></span> <span data-ttu-id="487bd-117">WS-Management Protokoll fügt rename, partielle Get und partielle Put hinzu.</span><span class="sxs-lookup"><span data-stu-id="487bd-117">WS-Management protocol adds Rename, Partial Get, and Partial Put.</span></span>

<span data-ttu-id="487bd-118">Die Nachrichten folgen den Konventionen von [*SOAP (Simple Object Access Protocol)*](windows-remote-management-glossary.md) , die von allen Webdienst Protokollen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="487bd-118">The messages follow the conventions of [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md) which is used by all web service protocols.</span></span>

<span data-ttu-id="487bd-119">Das folgende Codebeispiel zeigt eine Meldung mit einem Get-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="487bd-119">The following code example shows a message with a Get operation.</span></span> <span data-ttu-id="487bd-120">Dieses Beispiel wird als Hilfe zum Verständnis der zugrunde liegenden Nachrichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="487bd-120">This example is shown as an aid to understanding what the underlying messages look like.</span></span> <span data-ttu-id="487bd-121">Sie müssen nicht wissen, wie SOAP-Nachrichten erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="487bd-121">You do not need to know how to produce SOAP messages.</span></span> <span data-ttu-id="487bd-122">Die Nachrichten werden von Windows-Remoteverwaltung assembliert, wenn Sie mit dem **WinRM** -Befehlszeilen Tool einen Befehl ausführen oder ein Skript ausführen, das mit der [WinRM-Skript-API](winrm-scripting-api.md)geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="487bd-122">The messages are assembled by Windows Remote Management when you execute a command using the **Winrm** command-line tool or run a script written with the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="487bd-123">Die Meldung ist eine Anforderung, die Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) mit der **DeviceID** -Eigenschaft "c:" von einem Server mit dem Namen "Remotecomputer" zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="487bd-123">The message is a request to get the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) with a **DeviceID** property of "c:" from a server named RemoteComputer.</span></span> <span data-ttu-id="487bd-124">Die Anforderung verwendet den HTTP-Transport über Port 80.</span><span class="sxs-lookup"><span data-stu-id="487bd-124">The request uses the HTTP transport through port 80.</span></span> <span data-ttu-id="487bd-125">Das Konto, das die Anforderung sendet, muss sich in der lokalen Gruppe "Administratoren" auf dem Remote Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="487bd-125">The account sending the request must be in the local administrators group on the remote computer.</span></span>

<span data-ttu-id="487bd-126">Die Zeichen vor dem Doppelpunkt am Anfang jedes Tags geben an, welcher Standard das XML-Element definiert.</span><span class="sxs-lookup"><span data-stu-id="487bd-126">The characters before the colon at the beginning of each tag indicate which standard defines the XML element.</span></span> <span data-ttu-id="487bd-127">Beispielsweise ` <wsa:To>` gibt an, dass das to-Element durch den WS-Addressing-Standard definiert wird, und `<s:Header>` gibt den Anfang des Header Inhalts in einer SOAP-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="487bd-127">For example, ` <wsa:To>` indicates that the To element is defined by the WS-Addressing standard and `<s:Header>` indicates the beginning of the header content in a SOAP message.</span></span> <span data-ttu-id="487bd-128">Beachten Sie, dass der Großteil der Nachricht aus XML-Elementen besteht, die von SOAP oder WS-Adressierung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="487bd-128">Be aware that the majority of the message is composed of XML elements defined by SOAP or WS-Addressing.</span></span> <span data-ttu-id="487bd-129">WS-Management Protokoll fügt MaxEnvelopeSize, Selector und selectorset hinzu.</span><span class="sxs-lookup"><span data-stu-id="487bd-129">WS-Management protocol adds MaxEnvelopeSize, Selector, and SelectorSet.</span></span>


```XML
<s:Envelope xmlns:s="https://www.w3.org/2003/05/soap-envelope" 
            xmlns:a="https://schemas.xmlsoap.org/ws/2004/08/addressing" 
            xmlns:w="https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd">
  <s:Header>
    <a:To>https://RemoteComputer:80/wsman</a:To> 
    <w:ResourceURI s:mustUnderstand="true">
      http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_logicaldisk
    </w:ResourceURI> 
    <a:ReplyTo>
    <a:Address s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </a:Address> 
    </a:ReplyTo>
    <a:Action s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </a:Action> 
    <w:MaxEnvelopeSize s:mustUnderstand="true">153600</w:MaxEnvelopeSize> 
    <a:MessageID>uuid:4ED2993C-4339-4E99-81FC-C2FD3812781A</a:MessageID> 
    <w:Locale xml:lang="en-US" s:mustUnderstand="false"/> 
    <w:SelectorSet>
    <w:Selector Name="DeviceId">c:</w:Selector> 
    </w:SelectorSet>
    <w:OperationTimeout>PT60.000S</w:OperationTimeout> 
  </s:Header>
  <s:Body/> 
</s:Envelope>
```



## <a name="related-topics"></a><span data-ttu-id="487bd-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="487bd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="487bd-131">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="487bd-131">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="487bd-132">Remote Hardware Verwaltung</span><span class="sxs-lookup"><span data-stu-id="487bd-132">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> </dl>

 

 