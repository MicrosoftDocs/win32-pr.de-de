---
description: Tritt ein, wenn eine Taste gedrückt wird, während das InkPicture-Steuerelement den Fokus besitzt.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: InkPicture.KeyPress-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7545b0de722ec9b48c66aa5d2236bf81eb576d87916c15e618508e537981a2cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939010"
---
# <a name="inkpicturekeypress-event"></a>InkPicture.KeyPress-Ereignis

Tritt ein, wenn eine Taste gedrückt wird, während das [InkPicture-Steuerelement](inkpicture-control-reference.md) den Fokus besitzt.

## <a name="syntax"></a>Syntax


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*KeyAscii* \[ in, out\]
</dt> <dd>

Der ASCII-Wert der Taste, die gedrückt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IPEKeyPress.

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

 

