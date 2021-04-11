---
title: WMDRM_IMPORT_SESSION_KEY Struktur (drmexternals. h)
description: Die Schlüsselstruktur der WMDRM- \_ Import \_ Sitzung \_ enthält den Sitzungsschlüssel zum Importieren geschützter Inhalte.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- WMDRM_IMPORT_SESSION_KEY Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105303"
---
# <a name="wmdrm_import_session_key-structure"></a>WMDRM- \_ Struktur zum Importieren von \_ Sitzungs \_ Schlüsseln

Die **Schlüsselstruktur der WMDRM- \_ Import \_ Sitzung \_** enthält den Sitzungsschlüssel zum Importieren geschützter Inhalte.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**dwkeytype**
</dt> <dd>

Der Sitzungs Schlüsseltyp. Legen Sie auf WMDRM \_ KeyType \_ RC4 fest.

</dd> <dt>

**cbKey**
</dt> <dd>

Größe des Sitzungsschlüssels in Bytes. Dieser Wert kann so groß sein, wie Sie benötigen, wenn die Grenzen eines einzelnen RSA-OAEP-Vorgangs über die gesamte Nachricht (diese Struktur und den Sitzungsschlüssel) liegen.

</dd> <dt>

**rgbKey**
</dt> <dd>

Adresse eines Puffers, der den Sitzungsschlüssel enthält. Die Puffergröße muss mit dem Wert von **cbkey** identisch sein. Die Daten im Puffer sind ein zufällig generierter Schlüsselwert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur, einschließlich des Puffers, der den Sitzungsschlüssel enthält, muss mit dem öffentlichen Schlüssel des Windows Media DRM-Computers verschlüsselt und im Member **pbencryptedsessionkeymess** der [**WMDRM-Struktur \_ Import \_ Init \_ struct**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) enthalten sein.

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

 

 





