---
description: Die PROPERTYINSTEX-Struktur definiert eine Freiforminstanz für erweiterte Eigenschaften.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: PROPERTYINSTEX-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 533169a98d17c56a32df56f77c30d403d0dbb28c6a51159debc9692a505da52b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036970"
---
# <a name="propertyinstex-structure"></a>PROPERTYINSTEX-Struktur

Die **PROPERTYINSTEX-Struktur** definiert eine Freiforminstanz für erweiterte Eigenschaften.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a>Member

<dl> <dt>

**Länge**
</dt> <dd>

Länge der Daten in Bytes.

</dd> <dt>

**LengthEx**
</dt> <dd>

Länge der erweiterten Daten.

</dd> <dt>

**lpData**
</dt> <dd>

Zeiger auf die erweiterten Daten.

</dd> <dt>

**Byte**
</dt> <dd>

Zeiger auf die **BYTE-Daten.**

</dd> <dt>

**Word**
</dt> <dd>

Zeiger auf die **WORD-Daten.**

</dd> <dt>

**Dword**
</dt> <dd>

Zeiger auf die **DWORD-Daten.**

</dd> <dt>

**LargeInt**
</dt> <dd>

Zeiger auf die **LARGEINT-Daten.**

</dd> <dt>

**Systime**
</dt> <dd>

Zeiger auf die **SYSTEMTIME-Daten.**

</dd> <dt>

**TypedString**
</dt> <dd>

Eine typisierte Zeichenfolge, die möglicherweise erweiterte Daten enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




