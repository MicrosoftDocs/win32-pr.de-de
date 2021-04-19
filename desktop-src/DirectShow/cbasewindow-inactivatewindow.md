---
description: Die inactivatewindow-Methode aktiviert das Fenster. In der Basisklasse blendet diese Methode das Fenster aus.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Cbasewindow. inactivatewindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371110"
---
# <a name="cbasewindowinactivatewindow-method"></a>Cbasewindow. inactivatewindow-Methode

Mit der- `InactivateWindow` Methode wird das Fenster deaktiviert. In der Basisklasse blendet diese Methode das Fenster aus.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                             | Beschreibung                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                    |
| <dl> <dt>**S \_ false**</dt> </dl> | Das Fenster ist bereits inaktiv.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




