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
# <a name="attribute_list_entry-structure"></a>Struktur des Attribut \_ Listen \_ Eintrags

\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]

Stellt einen Eintrag in der Attribut Liste dar.

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**Attributetypecode**
</dt> <dd>

Der Attributtyp Code.



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_ Informationen**</dt> <dt>0x10</dt> </dl> | Dateiattribute (z. b. "schreibgeschützt" und "Archiv"), Zeitstempel (z. b. Dateierstellung und Letzte Änderung) und die Anzahl der festen Links.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ Liste**</dt> <dt>0x20</dt> </dl>                   | Eine Liste der Attribute, die die Datei bilden, und der Datei Verweis des MFT-Datei Datensatzes, in dem sich die einzelnen Attribute befinden.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ Name**</dt> <dt>0x30</dt> </dl>                                  | Der Name der Datei in Unicode-Zeichen.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ ID**</dt> <dt>0x40</dt> </dl>                                  | Ein 16-Byte-Objekt Bezeichner, der vom Link Überwachungsdienst zugewiesen wird.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$Volume \_ Name**</dt> <dt>0x60</dt> </dl>                            | Die Volumebezeichnung. In der $Volume-Datei vorhanden.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$Volume \_ Informationen**</dt> <dt>0x70</dt> </dl>       | Die Volumeinformationen. In der $Volume-Datei vorhanden.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$Data**</dt> <dt>0x80</dt> </dl>                                                  | Der Inhalt der Datei.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$Index \_**</dt>Stamm <dt>0x90</dt> </dl>                               | Wird verwendet, um die Dateinamen Zuordnung für große Verzeichnisse zu implementieren.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$Index \_ Zuordnung**</dt> <dt>0xa0</dt> </dl>             | Wird verwendet, um die Dateinamen Zuordnung für große Verzeichnisse zu implementieren.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$Bitmap**</dt> <dt>0xb0</dt> </dl>                                            | Ein Bitmapindex für ein großes Verzeichnis.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ Punkt**</dt> <dt>0xC0</dt> </dl>                      | Die Daten des Analyse Punkts.<br/>                                                                                                          |



 

</dd> <dt>

**RecordLength**
</dt> <dd>

Die Größe dieser-Struktur zuzüglich des optionalen namens Puffers in Bytes.

</dd> <dt>

**Attributenamelength**
</dt> <dd>

Die Größe des optionalen Attribut namens in Zeichen. Wenn ein Name vorhanden ist, ist dieser Wert ungleich NULL, und der Struktur wird sofort eine Unicode-Zeichenfolge mit der angegebenen Anzahl von Zeichen folgen.

</dd> <dt>

**Attributenameoffset**
</dt> <dd>

Reserviert.

</dd> <dt>

**Lowestvcn**
</dt> <dd>

Die niedrigste virtuelle Cluster Nummer (VCN) für dieses Attribut. Dieser Member ist 0 (null), es sei denn, das Attribut erfordert mehrere Datei Daten Satz Segmente und es sei denn, dieser Eintrag ist ein Verweis auf ein anderes Segment als das erste. In diesem Fall ist dieser Wert die niedrigste VCN, die vom referenzierten Segment beschrieben wird.

</dd> <dt>

**Segmentreference**
</dt> <dd>

Das MFT-Segment (Master File Table), in dem sich das Attribut befindet. Siehe [**\_ \_ Referenz zu MFT-Segmenten**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**AttributeName**
</dt> <dd>

Der Anfang des optionalen Attribut namens.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Liste der Attribute ist eine geordnete Liste von in der Quadword ausgerichteten **Attribut \_ Listen \_ Eintrags** Strukturen. Diese Liste wird zuerst nach dem Attributtyp Code und dann nach dem Attributnamen (falls vorhanden) geordnet. Zwei Attribute können nicht den gleichen Typcode, den gleichen Namen und den niedrigsten VCN aufweisen. Daher kann es höchstens ein Attribut für jeden Typcode ohne Namen geben.

Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.

Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Master Dateitabelle](master-file-table.md)
</dt> </dl>

 

 
