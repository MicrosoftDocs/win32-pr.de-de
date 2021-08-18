---
description: Die PrepareWindow-Methode erstellt das Fenster.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: CBaseWindow.PrepareWindow-Methode (Winutil.h)
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
ms.openlocfilehash: 7b2811e307b370323c331d3f894116ad0ff01af25ad76e1ea775dae5489dfb15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074564"
---
# <a name="cbasewindowpreparewindow-method"></a>CBaseWindow.PrepareWindow-Methode

Die `PrepareWindow` -Methode erstellt das Fenster.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                            | Beschreibung         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Fehler.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nach dem Erstellen des -Objekts auf. Diese Methode führt eine anfängliche Buchhaltung durch und ruft dann die [**CBaseWindow::D oCreateWindow-Methode**](cbasewindow-docreatewindow.md) auf, um das Fenster zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




