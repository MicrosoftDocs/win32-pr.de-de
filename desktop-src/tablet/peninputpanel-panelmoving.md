---
description: Veraltet. Der "tzinputpanel" wurde durch den Text Eingabe Panel (Tip) ersetzt. Tritt auf, wenn das Objekt "pinputpanel" verschoben wird.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: "\"Pinputpanel. PanelMoving\"-Ereignis (\"msink AUT. h\")"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352372"
---
# <a name="peninputpanelpanelmoving-event"></a>"Pinputpanel. PanelMoving"-Ereignis

Veraltet. Der " [**tzinputpanel**](peninputpanel-class.md) " wurde durch den [Text Eingabe Panel (Tip)](text-input-panel-reference.md)ersetzt.

Tritt auf, wenn das Objekt " [**pinputpanel**](peninputpanel-class.md) " verschoben wird.

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

Die neue horizontale bzw. x-Achse, Position des linken Rands des " [**tabinputpanel**](peninputpanel-class.md) "-Objekts in Bildschirm Koordinaten.

</dd> <dt>

Nach *oben* \[ in, out\]
</dt> <dd>

Die neue vertikale Achse bzw. y-Achse, Position des linken Randes des ""- [**raninputpanel**](peninputpanel-class.md) -Objekts in Bildschirm Koordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das **PanelMoving** -Ereignis ist so konzipiert, dass es verwendet wird, um die Position des Stift Eingabe Panels durch Ändern des *linken* und des *oberen* Parameters zu ändern.

Die Methoden " [**pveto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) " und " [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) " bewirken, dass das Objekt " [**pinputpanel**](peninputpanel-class.md) " seinen automatischen Positions Code aufruft, der ein **PanelMoving** -Ereignis auslöst. Folglich kann das Aufrufen dieser Methoden in einem **PanelMoving** -Handler zu einer rekursiven Endlosschleife führen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Pendel Panel"**](peninputpanel-class.md)
</dt> </dl>

 

 




