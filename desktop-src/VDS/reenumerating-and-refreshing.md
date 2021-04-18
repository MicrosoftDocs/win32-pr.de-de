---
description: Erneute Aufzählung und Aktualisierung
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Erneute Aufzählung und Aktualisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358955"
---
# <a name="reenumerating-and-refreshing"></a><span data-ttu-id="a59a8-103">Erneute Aufzählung und Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="a59a8-103">Reenumerating and Refreshing</span></span>

<span data-ttu-id="a59a8-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="a59a8-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="a59a8-105">Der Vorgang reenumeration ermittelt neu verbundene und neu getrennte Geräte.</span><span class="sxs-lookup"><span data-stu-id="a59a8-105">The reenumeration operation discovers newly connected and newly disconnected devices.</span></span> <span data-ttu-id="a59a8-106">Der Aktualisierungs Vorgang aktualisiert die Konfigurationsinformationen vorhandener Geräte.</span><span class="sxs-lookup"><span data-stu-id="a59a8-106">The refresh operation updates the configuration information of existing devices.</span></span>

<span data-ttu-id="a59a8-107">**So können Sie Softwareanbieter Objekte erneut aufzählen**</span><span class="sxs-lookup"><span data-stu-id="a59a8-107">**To reenumerate software provider objects**</span></span>

-   <span data-ttu-id="a59a8-108">Aufrufen der [**ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a59a8-108">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method.</span></span> <span data-ttu-id="a59a8-109">Diese Methode ermittelt alle neu verbundenen und nicht verbundenen Datenträger und CD-ROM-Laufwerke und stellt sicher, dass alle Datenträger über den richtigen Besitzer verfügen.</span><span class="sxs-lookup"><span data-stu-id="a59a8-109">This method discovers all newly connected and disconnected disks and CD-ROM drives, and ensures that all disks have the proper owner.</span></span> <span data-ttu-id="a59a8-110">VDS besitzt unformatierte Datenträger oder Datenträger mit Fehlern. der Basic-Anbieter besitzt Basis Datenträger. und der dynamische Anbieter besitzt dynamische Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a59a8-110">VDS owns raw disks or disks with failures; the basic provider owns basic disks; and the dynamic provider owns dynamic disks.</span></span> <span data-ttu-id="a59a8-111">Dieser Vorgang kann das Scannen interner subsystembusse und das warten auf Timeouts einschließen.</span><span class="sxs-lookup"><span data-stu-id="a59a8-111">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="a59a8-112">**So können Sie Softwareanbieter Objekte erneut auflisten und aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="a59a8-112">**To reenumerate and refresh software provider objects**</span></span>

-   <span data-ttu-id="a59a8-113">Aufrufen der [**ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) -Methode und anschließendes Aufrufen der [**ivdsservice:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a59a8-113">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method and then call the [**IVdsService::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) method.</span></span> <span data-ttu-id="a59a8-114">Durch diese Kombination von Methoden werden nicht nur neu verbundene und nicht verbundene Datenträger und CD-ROM-Laufwerke ermittelt, sondern alle Datenträger-, Volume-und Plex-Informationen im VDS-Cache für Datenträger, die nicht vor kurzem verbunden oder getrennt wurden.</span><span class="sxs-lookup"><span data-stu-id="a59a8-114">In addition to discovering newly connected and disconnected disks and CD-ROM drives, this combination of methods updates all disk, volume, and plex information in the VDS cache for disks that have not been recently connected or disconnected.</span></span> <span data-ttu-id="a59a8-115">Aufrufen von " **Aktualisieren** ", um die Eigenschafts Informationen vorhandener Objekte im Cache zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a59a8-115">Call **Refresh** alone to refresh the property information of existing objects in the cache.</span></span> <span data-ttu-id="a59a8-116">Dieser Vorgang kann das Scannen interner subsystembusse und das warten auf Timeouts einschließen.</span><span class="sxs-lookup"><span data-stu-id="a59a8-116">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span> <span data-ttu-id="a59a8-117">Beachten Sie, dass VDS den Cache automatisch aktualisiert, sobald eine Änderung auftritt, die eine Benachrichtigung auslöst.</span><span class="sxs-lookup"><span data-stu-id="a59a8-117">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="a59a8-118">Außerdem kann das Aufrufen einer **Aktualisierung** als Antwort auf eine VDS-Benachrichtigung dazu führen, dass eine Endlosschleife von Benachrichtigungen gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a59a8-118">Also, calling **Refresh** in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="a59a8-119">Aus diesen Gründen sollte die **Aktualisierung** nur aufgerufen werden, wenn angezeigt wird, dass der Cache nicht ordnungsgemäß aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a59a8-119">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

<span data-ttu-id="a59a8-120">**So können Sie Hardware Subsysteme erneut aufzählen**</span><span class="sxs-lookup"><span data-stu-id="a59a8-120">**To reenumerate hardware subsystems**</span></span>

-   <span data-ttu-id="a59a8-121">Aufrufen der [**ivdshwprovider:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a59a8-121">Call the [**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) method.</span></span> <span data-ttu-id="a59a8-122">Je nach Anbieter kann dieser Vorgang das Senden von Netzwerk Paketen und das warten auf Timeouts, das neudurch führen von SCSI-Bussen und das warten auf Timeouts usw. umfassen.</span><span class="sxs-lookup"><span data-stu-id="a59a8-122">Depending on the provider, this operation can involve sending network packets and waiting for time-outs, rescanning SCSI buses and waiting for time-outs, and so on.</span></span>

<span data-ttu-id="a59a8-123">**So können Sie Hardware Subsystem-Objekte erneut aufzählen**</span><span class="sxs-lookup"><span data-stu-id="a59a8-123">**To reenumerate hardware subsystem objects**</span></span>

-   <span data-ttu-id="a59a8-124">Nennen Sie die [**ivdssubsystem:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) -Methode, um die Objekte (in der Regel Laufwerke) im-Subsystem zu inventarisieren.</span><span class="sxs-lookup"><span data-stu-id="a59a8-124">Call the [**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) method to inventory the objects (typically drives) in the subsystem.</span></span> <span data-ttu-id="a59a8-125">Abhängig vom Subsystem kann dieser Vorgang das Scannen interner subsystembusse und das warten auf Timeouts einschließen.</span><span class="sxs-lookup"><span data-stu-id="a59a8-125">Depending on the subsystem, this operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="a59a8-126">**So aktualisieren Sie Hardware Subsysteme und Subsystem-Objekte**</span><span class="sxs-lookup"><span data-stu-id="a59a8-126">**To refresh hardware subsystems and subsystem objects**</span></span>

-   <span data-ttu-id="a59a8-127">Aufrufen der [**ivdshwprovider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) -Methode, um den VDS-Cache mit Informationen zu vorhandenen Subsystemen zu aktualisieren, die von VDS-Hardwareanbietern verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a59a8-127">Call the [**IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) method to refresh the VDS cache of information about existing subsystems that are managed by VDS hardware providers.</span></span> <span data-ttu-id="a59a8-128">Beachten Sie, dass VDS den Cache automatisch aktualisiert, sobald eine Änderung auftritt, die eine Benachrichtigung auslöst.</span><span class="sxs-lookup"><span data-stu-id="a59a8-128">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="a59a8-129">Außerdem kann das Aufrufen einer [**Aktualisierung**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) als Antwort auf eine VDS-Benachrichtigung dazu führen, dass eine Endlosschleife von Benachrichtigungen gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a59a8-129">Also, calling [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="a59a8-130">Aus diesen Gründen sollte die **Aktualisierung** nur aufgerufen werden, wenn angezeigt wird, dass der Cache nicht ordnungsgemäß aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a59a8-130">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a59a8-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a59a8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a59a8-132">Verwenden von VDS</span><span class="sxs-lookup"><span data-stu-id="a59a8-132">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="a59a8-133">**Ivdsservice:: REENUMERATE**</span><span class="sxs-lookup"><span data-stu-id="a59a8-133">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="a59a8-134">**Ivdsservice:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="a59a8-134">**IVdsService::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[<span data-ttu-id="a59a8-135">**Ivdshwprovider:: REENUMERATE**</span><span class="sxs-lookup"><span data-stu-id="a59a8-135">**IVdsHwProvider::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[<span data-ttu-id="a59a8-136">**Ivdssubsystem:: REENUMERATE**</span><span class="sxs-lookup"><span data-stu-id="a59a8-136">**IVdsSubSystem::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[<span data-ttu-id="a59a8-137">**Ivdshwprovider:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="a59a8-137">**IVdsHwProvider::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
