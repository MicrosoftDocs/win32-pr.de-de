---
description: Die \_ KEYSVC-BLOB-Struktur definiert ein Schlüsseldienst-BLOB. Diese Struktur wird von der RKeyPFXInstall-Funktion verwendet.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: KEYSVC_BLOB -Struktur (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 7e71a090558b31444c550146a2cb99f062080db9b80e7d69561ff891b93262b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992970"
---
# <a name="keysvc_blob-structure"></a>\_KEYSVC-BLOB-Struktur

Die **\_ KEYSVC-BLOB-Struktur** definiert ein Schlüsseldienst-BLOB. Diese Struktur wird von der [**RKeyPFXInstall-Funktion**](rkeypfxinstall.md) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a>Member

<dl> <dt>

**Cb**
</dt> <dd>

Ein **ULONG-Wert,** der die Größe von pb in Bytes **angibt.**

</dd> <dt>

**pb**
</dt> <dd>

Ein Zeiger auf ein **BYTE,** das das BLOB enthält, im [*PKCS \# 12-Format.*](../secgloss/p-gly.md)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**\_KEYSVC-UNICODE-ZEICHENFOLGE \_**](keysvc-unicode-string.md)
</dt> </dl>

 

 
