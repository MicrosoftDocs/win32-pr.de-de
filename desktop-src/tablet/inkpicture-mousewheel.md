---
description: Tritt ein, wenn das Mausrad bewegt wird, während das InkPicture-Steuerelement den Fokus besitzt.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: InkPicture.MouseWheel-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e139604b4fbfd3293203d82b44be15fa36c090e72f40cfedc8ce0641b75b27b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938990"
---
# <a name="inkpicturemousewheel-event"></a>InkPicture.MouseWheel-Ereignis

Tritt ein, wenn das Mausrad bewegt wird, während das [InkPicture-Steuerelement](inkpicture-control-reference.md) den Fokus besitzt.

## <a name="syntax"></a>Syntax


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schaltfläche* \[ In\]
</dt> <dd>

Die Schaltfläche, die gedrückt wurde.

</dd> <dt>

*Umschalten* \[ In\]
</dt> <dd>

Der Zustand der UMSCHALTTASTE.

</dd> <dt>

*Delta* \[ In\]
</dt> <dd>

Der Abstand, den das Mausrad gedreht hat.

</dd> <dt>

*x* \[ in\]
</dt> <dd>

Die x-Koordinate des [**IInkCursor-Objekts**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) in Pixel.

</dd> <dt>

*y* \[ in\]
</dt> <dd>

Die y-Koordinate des [**IInkCursor-Objekts**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) in Pixel.

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

VARIANT \_ TRUE, um das **MouseWheel-Ereignis** für das übergeordnete Steuerelement abzubrechen, andernfalls VARIANT \_ FALSE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Parameter *x* und *y* sind in Pixel und nicht die HIMETRIC-Einheiten, die dem Freihandraumkoordinatensystem zugeordnet sind. Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Anwendung ersetzt, die keinen Stift erkennt, und dieser Anwendungstyp sich nur auf Pixel bezieht.

 

Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IPEMouseWheel.

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

 

