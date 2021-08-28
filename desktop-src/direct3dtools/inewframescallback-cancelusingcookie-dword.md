---
description: Ein Rückruf, der den Host über eine abgebrochene Anforderung benachrichtigt, indem ein Cookie verwendet wird, das die Anforderung eindeutig identifiziert.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCookie\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: INewFramesCallback::CancelUsingCookie-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36176554-BB4F-40CB-AB7B-4957DA84BAA8
api_name:
- INewFramesCallback.CancelUsingCookie
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9c7324d4ac1b992c7a2e414184ab439acc78722c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628449"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcookie_dwordspaninewframescallbackcancelusingcookie-method"></a><span id="vspixengine.inewframescallback_cancelusingcookie_dword"></span>INewFramesCallback::CancelUsingCookie-Methode

Ein Rückruf, der den Host über eine abgebrochene Anforderung benachrichtigt, indem ein Cookie verwendet wird, das die Anforderung eindeutig identifiziert.

## <a name="syntax"></a>Syntax


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a>Parameter

*requestCookie*   
Das Cookie, das die abgebrochene Anforderung eindeutig idenfigt.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**INewFramesCallback**](/windows/desktop/direct3dtools/inewframescallback)

 

 
