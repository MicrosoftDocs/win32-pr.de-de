---
description: Tritt auf, wenn eine System Bewegung erkannt wird.
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.Systemgesten-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918198e4d18a854bb4238ce9d878dc70ab1f2f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352344"
---
# <a name="inkpicturesystemgesture-event"></a>InkPicture.Systemgesten-Ereignis

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

System Gesten enthalten Informationen über das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das zum Erstellen der Geste verwendet wird. Außerdem stellen Sie Verknüpfungen zu Kombinationen von Mausereignissen bereit und bieten Möglichkeiten, Mausereignisse zu erkennen, die weniger Auswirkungen auf die Leistung haben.

Anstatt z. b. nach einem [**MouseUp-Ereignis \[ \]**](inkpicture-mouseup.md)InkPicture-Steuer / [**\[ \]**](inkpicture-mousedown.md) Element paar-Ereignisse zu suchen, bei denen keine anderen Mausereignisse dazwischen auftreten, können Sie nach der TAP-oder RightTap-System Geste suchen.

Ein weiteres Beispiel: anstatt das [**MouseDown \[ \]**](inkpicture-mousedown.md)-Ereignis InkPicture-Steuerelement / [**\[ \] MouseMove-Ereignis InkPicture**](inkpicture-mousemove.md) zu überwachen und zahlreiche **MouseMove- \[ Ereignisbild-Steuer \]** Elemente zu erhalten, können Sie die System Gesten von Drag oder RightDrag ansehen, solange Sie nicht an den (x, y)-Koordinaten jeder Position der Maus interessiert sind. Dies ermöglicht es Ihnen, anstelle von zahlreichen **mousmove- \[ ereignissteuerungsmeldungen \]** nur eine Nachricht zu empfangen.

Eine Liste der spezifischen System Gesten finden Sie unter der [**inksystemgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) -Enumerationstyp. Weitere Informationen zu System Gesten finden Sie unter [Verwenden von Gesten](using-gestures.md) und [Befehlseingaben auf dem Tablet PC](/previous-versions//dd314533(v=vs.85)).

Diese Ereignismethode wird in den Schnittstellen **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icesystemgesten definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Inksystemgesten-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> </dl>

 

