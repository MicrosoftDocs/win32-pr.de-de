---
description: Die OnClose-Methode verarbeitet WM \_ CLOSE-Nachrichten.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: CBaseWindow.OnClose-Methode (Winutil.h)
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
ms.openlocfilehash: 880e82ca527972b5074ac290fda34ad1c7868a33cbbe1cad12885b56720cef99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635140"
---
# <a name="cbasewindowonclose-method"></a>CBaseWindow.OnClose-Methode

Die `OnClose` -Methode verarbeitet WM \_ CLOSE-Nachrichten.

## <a name="syntax"></a>Syntax


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück.

## <a name="remarks"></a>Hinweise

In der Basisklasse blendet diese Methode einfach das Fenster aus. In der Regel überschreibt eine abgeleitete Klasse diese Methode, sodass sie auch ein [**EC \_ USERABORT-Ereignis**](ec-userabort.md) sendet. Überschreiben Sie nicht die -Methode, um das Fenster zu zerstören. Rufen Sie stattdessen die [**CBaseWindow::D oneWithWindow-Methode**](cbasewindow-donewithwindow.md) auf, wenn der besitzende Filter zerstört wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




