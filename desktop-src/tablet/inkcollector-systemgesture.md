---
description: 'InkCollector.SystemGesture-Ereignis: Tritt auf, wenn eine Systemgeste erkannt wird.'
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: InkCollector.SystemGesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f753807d8aaaf03c2de2fd9810ef1e044bcbe05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110050"
---
# <a name="inkcollectorsystemgesture-event"></a>InkCollector.SystemGesture-Ereignis

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

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **SystemGesture-Ereignis** generiert hat.

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

Ein -Wert, der angibt, ob sich das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) im Normalen- oder Radierermodus befindet. 1 gilt für den normalen Modus und 2 für den Radierermodus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Systemgesten sind nützlich, da sie Informationen über das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) liefern, das zum Erstellen der Geste verwendet wird. Sie bieten auch Verknüpfungen zu Kombinationen von Mausereignissen und sind "kostengünstigere" Methoden zum Erkennen von Mausereignissen.

Anstatt beispielsweise nach einem [**MouseDown-Ereignispaar**](inkcollector-mouseup.md)für MouseUp-Ereignisse zu suchen, in dem keine anderen Mausereignisse dazwischen auftreten, können Sie nach den Systemgesten Tap oder  /  [](inkcollector-mousedown.md) **RightTap** suchen. [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)

Ein weiteres Beispiel: Anstatt auf [**MouseDown Event**](inkcollector-mousedown.md)MouseMove Event-Ereignisse zu lauschen und zahlreiche  /  [](inkcollector-mousemove.md) **MouseMove-Ereignismeldungen** zu erhalten, können Sie nach den Drag- oder **RightDrag-Systemgesten** sehen, solange Sie nicht an den Koordinaten (x, y) jeder Position der Maus interessiert sind. [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) Dadurch können Sie anstelle zahlreicher **MouseMove-Ereignismeldungen nur** eine Nachricht empfangen.

Eine Liste mit bestimmten Systemgesten finden Sie unter [**InkSystemGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) Weitere Informationen zu Systemgesten finden Sie unter Verwenden von Gesten und [Befehlseingabe](using-gestures.md) [auf dem Tablet PC.](/previous-versions//dd314533(v=vs.85))

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICESystemGesture definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
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

 

