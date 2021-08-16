---
description: Stellt eine Adresse in der Masterdateitabelle (Master File Table, MFT) dar. Die Adresse wird mit einer zirkulären wiederverwendeten Sequenznummer gekennzeichnet, die zum Zeitpunkt der Gültigkeit des MFT-Segmentverweises festgelegt wurde.
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
ms.openlocfilehash: 0ef3ad4e727465b5ceb24c1ecc785f62b747da8113b8853bffc3431604089066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827086"
---
# <a name="mft_segment_reference-structure"></a>MFT \_ SEGMENT \_ REFERENCE-Struktur

\[Diese Struktur ist nur für Version 3 von NTFS-Volumes gültig. Sie kann in zukünftigen Versionen geändert werden.\]

Stellt eine Adresse in der Masterdateitabelle (Master File Table, MFT) dar. Die Adresse wird mit einer zirkulären wiederverwendeten Sequenznummer gekennzeichnet, die zum Zeitpunkt der Gültigkeit des MFT-Segmentverweises festgelegt wurde.

## <a name="syntax"></a>Syntax


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a>Member

<dl> <dt>

**SegmentNumberLowPart**
</dt> <dd>

Der untere Teil der Segmentnummer.

</dd> <dt>

**SegmentNumberHighPart**
</dt> <dd>

Der hohe Teil der Segmentnummer.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Die Sequenznummer ungleich 0 (null). Der Wert 0 ist reserviert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass für diese Struktur keine Headerdatei zugeordnet ist.

Diese Strukturdefinition ist nur für Hauptversion 3 und Nebenversion 0 oder 1 gültig, wie von [**FSCTL \_ GET \_ NTFS \_ VOLUME \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)gemeldet.

Der **FILE \_ REFERENCE-Datentyp** ist wie folgt definiert.

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Masterdateitabelle](master-file-table.md)
</dt> </dl>

 

 
