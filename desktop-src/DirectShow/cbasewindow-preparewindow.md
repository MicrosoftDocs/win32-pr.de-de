---
description: Die preparewindow-Methode erstellt das Fenster.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Cbasewindow. preparewindow-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370318"
---
# <a name="cbasewindowpreparewindow-method"></a>Cbasewindow. preparewindow-Methode

Mit der- `PrepareWindow` Methode wird das-Fenster erstellt.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                            | Beschreibung         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Fehler.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ruft diese Methode auf, nachdem das-Objekt erstellt wurde. Diese Methode führt eine anfängliche Buchführung aus und ruft dann die [**cbasewindow::D okreatewindow**](cbasewindow-docreatewindow.md) -Methode auf, um das Fenster zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




