---
description: Die LABELED \_ BYTE-Struktur definiert ein bezeichnetes BIT-Paar. Die Bezeichnung des bezeichneten BIT-Paars wird angezeigt, wenn ein bestimmter Byteeigenschaftswert erkannt wird.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: LABELED_BYTE -Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 05aa29942768c0c40816eafce112f12a95cd0a713bebe612d2e5ad32776a33a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494980"
---
# <a name="labeled_byte-structure"></a>LABELED \_ BYTE-Struktur

Die **LABELED \_ BYTE-Struktur** definiert ein bezeichnetes BIT-Paar. Die **Bezeichnung** des bezeichneten BIT-Paars wird angezeigt, wenn ein bestimmter Byteeigenschaftswert erkannt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a>Member

<dl> <dt>

**Wert**
</dt> <dd>

BYTE-Wert der Eigenschaft, die Sie erkennen möchten.

</dd> <dt>

**Label**
</dt> <dd>

Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Value-Member** angegebene Wert erkannt wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der **lpLabeledByteTable-Member** der [SET-Struktur](set.md) zeigt auf ein Array von **SET-Strukturen,** die einen oder mehrere **Label-Member** der BYTE-Wertpaare definieren. Diese Paare werden verwendet, wenn Sie eine Bezeichnung statt eines bestimmten BYTE-Werts anzeigen möchten, der im Protokollpaket gefunden wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




