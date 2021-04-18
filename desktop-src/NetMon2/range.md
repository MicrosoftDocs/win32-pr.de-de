---
description: Die Bereichs Struktur definiert einen Bereich gültiger Eigenschaftswerte.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Bereichs Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347118"
---
# <a name="range-structure"></a>Bereichs Struktur

Die **Bereichs** Struktur definiert einen Bereich gültiger Eigenschaftswerte.

## <a name="syntax"></a>Syntax


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>Member

<dl> <dt>

**MinValue**
</dt> <dd>

Der niedrigste mögliche Wert in einem Bereich.

</dd> <dt>

**MaxValue**
</dt> <dd>

Höchstmöglicher Wert in einem Bereich.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Bereichs** Struktur wird verwendet, um einen gültigen Bereich von Zahlen für eine Protokoll Eigenschaft anzugeben. Wenn das **dataqualifier** -Element der **PropertyInfo** -Struktur auf den **Prop-Wert \_ \_ Bereich** festgelegt ist, muss der **lprange** -Member der [PropertyInfo](propertyinfo.md) -Struktur einen Zeiger auf eine **Bereichs** Struktur bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




