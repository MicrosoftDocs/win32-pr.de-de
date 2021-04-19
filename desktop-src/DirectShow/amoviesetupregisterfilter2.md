---
description: Die AMovieSetupRegisterFilter2-Funktion registriert die Vorzüge, Pins und Medientypen eines Filters mithilfe der IFilterMapper2-Schnittstelle in der Registrierung.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: AMovieSetupRegisterFilter2-Funktion (dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359736"
---
# <a name="amoviesetupregisterfilter2-function"></a>AMovieSetupRegisterFilter2-Funktion

Die **AMovieSetupRegisterFilter2** -Funktion registriert die Vorzüge, Pins und Medientypen eines Filters mithilfe der [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle in der Registrierung.

## <a name="syntax"></a>Syntax


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psetupdata* 
</dt> <dd>

Zeiger auf die [**amoviesetup- \_ Filter**](amoviesetup-filter.md) Daten.

</dd> <dt>

*pIFM2* 
</dt> <dd>

Zeiger auf die [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle.

</dd> <dt>

*bregister* 
</dt> <dd>

Wert, der angibt, ob der Filter registriert werden soll. **True** gibt den Filter registrieren an, **false** bedeutet, dass die Registrierung aufgehoben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) -Funktion ruft diese Hilfsfunktion auf, um einen Filter zu registrieren, nachdem der com-Server registriert wurde.

In der Regel verwendet ein Filter [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) und ruft diese Funktion nicht direkt auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dllsetup. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DLL-Setup Funktionen**](dll-setup-functions.md)
</dt> </dl>

 

 




