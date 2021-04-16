---
description: Wählt ein Client Zertifikat aus, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'Iwinhttprequest:: setclientcertificate-Methode'
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
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347208"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>Iwinhttprequest:: setclientcertificate-Methode

Mit der **setclientcertificate** -Methode wird ein Client Zertifikat ausgewählt, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ClientCertificate* \[ in\]
</dt> <dd>

Gibt den Speicherort, den [*Zertifikat Speicher*](glossary.md)und den Betreff eines Client Zertifikats an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.

## <a name="remarks"></a>Bemerkungen

Die im *ClientCertificate* -Parameter angegebene Zeichenfolge besteht aus dem Zertifikat Speicherort, dem Zertifikat Speicher und dem Antragsteller Namen, die durch umgekehrte Schrägstriche getrennt sind. Weitere Informationen zu den Komponenten der Zertifikat Zeichenfolge finden Sie unter [Client Zertifikate](ssl-in-winhttp.md).

Der Name und Speicherort des Zertifikat Speicher sind optional. Wenn Sie jedoch einen Zertifikat Speicher angeben, müssen Sie auch den Speicherort dieses Zertifikat Speicher angeben. Der Standard Speicherort ist aktueller \_ Benutzer und der Standard Zertifikat Speicher "My". Ein leerer Betreff gibt an, dass das erste Zertifikat im Zertifikat Speicher verwendet werden soll.

Rufen Sie **setclientcertificate** auf, um ein Zertifikat auszuwählen, bevor [**Sie Send**](iwinhttprequest-send.md) aufrufen, um die Anforderung zu senden.

Microsoft Windows HTTP-Dienste (WinHTTP) stellen keine Client Zertifikate für Proxy Server bereit, die Zertifikate für die Authentifizierung anfordern.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.

 

## <a name="examples"></a>Beispiele

Im folgenden Skript Beispiel wird gezeigt, wie Sie ein Client Zertifikat auswählen, das mit einer Anforderung gesendet werden soll. Ein Zertifikat mit dem Betreff "My Middle-Tier Certificate" wird aus dem Zertifikat Speicher "persönlich" in der Registrierung unter **HKEY \_ local \_ Machine** ausgewählt. Da dieses Codebeispiel spezifisch für Microsoft JScript ist, das den umgekehrten Schrägstrich als Escapezeichen verwendet, sind zwei aufeinander folgende umgekehrte Schrägstriche erforderlich, um die Komponenten der Zertifikat Zeichenfolge zu begrenzen.


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
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwinhttprequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[SSL in WinHTTP](ssl-in-winhttp.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

 




