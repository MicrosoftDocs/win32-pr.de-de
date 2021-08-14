---
description: 'InkOverlay.SystemGesture-Ereignis: Tritt auf, wenn eine Systemgeste erkannt wird.'
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: InkOverlay.SystemGesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e1e55048a60edef4344ec3b566b08de29d9f3d0a16ccccc1f3094949c2aec86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218763"
---
# <a name="inkoverlaysystemgesture-event"></a>InkOverlay.SystemGesture-Ereignis

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

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**SystemGesture-Ereignis generiert**](inkcollector-systemgesture.md) hat.

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

Systemgesten sind nützlich, da sie Informationen über das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) geben, das zum Erstellen der Geste verwendet wird. Sie bieten auch Verknüpfungen zu Kombinationen von Mausereignissen und sind "kostengünstigere" Möglichkeiten, Mausereignisse zu erkennen.

Anstatt beispielsweise nach einem [**MouseDown-Ereignispaar**](inkcollector-mouseup.md)für MouseUp-Ereignisse zu suchen, in dem keine anderen Mausereignisse dazwischen auftreten, können Sie nach den Systemgesten Tap oder  /  [](inkcollector-mousedown.md) **RightTap** suchen. [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)

Ein weiteres Beispiel: Anstatt auf [**MouseDown**](inkcollector-mousedown.md)Event MouseMove Event-Ereignisse zu lauschen und zahlreiche MouseMove-Ereignismeldungen zu erhalten, können Sie auf die Drag- oder RightDrag-Systemgesten achten, solange Sie nicht an den  /  [](inkcollector-mousemove.md) (x, y)-Koordinaten  [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) jeder Position der Maus interessiert sind.  Dadurch können Sie anstelle zahlreicher **MouseMove-Ereignismeldungen nur** eine Nachricht empfangen.

Eine Liste mit bestimmten Systemgesten finden Sie unter [**InkSystemGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) Weitere Informationen zu Systemgesten finden Sie unter Verwenden von Gesten und [Befehlseingabe](using-gestures.md) [auf dem Tablet PC.](/previous-versions//dd314533(v=vs.85))

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICESystemGesture definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**InkSystemGesture-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> <dt>

[Stifteingabe, Ink und Erkennung](pen-input--ink--and-recognition.md)
</dt> <dt>

[Befehlseingabe auf dem Tablet-PC](/previous-versions//dd314533(v=vs.85))
</dt> </dl>

 

