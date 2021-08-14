---
description: Die LABELED \_ BIT-Struktur definiert ein BIT-Bezeichnungspaar.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: LABELED_BIT-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fe08288929a5f14c4a920c52121c2ccfbdb35888f2ed220291e30e53a3ef0c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364835"
---
# <a name="labeled_bit-structure"></a>BEZEICHNETE \_ BIT-Struktur

Die **LABELED \_ BIT-Struktur** definiert ein BIT-Bezeichnungspaar.

## <a name="syntax"></a>Syntax


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a>Member

<dl> <dt>

**BitNumber**
</dt> <dd>

BIT-Nummer des BIT-Bezeichnungspaars. Die Werte liegen zwischen 0 und 255. Legen Sie den **Bitnumber-Member** auf das BIT fest, das beim Vergleich des Eigenschaftswerts verwendet wird.

</dd> <dt>

**LabelOff**
</dt> <dd>

Zeichenfolge oder Bezeichnung, die angezeigt wird, wenn der in **BitNumber** angegebene BIT gleich 0 (null) ist. Eine mögliche Bezeichnung ist beispielsweise "Bit OFF".

</dd> <dt>

**LabelOn**
</dt> <dd>

Zeichenfolge oder Bezeichnung, die angezeigt wird, wenn das in **BitNumber** angegebene BIT gleich 1 ist. Eine mögliche Bezeichnung ist beispielsweise "Bit ON".

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Array von **LABELED \_ BIT-Strukturen** wird verwendet, um einen Satz von Bezeichnungs-BIT-Paaren zu definieren. Ein Zeiger auf das Array wird im **lpLabeledBit-Member** der [SET-Struktur](set.md) angegeben. Die Paare werden verwendet, wenn Sie eine Bezeichnung basierend auf der Einstellung der einzelnen BIT-Bits anzeigen möchten. In der Regel wird dieser Satztyp verwendet, um den ON- oder OFF-Wert von BITs anzugeben.

Wenn ein BIT-Satz angegeben wird, zeigt Netzwerkmonitor nur die BITs an, die im Array von **SET-Strukturen** enthalten sind. BITs, die sich nicht in der **SET-Struktur** befinden, werden nicht angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




