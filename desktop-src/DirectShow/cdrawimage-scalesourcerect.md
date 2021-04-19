---
description: Die scalesourcerect-Methode skaliert ein Rechteck, wenn es einen Unterschied zwischen der nativen Videogröße und dem Medientyp Format gibt.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Cdrawimage. scalesourcerect-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369572"
---
# <a name="cdrawimagescalesourcerect-method"></a>Cdrawimage. scalesourcerect-Methode

Die `ScaleSourceRect` -Methode skaliert ein Rechteck, wenn es einen Unterschied zwischen der nativen Videogröße und dem Medientyp Format gibt.

## <a name="syntax"></a>Syntax


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psource* 
</dt> <dd>

Zeiger auf ein nicht skaliertes Rechteck.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das skalierte Rechteck zurück.

## <a name="remarks"></a>Bemerkungen

In der **cdrawimage** -Klasse gibt diese Methode *psource* ohne Änderung zurück. Sie können diese Methode überschreiben, wenn der Filter das eingehende Video Bild ausdehnt. Beispielsweise könnte die Größe des nativen Videos 320 240 lauten, der Medientyp der Eingabe-PIN kann jedoch 640 480 lauten. In diesem Fall muss der Filter das Quell Rechteck mit dem Faktor 2 skalieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrawimage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




