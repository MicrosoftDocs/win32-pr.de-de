---
description: Die Abort-Methode bricht eine WinHTTP Send-Methode ab.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: IWinHttpRequest::Abort-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: ca70917139059e8b0d038797ad61b137a259d615f6098a52bc86466f8054c7b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071770"
---
# <a name="iwinhttprequestabort-method"></a>IWinHttpRequest::Abort-Methode

Die **Abort-Methode** bricht eine [WinHTTP Send-Methode](about-winhttp.md) [](iwinhttprequest-send.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Abort();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist **S \_ OK bei** Erfolg oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Hinweise

Sie können sowohl asynchrone als auch synchrone [**Send-Methoden**](iwinhttprequest-send.md) abbrechen. Um eine synchrone [**Send-Methode zu**](iwinhttprequest-send.md) abbrechen, müssen Sie **Abort innerhalb** eines [**IWinHttpRequestEvents-Ereignisses**](iwinhttprequestevents-interface.md) aufrufen.

> [!Note]  
> Informationen Windows XP und Windows 2000 finden Sie im Abschnitt Laufzeitanforderungen der [WinHttp-Startseite.](winhttp-start-page.md)

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher unter Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




