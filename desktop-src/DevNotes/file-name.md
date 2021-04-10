---
description: Stellt ein Dateiname-Attribut dar. Eine Datei verfügt über ein Dateiname-Attribut für jedes Verzeichnis, in das Sie eingegeben wird.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: File_name Struktur
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
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041329"
---
# <a name="file_name-structure"></a>Datei \_ Namen Struktur

\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]

Stellt ein Dateiname-Attribut dar. Eine Datei verfügt über ein Dateiname-Attribut für jedes Verzeichnis, in das Sie eingegeben wird.

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

**"Element Verzeichnis"**
</dt> <dd>

Ein Datei Verweis auf das Verzeichnis, das diesen Namen indiziert. Siehe [**\_ \_ Referenz zu MFT-Segmenten**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**Datamelength**
</dt> <dd>

Die Länge des Datei namens in Unicode-Zeichen.

</dd> <dt>

**Flags**
</dt> <dd>

Die Dateiname-Flags.

<dl> <dt>

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**Datei \_ Name \_ NTFS** (0x01)
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**Datei \_ Name \_ DOS** (0x02)
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

Das erste Zeichen des Datei namens.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.

Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Master Dateitabelle](master-file-table.md)
</dt> </dl>

 

 
