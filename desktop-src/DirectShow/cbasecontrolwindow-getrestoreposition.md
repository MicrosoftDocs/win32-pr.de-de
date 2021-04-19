---
description: Die getrestoreposition-Methode ruft die Position ab, an der das Fenster wieder hergestellt wird, wenn es nicht maximiert oder minimiert wird.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Cbasecontrolwindow. getrestoreposition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372049"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a>Cbasecontrolwindow. getrestoreposition-Methode

Die- `GetRestorePosition` Methode ruft die Position ab, an der das Fenster wieder hergestellt wird, wenn es nicht maximiert oder minimiert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pleft* 
</dt> <dd>

Zeiger auf den Wert für die äußteste linke Koordinate.

</dd> <dt>

*ptop* 
</dt> <dd>

Zeiger auf den Wert für den oberen Rand des Fensters.

</dd> <dt>

*pWidth* 
</dt> <dd>

Zeiger auf den Wert für die Breite des Fensters.

</dd> <dt>

*pHeight* 
</dt> <dd>

Zeiger auf den Wert für die Höhe des Fensters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dies entspricht den Werten, die von der [**cbasecontrolwindow:: getwindowposition**](cbasecontrolwindow-getwindowposition.md) -Funktion zurückgegeben werden, wenn das Fenster weder maximiert noch minimiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




