---
description: 'Die getrate-Methode ruft die Wiedergabe Rate ab. Diese Methode implementiert die imediaseeking:: getrate-Methode.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Csourceseeking. getrate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b14cad0b043193f7ee410455aaa399e3bcb26715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366751"
---
# <a name="csourceseekinggetrate-method"></a>Csourceseeking. getrate-Methode

Die- `GetRate` Methode ruft die Wiedergabe Rate ab. Diese Methode implementiert die [**imediaseeking:: getrate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdrate* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Wiedergabe Rate empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeiger Wert<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Wiedergabe Rate wird von der Element Variablen [**csourceseeking:: m \_ drateseeking**](csourceseeking-m-drateseeking.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




