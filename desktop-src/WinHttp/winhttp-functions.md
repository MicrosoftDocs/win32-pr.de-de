---
description: In diesem Thema werden die Funktionen identifiziert, die WinHTTP bereitstellt.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: WinHTTP-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e3fdd7a0e6e42dcc30a214d429744ffadc1345e8a88fcc70a35a5f7ccace95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114163"
---
# <a name="winhttp-functions"></a>WinHTTP-Funktionen

WinHTTP stellt die folgenden Funktionen bereit:

<dl> <dt>

[**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

Fügt dem HTTP-Anforderungshandle mindestens einen HTTP-Anforderungsheader hinzu.

</dd> <dt>

[**WinHttpAddRequestHeadersEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheadersex)
</dt> <dd>

Fügt einem HTTP-Anforderungshandle mindestens einen HTTP-Anforderungsheader hinzu, sodass Sie separate Namens-/Wertzeichenfolgen verwenden können.

</dd> <dt>

[**WinHttpCheckPlatform**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

Bestimmt, ob die aktuelle Plattform von WinHTTP unterstützt wird.

</dd> <dt>

[**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

Schließt ein einzelnes [HINTERNET-Handle.](hinternet-handles-in-winhttp.md)

</dd> <dt>

[**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

Gibt den ursprünglichen Zielserver einer HTTP-Anforderung an.

</dd> <dt>

[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

Trennt eine URL in ihre Komponenten, z. B. Hostname und Pfad.

</dd> <dt>

[**WinHttpCreateProxyResolver**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

Erstellt ein Handle für die Verwendung durch [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)

</dd> <dt>

[**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

Erstellt eine URL aus Komponententeilen, z. B. dem Hostnamen und dem Pfad.

</dd> <dt>

[**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

Sucht die URL für die PAC-Datei (Proxy Auto-Configuration). Diese Funktion meldet die URL der PAC-Datei, lädt die Datei jedoch nicht herunter.

</dd> <dt>

[**WinHttpFreeProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

Gibt die Daten frei, die aus einem vorherigen Aufruf von [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)abgerufen wurden.

</dd> <dt>

[**WinHttpFreeQueryConnectionGroupResult**](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

Gibt den durch einen vorherigen Aufruf von [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)belegten Arbeitsspeicher frei.

</dd> <dt>

[**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

Ruft die WinHTTP-Standardproxykonfiguration aus der Registrierung ab.

</dd> <dt>

[**WinHTTPGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

Ruft die Proxykonfiguration für Internet Explorer (IE) für den aktuellen Benutzer ab.

</dd> <dt>

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

Ruft die Proxyinformationen für die angegebene URL ab.

</dd> <dt>

[**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

Ruft die Proxyinformationen für die angegebene URL ab.

</dd> <dt>

[**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

Ruft die Ergebnisse eines Aufrufs von [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)ab.

</dd> <dt>

[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

Initialisiert die Verwendung der WinHTTP-Funktionen durch eine Anwendung.

</dd> <dt>

[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

Erstellt ein HTTP-Anforderungshandle.

</dd> <dt>

[**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

Gibt die Autorisierungsschemas zurück, die der Server unterstützt.

</dd> <dt>

[**WinHttpQueryConnectionGroup**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

Ruft eine Beschreibung des aktuellen Status der WinHttp-Verbindungen ab.

</dd> <dt>

[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

Gibt die Anzahl der Datenbytes zurück, die sofort zum Lesen mit [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)verfügbar sind.

</dd> <dt>

[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

Ruft Headerinformationen ab, die einer HTTP-Anforderung zugeordnet sind.

</dd> <dt>

[**WinHttpQueryHeadersEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheadersex)
</dt> <dd>

Ruft Headerinformationen ab, die einer HTTP-Anforderung zugeordnet sind. bietet eine Möglichkeit, analysierte Headernamen und Wertzeichenfolgen abzurufen.

</dd> <dt>

[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

Fragt eine Internetoption für das angegebene Handle ab.

</dd> <dt>

[**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

Liest Daten aus einem Handle, das von der [**WinHttpOpenRequest-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) geöffnet wird.

</dd> <dt>

[**WinHttpReadDataEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddataex)
</dt> <dd>

Liest Daten aus einem Handle, das von der [**WinHttpOpenRequest-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) geöffnet wird.

</dd> <dt>

[**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

Beendet eine HTTP-Anforderung, die von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)initiiert wird.

</dd> <dt>

[**WinHttpResetAutoProxy**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

Setzt den automatischen Proxy zurück.

</dd> <dt>

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

Sendet die angegebene Anforderung an den HTTP-Server.

</dd> <dt>

[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

Übergibt die erforderlichen Autorisierungsanmeldeinformationen an den Server.

</dd> <dt>

[**WinHttpSetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

Legt die WinHTTP-Standardproxykonfiguration in der Registrierung fest.

</dd> <dt>

[**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

Legt eine Internetoption fest.

</dd> <dt>

[**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

Richtet eine Rückruffunktion ein, die WinHTTP aufrufen kann, wenn der Fortschritt während eines Vorgangs erfolgt.

</dd> <dt>

[**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

Legt die verschiedenen Time outs fest, die an HTTP-Transaktionen beteiligt sind.

</dd> <dt>

[**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

Formatiert ein Datum und eine Uhrzeit gemäß der HTTP-Version 1.0-Spezifikation.

</dd> <dt>

[**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

Verwendet eine HTTP-Zeit-/Datumszeichenfolge und konvertiert sie in eine [**SYSTEMTIME-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> <dt>

[**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

Schreibt Anforderungsdaten auf einen HTTP-Server.

</dd> <dt>

[**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

Schließt eine WebSocket-Verbindung.

</dd> <dt>

[**WinHttpWebSocketCompleteUpgrade**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

Schließt einen Von [**WinHttpSendRequest gestarteten**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)WebSocket-Handshake ab.

</dd> <dt>

[**WinHttpWebSocketQueryCloseStatus**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

Ruft den von einem Server gesendeten Schließstatus ab.

</dd> <dt>

[**WinHttpWebSocketReceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

Empfängt Daten von einer WebSocket-Verbindung.

</dd> <dt>

[**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

Sendet Daten über eine WebSocket-Verbindung.

</dd> <dt>

[**WinHttpWebSocketShutdown**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

Sendet einen schließenden Frame an eine WebSocket-Verbindung.

</dd> </dl>


