---
description: Die checkmediatype-Methode bestimmt, ob ein vorgeschlagene Medientyp mit dem Anzeige Format kompatibel ist.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Cimagedisplay. checkmediatype-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366906"
---
# <a name="cimagedisplaycheckmediatype-method"></a>Cimagedisplay. checkmediatype-Methode

Die- `CheckMediaType` Methode bestimmt, ob ein vorgeschlagene Medientyp mit dem Anzeige Format kompatibel ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmtin* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>       | Ungültiger Medientyp.<br/>           |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültiger Medientyp.<br/>           |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Medientyp ist kompatibel.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagedisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




