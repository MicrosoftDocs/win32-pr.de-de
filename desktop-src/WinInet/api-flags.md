---
title: API-Flags (WinInet. h)
description: Viele der WinInet-Funktionen akzeptieren ein Array von Flags als Parameter. Im folgenden finden Sie eine kurze Beschreibung der definierten Flags.
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339347"
---
# <a name="api-flags"></a>API-Flags

Viele der WinInet-Funktionen akzeptieren ein Array von Flags als Parameter. Im folgenden finden Sie eine kurze Beschreibung der definierten Flags.

<dl> <dt>

<span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**Internet \_ Cookie \_ \_ P3P auswerten**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Gibt an, dass eine Plattform für den P3P-Header (Privacy Protection) einem Cookie zugeordnet werden soll.


</dt> </dl> </dd> <dt>

<span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**Internet \_ Cookie, \_ Dritt \_ Anbieter**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Gibt an, dass ein Drittanbieter Cookie festgelegt oder abgerufen wird.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**Internet \_ Kennzeichen \_ Async**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Macht nur asynchrone Anforderungen an Handles, die von dem von dieser Funktion zurückgegebenen handle abgeleitet werden. Nur die [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion verwendet dieses Flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**Internet- \_ Flag- \_ Cache \_ Async**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Ermöglicht einen verzögerten Cache Schreibvorgang.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**Internet- \_ Flag- \_ Cache, \_ Wenn \_ net \_ fehlschlägt**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Gibt die Ressource aus dem Cache zurück, wenn die Netzwerk Anforderung für die Ressource aufgrund eines [Fehlers \_ beim \_ \_ Zurücksetzen der Internetverbindung](wininet-errors.md) oder des Fehlers " [ \_ Internet \_ kann nicht \_ verbunden](wininet-errors.md) werden" fehlschlägt. Dieses Flag wird von [**httpoperrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**internetflag nicht zwischen \_ \_ \_ Speichern**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Fügt die zurückgegebene Entität nicht dem Cache hinzu. Dies ist identisch mit dem bevorzugten Wert, [Internet \_ Flag \_ kein \_ Cache \_ Schreibvorgang](/windows).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**\_vorhandenes Internet Flag " \_ \_ Connect"**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Versucht, ein vorhandenes [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Objekt zu verwenden, wenn es mit denselben Attributen vorhanden ist, die für die Anforderung erforderlich sind. Dies ist nur bei FTP-Vorgängen nützlich, da FTP das einzige Protokoll ist, das in der Regel mehrere Vorgänge während der gleichen Sitzung ausführt. WinInet speichert ein einzelnes Verbindungs Handle für jedes [**hinternethandle**](appendix-a-hinternet-handles.md) zwischen, das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)generiert wurde. Die Funktionen [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und **InternetConnect** verwenden dieses Flag für http-und FTP-Verbindungen.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**Internet \_ Flag \_ zum \_ Senden von Formularen**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Gibt an, dass dies eine Formular Übermittlung ist.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**Internet \_ Kennzeichen \_ aus dem \_ Cache**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Keine Netzwerk Anforderungen. Alle Entitäten werden aus dem Cache zurückgegeben. Wenn sich das angeforderte Element nicht im Cache befindet, wird ein geeigneter Fehler (z \_ . b. Fehler Datei \_ nicht \_ gefunden) zurückgegeben. Nur die [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion verwendet dieses Flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**Internet Kennzeichen- \_ Flag \_ \_ zurück**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Gibt an, dass die Funktion die Kopie der Ressource verwenden soll, die sich derzeit im Internet Cache befindet. Das Ablaufdatum und andere Informationen über die Ressource werden nicht geprüft. Wenn das angeforderte Element nicht im Internet Cache gefunden wird, versucht das System, die Ressource im Netzwerk zu finden. Dieser Wert wurde in Microsoft Internet Explorer 5 eingeführt und ist den vorwärts-und **rückwärts** -Schaltflächen **Vorgängen** von Internet Explorer zugeordnet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**Hyperlink zum Internet Kennzeichen \_ \_**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Erzwingt ein erneutes Laden, wenn keine Ablaufzeit und keine LastModified-Zeit vom Server zurückgegeben wird, wenn bestimmt wird, ob das Element aus dem Netzwerk neu geladen werden soll. Dieses Flag kann von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet werden.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von " [**gopherfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) " und " [**gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)" verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**Internet \_ Kennzeichen \_ Ignorieren von \_ Zertifikat \_ CN \_ ungültig**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Deaktiviert die Überprüfung von SSL/PCT-basierten Zertifikaten, die vom Server zurückgegeben werden, mit dem in der Anforderung angegebenen Hostnamen. WinInet verwendet eine einfache Überprüfung auf Zertifikate, indem Sie übereinstimmende Hostnamen und einfache Platzhalter Regeln vergleicht. Dieses Flag kann von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**Internet Kennzeichen " \_ \_ Zertifikat ignorieren" \_ \_ \_ ungültig**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Deaktiviert die Überprüfung von SSL-/PCT-basierten Zertifikaten auf ordnungsgemäße Gültigkeits Daten. Dieses Flag kann von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**Internet- \_ Flag " \_ \_ Umleitung \_ an \_ http ignorieren"**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Deaktiviert die Erkennung dieses besonderen Umleitungs Typs. Wenn dieses Flag verwendet wird, lässt WinInet transparent Umleitungen von HTTPS an HTTP-URLs zu. Dieses Flag kann von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**Internet- \_ Flag " \_ \_ Umleitung \_ an \_ https ignorieren"**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Deaktiviert die Erkennung dieses besonderen Umleitungs Typs. Wenn dieses Flag verwendet wird, lässt WinInet transparent Umleitungen von http-zu-HTTPS-URLs zu. Dieses Flag kann von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**\_internetflag \_ \_ Verbindung beibehalten**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Verwendet die Keep-Alive-Semantik (falls verfügbar) für die Verbindung. Dieses Flag wird von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet. Dieses Flag ist für Microsoft Network (MSN), NTLM und andere Arten der Authentifizierung erforderlich.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**\_internetflag \_ \_ dauerhaft machen**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Wird nicht mehr unterstützt.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**Internet \_ Kennzeichen \_ muss \_ Anforderung Zwischenspeichern \_**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Identisch mit dem bevorzugten Wert, **Internet \_ Flag \_ benötigt \_ Datei**. Bewirkt, dass eine temporäre Datei erstellt wird, wenn die Datei nicht zwischengespeichert werden kann. Dieses Flag kann von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet werden.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von " [**gopherfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) " und " [**gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)" verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**Internet- \_ Flag \_ benötigt \_ Datei**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Bewirkt, dass eine temporäre Datei erstellt wird, wenn die Datei nicht zwischengespeichert werden kann. Dieses Flag kann von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet werden.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von " [**gopherfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) " und " [**gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)" verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**Internet \_ Flag \_ nicht \_ Authentifizierung.**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Versucht nicht, automatisch eine Authentifizierung durchführen. Dieses Flag kann von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**Internet \_ Flag \_ keine \_ automatische \_ Umleitung**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Führt keine automatische Umleitung in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)aus. Dieses Flag kann auch von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) für HTTP-Anforderungen verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**Internet \_ Kennzeichen \_ ohne \_ Cache \_ Schreibvorgang**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Fügt die zurückgegebene Entität nicht dem Cache hinzu. Dieses Flag wird von, [**httpopaufrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von " [**gopherfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) " und " [**gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)" verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**Internet \_ Flag \_ No \_ Cookies**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Fügt nicht automatisch Cookieheader zu Anforderungen hinzu und fügt der cookiedatenbank automatisch zurückgegebene Cookies hinzu. Dieses Flag kann von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**Internet \_ Flag \_ keine \_ Benutzeroberfläche**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Deaktiviert das Cookie-Dialogfeld. Dieses Flag kann von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet werden (nur HTTP-Anforderungen).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**Internet- \_ Flag \_ Offline**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Identisch mit **dem \_ internetflag \_ aus dem \_ Cache**. Keine Netzwerk Anforderungen. Alle Entitäten werden aus dem Cache zurückgegeben. Wenn sich das angeforderte Element nicht im Cache befindet, wird ein geeigneter Fehler (z \_ . b. Fehler Datei \_ nicht \_ gefunden) zurückgegeben. Nur die [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion verwendet dieses Flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**\_internetflag \_ passiv**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Verwendet passive FTP-Semantik. Dieses Flag wird nur von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet dieses Flag für FTP-Anforderungen, und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet dieses Flag für FTP-Dateien und-Verzeichnisse.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**Internet \_ Flag \_ pragma \_ NoCache**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Erzwingt, dass die Anforderung vom Ursprungsserver aufgelöst wird, auch wenn eine zwischengespeicherte Kopie auf dem Proxy vorhanden ist. Die Funktion " [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) " (nur bei http-und HTTPS-Anforderungen) und die Funktion " [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) " verwenden dieses Flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**\_internetflag \_ für \_ Rohdaten**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Gibt die Daten beim Abrufen von FTP-Verzeichnisinformationen als [**Win32- \_ \_ Datenstruktur suchen**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) zurück. Wenn dieses Flag nicht angegeben ist oder der-Aufrufe über einen CERN-Proxy erfolgt, gibt [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) die HTML-Version des Verzeichnisses zurück. Nur die [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) -Funktion verwendet dieses Flag.

**Windows XP und Windows Server 2003 R2 und früher:** Gibt beim Abrufen von Gopher-Verzeichnisinformationen auch eine [**Gopher \_ Find \_ Data**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) -Struktur zurück.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**Internet \_ Kennzeichen \_ Lese \_ Vorabruf**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Dieses Flag ist zurzeit deaktiviert.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**Internet Kennzeichen erneut \_ \_ Laden**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Erzwingt einen Download der angeforderten Datei, des angeforderten Objekts oder der angeforderten Verzeichnisliste vom ursprünglichen Server, nicht aus dem Cache. Dieses Flag wird von den Funktionen [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von " [**gopherfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) " und " [**gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)" verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_Zone mit \_ eingeschränkten Internet Kennzeichen \_**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Gibt an, dass das festgelegte Cookie einer nicht vertrauenswürdigen Site zugeordnet ist.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**Internet- \_ Flag \_ erneut synchronisieren**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Lädt http-Ressourcen erneut, wenn die Ressource seit dem letzten herunterladen geändert wurde. Alle FTP-Ressourcen werden erneut geladen. Dieses Flag kann von [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet werden.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von [**gopherfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) und [**gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)verwendet, und Gopher-Ressourcen werden erneut geladen.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**Internet \_ Kennzeichen \_ sicher**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



Verwendung eine sichere Transaktionssemantik. Dies bedeutet, dass Secure Sockets Layer/private Communications Technology (SSL/PCT) verwendet wird und nur in HTTP-Anforderungen sinnvoll ist. Dieses Flag wird von [**httpopzurequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet. Dies ist jedoch redundant, wenn https://in der URL angezeigt wird. Die [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion verwendet dieses Flag für http-Verbindungen. Alle Anforderungs Handles, die unter dieser Verbindung erstellt werden, erben dieses Flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**Internet \_ Flag \_ Transfer \_ ASCII**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Überträgt die Datei als ASCII (nur FTP). Dieses Flag kann von [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)und [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**Internet- \_ Flag- \_ Übertragungs \_ Binärdatei**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Überträgt die Datei als Binärdatei (nur FTP). Dieses Flag kann von [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**ftpgetfile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)und [**ftpputfile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**Internet \_ kein \_ Rückruf**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Gibt an, dass für diese API keine Rückrufe erstellt werden sollen. Dies wird für den *dxcontext* -Parameter der Funktionen verwendet, die asynchrone Vorgänge zulassen.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**Internet \_ Option \_ Server Authentifizierung unterdrücken \_ \_**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Legt ein HTTP-Anforderungs Objekt so fest, dass es sich nicht bei Ursprungs Servern anmelden, sondern die automatische Anmeldung bei http-Proxy Servern ausführt. Diese Option unterscheidet sich vom anwendungsflag Internet \_ Flag \_ No \_ auth, das die Authentifizierung bei Proxy Servern und Ursprungs Servern verhindert. Wenn Sie diesen Modus festlegen, wird bei der Kommunikation mit einem Ursprungsserver die Verwendung von Anmelde Informationsmaterial (entweder zuvor bereitgestellter Benutzername/Kennwort oder Client-SSL-Zertifikat) unterdrückt. Wenn die Anforderung jedoch über einen authentifizier enden Proxy übertragen werden muss, führt WinInet weiterhin eine automatische Authentifizierung für den HTTP-Proxy Gemäß den Intranet-Zonen Einstellungen für den Benutzer aus. Die Standardeinstellung für die Intranetzone besteht darin, die automatische Anmeldung mithilfe der Standard Anmelde Informationen des Benutzers zuzulassen. Um die Unterdrückung aller identifizierenden Informationen sicherzustellen, sollte der Aufrufer die Internet \_ Option Server Authentifizierung unter \_ drücken \_ \_ mit dem Anforderungs Kennzeichen Internet \_ Flag \_ No \_ Cookies kombinieren. Diese Option kann nur für Anforderungs Objekte festgelegt werden, bevor Sie gesendet wurden. Wenn versucht wird, diese Option festzulegen, nachdem die Anforderung gesendet wurde, wird der Fehler " \_ Internet \_ fehlerhafter Handle" zurückgegeben \_ \_ . Für diese Option ist kein Puffer erforderlich. Diese wird von InternetSetOption bei Handles verwendet, die nur von httpopanrequest zurückgegeben werden. Version: erfordert Internet Explorer 8,0 oder höher.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**WinInet- \_ API- \_ Flag " \_ Async"**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Erzwingt asynchrone Vorgänge.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**Synchronisierung der WinInet- \_ API \_ \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Erzwingt synchrone Vorgänge.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**WinInet- \_ API- \_ Flag verwenden des \_ \_ Kontexts**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Erzwingt, dass die API den Kontextwert verwendet, auch wenn Sie auf 0 (null) festgelegt ist.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



 

