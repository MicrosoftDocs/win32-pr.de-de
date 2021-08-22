---
description: Die DoneWithWindow-Methode zerstört das Fenster.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: CBaseWindow.DoneWithWindow-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6871a42e1a08693a7daf691195b86cd5a41dd208295dc625a33e41083b53adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016668"
---
# <a name="cbasewindowdonewithwindow-method"></a>CBaseWindow.DoneWithWindow-Methode

Die `DoneWithWindow` -Methode zerstört das Fenster.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode aus der Destruktormethode des abgeleiteten Objekts auf.

Wenn diese Methode aus demselben Thread aufgerufen wird, der das Fenster erstellt hat, führt die -Methode die folgenden Aktionen aus:

-   Ruft die [**CBaseWindow::InactivateWindow-Methode**](cbasewindow-inactivatewindow.md) auf, die das Fenster deaktiviert.
-   Ruft die [**CBaseWindow::UninitialiseWindow-Methode**](cbasewindow-uninitialisewindow.md) auf, die vom Fenster verwendete Ressourcen frei gibt.
-   Zerstört das Fenster.

Wenn der Thread, der aufruft, nicht der Thread ist, der das Fenster erstellt hat, sendet die Methode eine `DoneWithWindow` private "destroy"-Nachricht an das Fenster. Wenn das Fenster diese Meldung empfängt, ruft es `DoneWithWindow` für sich selbst auf. (Wenn [**CBaseWindow::m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) **true ist,** gibt das Fenster die Meldung aus.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




