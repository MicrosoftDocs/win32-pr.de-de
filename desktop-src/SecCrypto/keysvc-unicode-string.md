---
description: Die keysvc \_ \_ -Unicode-Zeichen folgen Struktur definiert eine Unicode-Zeichenfolge und eine maximale Länge für die Zeichenfolge. Diese Struktur wird von der Funktion rkeypfxinstall verwendet.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: KEYSVC_UNICODE_STRING Struktur (rkeysvcc. h)
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
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351583"
---
# <a name="keysvc_unicode_string-structure"></a>Keysvc- \_ Unicode- \_ Zeichen folgen Struktur

Die **keysvc- \_ Unicode- \_ Zeichen** folgen Struktur definiert eine [*Unicode*](../secgloss/u-gly.md) -Zeichenfolge und eine maximale Länge für die Zeichenfolge. Diese Struktur wird von der Funktion [**rkeypfxinstall**](rkeypfxinstall.md) verwendet.

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

Ein **UShort** -Wert, der die Länge in Bytes angibt, die für den **Puffer** verwendet wird.

</dd> <dt>

**MaximumLength**
</dt> <dd>

Ein **UShort** -Wert, der die maximale Länge (in Byte) angibt, die für den **Puffer** zulässig ist.

</dd> <dt>

**Buffer**
</dt> <dd>

Ein Zeiger auf einen **UShort** , der die Unicode-Zeichenfolge darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rkeypfxinstall**](rkeypfxinstall.md)
</dt> <dt>

[**keysvc- \_ BLOB**](keysvc-blob.md)
</dt> </dl>

 

 
