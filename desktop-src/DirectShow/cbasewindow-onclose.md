---
description: Die OnClose-Methode behandelt WM- \_ Schließen-Nachrichten.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Cbasewindow. OnClose-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369991"
---
# <a name="cbasewindowonclose-method"></a>Cbasewindow. OnClose-Methode

Die- `OnClose` Methode behandelt WM- \_ Schließen-Nachrichten.

## <a name="syntax"></a>Syntax


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück.

## <a name="remarks"></a>Bemerkungen

In der Basisklasse blendet diese Methode einfach das Fenster aus. In der Regel wird diese Methode von einer abgeleiteten Klasse überschrieben, sodass auch ein [**EC \_ userabort**](ec-userabort.md) -Ereignis gesendet wird. Überschreiben Sie die-Methode nicht, um das Fenster zu zerstören. Stattdessen wird die Methode [**cbasewindow::D onewithwindow**](cbasewindow-donewithwindow.md) aufgerufen, wenn der besitzende Filter zerstört wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




