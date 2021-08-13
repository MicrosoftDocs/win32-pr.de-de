---
description: Die ActivateWindow-Methode größent das Fenster entsprechend den Anforderungen der abgeleiteten Klasse.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: CBaseWindow.ActivateWindow-Methode (Winutil.h)
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
ms.openlocfilehash: e00c3ccc43e2583ce8664e62967a22f753148cfa271dd1995e2374c2bfa53c71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658244"
---
# <a name="cbasewindowactivatewindow-method"></a>CBaseWindow.ActivateWindow-Methode

Die `ActivateWindow` -Methode größent das Fenster entsprechend den Anforderungen der abgeleiteten Klasse.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                             | Beschreibung                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Das Fenster wurde bereits aktiviert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                      |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**CBaseWindow::GetDefaultRect-Methode**](cbasewindow-getdefaultrect.md) auf, um die Fenstergröße zu bestimmen. Die abgeleitete Klasse sollte **GetDefaultRect** überschreiben, um die Größe der bilder zurückzugeben, die angezeigt werden.

Wenn das Fenster bereits aktiv ist, verschiebt der Aufruf `ActivateWindow` von das Fenster an den Anfang der Z-Reihenfolge, ändert jedoch nicht die Größe des Fensters. Dasselbe gilt, wenn das Fenster über ein übergeordnetes Element verfügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




