---
description: 'InkPicture.SystemGesture-Ereignis: Tritt auf, wenn eine Systemgeste erkannt wird.'
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.SystemGesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cde11b73b6b0d3861a79538a7f9ee19487b6384
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113688"
---
# <a name="inkpicturesystemgesture-event"></a>InkPicture.SystemGesture-Ereignis

Tritt ein, wenn eine Systemgeste erkannt wird.

## <a name="syntax"></a>Syntax


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **SystemGesture-Ereignis generiert** hat.

</dd> <dt>

*ID* \[ in\]
</dt> <dd>

Der Wert der Systemgeste.

</dd> <dt>

*X* \[ in\]
</dt> <dd>

Die x-Koordinate der Position der Geste.

</dd> <dt>

*Y* \[ in\]
</dt> <dd>

Die y-Koordinate der Position der Geste.

</dd> <dt>

*Modifizierer* \[ In\]
</dt> <dd>

Reserviert.

</dd> <dt>

*Zeichen* \[ In\]
</dt> <dd>

Reserviert.

</dd> <dt>

*CursorMode* \[ In\]
</dt> <dd>

Ein -Wert, der angibt, ob sich [**das IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) im normalen Modus oder Radierermodus befindet. 1 ist für den normalen Modus und 2 für radierermodus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Systemgesten enthalten Informationen zum [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das zum Erstellen der Geste verwendet wird. Sie bieten auch Verknüpfungen zu Kombinationen von Mausereignissen und sind Möglichkeiten, Mausereignisse mit geringeren Auswirkungen auf die Leistung zu erkennen.

Anstatt beispielsweise nach einem [**MouseUp Event \[ InkPicture Control \]**](inkpicture-mouseup.md) / [**MouseDown Event \[ InkPicture Control-Paar \]**](inkpicture-mousedown.md) von Ereignissen zu suchen, bei dem keine anderen Mausereignisse dazwischen auftreten, können Sie nach den Systemgesten Tap oder RightTap suchen.

Ein weiteres Beispiel: Anstatt auf [**MouseDown Event \[ InkPicture Control \]**](inkpicture-mousedown.md) / [**MouseMove Event \[ InkPicture \] Control-Ereignisse**](inkpicture-mousemove.md) zu lauschen und zahlreiche **MouseMove Event \[ InkPicture Control-Meldungen \]** zu erhalten, können Sie auf die Drag- oder RightDrag-Systemgesten achten, solange Sie nicht an den (x, y) Koordinaten jeder Position der Maus interessiert sind. Dadurch können Sie anstelle zahlreicher **MouseMove Event \[ InkPicture \] Control-Meldungen** nur eine Nachricht empfangen.

Eine Liste der spezifischen Systemgesten finden Sie unter [**InkSystemGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) Weitere Informationen zu Systemgesten finden Sie unter Verwenden von Gesten und [Befehlseingaben auf dem Tablet PC.](/previous-versions//dd314533(v=vs.85)) [](using-gestures.md)

Diese Ereignismethode wird in den Dispatch-Only-Schnittstellen **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICESystemGesture definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**InkSystemGesture-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> </dl>

 

