---
description: Die "adresssstable"-Struktur enthält eine Tabelle mit Adress Paaren.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Adresssstable-Struktur (Netmon. h)
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
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485403"
---
# <a name="addresstable-structure"></a>Adresssstable-Struktur

Die " **adresssstable** "-Struktur enthält eine Tabelle mit Adress Paaren.

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

**nadresssspairs**
</dt> <dd>

Anzahl der Adress Paare im **adresssspair** -Array.

</dd> <dt>

**nnonmacadresssspairs**
</dt> <dd>

Anzahl der nicht-Mac-Adress Paare.

</dd> <dt>

**Adresssspair**
</dt> <dd>

Array von Adress Paaren. Beachten Sie, dass Sie nur bis zu acht Adress Paare pro adresstabiler Struktur speichern können.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Struktur als Teil des Erfassungs Filter Erstellungs Prozesses. Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungs Filter](capture-filters.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Adresssspair](addresspair.md)
</dt> <dt>

[Capturefilter](capturefilter.md)
</dt> </dl>

 

 




