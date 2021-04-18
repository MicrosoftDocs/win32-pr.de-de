---
description: Hinzufügen eines Laufwerk Buchstabens zu einer LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Hinzufügen eines Laufwerk Buchstabens zu einer LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426a4f3bf720b21a02462edde4a381012d2084d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347142"
---
# <a name="adding-a-drive-letter-to-a-lun"></a><span data-ttu-id="77571-103">Hinzufügen eines Laufwerk Buchstabens zu einer LUN</span><span class="sxs-lookup"><span data-stu-id="77571-103">Adding a Drive Letter to a LUN</span></span>

<span data-ttu-id="77571-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="77571-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="77571-105">Sie können volumeobjekten direkt Laufwerk Buchstaben zuweisen. Wenn Ihr Datenträger jedoch ein LUN-Objekt ist, sind einige zusätzliche Schritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="77571-105">You can assign drive letters to volume objects directly; however, if your disk is a LUN object, you have a few additional steps.</span></span>

<span data-ttu-id="77571-106">**So weisen Sie einem LUN-Objekt einen Laufwerk Buchstaben zu**</span><span class="sxs-lookup"><span data-stu-id="77571-106">**To assign a drive letter to a LUN object**</span></span>

1.  <span data-ttu-id="77571-107">Deaktivieren Sie ggf. die LUN auf dem lokalen Host.</span><span class="sxs-lookup"><span data-stu-id="77571-107">If necessary, unmask the LUN to the local host.</span></span>
    > [!Note]  
    > <span data-ttu-id="77571-108">Sie können keine Software Verwaltungsvorgänge für ein LUN-Objekt ausführen, das in der aktuellen VDS-Sitzung auf einem anderen Computer unmaskiert ist.</span><span class="sxs-lookup"><span data-stu-id="77571-108">You cannot perform software administrative operations on a LUN object that is unmasked to another computer within the current VDS session.</span></span>

     

2.  <span data-ttu-id="77571-109">Rufen Sie die [**ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) -Methode auf dem Computer auf, auf dem der Hardware Anbieter ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77571-109">Invoke the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method on the computer that is running the hardware provider.</span></span>
3.  <span data-ttu-id="77571-110">Initialisieren Sie die LUN als Basis Datenträger wie folgt:</span><span class="sxs-lookup"><span data-stu-id="77571-110">Initialize the LUN as a basic disk as follows:</span></span>
    1.  <span data-ttu-id="77571-111">Rufen Sie die [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode für das LUN-Objekt auf, um die [**ivdsdisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) -Schnittstelle abzufragen.</span><span class="sxs-lookup"><span data-stu-id="77571-111">Invoke the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the LUN object to query for the [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) interface.</span></span>
    2.  <span data-ttu-id="77571-112">Rufen Sie die [**ivdsswprovider:: | atepack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) -Methode auf, um ein Basic Pack zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77571-112">Invoke the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a basic pack.</span></span>
    3.  <span data-ttu-id="77571-113">Rufen Sie die [**ivdspack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) -Methode auf, um den Datenträger dem neuen Paket hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="77571-113">Invoke the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add the disk to the new pack.</span></span>
4.  <span data-ttu-id="77571-114">Erstellen Sie eine Partition auf dem Datenträger, und rufen Sie das Volume-Objekt wie folgt ab:</span><span class="sxs-lookup"><span data-stu-id="77571-114">Create a partition on the disk and obtain the volume object as follows:</span></span>
    1.  <span data-ttu-id="77571-115">Rufen Sie die [**ivdscreatepartitionex:: | atepartitionex**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) -Methode auf, um eine Partition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77571-115">Invoke the [**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) method to create a partition.</span></span>
    2.  <span data-ttu-id="77571-116">Rufen Sie die [**ivdsasync:: Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) -Methode für das Async-Objekt auf, das von " [**kreatepartitionex**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) " zurückgegeben wird, um den volumebezeichner aus der [**VDS- \_ Async- \_ Ausgabe**](/windows/desktop/api/Vds/ns-vds-vds_async_output) Struktur zu</span><span class="sxs-lookup"><span data-stu-id="77571-116">Invoke the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method on the async object that is returned by [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) to get the volume identifier from the [**VDS\_ASYNC\_OUTPUT**](/windows/desktop/api/Vds/ns-vds-vds_async_output) structure.</span></span>
    3.  <span data-ttu-id="77571-117">Übergeben Sie den volumebezeichner als Parameter an die [**ivdsservice:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) -Methode, um einen volumeobjektzeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="77571-117">Pass the volume identifier as a parameter to the [**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) method to get a volume object pointer.</span></span>
5.  <span data-ttu-id="77571-118">Rufen Sie die [**ivdsvolumemf:: addaccesspath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) -Methode auf, um den Laufwerk Buchstaben zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="77571-118">Invoke the [**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) method to assign the drive letter.</span></span>

> [!Note]  
> <span data-ttu-id="77571-119">Die [**ivdsadvanceddisk:: zuordtionsetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) -Methode weist Partitionen ohne zugeordnete Volumes (z. b. OEM-oder ESP-Partitionen) Laufwerk Buchstaben zu.</span><span class="sxs-lookup"><span data-stu-id="77571-119">The [**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) method assigns drive letters to partitions without associated volumes, such as OEM or ESP partitions.</span></span> <span data-ttu-id="77571-120">Sie können Sie nicht verwenden, um einem LUN-Objekt einen Laufwerk Buchstaben zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="77571-120">You cannot use it to assign a drive letter to a LUN object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="77571-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77571-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77571-122">Verwenden von VDS</span><span class="sxs-lookup"><span data-stu-id="77571-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="77571-123">**Ivdsservice:: REENUMERATE**</span><span class="sxs-lookup"><span data-stu-id="77571-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="77571-124">**Ivdsdisk**</span><span class="sxs-lookup"><span data-stu-id="77571-124">**IVdsDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[<span data-ttu-id="77571-125">**Ivdsswprovider:: kreatepack**</span><span class="sxs-lookup"><span data-stu-id="77571-125">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="77571-126">**Ivdspack:: adddisk**</span><span class="sxs-lookup"><span data-stu-id="77571-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[<span data-ttu-id="77571-127">**Ivdscreatepartitionex:: kreatepartitionex**</span><span class="sxs-lookup"><span data-stu-id="77571-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[<span data-ttu-id="77571-128">**Ivdsasync:: Wait**</span><span class="sxs-lookup"><span data-stu-id="77571-128">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="77571-129">**asynchrone VDS- \_ \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="77571-129">**VDS\_ASYNC\_OUTPUT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[<span data-ttu-id="77571-130">**Ivdsvolumemf:: addaccesspath**</span><span class="sxs-lookup"><span data-stu-id="77571-130">**IVdsVolumeMF::AddAccessPath**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[<span data-ttu-id="77571-131">**Ivdsadvanceddisk:: zuder zutragplatte**</span><span class="sxs-lookup"><span data-stu-id="77571-131">**IVdsAdvancedDisk::AssignDriveLetter**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
