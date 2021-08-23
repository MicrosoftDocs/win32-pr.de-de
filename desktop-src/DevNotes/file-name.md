---
description: Stellt ein Dateinamenattribut dar. Eine Datei verfügt über ein Dateinamenattribut für jedes Verzeichnis, in das sie eingegeben wird.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: FILE_NAME-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9b09b9c58228c9028a5ac9d26d834bdc21a5c02201338767af84dc713bc3aa60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076144"
---
# <a name="file_name-structure"></a>FILE \_ NAME-Struktur

\[Diese Struktur ist nur für Version 3 von NTFS-Volumes gültig. Sie kann in zukünftigen Versionen geändert werden.\]

Stellt ein Dateinamenattribut dar. Eine Datei verfügt über ein Dateinamenattribut für jedes Verzeichnis, in das sie eingegeben wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a>Member

<dl> <dt>

**ParentDirectory**
</dt> <dd>

Ein Dateiverweis auf das Verzeichnis, das diesen Namen indiziert. Weitere Informationen finden Sie [**unter \_ MFT-SEGMENTREFERENZ. \_**](mft-segment-reference.md)

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**FileNameLength**
</dt> <dd>

Die Länge des Dateinamens in Unicode-Zeichen.

</dd> <dt>

**Flags**
</dt> <dd>

Die Dateinamenflags.

<dl> <dt>

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**FILE \_ NAME \_ NTFS** (0x01)
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**FILE \_ NAME \_ DOS** (0x02)
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

Das erste Zeichen des Dateinamens.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass für diese Struktur keine Headerdatei zugeordnet ist.

Diese Strukturdefinition ist nur für Hauptversion 3 und Nebenversion 0 oder 1 gültig, wie von [**FSCTL \_ GET \_ NTFS \_ VOLUME \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)gemeldet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Masterdateitabelle](master-file-table.md)
</dt> </dl>

 

 
