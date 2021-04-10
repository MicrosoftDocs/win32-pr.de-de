---
description: Tritt auf, wenn die InkCollector-Klasse eine nicht herunter gebrannte Cursor Schaltfläche erkennt.
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: InkCollector. currsorbuttondown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3994782d1266af5060bad28dd2221fe1ba18874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343299"
---
# <a name="inkcollectorcursorbuttondown-event"></a>InkCollector. currsorbuttondown-Ereignis

Tritt auf, wenn die [**InkCollector-Klasse**](inkcollector-class.md) eine nicht herunter gebrannte Cursor Schaltfläche erkennt.

## <a name="syntax"></a>Syntax


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das **CursorButtonDown** -Ereignis generiert hat.

</dd> <dt>

*Schaltfläche* \[ in\]
</dt> <dd>

Die Schaltfläche, die gedrückt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Schaltfläche auf einer Stift Spitze ist nicht mehr angezeigt, wenn der Benutzer den Stift auf den Digitalisierer senkt und die Ablauf Verfolgung für einen Strich startet. Wenn die Schaltfläche gedrückt wird, wird eine Schaltfläche auf einem Fass heruntergedrückt.

Wenn Sie mit der rechten Maustaste auf die Rechte Maustaste klicken, erhalten Sie tatsächlich zwei **Cursor buttondown** -Ereignisse: einen für die Rechte Taste gedrückt und einen für die linke Schaltfläche.

Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icecursorbuttondown definiert.

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

[**Ereignis "Cursor"**](inkcollector-cursordown.md)
</dt> <dt>

[**Currsorbuttonup-Ereignis**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Iinkcursor Button-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




