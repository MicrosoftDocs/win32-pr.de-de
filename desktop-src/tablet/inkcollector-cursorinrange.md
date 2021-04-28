---
description: 'InkCollector.CursorInRange-Ereignis: Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tablet-Kontexts eintritt.'
ms.assetid: d05b240c-ba64-4008-b25d-e06c052eb5b0
title: InkCollector.CursorInRange-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9b7cd6204b2dbb29f9a46e48ecb12569e1301f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110288"
---
# <a name="inkcollectorcursorinrange-event"></a>InkCollector.CursorInRange-Ereignis

Tritt ein, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tablet-Kontexts eintritt.

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

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorInRange-Ereignis generiert** hat.

</dd> <dt>

*NewCursor* \[ In\]
</dt> <dd>

**VARIANT \_ TRUE,** um anzugeben, dass dieser Ink-Collector zum ersten Mal mit dem [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) in Kontakt gekommen ist, das das **CursorInRange-Ereignis generiert** hat. andernfalls **VARIANT \_ FALSE**.

</dd> <dt>

*ButtonsState* \[ In\]
</dt> <dd>

Der Zustand der Schaltflächen für den Cursor, der das **CursorInRange-Ereignis generiert** hat.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die TThis-Ereignismethode ist in den \_ Dispatchschnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorInRange definiert.

Das **CursorInRange-Ereignis** wird auch dann ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur im Ink-Modus. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.

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

[**CursorOutOfRange-Ereignis**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**InkCursorButtonState-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




