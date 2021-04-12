---
title: Windows-Remoteverwaltung
description: Windows-Remoteverwaltung (Windows-Remoteverwaltung) ist die Microsoft-Implementierung des WS-Management Protokolls, ein Standardmäßiges SOAP-basiertes, firewallfreundliches Protokoll, das die Interoperabilität von Hardware und Betriebssystemen von unterschiedlichen Anbietern ermöglicht.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Windows-Remoteverwaltung (WinRM), Start Seite
- WS-Verwaltung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948772"
---
# <a name="windows-remote-management"></a><span data-ttu-id="d9ef5-105">Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="d9ef5-105">Windows Remote Management</span></span>

## <a name="purpose"></a><span data-ttu-id="d9ef5-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="d9ef5-106">Purpose</span></span>

<span data-ttu-id="d9ef5-107">Bei der Windows-Remoteverwaltung (WinRM) handelt es sich um die Microsoft-Implementierung des [WS-Verwaltungsprotokolls](ws-management-protocol.md)– ein standardmäßiges, SOAP-basiertes und firewallfreundliches Protokoll, das die Zusammenarbeit von Hardware und Betriebssystemen unterschiedlicher Anbieter ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-107">Windows Remote Management (WinRM) is the Microsoft implementation of [WS-Management Protocol](ws-management-protocol.md), a standard Simple Object Access Protocol (SOAP)-based, firewall-friendly protocol that allows hardware and operating systems, from different vendors, to interoperate.</span></span>

<span data-ttu-id="d9ef5-108">Die WS-Management-Protokollspezifikation bietet eine gängige Möglichkeit für Systeme, auf Verwaltungsinformationen in einer IT-Infrastruktur zuzugreifen und diese auszutauschen.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-108">The WS-Management protocol specification provides a common way for systems to access and exchange management information across an IT infrastructure.</span></span> <span data-ttu-id="d9ef5-109">WinRM und [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md)zusammen mit dem [Ereignis Sammler](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) sind Komponenten der Windows- [Hardware Verwaltungs](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) Funktionen.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-109">WinRM and [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md), along with the [Event Collector](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) are components of the [Windows Hardware Management](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) features.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="d9ef5-110">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="d9ef5-110">Where applicable</span></span>

<span data-ttu-id="d9ef5-111">Mit WinRM-Skript Objekten, dem WinRM-Befehlszeilen Tool oder dem Windows-Remoteshell-Befehlszeilen Tool Winrs können Sie Verwaltungsdaten von lokalen Computern und Remote Computern abrufen, die möglicherweise über [*Baseboard-Verwaltungs Controller (Baseboard Management Controllers, BMCs)*](windows-remote-management-glossary.md)verfügen.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-111">You can use WinRM scripting objects, the WinRM command-line tool, or the Windows Remote Shell command line tool WinRS to obtain management data from local and remote computers that may have [*baseboard management controllers (BMCs)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="d9ef5-112">Wenn auf dem Computer eine Windows-basierte Betriebssystemversion mit WinRM ausgeführt wird, werden die Verwaltungsdaten von [Windows-Verwaltungsinstrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-112">If the computer runs a Windows-based operating system version that includes WinRM, the management data is supplied by [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

<span data-ttu-id="d9ef5-113">Sie können in Ihrem Unternehmen auch Hardware- und Systemdaten aus Implementierungen des WS-Verwaltungsprotokolls abrufen, die nicht unter Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-113">You can also obtain hardware and system data from WS-Management protocol implementations running on operating systems other than Windows in your enterprise.</span></span> <span data-ttu-id="d9ef5-114">WinRM richtet eine Sitzung mit einem Remotecomputer über das SOAP-basierte WS-Verwaltungsprotokoll ein, anstatt wie WMI eine Verbindung über DCOM herzustellen.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-114">WinRM establishes a session with a remote computer through the SOAP-based WS-Management protocol rather than a connection through DCOM, as WMI does.</span></span> <span data-ttu-id="d9ef5-115">An das WS-Verwaltungsprotokoll zurückgegebene Daten werden nicht als Objekte, sondern als XML-Daten formatiert.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-115">Data returned to WS-Management protocol are formatted in XML rather than in objects.</span></span>

<span data-ttu-id="d9ef5-116">Der WMI-Anbieter für die [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) ist ein standardmäßiger WMI-Anbieter mit Klassen, die BMC-Sensordaten von Computern mit entsprechender Hardware abrufen.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-116">The [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI provider is a standard WMI provider with classes that obtain BMC sensor data from computers with appropriate hardware.</span></span> <span data-ttu-id="d9ef5-117">Auf IPMI-Daten kann über die WinRM-Skript-API, die WMI- [Skript](/windows/desktop/WmiSdk/scripting-api-for-wmi)Erstellung oder über [com](/windows/desktop/WmiSdk/com-api-for-wmi) -APIs zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-117">IPMI data can be accessed using the WinRM scripting API, the WMI [Scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi), or [COM](/windows/desktop/WmiSdk/com-api-for-wmi) APIs.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d9ef5-118">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="d9ef5-118">Developer audience</span></span>

<span data-ttu-id="d9ef5-119">Die Entwicklergruppe ist der IT-Spezialist, der Skripts zum Automatisieren der Verwaltung von Servern oder des ISV-Entwicklers schreibt, der Daten für Verwaltungs Anwendungen erhält.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-119">The developer audience is the IT Pro who writes scripts to automate the management of servers or the ISV developer obtaining data for management applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d9ef5-120">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="d9ef5-120">Run-time requirements</span></span>

<span data-ttu-id="d9ef5-121">WinRM ist Teil des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-121">WinRM is part of the operating system.</span></span> <span data-ttu-id="d9ef5-122">Zum Abrufen von Daten von Remote Computern müssen Sie jedoch einen WinRM- [*Listener*](windows-remote-management-glossary.md#l)konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-122">However, to obtain data from remote computers, you must configure a WinRM [*listener*](windows-remote-management-glossary.md#l).</span></span> <span data-ttu-id="d9ef5-123">Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="d9ef5-123">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="d9ef5-124">Wenn beim Systemstart ein BMC erkannt wird, wird der IPMI-Anbieter geladen. Andernfalls sind die WinRM-Skript Objekte und das WinRM-Befehlszeilen Tool weiterhin verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-124">If a BMC is detected at system startup, then the IPMI provider loads; otherwise, the WinRM scripting objects and the WinRM command-line tool are still available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d9ef5-125">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d9ef5-125">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="d9ef5-126">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="d9ef5-126">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="d9ef5-127">Verknüpfung mit der öffentlichen WS-Management-Protokollspezifikation, WinRM-Architektur, Beziehung zu WMI, Hardware Verwaltung mit IPMI-Anbieter, Konfiguration und Installation.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-127">Link to public WS-Management protocol specification, WinRM architecture, relationship to WMI, hardware management with the IPMI provider, configuration and installation.</span></span>

</dd> <dt>

[<span data-ttu-id="d9ef5-128">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="d9ef5-128">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="d9ef5-129">Beginnen Sie mit der Verwendung der WinRM-Skript-API und der Hardware Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-129">Getting started using the WinRM scripting API and hardware management.</span></span>

</dd> <dt>

[<span data-ttu-id="d9ef5-130">Windows-Remoteverwaltung Referenz</span><span class="sxs-lookup"><span data-stu-id="d9ef5-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dd>

<span data-ttu-id="d9ef5-131">Liste der Skript Schnittstellen, die von Microsoft Web Services for Management (WS-Management)-Automatisierung und Klassendefinitionen der vom IPMI-Anbieter erstellten WMI-Klassen und Klassendefinitionen für die Kommunikation mit dem IPMI-Treiber zum Abrufen von [Baseboard-Verwaltungs Controller (BMC)](windows-remote-management-glossary.md) -Daten definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ef5-131">List of scripting interfaces defined by Microsoft Web Services for Management (WS-Management) Automation and class definitions of the WMI classes created by the IPMI provider and classes that communicate with the IPMI driver to obtain [baseboard management controller (BMC)](windows-remote-management-glossary.md) data.</span></span>

</dd> </dl>

 

 