---
description: Die get \_ WindowState-Methode ruft den aktuellen Fenster Zustand ab.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: CBaseControlWindow.get_WindowState-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371515"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a>Cbasecontrolwindow. get \_ WindowState-Methode

Die- `get_WindowState` Methode ruft den aktuellen Fenster Zustand ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwindowstate* 
</dt> <dd>

Zeiger auf den Fenster Zustand.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion gibt eine Teilmenge der Parameter der Microsoft Win32 **ShowWindow** -Funktion zurück. Vor allem gibt Sie in \_ \_ Abhängigkeit von der aktuellen Sichtbarkeit des Fensters "SW Show" und "SW Hide" zurück. Außerdem gibt es eine "SW \_ -minimieren" und "SW \_ maximieren" zurück, je nachdem, ob das Fenster ein Symbol ist oder erweitert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




