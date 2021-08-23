---
description: Die KEYSVC \_ UNICODE \_ STRING-Struktur definiert eine Unicode-Zeichenfolge und eine maximale Länge für die Zeichenfolge. Diese Struktur wird von der RKeyPFXInstall-Funktion verwendet.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: KEYSVC_UNICODE_STRING-Struktur (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ac1e82ab481b9844e8a21940112c6014a19f111cab53db2974c488dff0982027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622330"
---
# <a name="keysvc_unicode_string-structure"></a>KEYSVC \_ UNICODE \_ STRING-Struktur

Die **KEYSVC \_ UNICODE \_ STRING-Struktur** definiert eine [*Unicode-Zeichenfolge*](../secgloss/u-gly.md) und eine maximale Länge für die Zeichenfolge. Diese Struktur wird von der [**RKeyPFXInstall-Funktion**](rkeypfxinstall.md) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a>Member

<dl> <dt>

**Länge**
</dt> <dd>

Ein **USHORT-Wert,** der die Länge in Bytes angibt, die für **Buffer** verwendet wird.

</dd> <dt>

**MaximumLength**
</dt> <dd>

Ein **USHORT-Wert,** der die maximale Länge in Bytes angibt, die für **Buffer** zulässig ist.

</dd> <dt>

**Buffer**
</dt> <dd>

Ein Zeiger auf einen **USHORT,** der die Unicode-Zeichenfolge darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**\_KEYSVC-BLOB**](keysvc-blob.md)
</dt> </dl>

 

 
