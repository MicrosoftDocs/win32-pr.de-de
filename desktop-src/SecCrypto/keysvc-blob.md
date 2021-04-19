---
description: Die keysvc- \_ BLOB-Struktur definiert ein Schlüsseldienst-BLOB. Diese Struktur wird von der Funktion rkeypfxinstall verwendet.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: KEYSVC_BLOB Struktur (rkeysvcc. h)
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
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357093"
---
# <a name="keysvc_blob-structure"></a>Keysvc- \_ BLOB-Struktur

Die **keysvc- \_ BLOB** -Struktur definiert ein Schlüsseldienst-BLOB. Diese Struktur wird von der Funktion [**rkeypfxinstall**](rkeypfxinstall.md) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a>Member

<dl> <dt>

**betrieben**
</dt> <dd>

Ein **ulong** -Wert, der die Größe von **PB** in Byte angibt.

</dd> <dt>

**PB**
</dt> <dd>

Ein Zeiger auf ein **Byte** , das das BLOB enthält, im [*PKCS \# 12*](../secgloss/p-gly.md) -Format.

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

[**keysvc- \_ Unicode- \_ Zeichenfolge**](keysvc-unicode-string.md)
</dt> </dl>

 

 
