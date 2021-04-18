---
description: Die AMovieDllRegisterServer2-Funktion registriert Filter und hebt die Registrierung auf.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: AMovieDllRegisterServer2-Funktion (dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360984"
---
# <a name="amoviedllregisterserver2-function"></a>AMovieDllRegisterServer2-Funktion

Die **AMovieDllRegisterServer2** -Funktion registriert Filter und hebt die Registrierung auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bregister* 
</dt> <dd>

**True** gibt den Filter registrieren an, **false** bedeutet, dass die Registrierung aufgehoben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion, um die Filter einzurichten. Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dllsetup. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DLL-Setup Funktionen**](dll-setup-functions.md)
</dt> </dl>

 

 




