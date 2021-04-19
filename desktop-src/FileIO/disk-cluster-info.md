---
description: Stellt Informationen dar, die auf dem Partitions-Manager zu einem Datenträger, der Teil eines Clusters ist, verwaltet werden.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: DISK_CLUSTER_INFO Struktur (ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: f18e8f47cd5b1b527c9d6d2d19a09775528602d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362239"
---
# <a name="disk_cluster_info-structure"></a><span data-ttu-id="76875-103">Datenträger \_ Cluster- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="76875-103">DISK\_CLUSTER\_INFO structure</span></span>

<span data-ttu-id="76875-104">Stellt Informationen dar, die auf dem Partitions-Manager zu einem Datenträger, der Teil eines Clusters ist, verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="76875-104">Represents information maintained on the partition manager about a disk that is part of a cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="76875-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76875-105">Syntax</span></span>


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a><span data-ttu-id="76875-106">Member</span><span class="sxs-lookup"><span data-stu-id="76875-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="76875-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="76875-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="76875-108">Die Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="76875-108">The version number.</span></span> <span data-ttu-id="76875-109">Dieser Wert muss auf die Größe dieser Struktur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="76875-109">This value must be set to the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="76875-110">**Flags**</span><span class="sxs-lookup"><span data-stu-id="76875-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="76875-111">Eine Kombination von Flags, die sich auf Datenträger und Cluster beziehen.</span><span class="sxs-lookup"><span data-stu-id="76875-111">A combination of flags related to disks and clusters.</span></span>



| <span data-ttu-id="76875-112">Wert</span><span class="sxs-lookup"><span data-stu-id="76875-112">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="76875-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="76875-113">Meaning</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <span data-ttu-id="76875-114">Datenträger <dt>**\_ \_Clusterflag \_ aktiviert**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="76875-114"><dt>**DISK\_CLUSTER\_FLAG\_ENABLED**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="76875-115">Der Datenträger wird als Teil des Cluster Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="76875-115">The disk is used as part of the cluster service.</span></span><br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <span data-ttu-id="76875-116">Datenträger <dt>**\_ \_Clusterflag \_ CSV**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="76875-116"><dt>**DISK\_CLUSTER\_FLAG\_CSV**</dt> <dt>2</dt></span></span> </dl>                                                      | <span data-ttu-id="76875-117">Volumes auf dem Datenträger werden von csvfs auf allen Knoten des Clusters verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="76875-117">Volumes on the disk are exposed by CSVFS on all nodes of the cluster.</span></span><br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <span data-ttu-id="76875-118">Datenträger <dt>**\_ \_Clusterflag \_ in \_ Wartung**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="76875-118"><dt>**DISK\_CLUSTER\_FLAG\_IN\_MAINTENANCE**</dt> <dt>4</dt></span></span> </dl>                    | <span data-ttu-id="76875-119">Die dieser Festplatte zugeordnete Cluster Ressource befindet sich im Wartungsmodus.</span><span class="sxs-lookup"><span data-stu-id="76875-119">The cluster resource associated with this disk is in maintenance mode.</span></span><br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <span data-ttu-id="76875-120">Datenträger <dt>**\_ \_Clusterflag \_ PnP-Ankunft bei \_ \_ Abschluss**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="76875-120"><dt>**DISK\_CLUSTER\_FLAG\_PNP\_ARRIVAL\_COMPLETE**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="76875-121">Der Cluster Datenträger Treiber für den Kernel Modus (Clusdisk) hat eine PNP-Benachrichtigung über die Ankunft des Datenträgers erhalten.</span><span class="sxs-lookup"><span data-stu-id="76875-121">The cluster disk driver for kernel mode (clusdisk) has received PnP notification of the arrival of the disk.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="76875-122">**Flagsmask**</span><span class="sxs-lookup"><span data-stu-id="76875-122">**FlagsMask**</span></span>
</dt> <dd>

<span data-ttu-id="76875-123">Die Flags, die im **Flags** -Member geändert werden.</span><span class="sxs-lookup"><span data-stu-id="76875-123">The flags that are being modified in the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="76875-124">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="76875-124">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="76875-125">**True** , um eine layoutänderungsbenachrichtigung zu senden. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="76875-125">**TRUE** to send a layout change notification; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76875-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76875-126">Requirements</span></span>



| <span data-ttu-id="76875-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76875-127">Requirement</span></span> | <span data-ttu-id="76875-128">Wert</span><span class="sxs-lookup"><span data-stu-id="76875-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76875-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76875-129">Minimum supported client</span></span><br/> | <span data-ttu-id="76875-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="76875-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="76875-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76875-131">Minimum supported server</span></span><br/> | <span data-ttu-id="76875-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76875-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76875-133">Header</span><span class="sxs-lookup"><span data-stu-id="76875-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="76875-134"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="76875-134"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76875-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76875-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76875-136">Strukturen der Datenträgerverwaltung</span><span class="sxs-lookup"><span data-stu-id="76875-136">Disk Management Structures</span></span>](disk-management-structures.md)
</dt> <dt>

[<span data-ttu-id="76875-137">**ioctl-Datenträger \_ \_ get \_ Cluster \_ Info**</span><span class="sxs-lookup"><span data-stu-id="76875-137">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="76875-138">**ioctl-Datenträger \_ \_ Satz- \_ Cluster \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="76875-138">**IOCTL\_DISK\_SET\_CLUSTER\_INFO**</span></span>](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




