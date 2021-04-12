---
description: Tritt ein, wenn der Mauszeiger über das InkPicture-Steuerelement bewegt wird.
ms.assetid: b4c703da-0e4a-4d4c-9a6c-0e002344fb2f
title: InkPicture. mousermove-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5540831594674dd279fc14e822d6b3240b014c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216590"
---
# <a name="inkpicturemousemove-event"></a>InkPicture. mousermove-Ereignis

Tritt ein, wenn der Mauszeiger über das [InkPicture](inkpicture-control-reference.md) -Steuerelement bewegt wird.

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

*Schaltfläche* \[ in\]
</dt> <dd>

Die Schaltfläche, die gedrückt wurde.

</dd> <dt>

*UMSCHALT* \[ in\]
</dt> <dd>

Der Zustand der UMSCHALTTASTE.

</dd> <dt>

*px* \[ in\]
</dt> <dd>

Die x-Koordinate des [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekts in Pixel.

</dd> <dt>

*pY* \[ in\]
</dt> <dd>

Die y-Koordinate des [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekts in Pixel.

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**Variant \_ TRUE** , um dieses Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Parameter *px* und *pY* liegen in Pixel und nicht in den HIMETRIC-Einheiten, die dem Freihand Raumkoordinaten System zugeordnet sind. Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung ersetzt, die nicht mit Pen kompatibel ist, und dieser Anwendungstyp nur auf Pixel verweist.

 

> [!Caution]  
> Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**mouledown**](inkpicture-mousedown.md)-, **mousermove**-und [**mouberup**](inkpicture-mouseup.md) -Ereignissen. Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.

 

Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert. Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ ipemouabdown".

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

 

