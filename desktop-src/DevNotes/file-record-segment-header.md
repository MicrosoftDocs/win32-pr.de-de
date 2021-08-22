---
description: Stellt das Dateidatensatzsegment dar. Dies ist der Header für jedes Dateidatensatzsegment in der Masterdateitabelle (Master File Table, MFT).
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
ms.openlocfilehash: 0c9d7a3653ad965141e691546866f599d8615f5f12feb92fa25c861d7c429b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260600"
---
# <a name="file_record_segment_header-structure"></a>FILE \_ RECORD \_ SEGMENT \_ HEADER-Struktur

\[Diese Struktur ist nur für Version 3 von NTFS-Volumes gültig. Sie kann in zukünftigen Versionen geändert werden.\]

Stellt das Dateidatensatzsegment dar. Dies ist der Header für jedes Dateidatensatzsegment in der Masterdateitabelle (Master File Table, MFT).

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**MultiSectorHeader**
</dt> <dd>

Der vom Cache-Manager definierte Multisectorheader. Die [**MULTI \_ SECTOR \_ HEADER-Struktur**](multi-sector-header.md) enthält immer die Signatur "FILE" und eine Beschreibung des Speicherorts und der Größe des Updatesequenzarrays.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reserviert.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Die Sequenznummer. Dieser Wert wird jedes Mal erhöht, wenn ein Dateidatensatzsegment freigegeben wird. ist 0, wenn das Segment nicht verwendet wird. Das **SequenceNumber-Feld** eines Dateiverweis muss mit dem Inhalt dieses Felds übereinstimmen. Wenn sie nicht übereinstimmen, ist der Dateiverweis falsch und wahrscheinlich veraltet.

</dd> <dt>

**Reserviert 2**
</dt> <dd>

Reserviert.

</dd> <dt>

**FirstAttributeOffset**
</dt> <dd>

Der Offset des ersten Attributdatensatzes in Bytes.

</dd> <dt>

**Flags**
</dt> <dd>

Die Dateiflags.

<dl> <dt>

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**FILE \_ VERWENDETES \_ DATENSATZSEGMENT \_ \_** (0x0001)
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**FILE \_ \_ \_ DATEINAMENINDEX \_ VORHANDEN** (0x0002)
</dt> </dl> </dd> <dt>

**Reserviert3**
</dt> <dd>

Reserviert.

</dd> <dt>

**BaseFileRecordSegment**
</dt> <dd>

Ein Dateiverweis auf das Basisdateidatensatzsegment für diese Datei. Wenn dies der Basisdateidatensatz ist, ist der Wert 0. Weitere Informationen finden Sie [**unter \_ MFT-SEGMENTREFERENZ. \_**](mft-segment-reference.md)

</dd> <dt>

**Reserviert4**
</dt> <dd>

Reserviert.

</dd> <dt>

**UpdateSequenceArray**
</dt> <dd>

Das Updatesequenzarray zum Schutz von Multisectorübertragungen des Dateidatensatzsegments.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass für diese Struktur keine Headerdatei zugeordnet ist.

Diese Strukturdefinition ist nur für Hauptversion 3 und Nebenversion 0 oder 1 gültig, wie von [**FSCTL \_ GET \_ NTFS \_ VOLUME \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)gemeldet.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Masterdateitabelle](master-file-table.md)
</dt> </dl>

 

 
