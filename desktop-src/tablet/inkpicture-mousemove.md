---
description: Tritt ein, wenn der Mauszeiger über das InkPicture-Steuerelement bewegt wird.
ms.assetid: b4c703da-0e4a-4d4c-9a6c-0e002344fb2f
title: InkPicture.MouseMove-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd7a45d8c2829dd9721eebed918b54a9ad7fbb505988bc538563fefc46e33da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032048"
---
# <a name="inkpicturemousemove-event"></a>InkPicture.MouseMove-Ereignis

Tritt ein, wenn der Mauszeiger über das [InkPicture-Steuerelement bewegt](inkpicture-control-reference.md) wird.

## <a name="syntax"></a>Syntax


```C++
void MouseMove(
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

**VARIANT \_ TRUE,** um dieses Ereignis für das übergeordnete Steuerelement abzubricht; andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Parameter *pX* und *pY* befinden sich in Pixeln und nicht in den HIMETRIC-Einheiten, die dem Freiraumkoordinatensystem zugeordnet sind. Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Anwendung ersetzt, die nicht stiftbezogen ist, und dieser Anwendungstyp nur auf Pixel verweist.

 

> [!Caution]  
> Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**MouseDown-,**](inkpicture-mousedown.md) **MouseMove-** und [**MouseUp-Ereignissen.**](inkpicture-mouseup.md) Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.

 

Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IPEMouseDown.

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

 

