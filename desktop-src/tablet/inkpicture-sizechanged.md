---
description: Tritt ein, nachdem die Größe des InkPicture-Steuerelements geändert wurde, insbesondere nachdem sich der Width- oder Height-Eigenschaftswert geändert hat.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: InkPicture.SizeChanged-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4473bf580e1683c8d410cd1f2cdbaf271302485f51556b68c4fae7a5d6b99ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032038"
---
# <a name="inkpicturesizechanged-event"></a>InkPicture.SizeChanged-Ereignis

Tritt ein, nachdem die Größe des [InkPicture-Steuerelements](inkpicture-control-reference.md) geändert wurde, insbesondere nachdem sich der [**Width-**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) oder [**Height-Eigenschaftswert**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) geändert hat.

## <a name="syntax"></a>Syntax


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Links* \[ In\]
</dt> <dd>

Die x-Koordinate der linken Seite des [InkPicture-Steuerelements.](inkpicture-control-reference.md)

</dd> <dt>

*Top* \[ In\]
</dt> <dd>

Die y-Koordinate des oberen Rands des [InkPicture-Steuerelements.](inkpicture-control-reference.md)

</dd> <dt>

*Rechts* \[ In\]
</dt> <dd>

Die x-Koordinate der rechten Seite des [InkPicture-Steuerelements.](inkpicture-control-reference.md)

</dd> <dt>

*Unten* \[ In\]
</dt> <dd>

Die y-Koordinate des unteren Rands des [InkPicture-Steuerelements.](inkpicture-control-reference.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IPESizeChanged.

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

 

