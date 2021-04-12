---
description: Tritt auf, wenn die InkCollector-Klasse eine nicht herunter gebrannte Cursor Schaltfläche erkennt.
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: InkPicture. currsorbuttondown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4531f41ce597d9cbb1fa0b8665a1821a8a32dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217674"
---
# <a name="inkpicturecursorbuttondown-event"></a>InkPicture. currsorbuttondown-Ereignis

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

Diese Ereignismethode wird in **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** Dispatch-only Interface (Dispinterfaces) mit der ID DISPID \_ icecursorbuttondown definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Ereignis "Cursor"**](inkpicture-cursordown.md)
</dt> <dt>

[**Currsorbuttonup-Ereignis**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Iinkcursor Button-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




