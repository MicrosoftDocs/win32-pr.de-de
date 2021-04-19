---
description: Die Methode "dorealilpalette" erkennt die aktuelle Palette des Fensters.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Cbasewindow. dorealilpalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368309"
---
# <a name="cbasewindowdorealisepalette-method"></a>Cbasewindow. dorealilpalette-Methode

Die `DoRealisePalette` -Methode erkennt die aktuelle Palette des Fensters.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bForceBackground* 
</dt> <dd>

Boolescher Wert, der angibt, ob die Palette als Hintergrund Palette erzwungen werden soll. Weitere Informationen finden Sie unter **SelectPalette** im Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                             | Beschreibung                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Ein interner-Befehl von " **gdiflush** " hat einen Fehler zurückgegeben.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Die [**cbasewindow:: onpalettechange**](cbasewindow-onpalettechange.md) -Methode ruft diese Methode auf. Um eine neue Palette festzulegen, müssen Sie die [**cbasewindow:: SetPalette**](cbasewindow-setpalette.md) -Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




