---
description: Die Methode "dosetwindowstyle" ändert die typischen oder erweiterten Fenster Stile.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Cbasecontrolwindow. dosetwindowstyle-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364831"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>Cbasecontrolwindow. dosetwindowstyle-Methode

Die- `DoSetWindowStyle` Methode ändert die typischen oder erweiterten Fenster Stile.

## <a name="syntax"></a>Syntax


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Stil* 
</dt> <dd>

Geeignete Fenster Stile.

</dd> <dt>

*Windowlong* 
</dt> <dd>

Wert, der angibt, welche Stile festgelegt werden sollen. Dies muss eine der folgenden Ressourcen sein:



|              |                                      |
|--------------|--------------------------------------|
| GWL- \_ Stil   | Abrufen der Fenster Stile.          |
| GWL- \_ ExStyle | Ruft die erweiterten Fenster Stile ab. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion Ruft die Win32-Funktion **SetWindowLong** auf, um den Fenster Stil festzulegen, und zeigt dann das Fenster an der aktuellen Position erneut an. Diese Member-Funktion wird durch das [**cbasecontrolwindow::p UT \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) -und [**cbasecontrolwindow::p UT \_ windowstyleex**](cbasecontrolwindow-put-windowstyleex.md) -Member-Funktionen aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolwindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




