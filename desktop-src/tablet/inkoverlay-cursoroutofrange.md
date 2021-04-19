---
description: Tritt auf, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.
ms.assetid: c696b2a9-dc47-4b73-a556-9bb222f5bf59
title: InkOverlay. currsoroutfrange-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1510013d24bf092a08ba7d57b54c0f94bf7c2dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363737"
---
# <a name="inkoverlaycursoroutofrange-event"></a>InkOverlay. Cursor Event-Ereignis

Tritt auf, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.

## <a name="syntax"></a>Syntax


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor-Schnittstellen**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Objekt, das das [**cursoroutfrange**](inkcollector-cursoroutofrange.md) -Ereignis generiert hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icecursoroutofrange definiert.

Das Ereignis " [**Cursor**](inkcollector-cursoroutofrange.md) Ereignis" wird auch dann ausgelöst, wenn Sie sich im Modus "auswählen" oder "Löschen" befinden, nicht nur im frei Hand Modus. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**Cursor Event Range-Ereignis**](inkcollector-cursorinrange.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




