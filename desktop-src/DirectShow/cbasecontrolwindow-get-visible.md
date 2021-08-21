---
description: Die \_ Get Visible-Methode ruft die Sichtbarkeit des aktuellen Fensters ab.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: CBaseControlWindow.get_Visible-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef75aaf396e8677e9c470239d5dfca747729b534b67f8fef53a065280175f017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017378"
---
# <a name="cbasecontrolwindowget_visible-method"></a>CBaseControlWindow.get \_ Visible-Methode

Die `get_Visible` -Methode ruft die Sichtbarkeit des aktuellen Fensters ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVisible* 
</dt> <dd>

Zeiger auf ein boolesches Automation-Flag (0 ist deaktiviert, 1 ist aktiviert).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion gibt 1 zurück, wenn das Fenster über den \_ WS VISIBLE-Stil verfügt, andernfalls 0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




