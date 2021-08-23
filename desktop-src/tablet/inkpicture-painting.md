---
description: Tritt ein, bevor das InkPicture-Steuerelement sich selbst neu gedrammt.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: InkPicture.Painting-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129e5f74ee8097794112b70fb709ab9b9a3b8fadc9f3e5a2fd7d874c65c0d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966969"
---
# <a name="inkpicturepainting-event"></a>InkPicture.Painting-Ereignis

Tritt ein, bevor das [InkPicture-Steuerelement](inkpicture-control-reference.md) sich selbst neu gedrammt.

## <a name="syntax"></a>Syntax


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDC* \[ In\]
</dt> <dd>

Der Gerätekontext, in dem das Malen erfolgt.

</dd> <dt>

*Rect* \[ In\]
</dt> <dd>

Das Ink-Rechteck, das neu gepaint werden soll.

</dd> <dt>

*Zulassen* \[ in, out\]
</dt> <dd>

Gibt an, ob der Neupaint auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den dispatch-only-Schnittstellen (dispinterfaces) **\_ von IInkOverlayEvents** und **\_ IInkPictureEvents** mit der ID DISPID \_ IOEPainting definiert.

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

 

 




