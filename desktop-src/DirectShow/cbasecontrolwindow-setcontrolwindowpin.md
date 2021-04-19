---
description: Die setcontrolwindowpin-Methode legt die PIN fest, mit der synchronisiert werden soll.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Cbasecontrolwindow. setcontrolwindowpin-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362155"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a>Cbasecontrolwindow. setcontrolwindowpin-Methode

Die- `SetControlWindowPin` Methode legt die PIN fest, mit der synchronisiert werden soll.

## <a name="syntax"></a>Syntax


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* 
</dt> <dd>

Zeiger auf die PIN, mit der die Schnittstelle synchronisiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion legt die m \_ ppin-Member-Variable auf den ppin-Parameter fest. Wie im-Konstruktor beschrieben, kann die-Schnittstelle nur aufgerufen werden, wenn der Filter erfolgreich verbunden wurde. Das Objekt wird über diese Element Funktion an die PIN übergeben, mit der es synchronisiert werden soll. in den meisten Fällen wird festgestellt, ob die PIN verbunden ist, wenn Sie über eine Schnittstellen Methode mit dem Namen verfügt, und \_ \_ \_ Wenn Sie fehlschlägt, wird VFW E nicht verbunden zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




