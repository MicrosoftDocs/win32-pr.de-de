---
description: Die SetControlWindowPin-Methode legt den Pin fest, mit dem synchronisiert werden soll.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: CBaseControlWindow.SetControlWindowPin-Methode (Ctlutil.h)
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
ms.openlocfilehash: e9ab7cbb5d199b0908c2eb51ffb5a70eda7eb1336bd66a1645daad61b3202d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056710"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a>CBaseControlWindow.SetControlWindowPin-Methode

Die `SetControlWindowPin` -Methode legt den Pin fest, mit dem synchronisiert werden soll.

## <a name="syntax"></a>Syntax


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPin* 
</dt> <dd>

Zeiger auf den Stecknadel, mit dem die Schnittstelle synchronisiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion legt die m \_ pPin-Membervariable auf den pPin-Parameter fest. Wie im Konstruktor beschrieben, kann die -Schnittstelle nur aufgerufen werden, wenn der Filter erfolgreich verbunden wurde. Das -Objekt wird über diese Memberfunktion an den Pin übergeben, mit dem es synchronisiert werden soll. In den meisten Fällen wird ermittelt, ob der Stecknadel verbunden ist, wenn er über eine Schnittstellenmethode namens verfügt, und gibt VFW \_ E \_ NOT CONNECTED \_ zurück, wenn er ausfällt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




