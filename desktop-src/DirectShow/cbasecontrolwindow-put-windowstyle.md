---
description: Mit der Put- \_ Methode WindowStyle werden die Standardfenster Stile festgelegt.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: CBaseControlWindow.put_WindowStyle-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361060"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a>Cbasecontrolwindow. Put \_ WindowStyle-Methode

Die- `put_WindowStyle` Methode legt die Standardfenster Stile fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*WindowStyle* 
</dt> <dd>

Neue Fenster Stile.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Achten Sie darauf, die Fenster Stile zu ändern. In den meisten Fällen sollte eine Anwendung den aktuellen Stil abrufen und dann die unpassenden Bits hinzufügen oder entfernen. Diese Prozedur ermöglicht es, dass verschiedene interne Fenster Stile, die von Windows verwendet werden, intakt bleiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




