---
description: Veraltet. Verwenden Sie stattdessen AMovieSetupRegisterFilter2.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: Amoviesetupregisterfilter-Funktion (dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373808"
---
# <a name="amoviesetupregisterfilter-function"></a>Amoviesetupregisterfilter-Funktion

Veraltet. Verwenden Sie stattdessen [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) .

## <a name="syntax"></a>Syntax


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psetupdata* 
</dt> <dd>

Reserviert.

</dd> <dt>

*pifm* 
</dt> <dd>

Reserviert.

</dd> <dt>

*bregister* 
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dllsetup. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DLL-Setup Funktionen**](dll-setup-functions.md)
</dt> </dl>

 

 




