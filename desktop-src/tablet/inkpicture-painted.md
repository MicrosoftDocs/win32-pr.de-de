---
description: Tritt ein, wenn das InkPicture-Steuerelement die Neuzeichnung abgeschlossen hat.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: InkPicture.Painted-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201027ba2626cd3a3dd8d76a8794a1a5430785e0e1602633ee9f39ac36caa023
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451054"
---
# <a name="inkpicturepainted-event"></a>InkPicture.Painted-Ereignis

Tritt ein, wenn das [InkPicture-Steuerelement](inkpicture-control-reference.md) die Neuzeichnung selbst abgeschlossen hat.

## <a name="syntax"></a>Syntax


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDC* \[ In\]
</dt> <dd>

Der Gerätekontext, in dem das Ereignis aufgetreten ist.

</dd> <dt>

*Rect* \[ In\]
</dt> <dd>

Der [**neu gepainte InkRectangle.**](inkrectangle-class.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den **\_ Disp-Interfaces IInkOverlayEvents** und **\_ IInkPictureEvents** mit der ID DISPID \_ IOEPainted definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




