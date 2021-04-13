---
description: Tritt auf, wenn eine System Bewegung erkannt wird.
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: InkCollector.Systemgesten-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282f28e5ef1bc3a86f51b6d345be6e00d78c8213
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525946"
---
# <a name="inkcollectorsystemgesture-event"></a>InkCollector.Systemgesten-Ereignis

Tritt auf, wenn eine System Bewegung erkannt wird.

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

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das **systemgesten** -Ereignis generiert hat.

</dd> <dt>

*ID* \[ in\]
</dt> <dd>

Der Wert der System Geste.

</dd> <dt>

*X* \[ in\]
</dt> <dd>

Die x-Koordinate der Position der Bewegung.

</dd> <dt>

*J* \[ in\]
</dt> <dd>

Die y-Koordinate der Position der Bewegung.

</dd> <dt>

*Modifizierer* \[ in\]
</dt> <dd>

Reserviert.

</dd> <dt>

*Zeichen* \[ in\]
</dt> <dd>

Reserviert.

</dd> <dt>

*Cursor Mode* \[ in\]
</dt> <dd>

Ein Wert, der angibt, ob sich das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt im normalen Modus oder im Radierermodus befindet. 1 ist für den normalen Modus und 2 für den Radierermodus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

System Gesten sind nützlich, da Sie Informationen über das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt enthalten, das zum Erstellen der Geste verwendet wird. Außerdem stellen Sie Verknüpfungen zu Kombinationen von Mausereignissen bereit und sind "kostengünstiger" Möglichkeiten zum Erkennen von Mausereignissen.

Anstatt z. b. nach einem [**MouseUp Event**](inkcollector-mouseup.md)  /  [**MouseDown-Ereignis**](inkcollector-mousedown.md) paar von Ereignissen zu suchen, bei denen keine anderen Mausereignisse zwischen auftreten, können Sie nach der [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) -oder **RightTap** -System Gesten suchen.

Ein weiteres Beispiel: statt auf [**MouseDown**](inkcollector-mousedown.md)  /  -Ereignis [**MouseMove**](inkcollector-mousemove.md) -Ereignis Ereignisse zu lauschen und zahlreiche **MouseMove-Ereignis** Meldungen zu erhalten, können Sie die Bewegungen des [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) -oder **RightDrag** -Systems überwachen, solange Sie nicht an den (x, y)-Koordinaten jeder Position der Maus interessiert sind. Dies ermöglicht es Ihnen, anstelle von zahlreichen **mougmove-Ereignis** Nachrichten nur eine Nachricht zu empfangen.

Eine Liste der spezifischen System Gesten finden Sie unter der [**inksystemgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) -Enumerationstyp. Weitere Informationen zu System Gesten finden Sie unter [Verwenden von Gesten](using-gestures.md) und [Befehlseingaben auf dem Tablet PC](/previous-versions//dd314533(v=vs.85)).

Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icesystemgesten definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**Inksystemgesten-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> <dt>

[Stift Eingabe, frei Hand Eingabe und-Erkennung](pen-input--ink--and-recognition.md)
</dt> <dt>

[Befehls Eingabe auf dem Tablet PC](/previous-versions//dd314533(v=vs.85))
</dt> </dl>

 

