---
description: Veraltet. Das PenInputPanel wurde durch den Texteingabebereich (TIP) ersetzt. Tritt ein, wenn das PenInputPanel-Objekt sich selbst angezeigt oder ausgeblendet hat.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: PenInputPanel.VisibleChanged-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc917f34c09ef0d4f079fd55e476bbbc4cea266e1b1c436a62b20d6c08ed1b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596609"
---
# <a name="peninputpanelvisiblechanged-event"></a>PenInputPanel.VisibleChanged-Ereignis

Veraltet. Das [**PenInputPanel**](peninputpanel-class.md) wurde durch den [Texteingabebereich (TIP) ersetzt.](text-input-panel-reference.md)

Tritt ein, wenn [**das PenInputPanel-Objekt**](peninputpanel-class.md) sich selbst angezeigt oder ausgeblendet hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVisibility* \[ In\]
</dt> <dd>

**VARIANT \_ TRUE,** damit das [**PenInputPanel-Objekt**](peninputpanel-class.md) sichtbar wird; andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Das **VisibleChanged-Ereignis** gilt für das Tablet PC Input Panel Hover-Ziel. Sie wird jedoch nicht ausgelöst, wenn das Hoverziel erweitert wird, um den vollständigen Tablet PC-Eingabebereich zu zeigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Peninputpanel**](peninputpanel-class.md)
</dt> </dl>

 

 




