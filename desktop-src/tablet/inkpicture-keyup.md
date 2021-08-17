---
description: Tritt ein, wenn ein Schlüssel losgelassen wird, während das InkPicture-Steuerelement den Fokus besitzt.
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: InkPicture.KeyUp-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481e06556f3b4797f04e6b818ea5952d4275bf66467c7d6d0a0bd0e370c6ea12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218421"
---
# <a name="inkpicturekeyup-event"></a>InkPicture.KeyUp-Ereignis

Tritt ein, wenn ein Schlüssel losgelassen wird, während das [InkPicture-Steuerelement](inkpicture-control-reference.md) den Fokus besitzt.

## <a name="syntax"></a>Syntax


```C++
void KeyUp(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*KeyCode* \[ in, out\]
</dt> <dd>

Der ASCII-Wert der Taste, die gedrückt wird.

</dd> <dt>

*Umschalten* \[ in, out\]
</dt> <dd>

Der Zustand der UMSCHALTTASTE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IPEKeyUp.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

