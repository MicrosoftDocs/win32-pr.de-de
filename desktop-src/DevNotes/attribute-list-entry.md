---
description: Stellt einen Eintrag in der Attributliste dar.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: ATTRIBUTE_LIST_ENTRY-Struktur
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
ms.openlocfilehash: 0c0154de52dbefa6d29278ca05e924db6f6c1d84b124fe21b3092e728a0d07fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956139"
---
# <a name="attribute_list_entry-structure"></a>ATTRIBUTE \_ LIST \_ ENTRY-Struktur

\[Diese Struktur ist nur für Version 3 von NTFS-Volumes gültig. sie kann in zukünftigen Versionen geändert werden.\]

Stellt einen Eintrag in der Attributliste dar.

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

**AttributeTypeCode**
</dt> <dd>

Der Attributtypcode.



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$STANDARD \_ INFORMATION**</dt> <dt>0X10</dt> </dl> | Dateiattribute (z. B. schreibgeschützt und archivieren), Zeitstempel (z. B. Dateierstellung und letzte Änderung) und die Anzahl der hardlinks.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$ATTRIBUTE \_ LIST**</dt> <dt>0x20</dt> </dl>                   | Eine Liste der Attribute, aus denen die Datei besteht, und der Dateiverweis des MFT-Dateidatensatz, in dem sich jedes Attribut befindet.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$FILE \_ NAME**</dt> <dt>0x30</dt> </dl>                                  | Der Name der Datei in Unicode-Zeichen.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$OBJECT \_ ID-0x40**</dt> <dt></dt> </dl>                                  | Ein vom Linkverfolgungsdienst zugewiesener 16-Byte-Objektbezeichner.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$VOLUME \_ NAME**</dt> <dt>0x60</dt> </dl>                            | Die Volumebezeichnung. In der $Volume vorhanden.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$VOLUME \_ INFORMATION**</dt> <dt>0X70</dt> </dl>       | Die Volumeinformationen. In der $Volume vorhanden.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$DATA**</dt> <dt>0x80</dt> </dl>                                                  | Der Inhalt der Datei.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$INDEX \_ ROOT-0x90**</dt> <dt></dt> </dl>                               | Wird zum Implementieren der Dateinamenzuordnung für große Verzeichnisse verwendet.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$INDEX \_ ZUORDNUNGS 0XA0**</dt> <dt></dt> </dl>             | Wird zum Implementieren der Dateinamenzuordnung für große Verzeichnisse verwendet.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$BITMAP**</dt> <dt>0xB0</dt> </dl>                                            | Ein Bitmapindex für ein großes Verzeichnis.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ POINT**</dt> <dt>0xC0</dt> </dl>                      | Die Reparsepunktdaten.<br/>                                                                                                          |



 

</dd> <dt>

**Recordlength**
</dt> <dd>

Die Größe dieser Struktur sowie der optionale Namenspuffer in Bytes.

</dd> <dt>

**AttributeNameLength**
</dt> <dd>

Die Größe des optionalen Attributnamens in Zeichen. Wenn ein Name vorhanden ist, ist dieser Wert ungleich null, und auf die Struktur folgt sofort eine Unicode-Zeichenfolge mit der angegebenen Anzahl von Zeichen.

</dd> <dt>

**AttributeNameOffset**
</dt> <dd>

Reserviert.

</dd> <dt>

**LowestVcn**
</dt> <dd>

Die niedrigste virtuelle Clusternummer (VCN) für dieses Attribut. Dieser Member ist 0 (null), es sei denn, das Attribut erfordert mehrere Dateidatensatzsegmente, und es sei denn, dieser Eintrag ist ein Verweis auf ein anderes Segment als das erste. In diesem Fall ist dieser Wert der niedrigste VCN, der vom Referenzsegment beschrieben wird.

</dd> <dt>

**SegmentReference**
</dt> <dd>

Das MFT-Segment (Master File Table), in dem sich das Attribut befindet. Siehe [**\_ MFT-SEGMENTREFERENZ \_**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**AttributeName**
</dt> <dd>

Der Anfang des optionalen Attributnamens.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Attributliste ist eine geordnete Liste von ATTRIBUTE **\_ LIST \_ ENTRY-Strukturen** mit Quadword-Ausrichtung. Diese Liste wird zuerst nach dem Attributtypcode und dann nach dem Attributnamen (sofern vorhanden) geordnet. Zwei Attribute können nicht denselben Typcode, Namen und niedrigsten VCN haben. Daher kann es für jeden Typcode ohne Namen nur ein Attribut geben.

Diese Strukturdefinition ist nur für Hauptversion 3 und Nebenversion 0 oder 1 gültig, wie von [**FSCTL \_ GET NTFS VOLUME DATA \_ \_ \_ gemeldet.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)

Beachten Sie, dass keine zugeordnete Headerdatei für diese -Struktur enthalten ist.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Masterdateitabelle](master-file-table.md)
</dt> </dl>

 

 
