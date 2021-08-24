---
description: Veraltet. PenInputPanel wurde durch den Texteingabebereich (TIP) ersetzt. Tritt ein, wenn das PenInputPanel-Objekt verschoben wird.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: PenInputPanel.PanelMoving-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4a152afdef9fcd10fb92fdec55d9a460faf58ca91536e96c9876203fbad44c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596599"
---
# <a name="peninputpanelpanelmoving-event"></a>PenInputPanel.PanelMoving-Ereignis

Veraltet. Das [**PenInputPanel**](peninputpanel-class.md) wurde durch den [Texteingabebereich (TIP)](text-input-panel-reference.md)ersetzt.

Tritt ein, wenn das [**PenInputPanel-Objekt**](peninputpanel-class.md) verschoben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Links* \[ in, out\]
</dt> <dd>

Die neue horizontale Position (x-Achse) des linken Rands des [**PenInputPanel-Objekts**](peninputpanel-class.md) in Bildschirmkoordinaten.

</dd> <dt>

*Top* \[ in, out\]
</dt> <dd>

Die neue vertikale Position (y-Achse) des linken Rands des [**PenInputPanel-Objekts**](peninputpanel-class.md) in Bildschirmkoordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Das **PanelMoving-Ereignis** wurde entwickelt, um die Position des Stifteingabebereichs durch Ändern der Parameter *Left* und *Top* zu ändern.

Die [**Methoden MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) und [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) bewirken, dass das [**PenInputPanel-Objekt**](peninputpanel-class.md) seinen Automatischpositionierungscode aufruft, der ein **PanelMoving-Ereignis** auslöst. Folglich kann das Aufrufen dieser Methoden innerhalb eines **PanelMoving-Handlers** zu einer rekursiven Endlosschleife führen.

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

 

 




