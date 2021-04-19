---
description: Veraltet. Verwenden Sie stattdessen AMovieDllRegisterServer2.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Amoviedllunregisterserver-Funktion (dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cab526a69f14cdd4c4f48767ca34722f61002eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359737"
---
# <a name="amoviedllunregisterserver-function"></a>Amoviedllunregisterserver-Funktion

Veraltet. Verwenden Sie stattdessen [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .

## <a name="syntax"></a>Syntax


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

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

 

 




