---
description: In diesem Thema werden die von WinHTTP bereitgestellten Funktionen beschrieben.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: WinHTTP-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6511d2e66acc923072cc7a961aae3cb572b8e466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347766"
---
# <a name="winhttp-functions"></a>WinHTTP-Funktionen

WinHTTP bietet die folgenden Funktionen:

<dl> <dt>

[**Winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

Fügt dem HTTP-Anforderungs handle mindestens einen HTTP-Anforderungs Header hinzu.

</dd> <dt>

[**Winhttpcheckplatform**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

Bestimmt, ob die aktuelle Plattform von WinHTTP unterstützt wird.

</dd> <dt>

[**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

Schließt ein einzelnes [HINTERNET](hinternet-handles-in-winhttp.md) -handle.

</dd> <dt>

[**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

Gibt den ursprünglichen Zielserver einer HTTP-Anforderung an.

</dd> <dt>

[**Winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

Trennt eine URL in Ihre Komponenten Teile, z. b. Hostname und Pfad.

</dd> <dt>

[**Winhttpkreateproxyresolver**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

Erstellt ein Handle für die Verwendung durch [**winhttpgetproxyforurlex**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).

</dd> <dt>

[**Winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

Erstellt eine URL aus Komponenten teilen, z. b. den Hostnamen und den Pfad.

</dd> <dt>

[**Winhttpdetectautoproxyconfigurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

Sucht die URL für die Datei mit der Proxy automatischen Konfiguration (PAC). Diese Funktion meldet die URL der PAC-Datei, aber Sie lädt die Datei nicht herunter.

</dd> <dt>

[**Winhttpfreproxyresult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

Gibt die Daten frei, die von einem vorherigen Aufrufen von " [**winhttpgetproxyresult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)" abgerufen wurden.

</dd> <dt>

[**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

Ruft die standardmäßige WinHTTP-Proxykonfiguration aus der Registrierung ab.

</dd> <dt>

[**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

Ruft die Internet Explorer-Proxykonfiguration für den aktuellen Benutzer ab.

</dd> <dt>

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

Ruft die Proxy Informationen für die angegebene URL ab.

</dd> <dt>

[**Winhttpgetproxyforurlex**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

Ruft die Proxy Informationen für die angegebene URL ab.

</dd> <dt>

[**Winhttpgetproxyresult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

Ruft die Ergebnisse eines Aufrufens von [**winhttpgetproxyforurlex**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)ab.

</dd> <dt>

[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

Initialisiert die Verwendung der WinHTTP-Funktionen einer Anwendung.

</dd> <dt>

[**Winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

Erstellt ein HTTP-Anforderungs handle.

</dd> <dt>

[**Winhttpqueryauthschemas**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

Gibt die Autorisierungs Schemas zurück, die der Server unterstützt.

</dd> <dt>

[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

Gibt die Anzahl der Daten Bytes zurück, die sofort verfügbar sind, um mit [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)gelesen zu werden.

</dd> <dt>

[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

Ruft Header Informationen ab, die einer HTTP-Anforderung zugeordnet sind.

</dd> <dt>

[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

Fragt eine Internet Option für das angegebene Handle ab.

</dd> <dt>

[**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

Liest Daten aus einem Handle, das von der [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) -Funktion geöffnet wurde.

</dd> <dt>

[**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

Beendet eine HTTP-Anforderung, die von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)initiiert wird.

</dd> <dt>

[**Winhttpre\tautoproxy**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

Setzt den automatischen Proxy zurück.

</dd> <dt>

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

Sendet die angegebene Anforderung an den HTTP-Server.

</dd> <dt>

[**Winhttpsetanmelde Informationen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

Übergibt die erforderlichen Autorisierungs Anmelde Informationen an den Server.

</dd> <dt>

[**WinHttpSetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

Legt die WinHTTP-Standard Proxykonfiguration in der Registrierung fest.

</dd> <dt>

[**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

Legt eine Internet Option fest.

</dd> <dt>

[**Winhttpsetstatus-Rückruf**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

Richtet eine Rückruffunktion ein, die von WinHTTP aufgerufen werden kann, während ein Vorgang durchgeführt wird.

</dd> <dt>

[**Winhttpsettimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

Legt die verschiedenen Timeouts fest, die an http-Transaktionen beteiligt sind.

</dd> <dt>

[**Winhttptimefromsystemtime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

Formatiert ein Datum und eine Uhrzeit gemäß der Spezifikation der HTTP-Version 1,0.

</dd> <dt>

[**Winhttptimeumsystemtime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

Nimmt eine HTTP-Zeit-/Datum-Zeichenfolge und konvertiert sie in eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur.

</dd> <dt>

[**Winhttpschreitedata**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

Schreibt Anforderungs Daten auf einen HTTP-Server.

</dd> <dt>

[**Winhttpwebsocketclose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

Schließt eine WebSocket-Verbindung.

</dd> <dt>

[**Winhttpwebsocketcompleteupgrade**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

Schließt einen WebSocket-Handshake ab, der von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)gestartet wurde.

</dd> <dt>

[**Winhttpwebsocketqueryclosestatus**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

Ruft den von einem Server gesendeten Schluss Status ab.

</dd> <dt>

[**Winhttpwebsocketreceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

Empfängt Daten von einer WebSocket-Verbindung.

</dd> <dt>

[**Winhttpwebsocketsend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

Sendet Daten über eine WebSocket-Verbindung.

</dd> <dt>

[**Winhttpwebsocketshutdown**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

Sendet einen close-Frame an eine WebSocket-Verbindung.

</dd> </dl>

 

 
