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
# <a name="mft_segment_reference-structure"></a>MFT- \_ Segment \_ Verweis Struktur

\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]

Stellt eine Adresse in der Master Dateitabelle (MFT) dar. Die Adresse wird mit einer zirkulär wiederverwendeten Sequenznummer gekennzeichnet, die zum Zeitpunkt der Gültigkeit des MFT-Segment Verweises festgelegt wird.

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

**Segmentnumlowpart**
</dt> <dd>

Der niedrige Teil der Segment Nummer.

</dd> <dt>

**Segmentnumhighpart**
</dt> <dd>

Der hohe Teil der Segment Nummer.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Die Sequenznummer ungleich 0 (null). Der Wert 0 ist reserviert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.

Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.

Der **Datentyp " \_ Dateiverweis** " ist wie folgt definiert.

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Master Dateitabelle](master-file-table.md)
</dt> </dl>

 

 
