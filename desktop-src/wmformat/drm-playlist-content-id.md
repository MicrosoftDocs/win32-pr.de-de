---
title: DRM_PLAYLIST_CONTENT_ID Struktur (drmexternals. h)
description: Die Struktur der DRM- \_ Wiedergabelisten \_ Inhalts- \_ ID enthält Informationen zu Inhalten, die im Rahmen einer Wiedergabeliste auf CD kopiert werden sollen.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- DRM_PLAYLIST_CONTENT_ID Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341408"
---
# <a name="drm_playlist_content_id-structure"></a>Struktur der DRM- \_ Wiedergabelisten \_ Content \_ ID

Die Struktur der **DRM- \_ Wiedergabelisten Inhalts- \_ \_ ID** enthält Informationen zu Inhalten, die im Rahmen einer Wiedergabeliste auf CD kopiert werden sollen.

## <a name="syntax"></a>Syntax


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**lpcwszV2Header**
</dt> <dd>

DRM-Header. Verwenden Sie dieses Mitglied, wenn der Inhalt durch Windows Media DRM Version 2 oder höher geschützt wird.

</dd> <dt>

**lpcszV1KID**
</dt> <dd>

Schlüssel-ID Verwenden Sie dieses Mitglied, wenn der Inhalt durch Windows Media DRM, Version 1, geschützt ist.

</dd> <dt>

**pbotherdata**
</dt> <dd>

Puffer mit ergänzenden Daten.

</dd> <dt>

**cbotherdata**
</dt> <dd>

Größe des **pbotherdata** -Puffers in Bytes.

</dd> <dt>

**dwuniqueidforsession**
</dt> <dd>

Eindeutiger Bezeichner für den in der aktuellen Sitzung zu verwendenden Inhalt.

</dd> <dt>

**dwvalidfields**
</dt> <dd>

**DWORD** , das die gültigen Felder dieser-Struktur angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                      |
| Version<br/>                  | SDK für Windows Media-Format 11<br/>                                                    |
| Header<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





