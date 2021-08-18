---
title: WMDRM_IMPORT_SESSION_KEY -Struktur (Drmexternals.h)
description: Die WMDRM \_ IMPORT \_ SESSION \_ KEY-Struktur enthält den Sitzungsschlüssel zum Importieren geschützter Inhalte.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- WMDRM_IMPORT_SESSION_KEY struktur windows media format
- Strukturfenster Medienformat
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
ms.openlocfilehash: d34cdff6d17ad6ce60dd40478b56c9718be0863295422d2e5c60fee2c437dc6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844059"
---
# <a name="wmdrm_import_session_key-structure"></a>WMDRM \_ IMPORT \_ SESSION \_ KEY-Struktur

Die **WMDRM \_ IMPORT SESSION \_ \_ KEY-Struktur** enthält den Sitzungsschlüssel zum Importieren geschützter Inhalte.

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

**dwKeyType**
</dt> <dd>

Sitzungsschlüsseltyp. Legen Sie auf WMDRM \_ KEYTYPE \_ RC4 fest.

</dd> <dt>

**cbKey**
</dt> <dd>

Größe des Sitzungsschlüssels in Bytes. Dieser Wert kann bei den Grenzwerten eines einzelnen RSA-OAEP-Vorgangs für die gesamte Nachricht (diese Struktur plus Sitzungsschlüssel) so groß sein, wie Sie benötigen.

</dd> <dt>

**Rgbkey**
</dt> <dd>

Adresse eines Puffers, der den Sitzungsschlüssel enthält. Die Puffergröße muss mit dem Wert von **cbKey übereinstimmen.** Die Daten im Puffer sind zufällig generierte Schlüsselwerte.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur, einschließlich des Puffers, der den Sitzungsschlüssel enthält, muss mit dem öffentlichen Schlüssel des Windows Media DRM-Computers verschlüsselt und im **pbEncryptedSessionKeyMessage-Member** der [**WMDRM \_ IMPORT \_ INIT \_ STRUCT-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) enthalten sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                      |
| Version<br/>                  | Windows Medienformat 11 SDK<br/>                                                    |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





