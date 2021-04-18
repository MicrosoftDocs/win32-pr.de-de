---
description: Die iwinhttprequest-Schnittstelle stellt alle nichtereignis Methoden für Microsoft Windows HTTP-Dienste (WinHTTP) bereit.
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Iwinhttprequest-Schnittstelle
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
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216328"
---
# <a name="iwinhttprequest-interface"></a>Iwinhttprequest-Schnittstelle

Die **iwinhttprequest** -Schnittstelle stellt alle nichtereignis Methoden für [Microsoft Windows HTTP-Dienste (WinHTTP)](about-winhttp.md)bereit.

## <a name="members"></a>Member

Die **iwinhttprequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwinhttprequest** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iwinhttprequest** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbruch**](iwinhttprequest-abort.md)                                 | Bricht eine [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) -Methode ab.<br/>                                           |
| [**Getallresponcheaders**](iwinhttprequest-getallresponseheaders.md) | Ruft alle HTTP-Antwortheader ab.<br/>                                                                                         |
| [**Getresponsheader**](iwinhttprequest-getresponseheader.md)         | Ruft die HTTP-Antwortheader ab.<br/>                                                                                         |
| [**Eren**](iwinhttprequest-open.md)                                   | Öffnet eine HTTP-Verbindung mit einer HTTP-Ressource.<br/>                                                                                |
| [**Senden**](iwinhttprequest-send.md)                                   | Sendet eine HTTP-Anforderung an einen HTTP-Server.<br/>                                                                                     |
| [**"Abtautologonpolicy"**](iwinhttprequest-setautologonpolicy.md)       | Legt die aktuelle [Richtlinie für die automatische Anmeldung](authentication-in-winhttp.md)fest.<br/>                             |
| [**Setclientcertificate**](iwinhttprequest-setclientcertificate.md)   | Wählt ein Client Zertifikat aus, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.<br/>                                 |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Legt Anmelde Informationen für die Verwendung mit einem HTTP-Server fest, entweder einen Proxy Server oder einen ursprünglichen Server.<br/>                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Legt Proxy Server Informationen fest.<br/>                                                                                               |
| [**"Ltrequestheader"**](iwinhttprequest-setrequestheader.md)           | Fügt einen HTTP-Anforderungs Header hinzu, ändert oder löscht ihn.<br/>                                                                            |
| [**Settimeouts**](iwinhttprequest-settimeouts.md)                     | Gibt die einzelnen Timeout Komponenten eines Sende-/Empfangsvorgangs in Millisekunden an.<br/>                                   |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Wartet auf den Abschluss einer asynchronen [**Sende**](iwinhttprequest-send.md) Methode (mit optionalem Timeout Wert) in Sekunden.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **iwinhttprequest** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Option**](iwinhttprequest-option.md)<br/>                 | Lesen/Schreiben<br/> | Ein WinHTTP-Optionswert.<br/>                                    |
| [**Response Body**](iwinhttprequest-responsebody.md)<br/>     | Schreibgeschützt<br/>  | Der Antwort Entitäts Text als Array nicht signierter bytes.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Schreibgeschützt<br/>  | Der Antwort Entitäts Text als [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**Response Text**](iwinhttprequest-responsetext.md)<br/>     | Schreibgeschützt<br/>  | Der Antwort Entitäts Text.<br/>                                  |
| [**Status**](iwinhttprequest-status.md)<br/>                 | Schreibgeschützt<br/>  | Der HTTP-Statuscode der letzten Antwort.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Schreibgeschützt<br/>  | Der HTTP-Status Text.<br/>                                      |



 

## <a name="remarks"></a>Bemerkungen

Die in HttpRequest. idl definierte **iwinhttprequest** -Schnittstelle wird von einer Klasse mit der ID **CLSID \_ WinHttpRequest** implementiert. Eine Anwendung ruft diese Schnittstelle durch Aufrufen von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit der Klassen-ID **CLSID \_ WinHttpRequest** und der Schnittstellen-ID **\_ IID iwinhttprequest** ab.

> [!Note]  
> Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.

 

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

[**Iwinhttprequestevents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

