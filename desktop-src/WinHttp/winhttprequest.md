---
Description: Dieses Thema enthält Informationen zur Verwendung des WinHTTP WinHttpRequest com-Objekts mit Skriptsprachen.
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
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364971"
---
# <a name="winhttprequest-object"></a>WinHttpRequest-Objekt

Dieses Thema enthält Informationen zur Verwendung des WinHTTP **WinHttpRequest** com-Objekts mit Skriptsprachen. Weitere Informationen, einschließlich der C++-API (WinHTTP), finden Sie unter [Informationen zu WinHTTP](about-winhttp.md). Einen Vergleich dieser Schnittstellen finden Sie unter [Auswählen einer WinHTTP-Schnittstelle](choosing-a-winhttp-interface.md) .

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

Code Beispiele, die von der [iwinhttprequest:: Status-Eigenschaft](iwinhttprequest-status.md)übernommen werden.



## <a name="members"></a>Member

Das **WinHttpRequest** -Objekt verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **WinHttpRequest** -Objekt enthält diese Ereignisse.



| Ereignis                                                                            | BESCHREIBUNG                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Tritt auf, wenn in der Anwendung ein Laufzeitfehler auftritt.<br/> |
| [**Onresponondataavailable**](iwinhttprequestevents-onresponsedataavailable.md) | Tritt auf, wenn Daten aus der Antwort verfügbar sind.<br/>          |
| [**Onresponendabgeschlossen**](iwinhttprequestevents-onresponsefinished.md)           | Tritt auf, wenn die Antwortdaten fertig sind.<br/>                |
| [**Onresponse-Start**](iwinhttprequestevents-onresponsestart.md)                 | Tritt auf, wenn die Antwortdaten empfangen werden.<br/>      |



 

### <a name="methods"></a>Methoden

Das **WinHttpRequest** -Objekt verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbruch**](iwinhttprequest-abort.md)                                 | Bricht eine [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) -Methode ab.<br/>                                                              |
| [**Getallresponcheaders**](iwinhttprequest-getallresponseheaders.md) | Ruft alle HTTP-Antwortheader ab.<br/>                                                                                                            |
| [**Getresponsheader**](iwinhttprequest-getresponseheader.md)         | Ruft die HTTP-Antwortheader ab.<br/>                                                                                                            |
| [**Eren**](iwinhttprequest-open.md)                                   | Öffnet eine HTTP-Verbindung mit einer HTTP-Ressource.<br/>                                                                                                   |
| [**Senden**](iwinhttprequest-send.md)                                   | Sendet eine HTTP-Anforderung an einen HTTP-Server.<br/>                                                                                                        |
| [**"Abtautologonpolicy"**](iwinhttprequest-setautologonpolicy.md)       | Legt die aktuelle [Richtlinie für die automatische Anmeldung](authentication-in-winhttp.md)fest.<br/>                                                |
| [**Setclientcertificate**](iwinhttprequest-setclientcertificate.md)   | Wählt ein Client Zertifikat aus, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.<br/>                                                    |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Legt Anmelde Informationen fest, die mit einem HTTP-Server entweder als Ursprung oder als Proxy Server verwendet werden sollen.<br/>                                                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Legt Proxy Server Informationen fest.<br/>                                                                                                                  |
| [**"Ltrequestheader"**](iwinhttprequest-setrequestheader.md)           | Fügt einen HTTP-Anforderungs Header hinzu, ändert oder löscht ihn.<br/>                                                                                               |
| [**Settimeouts**](iwinhttprequest-settimeouts.md)                     | Gibt die einzelnen Timeout Komponenten eines Sende-/empfangvorgangs in Millisekunden an.<br/>                                                     |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Gibt die Wartezeit (in Sekunden) für die Ausführung einer asynchronen [**Sende**](iwinhttprequest-send.md) Methode mit optionalem Timeout Wert an.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **WinHttpRequest** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [**Option**](iwinhttprequest-option.md)<br/>                 | Lesen/Schreiben<br/> | Legt einen WinHTTP-Optionswert fest oder ruft ihn ab.<br/>                            |
| [**Response Body**](iwinhttprequest-responsebody.md)<br/>     | Schreibgeschützt<br/>  | Ruft den Entitäts Text der Antwort als Array nicht signierter Bytes ab.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Schreibgeschützt<br/>  | Ruft den Entitäts Text der Antwort als [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)ab.<br/> |
| [**Response Text**](iwinhttprequest-responsetext.md)<br/>     | Schreibgeschützt<br/>  | Ruft den Text der Antwort Entität als Text ab.<br/>                          |
| [**Status**](iwinhttprequest-status.md)<br/>                 | Schreibgeschützt<br/>  | Ruft den HTTP-Statuscode von der letzten Antwort ab.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Schreibgeschützt<br/>  | Ruft den HTTP-Status Text ab.<br/>                                          |



 

## <a name="remarks"></a>Bemerkungen

Das **WinHttpRequest** -Objekt verwendet die [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) -Schnittstelle zum Bereitstellen von Fehler Daten. Eine Beschreibung und ein numerischer Fehlerwert können mit dem [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt in Microsoft Visual Basic Scripting Edition (VBScript) und dem [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) -Objekt in Microsoft JScript abgerufen werden. Die unteren 16 Bits einer Fehlernummer entsprechen den Werten, die in [**Fehlermeldungen**](error-messages.md)gefunden werden.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie unter [Lauf Zeitanforderungen](winhttp-start-page.md).

 

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

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

