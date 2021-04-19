---
description: Der Dienst für virtuelle Datenträger (Virtual Disk Service, VDS) verwaltet eine große Bandbreite an Speicherkonfigurationen von Desktops mit einem Datenträger bis hin zu externen Speicherarrays. Der Dienst macht eine Anwendungsprogrammierschnittstelle (Application Programming Interface, API) verfügbar.
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Dienst für virtuelle Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362257"
---
# <a name="virtual-disk-service"></a><span data-ttu-id="ad56c-104">Dienst für virtuelle Datenträger</span><span class="sxs-lookup"><span data-stu-id="ad56c-104">Virtual Disk Service</span></span>

<span data-ttu-id="ad56c-105">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des virtuellen Festplatten Dienstanbieter durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="ad56c-105">\[Beginning with Windows 8 and Windows Server 2012, the Virtual Disk Service COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="ad56c-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="ad56c-106">Purpose</span></span>

<span data-ttu-id="ad56c-107">Der Dienst für virtuelle Datenträger (Virtual Disk Service, VDS) verwaltet eine große Bandbreite an Speicherkonfigurationen von Desktops mit einem Datenträger bis hin zu externen Speicherarrays.</span><span class="sxs-lookup"><span data-stu-id="ad56c-107">The Virtual Disk Service (VDS) manages a wide range of storage configurations, from single-disk desktops to external storage arrays.</span></span> <span data-ttu-id="ad56c-108">Der Dienst macht eine Anwendungsprogrammierschnittstelle (Application Programming Interface, API) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad56c-108">The service exposes an application programming interface (API).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="ad56c-109">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="ad56c-109">Where applicable</span></span>

<span data-ttu-id="ad56c-110">Ab Windows 8 und Windows Server 8 wird die COM-Schnittstelle des virtuellen Datenträger Dienstanbieter durch die Speicherverwaltungs-API ersetzt, eine WMI-basierte Programmierschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ad56c-110">Beginning with Windows 8 and Windows Server 8, the Virtual Disk Service COM interface is superseded by the Storage Management API, a WMI-based programming interface.</span></span> <span data-ttu-id="ad56c-111">Zum Verwalten von Speicher Subsystemen, (Windows)-Datenträgern, Partitionen und Volumes wird dringend empfohlen, die-Speicherverwaltungs-API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad56c-111">For managing storage subsystems, (Windows) disks, partitions, and volumes, we strongly recommend using the Storage Management API.</span></span> <span data-ttu-id="ad56c-112">Weitere Informationen finden Sie in der [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span><span class="sxs-lookup"><span data-stu-id="ad56c-112">For more information, see the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span></span>

<span data-ttu-id="ad56c-113">Für alle Verwendungen mit Ausnahme von Spiegelungs Start Volumes (mit einem Spiegelungs Volume zum Hosten des Betriebssystems) sind dynamische Datenträger veraltet.</span><span class="sxs-lookup"><span data-stu-id="ad56c-113">For all usages except mirror boot volumes (using a mirror volume to host the operating system ), dynamic disks are deprecated.</span></span> <span data-ttu-id="ad56c-114">Verwenden Sie für Daten, die Resilienz vor Laufwerks Fehlern erfordern, Speicherplätze, eine robuste Lösung für die Speichervirtualisierung.</span><span class="sxs-lookup"><span data-stu-id="ad56c-114">For data that requires resiliency against drive failure, use Storage Spaces, a resilient storage virtualization solution.</span></span> <span data-ttu-id="ad56c-115">Weitere Informationen finden Sie unter [Speicherplätze Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="ad56c-115">For more information, see [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span></span>

<span data-ttu-id="ad56c-116">Anwendungsentwickler, die die in diesem Handbuch beschriebenen Schnittstellen verwenden, können eine heterogene Gruppe von Hersteller-und intern verwaltetem Speicher Abfragen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ad56c-116">Application developers who use the interfaces described in this guide can query and configure a heterogeneous set of vendor-supplied and internally managed storage.</span></span> <span data-ttu-id="ad56c-117">VDS blendet die Komplexität von Anwendungen aus, die mit dem Speicher verbunden sind, sodass der Dienst sowohl Hersteller als auch technologieneutral ist.</span><span class="sxs-lookup"><span data-stu-id="ad56c-117">VDS hides from applications the complexities associated with storage, making the service both vendor and technology neutral.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ad56c-118">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="ad56c-118">Developer audience</span></span>

<span data-ttu-id="ad56c-119">Diese Dokumentation ist für Anwendungsentwickler gedacht, die mit den Speicherfunktionen von Microsoft Windows-Plattformen vertraut sind und die sich über die com-Entwicklung informieren.</span><span class="sxs-lookup"><span data-stu-id="ad56c-119">This documentation is intended for application developers who are familiar with the storage capabilities of Microsoft Windows platforms and who are knowledgeable about COM development.</span></span>

<span data-ttu-id="ad56c-120">Das Handbuch richtet sich auch an Hardware-Subsystem-Hersteller, die VDS-Hardware Anbieter Programme entwickeln und unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ad56c-120">The guide is also intended for hardware subsystem manufacturers who develop and support VDS hardware provider programs.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ad56c-121">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="ad56c-121">Run-time requirements</span></span>

<span data-ttu-id="ad56c-122">VDS wird unter Windows Server 2003, Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad56c-122">VDS is supported on Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="ad56c-123">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" in der Dokumentation für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="ad56c-123">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="ad56c-124">Das Ausführen von 32-Bit-VDS-Anwendungen unter WOW64 wird unterstützt, aber 64-Bit-VDS-Anbieter müssen als native Anwendungen auf 64-Bit-Windows-Versionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ad56c-124">Running 32-bit VDS applications under WOW64 is supported, but 64-bit VDS providers must run as native applications on 64-bit Windows versions.</span></span>

<span data-ttu-id="ad56c-125">VDS ist im Microsoft Windows Software Development Kit (SDK) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad56c-125">VDS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ad56c-126">Sie können das SDK für Windows 7 und Windows Server 2008 R2 aus dem [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279)installieren.</span><span class="sxs-lookup"><span data-stu-id="ad56c-126">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="ad56c-127">Diese Version des Windows SDK kann verwendet werden, um VDS-Anwendungen für Windows Server 2003, Windows Vista und höher zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="ad56c-127">This version of the Windows SDK can be used to develop VDS applications for Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="ad56c-128">Sie können auch die [ISO-Version](https://www.microsoft.com/download/details.aspx?id=8442) des SDK aus dem Windows Download Center herunterladen.</span><span class="sxs-lookup"><span data-stu-id="ad56c-128">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ad56c-129">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ad56c-129">In this section</span></span>



| <span data-ttu-id="ad56c-130">Thema</span><span class="sxs-lookup"><span data-stu-id="ad56c-130">Topic</span></span>                                         | <span data-ttu-id="ad56c-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad56c-131">Description</span></span>                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad56c-132">Informationen zu VDS</span><span class="sxs-lookup"><span data-stu-id="ad56c-132">About VDS</span></span>](about-vds.md)<br/>         | <span data-ttu-id="ad56c-133">Beschreibt das VDS-Objektmodell, Speicher Konfigurations Strategien und VDS-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="ad56c-133">Describes the VDS object model, storage-configuration strategies, and VDS notifications.</span></span><br/>    |
| [<span data-ttu-id="ad56c-134">Verwenden von VDS</span><span class="sxs-lookup"><span data-stu-id="ad56c-134">Using VDS</span></span>](using-vds.md)<br/>         | <span data-ttu-id="ad56c-135">Beschreibt die Verwendung von VDS zum Abfragen und Konfigurieren von Speichergeräten.</span><span class="sxs-lookup"><span data-stu-id="ad56c-135">Describes how to use VDS to query and configure storage devices.</span></span><br/>                            |
| [<span data-ttu-id="ad56c-136">VDS-Referenz</span><span class="sxs-lookup"><span data-stu-id="ad56c-136">VDS Reference</span></span>](vds-reference.md)<br/> | <span data-ttu-id="ad56c-137">Beschreibt VDS-Konstanten, Datentypen, Enumerationen, Schnittstellen, Strukturen und Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="ad56c-137">Describes VDS constants, data types, enumerations, interfaces, structures, and error codes.</span></span><br/> |



 

 

