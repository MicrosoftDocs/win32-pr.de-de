---
description: Wählt ein Clientzertifikat aus, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: IWinHttpRequest::SetClientCertificate-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 1f878b93fe0db24334f406c2a6c85663e7f37a05095998f157cbf44878b39daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562896"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>IWinHttpRequest::SetClientCertificate-Methode

Die **SetClientCertificate-Methode** wählt ein Clientzertifikat aus, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ClientCertificate* \[ In\]
</dt> <dd>

Gibt den Speicherort, [*den Zertifikatspeicher*](glossary.md)und den Antragsteller eines Clientzertifikats an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist bei Erfolg **S \_ OK,** andernfalls ein Fehlerwert.

## <a name="remarks"></a>Hinweise

Die im *ClientCertificate-Parameter* angegebene Zeichenfolge besteht aus dem Zertifikatspeicherort, dem Zertifikatspeicher und dem Antragstellernamen, die durch umgekehrte Schrägstriche getrennt sind. Weitere Informationen zu den Komponenten der Zertifikatzeichenfolge finden Sie unter [Clientzertifikate.](ssl-in-winhttp.md)

Name und Speicherort des Zertifikatspeichers sind optional. Wenn Sie jedoch einen Zertifikatspeicher angeben, müssen Sie auch den Speicherort dieses Zertifikatspeichers angeben. Der Standardspeicherort ist CURRENT \_ USER, und der Standardzertifikatspeicher ist "MY". Ein leerer Antragsteller gibt an, dass das erste Zertifikat im Zertifikatspeicher verwendet werden soll.

Rufen **Sie SetClientCertificate** auf, um ein Zertifikat auszuwählen, bevor [**Sie Senden**](iwinhttprequest-send.md) aufrufen, um die Anforderung zu senden.

Microsoft Windows HTTP Services (WinHTTP) stellt keine Clientzertifikate für Proxyserver bereit, die Zertifikate für die Authentifizierung anfordern.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Laufzeitanforderungen](winhttp-start-page.md) der WinHTTP-Startseite.

 

## <a name="examples"></a>Beispiele

Das folgende Skriptbeispiel zeigt, wie Sie ein Clientzertifikat auswählen, das mit einer Anforderung gesendet werden soll. Ein Zertifikat mit dem Betreff "Mein Middle-Tier Zertifikat" wird aus dem "persönlichen" Zertifikatspeicher in der Registrierung unter **HKEY \_ LOCAL \_ MACHINE** ausgewählt. Da dieses Codebeispiel spezifisch für Microsoft JScript ist, das den umgekehrten Schrägstrich als Escapezeichen verwendet, sind zwei angrenzende umgekehrte Schrägstriche erforderlich, um Komponenten der Zertifikatzeichenfolge zu begrenzen.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher auf Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[SSL in WinHTTP](ssl-in-winhttp.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




