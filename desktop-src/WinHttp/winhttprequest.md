---
Description: Dieses Thema enthält Informationen zur Verwendung des WinHTTP WinHttpRequest COM-Objekts mit Skriptsprachen.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: WinHttpRequest-Objekt
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 92fdcb9c6eff502dc5f19cb62d92af5d4db60e15890667c894f96cfb55a9e5ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132913"
---
# <a name="winhttprequest-object"></a>WinHttpRequest-Objekt

Dieses Thema enthält Informationen zur Verwendung des WinHTTP **WinHttpRequest** COM-Objekts mit Skriptsprachen. Weitere Informationen, einschließlich der C++-API (WinHTTP), finden Sie unter [Informationen zu WinHTTP.](about-winhttp.md) Einen Vergleich dieser Schnittstellen finden Sie unter [Auswählen einer WinHTTP-Schnittstelle.](choosing-a-winhttp-interface.md)

## <a name="example"></a>Beispiel

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

Codebeispiele aus der [IWinHttpRequest::Status-Eigenschaft](iwinhttprequest-status.md).



## <a name="members"></a>Member

Das **WinHttpRequest-Objekt** verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **WinHttpRequest-Objekt** verfügt über diese Ereignisse.



| Ereignis                                                                            | Beschreibung                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Tritt auf, wenn in der Anwendung ein Laufzeitfehler auftritt.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Tritt ein, wenn Daten aus der Antwort verfügbar sind.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Tritt ein, wenn die Antwortdaten abgeschlossen sind.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Tritt ein, wenn die Antwortdaten empfangen werden.<br/>      |



 

### <a name="methods"></a>Methoden

Das **WinHttpRequest-Objekt** verfügt über diese Methoden.



| Methode                                                                 | Beschreibung                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbrechen**](iwinhttprequest-abort.md)                                 | Bricht eine [WinHTTP](about-winhttp.md) [**Send-Methode**](iwinhttprequest-send.md) ab.<br/>                                                              |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Ruft alle HTTP-Antwortheader ab.<br/>                                                                                                            |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Ruft die HTTP-Antwortheader ab.<br/>                                                                                                            |
| [**Öffnen**](iwinhttprequest-open.md)                                   | Öffnet eine HTTP-Verbindung mit einer HTTP-Ressource.<br/>                                                                                                   |
| [**Senden**](iwinhttprequest-send.md)                                   | Sendet eine HTTP-Anforderung an einen HTTP-Server.<br/>                                                                                                        |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Legt die aktuelle Richtlinie für die [automatische Anmeldung fest.](authentication-in-winhttp.md)<br/>                                                |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Wählt ein Clientzertifikat aus, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.<br/>                                                    |
| [**Setcredentials**](iwinhttprequest-setcredentials.md)               | Legt die Anmeldeinformationen fest, die mit einem HTTP-Server verwendet werden sollen, entweder ein Ursprung oder ein Proxyserver.<br/>                                                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Legt Proxyserverinformationen fest.<br/>                                                                                                                  |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Fügt einen HTTP-Anforderungsheader hinzu, ändert oder löscht diesen.<br/>                                                                                               |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | Gibt die einzelnen Time out-Komponenten eines Sende-/Empfangsvorgangs in Millisekunden an.<br/>                                                     |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Gibt die Wartezeit in Sekunden für den Abschluss einer asynchronen [**Send-Methode**](iwinhttprequest-send.md) mit einem optionalen Time out-Wert an.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **WinHttpRequest-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | Beschreibung                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [**Option**](iwinhttprequest-option.md)<br/>                 | Lesen/Schreiben<br/> | Legt einen WinHTTP-Optionswert fest oder ruft einen Wert ab.<br/>                            |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Schreibgeschützt<br/>  | Ruft den Antwortentitätstext als Array von Bytes ohne Vorzeichen ab.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Schreibgeschützt<br/>  | Ruft den Antwortentitätstext als [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)ab.<br/> |
| [**Responsetext**](iwinhttprequest-responsetext.md)<br/>     | Schreibgeschützt<br/>  | Ruft den Antwortentitätstext als Text ab.<br/>                          |
| [**Status**](iwinhttprequest-status.md)<br/>                 | Schreibgeschützt<br/>  | Ruft den HTTP-Statuscode aus der letzten Antwort ab.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Schreibgeschützt<br/>  | Ruft HTTP-Statustext ab.<br/>                                          |



 

## <a name="remarks"></a>Hinweise

Das **WinHttpRequest-Objekt** verwendet die [**IErrorInfo-Schnittstelle,**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) um Fehlerdaten bereitzustellen. Eine Beschreibung und ein numerischer Fehlerwert können mit dem [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) in Microsoft Visual Basic Scripting Edition (VBScript) und dem [Error-Objekt](https://msdn.microsoft.com/library/dww52sbt.aspx) in Microsoft JScript abgerufen werden. Die unteren 16 Bits einer Fehlernummer entsprechen den Werten in [**Fehlermeldungen.**](error-messages.md)

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie unter [Laufzeitanforderungen.](winhttp-start-page.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>         |
| Verteilbare Komponente<br/>          | WinHTTP 5.0 und Internet Explorer 5.01 oder höher auf Windows XP und Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

