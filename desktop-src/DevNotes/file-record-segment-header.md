---
description: Stellt das Datei Daten Satz Segment dar. Dies ist der Header für jedes Datei Daten Satz Segment in der Master Dateitabelle (Master File Table, MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: FILE_RECORD_SEGMENT_HEADER Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214041"
---
# <a name="file_record_segment_header-structure"></a><span data-ttu-id="3ce33-104">\_Header Struktur des Datei Daten Satz \_ Segments \_</span><span class="sxs-lookup"><span data-stu-id="3ce33-104">FILE\_RECORD\_SEGMENT\_HEADER structure</span></span>

<span data-ttu-id="3ce33-105">\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]</span><span class="sxs-lookup"><span data-stu-id="3ce33-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="3ce33-106">Stellt das Datei Daten Satz Segment dar.</span><span class="sxs-lookup"><span data-stu-id="3ce33-106">Represents the file record segment.</span></span> <span data-ttu-id="3ce33-107">Dies ist der Header für jedes Datei Daten Satz Segment in der Master Dateitabelle (Master File Table, MFT).</span><span class="sxs-lookup"><span data-stu-id="3ce33-107">This is the header for each file record segment in the master file table (MFT).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce33-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ce33-108">Syntax</span></span>


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a><span data-ttu-id="3ce33-109">Member</span><span class="sxs-lookup"><span data-stu-id="3ce33-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ce33-110">**Multisector-Header**</span><span class="sxs-lookup"><span data-stu-id="3ce33-110">**MultiSectorHeader**</span></span>
</dt> <dd>

<span data-ttu-id="3ce33-111">Der durch den Cache-Manager definierte multisektorheader.</span><span class="sxs-lookup"><span data-stu-id="3ce33-111">The multisector header defined by the cache manager.</span></span> <span data-ttu-id="3ce33-112">Die [**\_ \_ multisektorheader**](multi-sector-header.md) -Struktur enthält immer die Signatur "file" und eine Beschreibung der Position und Größe des Update Sequenz Arrays.</span><span class="sxs-lookup"><span data-stu-id="3ce33-112">The [**MULTI\_SECTOR\_HEADER**](multi-sector-header.md) structure always contains the signature "FILE" and a description of the location and size of the update sequence array.</span></span>

</dd> <dt>

<span data-ttu-id="3ce33-113">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="3ce33-113">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="3ce33-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="3ce33-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="3ce33-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="3ce33-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="3ce33-116">Die Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="3ce33-116">The sequence number.</span></span> <span data-ttu-id="3ce33-117">Dieser Wert wird jedes Mal inkrementiert, wenn ein Datei Daten Satz Segment freigegeben wird. der Wert ist 0, wenn das Segment nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ce33-117">This value is incremented each time that a file record segment is freed; it is 0 if the segment is not used.</span></span> <span data-ttu-id="3ce33-118">Das **sequencenüberber** -Feld eines Datei Verweises muss mit dem Inhalt dieses Felds identisch sein. Wenn Sie nicht stimmen, ist der Datei Verweis falsch und wahrscheinlich veraltet.</span><span class="sxs-lookup"><span data-stu-id="3ce33-118">The **SequenceNumber** field of a file reference must match the contents of this field; if they do not match, the file reference is incorrect and probably obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="3ce33-119">**"Reserved2"**</span><span class="sxs-lookup"><span data-stu-id="3ce33-119">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="3ce33-120">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="3ce33-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="3ce33-121">**Firstatus tributeoffset**</span><span class="sxs-lookup"><span data-stu-id="3ce33-121">**FirstAttributeOffset**</span></span>
</dt> <dd>

<span data-ttu-id="3ce33-122">Der Offset des ersten Attributdaten Satzes in Byte.</span><span class="sxs-lookup"><span data-stu-id="3ce33-122">The offset of the first attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3ce33-123">**Flags**</span><span class="sxs-lookup"><span data-stu-id="3ce33-123">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="3ce33-124">Die Dateiflags.</span><span class="sxs-lookup"><span data-stu-id="3ce33-124">The file flags.</span></span>

<dl> <dt>

<span data-ttu-id="3ce33-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**Datei \_ \_ \_ \_ Verwendende Daten Satz Segment** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="3ce33-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**FILE\_RECORD\_SEGMENT\_IN\_USE** (0x0001)</span></span>
</dt> <dt>

<span data-ttu-id="3ce33-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**Datei \_ Der \_ Dateiname \_ Index ist \_ vorhanden** (0x0002).</span><span class="sxs-lookup"><span data-stu-id="3ce33-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**FILE\_FILE\_NAME\_INDEX\_PRESENT** (0x0002)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3ce33-127">**"Reserved3"**</span><span class="sxs-lookup"><span data-stu-id="3ce33-127">**Reserved3**</span></span>
</dt> <dd>

<span data-ttu-id="3ce33-128">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="3ce33-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="3ce33-129">**Basefilerecordsegment**</span><span class="sxs-lookup"><span data-stu-id="3ce33-129">**BaseFileRecordSegment**</span></span>
</dt> <dd>

<span data-ttu-id="3ce33-130">Ein Datei Verweis auf das Basisdatei Daten Satz Segment für diese Datei.</span><span class="sxs-lookup"><span data-stu-id="3ce33-130">A file reference to the base file record segment for this file.</span></span> <span data-ttu-id="3ce33-131">Wenn dies der Basisdatei Daten Satz ist, ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="3ce33-131">If this is the base file record, the value is 0.</span></span> <span data-ttu-id="3ce33-132">Siehe [**\_ \_ Referenz zu MFT-Segmenten**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3ce33-132">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ce33-133">**"Reserved4"**</span><span class="sxs-lookup"><span data-stu-id="3ce33-133">**Reserved4**</span></span>
</dt> <dd>

<span data-ttu-id="3ce33-134">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="3ce33-134">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="3ce33-135">**Updatesequencearray**</span><span class="sxs-lookup"><span data-stu-id="3ce33-135">**UpdateSequenceArray**</span></span>
</dt> <dd>

<span data-ttu-id="3ce33-136">Das Aktualisierungs Sequenz Array zum Schutz der multisektorübertragungen des Datei Daten Satz Segments.</span><span class="sxs-lookup"><span data-stu-id="3ce33-136">The update sequence array to protect multisector transfers of the file record segment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ce33-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ce33-137">Remarks</span></span>

<span data-ttu-id="3ce33-138">Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.</span><span class="sxs-lookup"><span data-stu-id="3ce33-138">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="3ce33-139">Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.</span><span class="sxs-lookup"><span data-stu-id="3ce33-139">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="3ce33-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ce33-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce33-141">Master Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="3ce33-141">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
