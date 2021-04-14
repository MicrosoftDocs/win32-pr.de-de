---
title: WMDRM_IMPORT_CONTENT_KEY Struktur (drmexternals. h)
description: Die WMDRM \_ - \_ Schlüsselstruktur zum Importieren von Inhalten \_ speichert den Inhalts Schlüssel, der beim Importieren geschützter Inhalte verwendet wird.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- WMDRM_IMPORT_CONTENT_KEY Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391578"
---
# <a name="wmdrm_import_content_key-structure"></a>WMDRM \_ - \_ Schlüsselstruktur zum Importieren von Inhalten \_

Die **WMDRM \_ - \_ \_ Schlüssel** Struktur zum Importieren von Inhalten speichert den Inhalts Schlüssel, der beim Importieren geschützter Inhalte verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Version.

</dd> <dt>

**cbstructsize**
</dt> <dd>

Größe der Struktur in Bytes.

</dd> <dt>

**dwivkeytype**
</dt> <dd>

Der Initialisierungs Schlüsseltyp. Legen Sie auf WMDRM \_ KeyType \_ RC4 fest.

</dd> <dt>

**cbivkey**
</dt> <dd>

Größe des Initialisierungs Vektor Schlüssels in Bytes.

</dd> <dt>

**dwcontentkeytype**
</dt> <dd>

Der Inhalts Schlüsseltyp. Legen Sie auf WMDRM \_ KeyType \_ Cocktail fest.

</dd> <dt>

**cbcontentkey**
</dt> <dd>

Größe des Inhalts Schlüssels in Bytes.

</dd> <dt>

**rgbkeydata**
</dt> <dd>

Adresse eines Puffers, der den Inhalts Schlüssel enthält. Die Puffergröße muss mit dem Wert von **cbcontentkey** identisch sein. Dieser Schlüssel sollte dem Schlüssel entsprechen, der aus der XMR-Lizenz Meldung importiert wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur, einschließlich des Puffers, der den Sitzungsschlüssel enthält, muss mit dem Sitzungsschlüssel verschlüsselt und in das **pbencryptedkeymess** -Member der [**WMDRM- \_ Import \_ Init \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) -Struktur-Struktur eingeschlossen werden.

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

 

 





