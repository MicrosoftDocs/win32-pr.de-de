---
description: Tritt auf, bevor IInkStrokeDisp-Objekte aus der Ink-Eigenschaft gelöscht werden.
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: InkPicture. strokeslösch-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042718"
---
# <a name="inkpicturestrokesdeleting-event"></a>InkPicture. strokeslösch-Ereignis

Tritt auf, bevor [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) -Eigenschaft gelöscht werden.

## <a name="syntax"></a>Syntax


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Striche* \[ in\]
</dt> <dd>

Die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die beim Auslösen des **strokeslösch** -Ereignisses gelöscht wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID "DISPID \_ ioestrokeslösch" definiert.

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
</dt> </dl>

 

