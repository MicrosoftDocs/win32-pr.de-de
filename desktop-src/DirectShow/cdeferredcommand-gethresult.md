---
description: Die GetHRESULT-Methode ruft den HRESULT-Wert aus dem aufgerufenen Befehl ab.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Cdeferredcommand. GetHRESULT-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371559"
---
# <a name="cdeferredcommandgethresult-method"></a>Cdeferredcommand. GetHRESULT-Methode

Die- `GetHResult` Methode ruft den **HRESULT** -Wert aus dem aufgerufenen Befehl ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phrresult* 
</dt> <dd>

Zeiger auf den **HRESULT** -Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ Abort zurück, wenn **m \_ pqueue** den Wert **null** hat. Andernfalls gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**ideferredcommand:: GetHRESULT**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdeferredcommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




