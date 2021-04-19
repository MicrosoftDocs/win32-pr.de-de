---
description: Die activatewindow-Methode passt das Fenster entsprechend den Anforderungen der abgeleiteten Klasse an.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Cbasewindow. activatewindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359677"
---
# <a name="cbasewindowactivatewindow-method"></a>Cbasewindow. activatewindow-Methode

Die- `ActivateWindow` Methode passt die Größe des Fensters gemäß den Anforderungen der abgeleiteten Klasse an.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                             | Beschreibung                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Das Fenster wurde bereits aktiviert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**cbasewindow:: getdefaultrect**](cbasewindow-getdefaultrect.md) -Methode auf, um die Fenstergröße zu bestimmen. Die abgeleitete Klasse sollte **getdefaultrect** überschreiben, um die Größe der angezeigten Bilder zurückzugeben.

Wenn das Fenster bereits aktiv ist, wird `ActivateWindow` beim Aufrufen von das Fenster an den Anfang der Z-Reihenfolge verschoben, aber die Größe des Fensters wird nicht geändert. Das gleiche gilt, wenn das Fenster über ein übergeordnetes Element verfügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




