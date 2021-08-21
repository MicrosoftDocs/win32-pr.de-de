---
description: Die IWinHttpRequest-Schnittstelle stellt alle Nichtereignismethoden für Microsoft Windows HTTP Services (WinHTTP) bereit.
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: IWinHttpRequest-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 87a31ebe116726d70eb847fe54d563be57477f7133147226657c4c74135defa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114399"
---
# <a name="iwinhttprequest-interface"></a>IWinHttpRequest-Schnittstelle

Die **IWinHttpRequest-Schnittstelle** stellt alle Nichtereignismethoden für [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md)bereit.

## <a name="members"></a>Member

Die **IWinHttpRequest-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWinHttpRequest** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWinHttpRequest-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                 | Beschreibung                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbrechen**](iwinhttprequest-abort.md)                                 | Bricht eine [WinHTTP](about-winhttp.md) [**Send-Methode**](iwinhttprequest-send.md) ab.<br/>                                           |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Ruft alle HTTP-Antwortheader ab.<br/>                                                                                         |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Ruft die HTTP-Antwortheader ab.<br/>                                                                                         |
| [**Öffnen**](iwinhttprequest-open.md)                                   | Öffnet eine HTTP-Verbindung mit einer HTTP-Ressource.<br/>                                                                                |
| [**Senden**](iwinhttprequest-send.md)                                   | Sendet eine HTTP-Anforderung an einen HTTP-Server.<br/>                                                                                     |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Legt die aktuelle Richtlinie für die [automatische Anmeldung fest.](authentication-in-winhttp.md)<br/>                             |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Wählt ein Clientzertifikat aus, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.<br/>                                 |
| [**Setcredentials**](iwinhttprequest-setcredentials.md)               | Legt die Anmeldeinformationen fest, die mit einem HTTP-Server verwendet werden sollen, entweder einem Proxyserver oder einem Ursprungsserver.<br/>                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Legt Proxyserverinformationen fest.<br/>                                                                                               |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Fügt einen HTTP-Anforderungsheader hinzu, ändert oder löscht diesen.<br/>                                                                            |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | Gibt die einzelnen Time out-Komponenten eines Sende-/Empfangsvorgangs in Millisekunden an.<br/>                                   |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Wartet auf den Abschluss einer asynchronen [**Send-Methode**](iwinhttprequest-send.md) mit optionalem Time out-Wert in Sekunden.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IWinHttpRequest-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | Beschreibung                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Option**](iwinhttprequest-option.md)<br/>                 | Lesen/Schreiben<br/> | Ein WinHTTP-Optionswert.<br/>                                    |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Schreibgeschützt<br/>  | Der Antwortentitätstext als Array von Bytes ohne Vorzeichen.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Schreibgeschützt<br/>  | Der Antwortentitätstext als [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream)<br/> |
| [**Responsetext**](iwinhttprequest-responsetext.md)<br/>     | Schreibgeschützt<br/>  | Der Antwortentitätstext.<br/>                                  |
| [**Status**](iwinhttprequest-status.md)<br/>                 | Schreibgeschützt<br/>  | Der HTTP-Statuscode aus der letzten Antwort.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Schreibgeschützt<br/>  | Der HTTP-Statustext.<br/>                                      |



 

## <a name="remarks"></a>Hinweise

Die in httprequest.idl definierte **IWinHttpRequest-Schnittstelle** wird von einer Klasse mit der ID **CLSID \_ WinHttpRequest** implementiert. Eine Anwendung ruft diese Schnittstelle ab, indem [**sie CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit einer Klassen-ID von **CLSID \_ WinHttpRequest** und einer Schnittstellen-ID von **IID \_ IWinHttpRequest aufruft.**

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Laufzeitanforderungen](winhttp-start-page.md) der WinHttp-Startseite.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher auf Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

