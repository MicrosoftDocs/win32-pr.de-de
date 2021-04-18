---
description: Die doshowwindow-Methode legt den Anzeige Zustand des Fensters fest.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Cbasewindow. doshowwindow-Methode (winutil. h)
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
ms.openlocfilehash: a2a1f7d4cd9bc4600733d5d33f9df6d3b6998f57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372382"
---
# <a name="cbasewindowdoshowwindow-method"></a>Cbasewindow. doshowwindow-Methode

Die **doshowwindow** -Methode legt den Anzeige Zustand des Fensters fest.

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

Flag, das angibt, wie das Fenster angezeigt werden soll. Der Wert kann eine beliebige Konstante sein, die für den *nCmdShow* -Parameter der [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion definiert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

