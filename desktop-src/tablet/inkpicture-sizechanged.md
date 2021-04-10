---
description: Tritt auf, nachdem die Größe des InkPicture-Steuer Elements geändert wurde, genauer gesagt, nachdem sich der Wert der Breite oder Höhe geändert hat.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: InkPicture. SizeChanged-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960668"
---
# <a name="inkpicturesizechanged-event"></a>InkPicture. SizeChanged-Ereignis

Tritt auf, nachdem die Größe des [InkPicture](inkpicture-control-reference.md) -Steuer Elements geändert wurde, genauer gesagt, nachdem sich der Wert der [**Breite**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) oder [**Höhe**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) geändert hat.

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

*Links* \[ in\]
</dt> <dd>

Die x-Koordinate der linken Seite des [InkPicture](inkpicture-control-reference.md) -Steuer Elements.

</dd> <dt>

Nach *oben* \[ in\]
</dt> <dd>

Die y-Koordinate des oberen Rands des [InkPicture](inkpicture-control-reference.md) -Steuer Elements.

</dd> <dt>

*Rechts* \[ in\]
</dt> <dd>

Die x-Koordinate der rechten Seite des [InkPicture](inkpicture-control-reference.md) -Steuer Elements.

</dd> <dt>

*Unten* \[ in\]
</dt> <dd>

Die y-Koordinate für den unteren Rand des [InkPicture](inkpicture-control-reference.md) -Steuer Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert. Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ iPeer SizeChanged".

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

 

