---
description: Die ADDRESSTABLE-Struktur enthält eine Tabelle mit Adresspaaren.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: ADDRESSTABLE-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c1c766e29033136954abab69755e1231e610983314cdaa01da3957889af5eb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064280"
---
# <a name="addresstable-structure"></a>ADDRESSTABLE-Struktur

Die **ADDRESSTABLE-Struktur** enthält eine Tabelle mit Adresspaaren.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**nAddressPairs**
</dt> <dd>

Anzahl von Adresspaaren im **AddressPair-Array.**

</dd> <dt>

**nNonMacAddressPairs**
</dt> <dd>

Anzahl von Nicht-MAC-Adresspaaren.

</dd> <dt>

**AddressPair**
</dt> <dd>

Array von Adresspaaren. Beachten Sie, dass Sie pro ADDRESSTABLE-Struktur nur bis zu acht Adresspaare speichern können.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Struktur als Teil des Erfassungsfilter-Konstruktionsprozesses. Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungsfilter](capture-filters.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




