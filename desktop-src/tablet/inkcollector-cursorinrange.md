---
description: 'InkCollector.CursorInRange-Ereignis: Tritt ein, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tabletkontexts eintritt.'
ms.assetid: d05b240c-ba64-4008-b25d-e06c052eb5b0
title: InkCollector.CursorInRange-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60115af8b207efd9c299ba1c6fdfe69f406608f2e9e590c5be796bb67db00372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043346"
---
# <a name="inkcollectorcursorinrange-event"></a>InkCollector.CursorInRange-Ereignis

Tritt ein, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tabletkontexts eintritt.

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

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorInRange-Ereignis** generiert hat.

</dd> <dt>

*NewCursor* \[ In\]
</dt> <dd>

**VARIANT \_ TRUE,** um anzugeben, dass dies das erste Mal ist, dass dieser Freihandsammler mit dem [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) in Kontakt kommt, das das **CursorInRange-Ereignis** generiert hat; Andernfalls **VARIANT \_ FALSE**.

</dd> <dt>

*ButtonsState* \[ In\]
</dt> <dd>

Der Zustand der Schaltflächen für den Cursor, der das **CursorInRange-Ereignis** generiert hat.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ Dispatchschnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents mit der ID DISPID \_ ICECursorInRange definiert.

Das **CursorInRange-Ereignis** wird auch dann ausgelöst, wenn es sich im Select- oder Erase-Modus befindet, nicht nur im Ink-Modus. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein höheres Bewusstsein für Plattformereignisse.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**CursorOutOfRange-Ereignis**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**InkCursorButtonState-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




