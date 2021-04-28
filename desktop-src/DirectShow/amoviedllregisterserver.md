---
description: 'AMovieDllRegisterServer-Funktion: Veraltet. Verwenden Sie stattdessen AMovieDllRegisterServer2.'
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: AMovieDllRegisterServer-Funktion (Dllsetup.h)
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
ms.openlocfilehash: 81b6e73b1988d3eb97abdf9a5d2415ecbd62d8c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099938"
---
# <a name="amoviedllregisterserver-function"></a>AMovieDllRegisterServer-Funktion

Veraltet. Verwenden [**Sie stattdessen AMovieDllRegisterServer2.**](amoviedllregisterserver2.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dllsetup.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DLL-Setupfunktionen**](dll-setup-functions.md)
</dt> </dl>

 

 




