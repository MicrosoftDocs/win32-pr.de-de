---
description: 'InkPicture.SystemGesture-Ereignis: Tritt auf, wenn eine Systemgeste erkannt wird.'
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.SystemGesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11567b94360c8fa2bf736d295bf828ebc636bb0bee7a21acb4cc063c22780352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966949"
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

## <a name="remarks"></a>Hinweise

Systemgesten enthalten Informationen zum [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das zum Erstellen der Geste verwendet wird. Sie bieten auch Verknüpfungen zu Kombinationen von Mausereignissen und sind Möglichkeiten, Mausereignisse mit geringeren Auswirkungen auf die Leistung zu erkennen.

Anstatt beispielsweise nach einem [**\[ MouseUp-Ereignis-InkPicture Control \]**](inkpicture-mouseup.md)MouseDown Event / [**\[ \] InkPicture Control-Ereignispaar**](inkpicture-mousedown.md) zu suchen, in dem keine anderen Mausereignisse dazwischen auftreten, können Sie nach den Systemgesten Tap oder RightTap suchen.

Ein weiteres Beispiel: Anstatt auf MouseDown Event [**\[ InkPicture Control \]**](inkpicture-mousedown.md)MouseMove Event InkPicture Control-Ereignisse / [**\[ \]**](inkpicture-mousemove.md) zu lauschen und zahlreiche **MouseMove Event \[ InkPicture \] Control-Meldungen** zu erhalten, können Sie auf die Drag- oder RightDrag-Systemgesten achten, solange Sie nicht an den Koordinaten (x, y) jeder Position der Maus interessiert sind. Dadurch können Sie anstelle zahlreicher **MouseMove-EreignisinkPicture \[ \]** Control-Meldungen nur eine Nachricht empfangen.

Eine Liste mit bestimmten Systemgesten finden Sie unter [**InkSystemGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) Weitere Informationen zu Systemgesten finden Sie unter Verwenden von Gesten und [Befehlseingabe](using-gestures.md) [auf dem Tablet PC.](/previous-versions//dd314533(v=vs.85))

Diese Ereignismethode wird in den Dispatch-Schnittstellen **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICESystemGesture definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**InkSystemGesture-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> </dl>

 

