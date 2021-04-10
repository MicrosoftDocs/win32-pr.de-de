---
description: Stellt eine Adresse in der Master Dateitabelle (MFT) dar. Die Adresse wird mit einer zirkulär wiederverwendeten Sequenznummer gekennzeichnet, die zum Zeitpunkt der Gültigkeit des MFT-Segment Verweises festgelegt wird.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: MFT_SEGMENT_REFERENCE Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125642"
---
# <a name="mft_segment_reference-structure"></a><span data-ttu-id="2892d-104">MFT- \_ Segment \_ Verweis Struktur</span><span class="sxs-lookup"><span data-stu-id="2892d-104">MFT\_SEGMENT\_REFERENCE structure</span></span>

<span data-ttu-id="2892d-105">\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]</span><span class="sxs-lookup"><span data-stu-id="2892d-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="2892d-106">Stellt eine Adresse in der Master Dateitabelle (MFT) dar.</span><span class="sxs-lookup"><span data-stu-id="2892d-106">Represents an address in the master file table (MFT).</span></span> <span data-ttu-id="2892d-107">Die Adresse wird mit einer zirkulär wiederverwendeten Sequenznummer gekennzeichnet, die zum Zeitpunkt der Gültigkeit des MFT-Segment Verweises festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="2892d-107">The address is tagged with a circularly reused sequence number that is set at the time the MFT segment reference was valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="2892d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2892d-108">Syntax</span></span>


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a><span data-ttu-id="2892d-109">Member</span><span class="sxs-lookup"><span data-stu-id="2892d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2892d-110">**Segmentnumlowpart**</span><span class="sxs-lookup"><span data-stu-id="2892d-110">**SegmentNumberLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="2892d-111">Der niedrige Teil der Segment Nummer.</span><span class="sxs-lookup"><span data-stu-id="2892d-111">The low part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="2892d-112">**Segmentnumhighpart**</span><span class="sxs-lookup"><span data-stu-id="2892d-112">**SegmentNumberHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="2892d-113">Der hohe Teil der Segment Nummer.</span><span class="sxs-lookup"><span data-stu-id="2892d-113">The high part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="2892d-114">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="2892d-114">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="2892d-115">Die Sequenznummer ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2892d-115">The nonzero sequence number.</span></span> <span data-ttu-id="2892d-116">Der Wert 0 ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="2892d-116">The value 0 is reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2892d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2892d-117">Remarks</span></span>

<span data-ttu-id="2892d-118">Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.</span><span class="sxs-lookup"><span data-stu-id="2892d-118">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="2892d-119">Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.</span><span class="sxs-lookup"><span data-stu-id="2892d-119">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="2892d-120">Der **Datentyp " \_ Dateiverweis** " ist wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="2892d-120">The **FILE\_REFERENCE** data type is defined as follows.</span></span>

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a><span data-ttu-id="2892d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2892d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2892d-122">Master Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="2892d-122">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
