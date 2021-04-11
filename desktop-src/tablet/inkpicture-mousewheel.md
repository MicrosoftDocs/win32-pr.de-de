---
description: Tritt auf, wenn das Mausrad bewegt wird, während das inkbilsteuerelement den Fokus besitzt.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: InkPicture. mouswheel-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cab870f3a00b2aa0cea3c003993e2b35cd2abbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346109"
---
# <a name="inkpicturemousewheel-event"></a>InkPicture. mouswheel-Ereignis

Tritt auf, wenn das Mausrad bewegt wird, während das [inkbilsteuerelement](inkpicture-control-reference.md) den Fokus besitzt.

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

*Schaltfläche* \[ in\]
</dt> <dd>

Die Schaltfläche, die gedrückt wurde.

</dd> <dt>

*UMSCHALT* \[ in\]
</dt> <dd>

Der Zustand der UMSCHALTTASTE.

</dd> <dt>

*Delta* \[ in\]
</dt> <dd>

Die Entfernung des Mausrades.

</dd> <dt>

*x* \[ in\]
</dt> <dd>

Die x-Koordinate des [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekts in Pixel.

</dd> <dt>

*j* \[ in\]
</dt> <dd>

Die y-Koordinate des [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekts in Pixel.

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

Variant \_ true, um das **mouswheel** -Ereignis für das übergeordnete Steuerelement abzubrechen, andernfalls Variant \_ false.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Parameter *x* und *y* befinden sich in Pixel, nicht jedoch die HIMETRIC-Einheiten, die dem Koordinatensystem des frei Hand Raum-Koordinatensystems zugeordnet sind. Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung ersetzt, die nicht mit Pen kompatibel ist, und dieser Anwendungstyp nur auf Pixel verweist.

 

Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert. Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ ipemouserwheel".

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

 

