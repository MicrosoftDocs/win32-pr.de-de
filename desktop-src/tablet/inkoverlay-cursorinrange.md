---
description: 'InkOverlay.CursorInRange-Ereignis: Tritt ein, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tabletkontexts eintritt.'
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: InkOverlay.CursorInRange-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bcf773a3fcb0b23d26912b6b338c1741c0d9d3e5bded84759cafc1f15506c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220763"
---
# <a name="inkoverlaycursorinrange-event"></a>InkOverlay.CursorInRange-Ereignis

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

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**CursorInRange-Ereignis**](inkcollector-cursorinrange.md) generiert hat.

</dd> <dt>

*NewCursor* \[ In\]
</dt> <dd>

Gibt an, ob dieser Freihandsammler zum ersten Mal Kontakt mit dem [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) hat, das das [**CursorInRange-Ereignis**](inkcollector-cursorinrange.md) generiert hat.

</dd> <dt>

*ButtonsState* \[ In\]
</dt> <dd>

Der Zustand der Schaltflächen für den Cursor, der das [**CursorInRange-Ereignis**](inkcollector-cursorinrange.md) generiert hat.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorInRange definiert.

Das [**CursorInRange-Ereignis**](inkcollector-cursorinrange.md) wird auch dann ausgelöst, wenn es sich im Select- oder Erase-Modus befindet, nicht nur im Ink-Modus. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein höheres Bewusstsein für Plattformereignisse.

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

[**CursorOutOfRange-Ereignis**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**InkCursorButtonState-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




