---
description: Die bezeichnete \_ bitstruktur definiert ein Bezeichnungs bitpaar.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: LABELED_BIT Struktur (Netmon. h)
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
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354529"
---
# <a name="labeled_bit-structure"></a>Bezeichnete \_ bitstruktur

Die **bezeichnete \_ bitstruktur** definiert ein Bezeichnungs bitpaar.

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

**Bitzahl**
</dt> <dd>

Bitnummer des Bezeichnungs bitpaars. Die Werte reichen von 0 bis 255. Legen Sie den **bitnumber** -Member auf das Bit fest, das beim Vergleich des Eigenschafts Werts verwendet wird.

</dd> <dt>

**Labeloff**
</dt> <dd>

Eine Zeichenfolge oder Bezeichnung, die angezeigt wird, wenn das in **bitnumber** angegebene Bit 0 (null) ist. Eine mögliche Bezeichnung ist beispielsweise "Bit Off".

</dd> <dt>

**Labelon**
</dt> <dd>

Eine Zeichenfolge oder Bezeichnung, die angezeigt wird, wenn das in **bitnumber** angegebene Bit 1 entspricht. Eine mögliche Bezeichnung ist beispielsweise "Bit ein".

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Array mit **beschrifteten \_ bitstrukturen** wird verwendet, um einen Satz von Bezeichnungs Bit Paaren zu definieren. Ein Zeiger auf das Array wird im **lplabeledbit** -Member der [set](set.md) -Struktur angegeben. Die Paare werden verwendet, wenn Sie eine Bezeichnung auf der Grundlage der Einstellung der einzelnen Bits anzeigen möchten. In der Regel wird dieser Typ von Set verwendet, um den ein-oder ausschalten-Wert von Bits anzugeben.

Wenn ein Bit festgelegt wird, zeigt Netzwerkmonitor nur die Bits an, die im Array der **Mengen Strukturen enthalten** sind. Bits, die sich nicht in der **Set** -Struktur befinden, werden nicht angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




