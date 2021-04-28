---
description: 'InkPicture.CursorOutOfRange-Ereignis: Tritt auf, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.'
ms.assetid: 0c71a4ad-3c09-4134-b0e7-82f29e8913ed
title: InkPicture.CursorOutOfRange-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d80584eafb7f1e5222316507f08bd73efb12fae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086568"
---
# <a name="inkpicturecursoroutofrange-event"></a>InkPicture.CursorOutOfRange-Ereignis

Tritt ein, wenn der Cursor den physischen Erkennungsbereich (Nähe) des Tablet-Kontexts verlässt.

## <a name="syntax"></a>Syntax


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Schnittstellenobjekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorOutOfRange-Ereignis generiert** hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den Dispatch-Schnittstellen **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICECursorOutOfRange definiert.

Das **CursorOutOfRange-Ereignis** wird auch dann ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur im Ink-Modus. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**CursorInRange-Ereignis**](inkpicture-cursorinrange.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




