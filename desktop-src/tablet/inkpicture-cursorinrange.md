---
description: 'InkPicture.CursorInRange-Ereignis: Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tablet-Kontexts eintritt.'
ms.assetid: e921e175-a2cf-45e6-bb81-dc82e384d3b1
title: InkPicture.CursorInRange-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a44b41e9eaffa4cb7a6939e1e6b8caf55cb7fbb8782d75cda490e4dc3d34a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042101"
---
# <a name="inkpicturecursorinrange-event"></a>InkPicture.CursorInRange-Ereignis

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

**VARIANT \_ TRUE,** wenn dieser Ink-Collector zum ersten Mal mit dem [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) in Kontakt gekommen ist, das das **CursorInRange-Ereignis generiert** hat. andernfalls **VARIANT \_ FALSE**.

</dd> <dt>

*ButtonsState* \[ In\]
</dt> <dd>

Der Zustand der Schaltflächen für den Cursor, der das **CursorInRange-Ereignis generiert** hat.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den Dispatch-Schnittstellen **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICECursorInRange definiert.

Das **CursorInRange-Ereignis** wird auch dann ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur im Ink-Modus. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.

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

[**CursorOutOfRange-Ereignis**](inkpicture-cursoroutofrange.md)
</dt> <dt>

[**InkCursorButtonState-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




