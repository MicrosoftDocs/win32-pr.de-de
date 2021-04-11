---
description: Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Near) des Tablet-Kontexts eintritt.
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: InkOverlay. Cursor Input Range-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65745e93bfb7351f7e1fa6d01965ce7a271bc0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960503"
---
# <a name="inkoverlaycursorinrange-event"></a>InkOverlay. currsorinrange-Ereignis

Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Near) des Tablet-Kontexts eintritt.

## <a name="syntax"></a>Syntax


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das [**CursorInRange**](inkcollector-cursorinrange.md) -Ereignis generiert hat.

</dd> <dt>

*NewCursor* \[ in\]
</dt> <dd>

Ob dies das erste Mal ist, wenn dieser frei Hand Sammler mit dem [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt kontaktiert wird, das das [**CursorInRange**](inkcollector-cursorinrange.md) -Ereignis generiert hat.

</dd> <dt>

*Buttonsstate* \[ in\]
</dt> <dd>

Der Zustand der Schaltflächen für den Cursor, der das [**CursorInRange**](inkcollector-cursorinrange.md) -Ereignis generiert hat.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ icecursorinrange definiert.

Das Ereignis [**Cursor**](inkcollector-cursorinrange.md) wird auch dann ausgelöst, wenn es sich im Modus auswählen oder löschen befindet, nicht nur im frei Hand Modus. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.

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

[**Cursor-Ereignis**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**Inkcurrsorbuttonstate-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




