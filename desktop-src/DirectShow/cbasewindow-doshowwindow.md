---
description: Die DoShowWindow-Methode legt den Showzustand des Fensters fest.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: CBaseWindow.DoShowWindow-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fef63e04d0e04f2fe0daa78cd6b33a22fa7c8fa14c57b1e022703dea0914dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074628"
---
# <a name="cbasewindowdoshowwindow-method"></a>CBaseWindow.DoShowWindow-Methode

Die **DoShowWindow-Methode** legt den Showzustand des Fensters fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ShowCmd* 
</dt> <dd>

Flag, das angibt, wie das Fenster angezeigt werden soll. Der Wert kann eine beliebige Konstante sein, die für den *nCmdShow-Parameter* der [**ShowWindow-Funktion definiert**](/windows/desktop/api/winuser/nf-winuser-showwindow) ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

