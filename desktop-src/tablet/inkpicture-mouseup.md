---
description: Tritt ein, wenn der Mauszeiger über das InkPicture-Steuerelement bewegt und eine Maustaste losgelassen wird.
ms.assetid: 5e49acc8-1ce1-45ff-b87c-04bdc653156a
title: InkPicture.MouseUp-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec780348191a4bfe8d0aadb0ad075a3784f49f23504c7dc02ca5f6da14c0d54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218376"
---
# <a name="inkpicturemouseup-event"></a>InkPicture.MouseUp-Ereignis

Tritt ein, wenn der Mauszeiger über das [InkPicture-Steuerelement](inkpicture-control-reference.md) bewegt und eine Maustaste losgelassen wird.

## <a name="syntax"></a>Syntax


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
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

*pX* \[ In\]
</dt> <dd>

Die x-Koordinate des [**IInkCursor-Objekts**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) in Pixel.

</dd> <dt>

*pY* \[ In\]
</dt> <dd>

Die y-Koordinate des [**IInkCursor-Objekts**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) in Pixel.

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE,** um das MouseUp-Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Parameter *pX* und *pY* sind in Pixel und nicht die HIMETRIC-Einheiten, die dem Freihandraumkoordinatensystem zugeordnet sind. Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Anwendung ersetzt, die keinen Stift erkennt, und dieser Anwendungstyp sich nur auf Pixel bezieht.

 

> [!Caution]  
> Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**MouseDown-,**](inkpicture-mousedown.md) [**MouseMove-**](inkpicture-mousemove.md)und **MouseUp-Ereignissen.** Das Abbrechen einiger dieser Ereignisse kann unerwartete Ergebnisse haben.

 

Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IPEMouseDown.

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

 

