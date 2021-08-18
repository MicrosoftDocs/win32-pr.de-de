---
description: Die RANGE-Struktur definiert einen Bereich gültiger Eigenschaftswerte.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: RANGE-Struktur (Netmon.h)
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
ms.openlocfilehash: 0e0135a6210aebbca38bfdede00231315dd2680461f366930b24925eda830604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063720"
---
# <a name="range-structure"></a>RANGE-Struktur

Die **RANGE-Struktur** definiert einen Bereich gültiger Eigenschaftswerte.

## <a name="syntax"></a>Syntax


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>Member

<dl> <dt>

**Minvalue**
</dt> <dd>

Niedrigster möglicher Wert in einem Bereich.

</dd> <dt>

**Maxvalue**
</dt> <dd>

Der höchste mögliche Wert in einem Bereich.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **RANGE-Struktur** wird verwendet, um einen gültigen Zahlenbereich für eine Protokolleigenschaft anzugeben. Wenn der **DataQualifier-Member** der **PROPERTYINFO-Struktur** auf **PROP \_ QUAL \_ RANGE** festgelegt ist, muss der **lpRange-Member** der [PROPERTYINFO-Struktur](propertyinfo.md) einen Zeiger auf eine **RANGE-Struktur** bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Propertyinfo](propertyinfo.md)
</dt> </dl>

 

 




