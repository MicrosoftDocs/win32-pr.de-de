---
description: Die CheckMediaType-Methode bestimmt, ob ein vorgeschlagener Medientyp mit dem Anzeigeformat kompatibel ist.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: CImageDisplay.CheckMediaType-Methode (Winutil.h)
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
ms.openlocfilehash: 6bad6a7242ba110ad3916d08070eef40a8fa1d5d658ea366732e14a1cd107d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087390"
---
# <a name="cimagedisplaycheckmediatype-method"></a>CImageDisplay.CheckMediaType-Methode

Die `CheckMediaType` -Methode bestimmt, ob ein vorgeschlagener Medientyp mit dem Anzeigeformat kompatibel ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmtIn* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Ungültiger Medientyp.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ungültiger Medientyp.<br/>           |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Medientyp ist kompatibel.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImageDisplay-Klasse**](cimagedisplay.md)
</dt> </dl>

 

 




