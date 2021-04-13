---
description: Hinzufügen von fremden Datenträgern zu einem Paket
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Hinzufügen von fremden Datenträgern zu einem Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbfa2ff3d00857fd4e1b92e78f1760c25ce516b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349279"
---
# <a name="adding-foreign-disks-to-a-pack"></a><span data-ttu-id="79ece-103">Hinzufügen von fremden Datenträgern zu einem Paket</span><span class="sxs-lookup"><span data-stu-id="79ece-103">Adding Foreign Disks to a Pack</span></span>

<span data-ttu-id="79ece-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="79ece-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="79ece-105">In den meisten Fällen ist ein fremd Datenträger ein dynamischer Datenträger, der auf einem Computer zugeordnet und physisch auf einen anderen Computer verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="79ece-105">Most commonly, a foreign disk is a dynamic disk that is allocated on one computer and physically moved to another computer.</span></span> <span data-ttu-id="79ece-106">Alle Datenträger, die einem anderen Paket als dem Online Paket angehören, werden jedoch als fremd Datenträger betrachtet, der zu einem fremden Festplatten Paket gehört.</span><span class="sxs-lookup"><span data-stu-id="79ece-106">However, any disk that belongs to a pack other than the online pack is considered to be a foreign disk that belongs to a foreign disk pack.</span></span>

<span data-ttu-id="79ece-107">Ein Foreign Pack verfügt über das **VDS- \_ PKF- \_ Fremd** Kennzeichen, das im **ulflags** -Member der prop-Struktur des [**VDS- \_ Pakets \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="79ece-107">A foreign pack has the **VDS\_PKF\_FOREIGN** flag set in the **ulFlags** member of the [**VDS\_PACK\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) structure.</span></span> <span data-ttu-id="79ece-108">Fremd Pakete sind immer offline.</span><span class="sxs-lookup"><span data-stu-id="79ece-108">Foreign packs are always offline.</span></span>

<span data-ttu-id="79ece-109">Im folgenden Verfahren wird beschrieben, wie ein oder mehrere fremd Datenträger importiert werden.</span><span class="sxs-lookup"><span data-stu-id="79ece-109">The following procedure describes how to import one or more foreign disks.</span></span>

<span data-ttu-id="79ece-110">**So importieren Sie einen oder mehrere fremd Datenträger**</span><span class="sxs-lookup"><span data-stu-id="79ece-110">**To import one or more foreign disks**</span></span>

1.  <span data-ttu-id="79ece-111">Verschieben Sie Datenträger auf den neuen Computer.</span><span class="sxs-lookup"><span data-stu-id="79ece-111">Move disks to the new computer.</span></span>
2.  <span data-ttu-id="79ece-112">Verwenden Sie auf dem neuen Computer die [**ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) -Methode, um die fremd Datenträger zu installieren.</span><span class="sxs-lookup"><span data-stu-id="79ece-112">On the new computer, use the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method to install the foreign disks.</span></span>
3.  <span data-ttu-id="79ece-113">Wählen Sie das Online Paket als Ziel Paket aus, das die fremden Datenträger empfängt.</span><span class="sxs-lookup"><span data-stu-id="79ece-113">Select the online pack to be the target pack that receives the foreign disks.</span></span> <span data-ttu-id="79ece-114">Wenn kein Online Paket vorhanden ist, verwenden Sie die [**ivdsswprovider:: Deepack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) -Methode, um ein neues leeres Paket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="79ece-114">If no online pack exists, use the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a new empty pack.</span></span>
4.  <span data-ttu-id="79ece-115">Verwenden Sie die [**ivdspack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) -Methode, um die Datenträger in das neue dynamische Paket zu importieren.</span><span class="sxs-lookup"><span data-stu-id="79ece-115">Use the [**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) method to import the disks to the new dynamic pack.</span></span>
5.  <span data-ttu-id="79ece-116">Verwenden Sie die [**ivdsswprovider:: querypacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) -Methode zum Auflisten der Pakete und [**ivdspack:: GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) , um zu bestimmen, welches Paket nun das Online Paket ist.</span><span class="sxs-lookup"><span data-stu-id="79ece-116">Use the [**IVdsSwProvider::QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) method to enumerate the packs and [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) to determine which pack is now the online pack.</span></span>

<span data-ttu-id="79ece-117">Wenn Sie ein neues leeres Ziel Paket erstellen, werden die fremd Datenträger nicht tatsächlich zu diesem Paket migriert.</span><span class="sxs-lookup"><span data-stu-id="79ece-117">If you create a new empty target pack, the foreign disks are not actually migrated to that pack.</span></span> <span data-ttu-id="79ece-118">Stattdessen ist das fremd Paket als Online gekennzeichnet, das **VDS \_ PKF- \_ Fremd** Kennzeichen für das Paket wird gelöscht (sodass das Paket nicht mehr fremd ist), und das von Ihnen erstellte Ziel Paket wird verworfen.</span><span class="sxs-lookup"><span data-stu-id="79ece-118">Instead, the foreign pack is marked online, the **VDS\_PKF\_FOREIGN** flag for the pack is cleared (so the pack is no longer foreign), and the target pack that you created is discarded.</span></span>

> [!Note]  
> <span data-ttu-id="79ece-119">Verwenden Sie die [**ivdspack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) -Methode, um nicht zugeordnete Datenträger – Datenträger, die nicht von einem Anbieter beansprucht werden – einem Paket hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="79ece-119">Use the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add unallocated disks—disks not claimed by a provider—to a pack.</span></span> <span data-ttu-id="79ece-120">Ein nicht zugeordneter Datenträger kann nicht fremd sein.</span><span class="sxs-lookup"><span data-stu-id="79ece-120">An unallocated disk cannot be foreign.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="79ece-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79ece-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79ece-122">Verwenden von VDS</span><span class="sxs-lookup"><span data-stu-id="79ece-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="79ece-123">**Ivdsservice:: REENUMERATE**</span><span class="sxs-lookup"><span data-stu-id="79ece-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="79ece-124">**Ivdsswprovider:: kreatepack**</span><span class="sxs-lookup"><span data-stu-id="79ece-124">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="79ece-125">**Ivdspack:: MigrateDisks**</span><span class="sxs-lookup"><span data-stu-id="79ece-125">**IVdsPack::MigrateDisks**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[<span data-ttu-id="79ece-126">**Ivdspack:: adddisk**</span><span class="sxs-lookup"><span data-stu-id="79ece-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
