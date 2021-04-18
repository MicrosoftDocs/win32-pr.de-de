---
description: Die propertyinstex-Struktur definiert eine frei Form erweiterte Eigenschafts Instanz.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Propertyinstex-Struktur (Netmon. h)
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
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345040"
---
# <a name="propertyinstex-structure"></a>Propertyinstex-Struktur

Die **propertyinstex** -Struktur definiert eine frei Form erweiterte Eigenschafts Instanz.

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

**Verlängert**
</dt> <dd>

Länge der erweiterten Daten.

</dd> <dt>

**lpdata**
</dt> <dd>

Zeiger auf die erweiterten Daten.

</dd> <dt>

**Byte**
</dt> <dd>

Zeiger auf die **Bytedaten** .

</dd> <dt>

**Word**
</dt> <dd>

Zeiger auf das **Word** -Daten.

</dd> <dt>

**DWORD**
</dt> <dd>

Zeiger auf die **DWORD** -Daten.

</dd> <dt>

**' Largeint**
</dt> <dd>

Zeiger auf die **largeint** -Daten.

</dd> <dt>

**SysTime**
</dt> <dd>

Zeiger auf die **SYSTEMTIME** -Daten.

</dd> <dt>

**Typedstring**
</dt> <dd>

Eine typisierte Zeichenfolge, die möglicherweise über erweiterte Daten verfügt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




