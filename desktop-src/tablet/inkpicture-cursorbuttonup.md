---
description: 'InkPicture.CursorButtonUp-Ereignis: Tritt auf, wenn der InkCollector eine Cursorschaltfläche erkennt, die aktiv ist.'
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: InkPicture.CursorButtonUp-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639d0cbd89e2ca44d8855b6508c5284f59a7c654
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086658"
---
# <a name="inkpicturecursorbuttonup-event"></a>InkPicture.CursorButtonUp-Ereignis

Tritt ein, wenn [**der InkCollector**](inkcollector-class.md) eine cursor-Schaltfläche erkennt, die aktiv ist.

## <a name="syntax"></a>Syntax


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Schnittstellenobjekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorButtonUp-Ereignis** generiert hat.

</dd> <dt>

*Schaltfläche* \[ In\]
</dt> <dd>

Die Schaltfläche, die freigegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Schaltfläche auf einer Stiftspitze wird angezeigt, wenn der Benutzer einen Strich abschließt und den Stift aus dem Digitizer hebt. Eine Schaltfläche an einem Fass ist hoch, wenn die Schaltfläche nicht gedrückt wird.

Wenn Sie die rechte Maustaste loslassen, erhalten Sie tatsächlich zwei **CursorButtonUp-Ereignisse:** eines für die rechte Schaltfläche nach oben und eines für die linke Schaltfläche nach oben.

Diese Ereignismethode wird in den **\_ Dispinterfaces IInkCollectorEvents**, **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** mit der ID DISPID \_ ICECursorButtonUp definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**CursorButtonDown-Ereignis**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**CursorDown-Ereignis**](inkpicture-cursordown.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




