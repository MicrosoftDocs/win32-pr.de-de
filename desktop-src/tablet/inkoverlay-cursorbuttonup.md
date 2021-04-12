---
description: Tritt auf, wenn der InkCollector eine Cursor Schaltfläche erkennt, die aktiv ist.
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: InkOverlay. currsorbuttonup-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8315f2cf87589bb24e5fb3c6ac6fd7128df426e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348678"
---
# <a name="inkoverlaycursorbuttonup-event"></a>InkOverlay. currsorbuttonup-Ereignis

Tritt auf, wenn der [**InkCollector**](inkcollector-class.md) eine Cursor Schaltfläche erkennt, die aktiv ist.

## <a name="syntax"></a>Syntax


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor-Schnittstellen**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Objekt, das das [**CursorButtonUp**](inkcollector-cursorbuttonup.md) -Ereignis generiert hat.

</dd> <dt>

*Schaltfläche* \[ in\]
</dt> <dd>

Die Schaltfläche, die freigegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Schaltfläche auf einer Stift Spitze ist aktiv, wenn der Benutzer einen Strich abschließt und den Stift vom Digitalisierer abhebt. Eine Schaltfläche auf einem Fass ist aktiv, wenn die Schaltfläche nicht gedrückt wird.

Wenn Sie die Rechte Maustaste loslassen, erhalten Sie tatsächlich zwei [**Cursor BUTTONUP**](inkcollector-cursorbuttonup.md) -Ereignisse: einen für die Rechte Taste nach oben und einen für die linke Schaltfläche.

Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icecursorbuttonup definiert.

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

[**Currsorbuttondown-Ereignis**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Ereignis "Cursor"**](inkcollector-cursordown.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Iinkcursor Button-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




