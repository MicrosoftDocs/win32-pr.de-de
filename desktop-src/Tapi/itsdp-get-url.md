---
description: Die Get \_ Url-Methode ruft die URL ab.
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: ITSdp::get_Url-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c024a176c4acadebad7973df01a8448cdbf83ed50b1b404f01baef00e8c8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873680"
---
# <a name="itsdpget_url-method"></a>ITSdp::get \_ Url-Methode

\[Steuerelemente und Schnittstellen für Rendezvous-IP-Telefoniekonferenzen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Get \_ Url-Methode** ruft die URL ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppUrl* \[ out\]
</dt> <dd>

Zeiger auf eine **BSTR-Darstellung** der URL.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Der *ppUrl-Parameter* ist kein gültiger Zeiger.<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Unbekannter Fehler.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die Anwendung muss [**SysFreeString verwenden,**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) um den für den *ppUrl-Parameter* zugeordneten Arbeitsspeicher frei zu geben.

Eine URL wird in der Regel verwendet, um auf eine Webseite zu verweisen, die zusätzliche Ressourcen oder Hintergrundinformationen zu einer Konferenz enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::p ut-URL \_**](itsdp-put-url.md)
</dt> </dl>

 

