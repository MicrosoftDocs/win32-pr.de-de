---
description: Tritt ein, wenn eine Taste gedrückt wird und sich in der nach unten positionierten Position befindet, während das InkPicture-Steuerelement den Fokus besitzt.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: InkPicture.KeyDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9cf86a8efaacd1094330861bff63d38ae03ef056f4686a1286e06c8aca1ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451109"
---
# <a name="inkpicturekeydown-event"></a>InkPicture.KeyDown-Ereignis

Tritt ein, wenn eine Taste gedrückt wird und sich in der nach unten positionierten Position befindet, während das [InkPicture-Steuerelement](inkpicture-control-reference.md) den Fokus besitzt.

## <a name="syntax"></a>Syntax


```C++
void KeyDown(
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

Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IPEKeyDown.

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

 

