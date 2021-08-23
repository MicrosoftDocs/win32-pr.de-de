---
description: Die GetRestorePosition-Methode ruft die Position ab, an der das Fenster wiederhergestellt wird, wenn es nicht maximiert oder minimiert wird.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: CBaseControlWindow.GetRestorePosition-Methode (Ctlutil.h)
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
ms.openlocfilehash: 215b71d731227641df02716dd2b760f7e023bbec0c50bc66ac6d390ed87d002e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757610"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a>CBaseControlWindow.GetRestorePosition-Methode

Die `GetRestorePosition` -Methode ruft die Position ab, an der das Fenster wiederhergestellt wird, wenn es nicht maximiert oder minimiert wird.

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

*pLeft* 
</dt> <dd>

Zeiger auf den Wert für die äußerste linke Koordinate.

</dd> <dt>

*pTop* 
</dt> <dd>

Zeiger auf den Wert für den oberen Rand des Fensters.

</dd> <dt>

*pWidth* 
</dt> <dd>

Zeiger auf den Wert für die Breite des Fensters.

</dd> <dt>

*pHeight* 
</dt> <dd>

Zeiger auf den Wert für die Fensterhöhe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Dies entspricht den Werten, die von der [**CBaseControlWindow::GetWindowPosition-Funktion**](cbasecontrolwindow-getwindowposition.md) zurückgegeben werden, wenn das Fenster weder maximiert noch minimiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




