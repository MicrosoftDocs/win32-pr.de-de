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
# <a name="file_record_segment_header-structure"></a>\_Header Struktur des Datei Daten Satz \_ Segments \_

\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]

Stellt das Datei Daten Satz Segment dar. Dies ist der Header für jedes Datei Daten Satz Segment in der Master Dateitabelle (Master File Table, MFT).

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

**Multisector-Header**
</dt> <dd>

Der durch den Cache-Manager definierte multisektorheader. Die [**\_ \_ multisektorheader**](multi-sector-header.md) -Struktur enthält immer die Signatur "file" und eine Beschreibung der Position und Größe des Update Sequenz Arrays.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reserviert.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Die Sequenznummer. Dieser Wert wird jedes Mal inkrementiert, wenn ein Datei Daten Satz Segment freigegeben wird. der Wert ist 0, wenn das Segment nicht verwendet wird. Das **sequencenüberber** -Feld eines Datei Verweises muss mit dem Inhalt dieses Felds identisch sein. Wenn Sie nicht stimmen, ist der Datei Verweis falsch und wahrscheinlich veraltet.

</dd> <dt>

**"Reserved2"**
</dt> <dd>

Reserviert.

</dd> <dt>

**Firstatus tributeoffset**
</dt> <dd>

Der Offset des ersten Attributdaten Satzes in Byte.

</dd> <dt>

**Flags**
</dt> <dd>

Die Dateiflags.

<dl> <dt>

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**Datei \_ \_ \_ \_ Verwendende Daten Satz Segment** (0x0001)
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**Datei \_ Der \_ Dateiname \_ Index ist \_ vorhanden** (0x0002).
</dt> </dl> </dd> <dt>

**"Reserved3"**
</dt> <dd>

Reserviert.

</dd> <dt>

**Basefilerecordsegment**
</dt> <dd>

Ein Datei Verweis auf das Basisdatei Daten Satz Segment für diese Datei. Wenn dies der Basisdatei Daten Satz ist, ist der Wert 0. Siehe [**\_ \_ Referenz zu MFT-Segmenten**](mft-segment-reference.md).

</dd> <dt>

**"Reserved4"**
</dt> <dd>

Reserviert.

</dd> <dt>

**Updatesequencearray**
</dt> <dd>

Das Aktualisierungs Sequenz Array zum Schutz der multisektorübertragungen des Datei Daten Satz Segments.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.

Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Master Dateitabelle](master-file-table.md)
</dt> </dl>

 

 
