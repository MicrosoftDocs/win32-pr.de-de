---
description: Die DoRealisePalette-Methode erkennt die aktuelle Palette des Fensters.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: CBaseWindow.DoRealisePalette-Methode (Winutil.h)
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
ms.openlocfilehash: ce593939ec9f8aa3f2675c95e7a70363465aabb6f501fde79de839c533a1d249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757480"
---
# <a name="cbasewindowdorealisepalette-method"></a>CBaseWindow.DoRealisePalette-Methode

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

Boolescher Wert, der angibt, ob die Palette als Hintergrundpalette erzwungen wird. Weitere Informationen finden Sie unter **SelectPalette** im Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                             | Beschreibung                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Ein interner Aufruf von **GdiFlush** hat einen Fehler zurückgegeben.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Die [**CBaseWindow::OnPaletteChange-Methode**](cbasewindow-onpalettechange.md) ruft diese Methode auf. Um eine neue Palette festzulegen, rufen Sie die [**CBaseWindow::SetPalette-Methode**](cbasewindow-setpalette.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




