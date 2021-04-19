---
description: Die dogetwindowstyle-Methode ruft die aktuellen normalen oder erweiterten Fenster Stile ab.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Cbasecontrolwindow. dogetwindowstyle-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367022"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>Cbasecontrolwindow. dogetwindowstyle-Methode

Die- `DoGetWindowStyle` Methode ruft die aktuellen normalen oder erweiterten Fenster Stile ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStyle* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Stil Informationen empfängt.

</dd> <dt>

*Windowlong* 
</dt> <dd>

Ein Wert, der angibt, welche Stile abgerufen werden sollen. Dies muss eine der folgenden Ressourcen sein:



|              |                                      |
|--------------|--------------------------------------|
| GWL- \_ Stil   | Abrufen der Fenster Stile.          |
| GWL- \_ ExStyle | Ruft die erweiterten Fenster Stile ab. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion Ruft die Win32 **GetWindowLong** -Funktion auf, um den Fenster Stil abzurufen. Sie wird von den Element Funktionen [**cbasecontrolwindow:: get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) und [**cbasecontrolwindow:: get \_ windowstyleex**](cbasecontrolwindow-get-windowstyleex.md) aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




