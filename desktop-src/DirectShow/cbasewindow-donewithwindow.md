---
description: Die Methode "donewithwindow" zerstört das Fenster.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Cbasewindow. donewithwindow-Methode (winutil. h)
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
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350795"
---
# <a name="cbasewindowdonewithwindow-method"></a>Cbasewindow. donewithwindow-Methode

Die- `DoneWithWindow` Methode zerstört das-Fenster.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Ruft diese Methode aus der dekonstruktormethode des abgeleiteten Objekts auf.

Wenn diese Methode vom gleichen Thread aufgerufen wird, der das Fenster erstellt hat, führt die-Methode die folgenden Aktionen aus:

-   Ruft die [**cbasewindow:: inactivatewindow**](cbasewindow-inactivatewindow.md) -Methode auf, die das Fenster deaktiviert.
-   Ruft die [**cbasewindow:: uninitialisetwindow**](cbasewindow-uninitialisewindow.md) -Methode auf, die vom Fenster verwendete Ressourcen freigibt.
-   Zerstört das Fenster.

Wenn der aufrufenden Thread `DoneWithWindow` nicht der Thread ist, der das Fenster erstellt hat, sendet die Methode eine private "Destroy"-Meldung an das Fenster. Wenn das Fenster diese Nachricht empfängt, ruft es `DoneWithWindow` auf sich selbst auf. (Wenn " [**cbasewindow:: m \_ bdopostdedestroy**](cbasewindow-m-bdoposttodestroy.md) " den Wert " **true**" hat, wird die Nachricht vom Fenster ausgegeben.)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




