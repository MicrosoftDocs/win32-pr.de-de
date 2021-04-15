---
description: Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Near) des Tablet-Kontexts eintritt.
ms.assetid: d05b240c-ba64-4008-b25d-e06c052eb5b0
title: InkCollector. Cursor Event Range-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c1d59927f9ed0a932fe28a2c5243f328a223c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525274"
---
# <a name="inkcollectorcursorinrange-event"></a>InkCollector. Cursor Event Range-Ereignis

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

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das **CursorInRange** -Ereignis generiert hat.

</dd> <dt>

*NewCursor* \[ in\]
</dt> <dd>

**Variant \_ TRUE** , um anzugeben, dass dies das erste Mal ist, dass dieser frei Hand Sammler mit dem [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt kontaktiert wird, das das **CursorInRange** -Ereignis generiert hat. Andernfalls ist der Wert **\_ false**.

</dd> <dt>

*Buttonsstate* \[ in\]
</dt> <dd>

Der Zustand der Schaltflächen für den Cursor, der das **CursorInRange** -Ereignis generiert hat.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

TDiese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ icecursorinrange definiert.

Das Ereignis **Cursor** wird auch dann ausgelöst, wenn es sich im Modus auswählen oder löschen befindet, nicht nur im frei Hand Modus. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.

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

[**Cursor-Ereignis**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**Inkcurrsorbuttonstate-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




