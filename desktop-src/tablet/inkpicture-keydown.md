---
description: Tritt auf, wenn eine Taste gedrückt wird, während das InkPicture-Steuerelement den Fokus besitzt.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: InkPicture. KeyDown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5d6bd3555aeec98ac28555c1674dfef32ecc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050582"
---
# <a name="inkpicturekeydown-event"></a>InkPicture. KeyDown-Ereignis

Tritt auf, wenn eine Taste gedrückt wird, während das [InkPicture](inkpicture-control-reference.md) -Steuerelement den Fokus besitzt.

## <a name="syntax"></a>Syntax


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Keycode* \[ in, out\]
</dt> <dd>

Der ASCII-Wert des Schlüssels, der gedrückt wird.

</dd> <dt>

*UMSCHALT* \[ in, out\]
</dt> <dd>

Der Zustand der UMSCHALTTASTE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert. Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ipinkeydown.

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

 

