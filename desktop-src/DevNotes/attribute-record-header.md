---
description: Stellt einen Attributdaten Satz dar.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: ATTRIBUTE_RECORD_HEADER Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860615"
---
# <a name="attribute_record_header-structure"></a><span data-ttu-id="4eb25-103">Attribut \_ Daten Satz- \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="4eb25-103">ATTRIBUTE\_RECORD\_HEADER structure</span></span>

<span data-ttu-id="4eb25-104">\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]</span><span class="sxs-lookup"><span data-stu-id="4eb25-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="4eb25-105">Stellt einen Attributdaten Satz dar.</span><span class="sxs-lookup"><span data-stu-id="4eb25-105">Represents an attribute record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb25-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4eb25-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="4eb25-107">Member</span><span class="sxs-lookup"><span data-stu-id="4eb25-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4eb25-108">**TypeCode**</span><span class="sxs-lookup"><span data-stu-id="4eb25-108">**TypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-109">Der Attributtyp Code.</span><span class="sxs-lookup"><span data-stu-id="4eb25-109">The attribute type code.</span></span>



| <span data-ttu-id="4eb25-110">Wert</span><span class="sxs-lookup"><span data-stu-id="4eb25-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="4eb25-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4eb25-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="4eb25-112"><dt>**$Standard \_ Informationen**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="4eb25-113">Dateiattribute (z. b. "schreibgeschützt" und "Archiv"), Zeitstempel (z. b. Dateierstellung und Letzte Änderung) und die Anzahl der festen Links.</span><span class="sxs-lookup"><span data-stu-id="4eb25-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="4eb25-114"><dt>**$Attribute \_ Liste**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="4eb25-115">Eine Liste der Attribute, die die Datei bilden, und der Datei Verweis des MFT-Datei Datensatzes, in dem sich die einzelnen Attribute befinden.</span><span class="sxs-lookup"><span data-stu-id="4eb25-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="4eb25-116"><dt>**$File \_ Name**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="4eb25-117">Der Name der Datei in Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4eb25-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="4eb25-118"><dt>**$Object \_ ID**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="4eb25-119">Ein 64-Byte-Objekt Bezeichner, der vom Link Überwachungsdienst zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4eb25-119">An 64-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="4eb25-120"><dt>**$Volume \_ Name**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="4eb25-121">Die Volumebezeichnung.</span><span class="sxs-lookup"><span data-stu-id="4eb25-121">The volume label.</span></span> <span data-ttu-id="4eb25-122">In der $Volume-Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4eb25-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="4eb25-123"><dt>**$Volume \_ Informationen**</dt> <dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="4eb25-124">Die Volumeinformationen.</span><span class="sxs-lookup"><span data-stu-id="4eb25-124">The volume information.</span></span> <span data-ttu-id="4eb25-125">In der $Volume-Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4eb25-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="4eb25-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="4eb25-127">Der Inhalt der Datei.</span><span class="sxs-lookup"><span data-stu-id="4eb25-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="4eb25-128"><dt>**$Index \_**</dt>Stamm <dt>0x90</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="4eb25-129">Wird verwendet, um die Dateinamen Zuordnung für große Verzeichnisse zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="4eb25-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="4eb25-130"><dt>**$Index \_ Zuordnung**</dt> <dt>0xa0</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="4eb25-131">Wird verwendet, um die Dateinamen Zuordnung für große Verzeichnisse zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="4eb25-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="4eb25-132"><dt>**$Bitmap**</dt> <dt>0xb0</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="4eb25-133">Ein Bitmapindex für ein großes Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="4eb25-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="4eb25-134"><dt>**$REPARSE \_ Punkt**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="4eb25-135">Die Daten des Analyse Punkts.</span><span class="sxs-lookup"><span data-stu-id="4eb25-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="4eb25-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="4eb25-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-137">Die Größe des Attributdaten Satzes in Byte.</span><span class="sxs-lookup"><span data-stu-id="4eb25-137">The size of the attribute record, in bytes.</span></span> <span data-ttu-id="4eb25-138">Dieser Wert gibt die erforderliche Größe für die Daten Satz Variante an und wird immer auf die nächstgelegene Quadword-Grenze gerundet.</span><span class="sxs-lookup"><span data-stu-id="4eb25-138">This value reflects the required size for the record variant and is always rounded to the nearest quadword boundary.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-139">**FormCode**</span><span class="sxs-lookup"><span data-stu-id="4eb25-139">**FormCode**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-140">Der Attribut Formular Code.</span><span class="sxs-lookup"><span data-stu-id="4eb25-140">The attribute form code.</span></span>



| <span data-ttu-id="4eb25-141">Wert</span><span class="sxs-lookup"><span data-stu-id="4eb25-141">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="4eb25-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4eb25-142">Meaning</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <span data-ttu-id="4eb25-143"><dt>**Residente \_ Formular**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-143"><dt>**RESIDENT\_FORM**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="4eb25-144">Der Wert ist im Datei Daten Satz enthalten und folgt unmittelbar dem Attributdaten Satz Header.</span><span class="sxs-lookup"><span data-stu-id="4eb25-144">The value is contained in the file record and immediately follows the attribute record header.</span></span><br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <span data-ttu-id="4eb25-145"><dt>**Nicht residente \_ Formular**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="4eb25-145"><dt>**NONRESIDENT\_FORM**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="4eb25-146">Der Wert ist in anderen Sektoren auf dem Datenträger enthalten.</span><span class="sxs-lookup"><span data-stu-id="4eb25-146">The value is contained in other sectors on the disk.</span></span><br/>                                           |



 

</dd> <dt>

<span data-ttu-id="4eb25-147">**NameLength**</span><span class="sxs-lookup"><span data-stu-id="4eb25-147">**NameLength**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-148">Die Größe des optionalen Attribut namens in Zeichen oder 0, wenn kein Attribut Name vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4eb25-148">The size of the optional attribute name, in characters, or 0 if there is no attribute name.</span></span> <span data-ttu-id="4eb25-149">Die maximale Länge des Attribut namens beträgt 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4eb25-149">The maximum attribute name length is 255 characters.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-150">**Nameoffset**</span><span class="sxs-lookup"><span data-stu-id="4eb25-150">**NameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-151">Der Offset des Attribut namens vom Anfang des Attributdaten Satzes in Byte.</span><span class="sxs-lookup"><span data-stu-id="4eb25-151">The offset of the attribute name from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="4eb25-152">Wenn der **namelength** -Member 0 ist, ist dieser Member nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4eb25-152">If the **NameLength** member is 0, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-153">**Flags**</span><span class="sxs-lookup"><span data-stu-id="4eb25-153">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-154">Die Attributflags.</span><span class="sxs-lookup"><span data-stu-id="4eb25-154">The attribute flags.</span></span>

<dl> <dt>

<span data-ttu-id="4eb25-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Attribut \_ Flag- \_ Komprimierungs \_ Maske** (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="4eb25-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATTRIBUTE\_FLAG\_COMPRESSION\_MASK** (0x00FF)</span></span>
</dt> <dt>

<span data-ttu-id="4eb25-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Attribut \_ \_Sparse-Flag** (0X8000)</span><span class="sxs-lookup"><span data-stu-id="4eb25-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATTRIBUTE\_FLAG\_SPARSE** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="4eb25-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Attribut \_ Flag \_ verschlüsselt** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="4eb25-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATTRIBUTE\_FLAG\_ENCRYPTED** (0x4000)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="4eb25-158">**Instanz**</span><span class="sxs-lookup"><span data-stu-id="4eb25-158">**Instance**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-159">Die eindeutige Instanz für dieses Attribut im Datei Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="4eb25-159">The unique instance for this attribute in the file record.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-160">**Form**</span><span class="sxs-lookup"><span data-stu-id="4eb25-160">**Form**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-161">Wenn sich der **FormCode** -Member in einem Residenten \_ Formular befindet, ist die Union eine **residente** Struktur.</span><span class="sxs-lookup"><span data-stu-id="4eb25-161">If the **FormCode** member is RESIDENT\_FORM, the union is a **Resident** structure.</span></span> <span data-ttu-id="4eb25-162">Wenn **FormCode** nicht residente \_ Form ist, ist die Union eine **nicht residente** Struktur.</span><span class="sxs-lookup"><span data-stu-id="4eb25-162">If **FormCode** is NONRESIDENT\_FORM, the union is a **Nonresident** structure.</span></span>

<dl> <dt>

<span data-ttu-id="4eb25-163">**Bewohnten**</span><span class="sxs-lookup"><span data-stu-id="4eb25-163">**Resident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb25-164">**Valuelength**</span><span class="sxs-lookup"><span data-stu-id="4eb25-164">**ValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-165">Die Größe des Attribut Werts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4eb25-165">The size of the attribute value, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-166">**Valueoffset**</span><span class="sxs-lookup"><span data-stu-id="4eb25-166">**ValueOffset**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-167">Der Offset bis zum Wert vom Anfang des Attributdaten Satzes in Byte.</span><span class="sxs-lookup"><span data-stu-id="4eb25-167">The offset to the value from the start of the attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-168">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="4eb25-168">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-169">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="4eb25-169">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4eb25-170">**Nicht residente**</span><span class="sxs-lookup"><span data-stu-id="4eb25-170">**Nonresident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb25-171">**Lowestvcn**</span><span class="sxs-lookup"><span data-stu-id="4eb25-171">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-172">Die niedrigste virtuelle Cluster Nummer (VCN), die von diesem Attributdaten Satz abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="4eb25-172">The lowest virtual cluster number (VCN) covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-173">**Highestvcn**</span><span class="sxs-lookup"><span data-stu-id="4eb25-173">**HighestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-174">Die höchste VCN, die von diesem Attributdaten Satz abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="4eb25-174">The highest VCN covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-175">**Mappingpaare**</span><span class="sxs-lookup"><span data-stu-id="4eb25-175">**MappingPairsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-176">Der Offset für das Array der Zuordnungspaare vom Anfang des Attributdaten Satzes (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="4eb25-176">The offset to the mapping pairs array from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="4eb25-177">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="4eb25-177">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-178">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="4eb25-178">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-179">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="4eb25-179">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-180">**Zu"zuder Länge"**</span><span class="sxs-lookup"><span data-stu-id="4eb25-180">**AllocatedLength**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-181">Die zugeordnete Größe der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4eb25-181">The allocated size of the file, in bytes.</span></span> <span data-ttu-id="4eb25-182">Dieser Wert ist ein gleich Vielfaches der Clustergröße.</span><span class="sxs-lookup"><span data-stu-id="4eb25-182">This value is an even multiple of the cluster size.</span></span> <span data-ttu-id="4eb25-183">Dieser Member ist ungültig, wenn der **lowestvcn** -Member ungleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="4eb25-183">This member is not valid if the **LowestVcn** member is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-184">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="4eb25-184">**FileSize**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-185">Die Dateigröße (das höchste Byte, das gelesen werden kann, plus 1) in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4eb25-185">The file size (highest byte that can be read plus 1), in bytes.</span></span> <span data-ttu-id="4eb25-186">Dieser Member ist ungültig, wenn **lowestvcn** ungleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="4eb25-186">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-187">**Validdatalength**</span><span class="sxs-lookup"><span data-stu-id="4eb25-187">**ValidDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-188">Die gültige Daten Länge (das höchste initialisierte Byte plus 1) in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4eb25-188">The valid data length (highest initialized byte plus 1), in bytes.</span></span> <span data-ttu-id="4eb25-189">Dieser Wert wird auf die nächste Cluster Grenze gerundet.</span><span class="sxs-lookup"><span data-stu-id="4eb25-189">This value is rounded to the nearest cluster boundary.</span></span> <span data-ttu-id="4eb25-190">Dieser Member ist ungültig, wenn **lowestvcn** ungleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="4eb25-190">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="4eb25-191">**Total zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="4eb25-191">**TotalAllocated**</span></span>
</dt> <dd>

<span data-ttu-id="4eb25-192">Die Gesamtmenge, die für die Datei zugewiesen wurde (die Summe der zugewiesenen Cluster).</span><span class="sxs-lookup"><span data-stu-id="4eb25-192">The total allocated for the file (the sum of the allocated clusters).</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4eb25-193">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4eb25-193">Remarks</span></span>

<span data-ttu-id="4eb25-194">Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.</span><span class="sxs-lookup"><span data-stu-id="4eb25-194">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="4eb25-195">Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.</span><span class="sxs-lookup"><span data-stu-id="4eb25-195">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="4eb25-196">Attributdaten Sätze werden immer an einer Quadword-Grenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="4eb25-196">Attribute records are always aligned on a quadword boundary.</span></span>

<span data-ttu-id="4eb25-197">Wenn das Attribut nicht Resident ist, enthält der Attributdaten Satz Header eine Liste mit Abruf Informationen, die eine Zuordnung zwischen VCN und logischer Cluster Nummer (LCN) für das Attribut bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4eb25-197">If the attribute is nonresident, the attribute record header contains a list of retrieval information that provides a mapping between VCN and logical cluster number (LCN) for the attribute.</span></span> <span data-ttu-id="4eb25-198">Wenn die Abruf Informationen nicht in das Basisdatei Segment passen, können Sie in einem externen Datei Daten Satz Segment eigenständig gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4eb25-198">If the retrieval information does not fit in the base file segment, it can be stored in an external file record segment by itself.</span></span> <span data-ttu-id="4eb25-199">Wenn es immer noch nicht in ein externes Datei Daten Satz Segment passt, gibt es eine Bereitstellung in der Attribut Liste, die mehrere Einträge für ein Attribut enthält, das zusätzliche Abruf Informationen erfordert.</span><span class="sxs-lookup"><span data-stu-id="4eb25-199">If it still does not fit into one external file record segment, there is a provision in the attribute list to contain multiple entries for an attribute that requires additional retrieval information.</span></span>

<span data-ttu-id="4eb25-200">Das Array der Zuordnungspaare wird in komprimierter Form gespeichert und geht davon aus, dass die Informationen dekomprimiert und vom System zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4eb25-200">The mapping pairs array is stored in a compressed form and assumes that the information is decompressed and cached by the system.</span></span> <span data-ttu-id="4eb25-201">Sie besteht aus einer Reihe von nextvcn/currentlcn-Paaren.</span><span class="sxs-lookup"><span data-stu-id="4eb25-201">It consists of a series of NextVcn/CurrentLcn pairs.</span></span> <span data-ttu-id="4eb25-202">Wenn eine Datei z. b. eine einzelne Ausführen von 8 Clustern, beginnend bei LCN 128, und die Datei bei lowestvcn 0 startet, verfügt das Array der Zuordnungspaare nur über einen Eintrag (nextvcn = 8 und currentlcn = 128).</span><span class="sxs-lookup"><span data-stu-id="4eb25-202">For example, if a file has a single run of 8 clusters starting at LCN 128 and the file starts at LowestVcn 0, then the mapping pairs array has just one entry, which is NextVcn=8 and CurrentLcn=128.</span></span> <span data-ttu-id="4eb25-203">Das Array ist ein Bytestream, der die Änderungen an den Arbeits Variablen speichert, wenn Sie sequenziell verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="4eb25-203">The array is a byte stream that stores the changes to the working variables when processed sequentially.</span></span> <span data-ttu-id="4eb25-204">Der Bytestream muss wie folgt als ein null terminierter Stream von drei-ELN interpretiert werden:</span><span class="sxs-lookup"><span data-stu-id="4eb25-204">The byte stream is to be interpreted as a zero-terminated stream of triples, as follows:</span></span>

<span data-ttu-id="4eb25-205">count Byte = *v* + (*l* \* 16)</span><span class="sxs-lookup"><span data-stu-id="4eb25-205">count byte = *v* + (*l* \* 16)</span></span>

<span data-ttu-id="4eb25-206">Dabei ist *v* die Anzahl der geänderten VCN-Bytes mit niedriger Ordnung und *l* die Anzahl der geänderten LCN-Bytes mit niedriger Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4eb25-206">where *v* is the number of changed low-order VCN bytes and *l* is the number of changed low-order LCN bytes.</span></span>

<span data-ttu-id="4eb25-207">Der Dekomprimierungs Algorithmus lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4eb25-207">The decompression algorithm is as follows:</span></span>

1.  <span data-ttu-id="4eb25-208">Initialisieren Sie nextvcn auf `Attribute->LowestVcn` und currentlcn auf 0.</span><span class="sxs-lookup"><span data-stu-id="4eb25-208">Initialize NextVcn to `Attribute->LowestVcn` and CurrentLcn to 0.</span></span>
2.  <span data-ttu-id="4eb25-209">Initialisieren Sie den bytestreamzeiger auf `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .</span><span class="sxs-lookup"><span data-stu-id="4eb25-209">Initialize the byte stream pointer to `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset`.</span></span>
3.  <span data-ttu-id="4eb25-210">Legen Sie currentvcn auf nextvcn fest.</span><span class="sxs-lookup"><span data-stu-id="4eb25-210">Set CurrentVcn to NextVcn.</span></span>
4.  <span data-ttu-id="4eb25-211">Liest das nächste Byte aus dem Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="4eb25-211">Read the next byte from the stream.</span></span> <span data-ttu-id="4eb25-212">Wenn der Wert 0 ist, dann unterbrechen. Extrahieren Sie andernfalls *v* und *l* wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4eb25-212">If it is 0, then break; else extract *v* and *l* as previously described.</span></span>
5.  <span data-ttu-id="4eb25-213">Interpretieren Sie die nächsten *v* Bytes als signierte Menge mit dem nieder wertigen Byte zuerst.</span><span class="sxs-lookup"><span data-stu-id="4eb25-213">Interpret the next *v* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="4eb25-214">Entpacken Sie die Anmelde Informationen in 64 Bits, und fügen Sie Sie nextvcn hinzu.</span><span class="sxs-lookup"><span data-stu-id="4eb25-214">Unpack it sign-extended into 64 bits and add it to NextVcn.</span></span>
6.  <span data-ttu-id="4eb25-215">Interpretieren Sie die nächsten *l* -Bytes als signierte Menge mit dem nieder wertigen Byte First.</span><span class="sxs-lookup"><span data-stu-id="4eb25-215">Interpret the next *l* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="4eb25-216">Entpacken Sie Sign-Extended in 64 Bits, und fügen Sie es currentlcn hinzu.</span><span class="sxs-lookup"><span data-stu-id="4eb25-216">Unpack it sign-extended into 64 bits and add it to CurrentLcn.</span></span> <span data-ttu-id="4eb25-217">Wenn dies eine currentlcn von 0 ergibt, wird der vcns von currentvcn zu nextvcn – 1 nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4eb25-217">If this produces a CurrentLcn of 0, then the VCNs from CurrentVcn to NextVcn–1 are unallocated.</span></span>
7.  <span data-ttu-id="4eb25-218">Aktualisieren Sie die zwischengespeicherten Mapping-Informationen von currentvcn, nextvcn und currentlcn.</span><span class="sxs-lookup"><span data-stu-id="4eb25-218">Update the cached mapping information from CurrentVcn, NextVcn, and CurrentLcn.</span></span>
8.  <span data-ttu-id="4eb25-219">Fahren Sie mit Schritt 3 fort.</span><span class="sxs-lookup"><span data-stu-id="4eb25-219">Go to step 3.</span></span>

## <a name="see-also"></a><span data-ttu-id="4eb25-220">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4eb25-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb25-221">Master Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="4eb25-221">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
