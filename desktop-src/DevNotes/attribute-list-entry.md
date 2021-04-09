---
description: Stellt einen Eintrag in der Attribut Liste dar.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: ATTRIBUTE_LIST_ENTRY Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860616"
---
# <a name="attribute_list_entry-structure"></a><span data-ttu-id="68fc7-103">Struktur des Attribut \_ Listen \_ Eintrags</span><span class="sxs-lookup"><span data-stu-id="68fc7-103">ATTRIBUTE\_LIST\_ENTRY structure</span></span>

<span data-ttu-id="68fc7-104">\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]</span><span class="sxs-lookup"><span data-stu-id="68fc7-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="68fc7-105">Stellt einen Eintrag in der Attribut Liste dar.</span><span class="sxs-lookup"><span data-stu-id="68fc7-105">Represents an entry in the attribute list.</span></span>

## <a name="syntax"></a><span data-ttu-id="68fc7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="68fc7-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a><span data-ttu-id="68fc7-107">Member</span><span class="sxs-lookup"><span data-stu-id="68fc7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="68fc7-108">**Attributetypecode**</span><span class="sxs-lookup"><span data-stu-id="68fc7-108">**AttributeTypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="68fc7-109">Der Attributtyp Code.</span><span class="sxs-lookup"><span data-stu-id="68fc7-109">The attribute type code.</span></span>



| <span data-ttu-id="68fc7-110">Wert</span><span class="sxs-lookup"><span data-stu-id="68fc7-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="68fc7-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="68fc7-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="68fc7-112"><dt>**$Standard \_ Informationen**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="68fc7-113">Dateiattribute (z. b. "schreibgeschützt" und "Archiv"), Zeitstempel (z. b. Dateierstellung und Letzte Änderung) und die Anzahl der festen Links.</span><span class="sxs-lookup"><span data-stu-id="68fc7-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="68fc7-114"><dt>**$Attribute \_ Liste**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="68fc7-115">Eine Liste der Attribute, die die Datei bilden, und der Datei Verweis des MFT-Datei Datensatzes, in dem sich die einzelnen Attribute befinden.</span><span class="sxs-lookup"><span data-stu-id="68fc7-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="68fc7-116"><dt>**$File \_ Name**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="68fc7-117">Der Name der Datei in Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="68fc7-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="68fc7-118"><dt>**$Object \_ ID**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="68fc7-119">Ein 16-Byte-Objekt Bezeichner, der vom Link Überwachungsdienst zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="68fc7-119">An 16-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="68fc7-120"><dt>**$Volume \_ Name**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="68fc7-121">Die Volumebezeichnung.</span><span class="sxs-lookup"><span data-stu-id="68fc7-121">The volume label.</span></span> <span data-ttu-id="68fc7-122">In der $Volume-Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="68fc7-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="68fc7-123"><dt>**$Volume \_ Informationen**</dt> <dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="68fc7-124">Die Volumeinformationen.</span><span class="sxs-lookup"><span data-stu-id="68fc7-124">The volume information.</span></span> <span data-ttu-id="68fc7-125">In der $Volume-Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="68fc7-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="68fc7-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="68fc7-127">Der Inhalt der Datei.</span><span class="sxs-lookup"><span data-stu-id="68fc7-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="68fc7-128"><dt>**$Index \_**</dt>Stamm <dt>0x90</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="68fc7-129">Wird verwendet, um die Dateinamen Zuordnung für große Verzeichnisse zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="68fc7-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="68fc7-130"><dt>**$Index \_ Zuordnung**</dt> <dt>0xa0</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="68fc7-131">Wird verwendet, um die Dateinamen Zuordnung für große Verzeichnisse zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="68fc7-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="68fc7-132"><dt>**$Bitmap**</dt> <dt>0xb0</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="68fc7-133">Ein Bitmapindex für ein großes Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="68fc7-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="68fc7-134"><dt>**$REPARSE \_ Punkt**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="68fc7-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="68fc7-135">Die Daten des Analyse Punkts.</span><span class="sxs-lookup"><span data-stu-id="68fc7-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="68fc7-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="68fc7-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="68fc7-137">Die Größe dieser-Struktur zuzüglich des optionalen namens Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="68fc7-137">The size of this structure, plus the optional name buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="68fc7-138">**Attributenamelength**</span><span class="sxs-lookup"><span data-stu-id="68fc7-138">**AttributeNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="68fc7-139">Die Größe des optionalen Attribut namens in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="68fc7-139">The size of the optional attribute name, in characters.</span></span> <span data-ttu-id="68fc7-140">Wenn ein Name vorhanden ist, ist dieser Wert ungleich NULL, und der Struktur wird sofort eine Unicode-Zeichenfolge mit der angegebenen Anzahl von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="68fc7-140">If a name exists, this value is nonzero and the structure is followed immediately by a Unicode string of the specified number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="68fc7-141">**Attributenameoffset**</span><span class="sxs-lookup"><span data-stu-id="68fc7-141">**AttributeNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="68fc7-142">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="68fc7-142">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="68fc7-143">**Lowestvcn**</span><span class="sxs-lookup"><span data-stu-id="68fc7-143">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="68fc7-144">Die niedrigste virtuelle Cluster Nummer (VCN) für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="68fc7-144">The lowest virtual cluster number (VCN) for this attribute.</span></span> <span data-ttu-id="68fc7-145">Dieser Member ist 0 (null), es sei denn, das Attribut erfordert mehrere Datei Daten Satz Segmente und es sei denn, dieser Eintrag ist ein Verweis auf ein anderes Segment als das erste.</span><span class="sxs-lookup"><span data-stu-id="68fc7-145">This member is zero unless the attribute requires multiple file record segments and unless this entry is a reference to a segment other than the first one.</span></span> <span data-ttu-id="68fc7-146">In diesem Fall ist dieser Wert die niedrigste VCN, die vom referenzierten Segment beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="68fc7-146">In this case, this value is the lowest VCN that is described by the referenced segment.</span></span>

</dd> <dt>

<span data-ttu-id="68fc7-147">**Segmentreference**</span><span class="sxs-lookup"><span data-stu-id="68fc7-147">**SegmentReference**</span></span>
</dt> <dd>

<span data-ttu-id="68fc7-148">Das MFT-Segment (Master File Table), in dem sich das Attribut befindet.</span><span class="sxs-lookup"><span data-stu-id="68fc7-148">The master file table (MFT) segment in which the attribute resides.</span></span> <span data-ttu-id="68fc7-149">Siehe [**\_ \_ Referenz zu MFT-Segmenten**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="68fc7-149">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="68fc7-150">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="68fc7-150">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="68fc7-151">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="68fc7-151">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="68fc7-152">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="68fc7-152">**AttributeName**</span></span>
</dt> <dd>

<span data-ttu-id="68fc7-153">Der Anfang des optionalen Attribut namens.</span><span class="sxs-lookup"><span data-stu-id="68fc7-153">The start of the optional attribute name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68fc7-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68fc7-154">Remarks</span></span>

<span data-ttu-id="68fc7-155">Die Liste der Attribute ist eine geordnete Liste von in der Quadword ausgerichteten **Attribut \_ Listen \_ Eintrags** Strukturen.</span><span class="sxs-lookup"><span data-stu-id="68fc7-155">The attributes list is an ordered list of quadword-aligned **ATTRIBUTE\_LIST\_ENTRY** structures.</span></span> <span data-ttu-id="68fc7-156">Diese Liste wird zuerst nach dem Attributtyp Code und dann nach dem Attributnamen (falls vorhanden) geordnet.</span><span class="sxs-lookup"><span data-stu-id="68fc7-156">This list is ordered first by the attribute type code and then by the attribute name (if present).</span></span> <span data-ttu-id="68fc7-157">Zwei Attribute können nicht den gleichen Typcode, den gleichen Namen und den niedrigsten VCN aufweisen.</span><span class="sxs-lookup"><span data-stu-id="68fc7-157">No two attributes can have the same type code, name, and lowest VCN.</span></span> <span data-ttu-id="68fc7-158">Daher kann es höchstens ein Attribut für jeden Typcode ohne Namen geben.</span><span class="sxs-lookup"><span data-stu-id="68fc7-158">Therefore, there can be at most one attribute for each type code without a name.</span></span>

<span data-ttu-id="68fc7-159">Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.</span><span class="sxs-lookup"><span data-stu-id="68fc7-159">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="68fc7-160">Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.</span><span class="sxs-lookup"><span data-stu-id="68fc7-160">Note that there is no associated header file for this structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="68fc7-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68fc7-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68fc7-162">Master Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="68fc7-162">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
