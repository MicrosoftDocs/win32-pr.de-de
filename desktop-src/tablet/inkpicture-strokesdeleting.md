---
description: Tritt ein, bevor IInkStrokeDisp-Objekte aus der Freihandeigenschaft gelöscht werden.
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: InkPicture.StrokesDeleting-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1a58dfe8f52ae6fc8ec5d7a74f3457a5e6306ad556ceee1bb50772d6a75d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041895"
---
# <a name="inkpicturestrokesdeleting-event"></a>InkPicture.StrokesDeleting-Ereignis

Tritt ein, bevor [**IInkStrokeDisp-Objekte**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) aus der [**Freihandeigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) gelöscht werden.

## <a name="syntax"></a>Syntax


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Striche* \[ In\]
</dt> <dd>

Die [Sammlung InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wurde gelöscht, wenn das **StrokesDeleting-Ereignis** ausgelöst wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ IOEStrokesDeleting definiert.

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
</dt> </dl>

 

