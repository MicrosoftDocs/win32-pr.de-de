---
description: Gültige Partitionstypen, die von Datenträger Treibern verwendet werden.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Datenträger-Partitionstypen (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359470"
---
# <a name="disk-partition-types"></a><span data-ttu-id="657c3-103">Datenträger-Partitionstypen</span><span class="sxs-lookup"><span data-stu-id="657c3-103">Disk Partition Types</span></span>

<span data-ttu-id="657c3-104">In der folgenden Tabelle sind die gültigen Partitionstypen aufgeführt, die von Datenträger Treibern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="657c3-104">The following table identifies the valid partition types that are used by disk drivers.</span></span>



| <span data-ttu-id="657c3-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="657c3-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="657c3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="657c3-106">Description</span></span>                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <span data-ttu-id="657c3-107"><dt>**Partition \_ Eintrag nicht \_ verwendet**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="657c3-107"><dt>**PARTITION\_ENTRY\_UNUSED**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="657c3-108">Eine nicht verwendete Eintrag-Partition.</span><span class="sxs-lookup"><span data-stu-id="657c3-108">An unused entry partition.</span></span><br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <span data-ttu-id="657c3-109"><dt>**Partition \_ Erweitert**</dt> <dt>0x05</dt></span><span class="sxs-lookup"><span data-stu-id="657c3-109"><dt>**PARTITION\_EXTENDED**</dt> <dt>0x05</dt></span></span> </dl>              | <span data-ttu-id="657c3-110">Eine erweiterte Partition.</span><span class="sxs-lookup"><span data-stu-id="657c3-110">An extended partition.</span></span><br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <span data-ttu-id="657c3-111"><dt>**Partition \_ FAT \_ 12**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="657c3-111"><dt>**PARTITION\_FAT\_12**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="657c3-112">Eine FAT12-Dateisystem Partition.</span><span class="sxs-lookup"><span data-stu-id="657c3-112">A FAT12 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <span data-ttu-id="657c3-113"><dt>**Partition \_ FAT \_ 16**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="657c3-113"><dt>**PARTITION\_FAT\_16**</dt> <dt>0x04</dt></span></span> </dl>                   | <span data-ttu-id="657c3-114">Eine FAT16-Dateisystem Partition.</span><span class="sxs-lookup"><span data-stu-id="657c3-114">A FAT16 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <span data-ttu-id="657c3-115"><dt>**Partition \_ FAT32**</dt> <dt>0x0B</dt></span><span class="sxs-lookup"><span data-stu-id="657c3-115"><dt>**PARTITION\_FAT32**</dt> <dt>0x0B</dt></span></span> </dl>                       | <span data-ttu-id="657c3-116">Eine FAT32-Dateisystem Partition.</span><span class="sxs-lookup"><span data-stu-id="657c3-116">A FAT32 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <span data-ttu-id="657c3-117"><dt>**Partition \_ IFS**</dt> <dt>0x07</dt></span><span class="sxs-lookup"><span data-stu-id="657c3-117"><dt>**PARTITION\_IFS**</dt> <dt>0x07</dt></span></span> </dl>                             | <span data-ttu-id="657c3-118">Eine IFS-Partition.</span><span class="sxs-lookup"><span data-stu-id="657c3-118">An IFS partition.</span></span><br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <span data-ttu-id="657c3-119"><dt>**Partition \_ LDM**</dt> <dt>0x42</dt></span><span class="sxs-lookup"><span data-stu-id="657c3-119"><dt>**PARTITION\_LDM**</dt> <dt>0x42</dt></span></span> </dl>                             | <span data-ttu-id="657c3-120">Eine LDM-Partition (Logical Disk Manager).</span><span class="sxs-lookup"><span data-stu-id="657c3-120">A logical disk manager (LDM) partition.</span></span><br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <span data-ttu-id="657c3-121"><dt>**Partition \_ NTFT**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="657c3-121"><dt>**PARTITION\_NTFT**</dt> <dt>0x80</dt></span></span> </dl>                          | <span data-ttu-id="657c3-122">Eine NTFT-Partition.</span><span class="sxs-lookup"><span data-stu-id="657c3-122">An NTFT partition.</span></span><br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <span data-ttu-id="657c3-123"><dt>**Gültig \_ NTFT**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="657c3-123"><dt>**VALID\_NTFT**</dt> <dt>0xC0</dt></span></span> </dl>                                      | <span data-ttu-id="657c3-124">Eine gültige NTFT-Partition.</span><span class="sxs-lookup"><span data-stu-id="657c3-124">A valid NTFT partition.</span></span><br/> <span data-ttu-id="657c3-125">Das hohe Bit eines Partitionstyp Codes gibt an, dass eine Partition Teil eines NTFT-Spiegels oder Stripesetarrays ist.</span><span class="sxs-lookup"><span data-stu-id="657c3-125">The high bit of a partition type code indicates that a partition is part of an NTFT mirror or striped array.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="657c3-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="657c3-126">Remarks</span></span>

<span data-ttu-id="657c3-127">Es gibt mehrere Makros, mit denen Sie den Partitionstyp erkennen können: **iscontainerpartition**, **isftpartition** und **iserkenzedpartition**.</span><span class="sxs-lookup"><span data-stu-id="657c3-127">There are several macros that can help you detect the partition type: **IsContainerPartition**, **IsFTPartition**, and **IsRecognizedPartition**.</span></span> <span data-ttu-id="657c3-128">Weitere Informationen finden Sie unter winioctl. h.</span><span class="sxs-lookup"><span data-stu-id="657c3-128">For more information, see WinIoCtl.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="657c3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="657c3-129">Requirements</span></span>



| <span data-ttu-id="657c3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="657c3-130">Requirement</span></span> | <span data-ttu-id="657c3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="657c3-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="657c3-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="657c3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="657c3-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="657c3-133">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="657c3-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="657c3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="657c3-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="657c3-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="657c3-136">Header</span><span class="sxs-lookup"><span data-stu-id="657c3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="657c3-137"><dt>Winioctl. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="657c3-137"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="657c3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="657c3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657c3-139">**Partitions \_ Informationen \_ Ex**</span><span class="sxs-lookup"><span data-stu-id="657c3-139">**PARTITION\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[<span data-ttu-id="657c3-140">**Partitions \_ Informationen \_ MBR**</span><span class="sxs-lookup"><span data-stu-id="657c3-140">**PARTITION\_INFORMATION\_MBR**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[<span data-ttu-id="657c3-141">**\_Partitions \_ Informationen festlegen**</span><span class="sxs-lookup"><span data-stu-id="657c3-141">**SET\_PARTITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




