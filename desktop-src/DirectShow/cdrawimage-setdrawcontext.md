---
description: Die setdrawcontext-Methode legt die zum Zeichnen verwendeten Geräte Kontexte fest.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Cdrawimage. setdrawcontext-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358029"
---
# <a name="cdrawimagesetdrawcontext-method"></a>Cdrawimage. setdrawcontext-Methode

Die- `SetDrawContext` Methode legt die zum Zeichnen verwendeten Geräte Kontexte fest.

## <a name="syntax"></a>Syntax


```C++
void SetDrawContext();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die Fenster-und Arbeitsspeicher-Geräte Kontexte aus dem besitzenden [**cbasewindow**](cbasewindow.md) -Objekt ab. Ruft diese Methode auf, nachdem das Fenster initialisiert wurde, jedoch bevor Sie mit dem Zeichnen beginnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




