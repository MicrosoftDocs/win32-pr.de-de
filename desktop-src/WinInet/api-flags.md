---
title: API-Flags (Wininet.h)
description: Viele winINet-Funktionen akzeptieren ein Array von Flags als Parameter. Im Folgenden werden die definierten Flags kurz beschrieben.
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
ms.openlocfilehash: 761677a7110e5291171b39618d4315052ea1f86fd95361ce4f51f174b130a012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386540"
---
# <a name="api-flags"></a>API-Flags

Viele winINet-Funktionen akzeptieren ein Array von Flags als Parameter. Im Folgenden werden die definierten Flags kurz beschrieben.

<dl> <dt>

<span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**\_ \_ INTERNETCOOKIE EVALUATE \_ P3P**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Gibt an, dass ein P3P-Header (Platform for Privacy Protection) einem Cookie zugeordnet werden soll.


</dt> </dl> </dd> <dt>

<span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**\_ \_ \_ INTERNETCOOKIE-DRITTANBIETER**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Gibt an, dass ein Drittanbietercookie festgelegt oder abgerufen wird.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**INTERNET \_ FLAG \_ ASYNC**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Führt nur asynchrone Anforderungen für Handles aus, die von dem von dieser Funktion zurückgegebenen Handle abgeleitet sind. Nur die [**InternetOpen-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopena) verwendet dieses Flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**INTERNET \_ FLAG \_ CACHE \_ ASYNC**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Ermöglicht einen verzögerten Cacheschreibvorgang.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**\_INTERNETFLAGCACHE \_ BEI \_ \_ \_ NET-FEHLER**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Gibt die Ressource aus dem Cache zurück, wenn die Netzwerkanforderung für die Ressource aufgrund eines FEHLERS BEI [ \_ DER \_ \_ ZURÜCKSETZUNG](wininet-errors.md) DER INTERNETVERBINDUNG oder eines [FEHLERS INTERNET CANNOT \_ \_ \_ CONNECT](wininet-errors.md) fehlschlägt. Dieses Flag wird von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**\_INTERNETFLAG \_ DONT \_ CACHE**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Fügt die zurückgegebene Entität nicht dem Cache hinzu. Dies ist identisch mit dem bevorzugten Wert INTERNET [ \_ FLAG NO CACHE \_ \_ \_ WRITE](/windows).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**\_INTERNETFLAG \_ : VORHANDENE \_ VERBINDUNG**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Versucht, ein vorhandenes [**InternetConnect-Objekt**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) zu verwenden, wenn eines mit den attributen vorhanden ist, die für die Anforderung erforderlich sind. Dies ist nur bei FTP-Vorgängen nützlich, da FTP das einzige Protokoll ist, das in der Regel mehrere Vorgänge während derselben Sitzung ausführt. WinINet speichert ein einzelnes Verbindungshandle für jedes [**HINTERNET-Handle**](appendix-a-hinternet-handles.md) zwischen, das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)generiert wird. Die Funktionen [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und **InternetConnect** verwenden dieses Flag für HTTP- und FTP-Verbindungen.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_ \_ INTERNETFLAGFORMULARE \_ ÜBERMITTELN**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Gibt an, dass es sich um eine Formularübermittlung handelt.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_INTERNETFLAG \_ AUS \_ CACHE**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Stellt keine Netzwerkanforderungen. Alle Entitäten werden aus dem Cache zurückgegeben. Wenn sich das angeforderte Element nicht im Cache befindet, wird ein geeigneter Fehler zurückgegeben, z. B. ERROR \_ FILE \_ NOT \_ FOUND. Nur die [**InternetOpen-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopena) verwendet dieses Flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**\_ \_ INTERNETFLAG FWD \_ BACK**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Gibt an, dass die Funktion die Kopie der Ressource verwenden soll, die sich derzeit im Internetcache befindet. Das Ablaufdatum und andere Informationen zur Ressource werden nicht überprüft. Wenn das angeforderte Element nicht im Internetcache gefunden wird, versucht das System, die Ressource im Netzwerk zu finden. Dieser Wert wurde in Microsoft Internet Explorer 5 eingeführt und ist **den** Vorwärts- und Zurück-Schaltflächenvorgängen von Internet Explorer zugeordnet. 


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**\_ \_ INTERNETFLAGLINK**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Erzwingt ein erneutes Laden, wenn keine Expires-Zeit und keine LastModified-Zeit vom Server zurückgegeben wird, wenn bestimmt wird, ob das Element erneut aus dem Netzwerk geladen werden soll. Dieses Flag kann von [**FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet werden.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) und [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**\_INTERNETFLAG \_ IGNORE \_ CERT \_ CN \_ INVALID**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Deaktiviert die Überprüfung von SSL-/PCT-basierten Zertifikaten, die vom Server anhand des in der Anforderung angegebenen Hostnamens zurückgegeben werden. WinINet verwendet eine einfache Überprüfung von Zertifikaten, indem auf übereinstimmende Hostnamen und einfache Platzhalterregeln verglichen wird. Dieses Flag kann von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**\_INTERNETFLAG \_ IGNORE \_ CERT DATE \_ \_ INVALID**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Deaktiviert die Überprüfung von SSL-/PCT-basierten Zertifikaten auf ordnungsgemäße Gültigkeitsdauern. Dieses Flag kann von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**\_INTERNETFLAG IGNORE REDIRECT TO HTTP \_ \_ (UMLEITUNG ZU \_ HTTP IGNORIEREN) \_**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Deaktiviert die Erkennung dieses speziellen Umleitungstyps. Wenn dieses Flag verwendet wird, lässt WinINet Umleitungen von HTTPS zu HTTP-URLs transparent zu. Dieses Flag kann von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**\_INTERNETFLAG IGNORE REDIRECT TO HTTPS \_ \_ (UMLEITUNG ZU \_ HTTPS IGNORIEREN) \_**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Deaktiviert die Erkennung dieses speziellen Umleitungstyps. Wenn dieses Flag verwendet wird, lässt WinINet Umleitungen von HTTP zu HTTPS-URLs transparent zu. Dieses Flag kann von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**\_INTERNETFLAG \_ " VERBINDUNG \_ BEIBEHALTEN"**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Verwendet die Keep-Alive-Semantik für die Verbindung, sofern verfügbar. Dieses Flag wird von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet. Dieses Flag ist für Microsoft Network (MSN), NTLM und andere Authentifizierungstypen erforderlich.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**\_INTERNETFLAG \_ MAKE \_ PERSISTENT**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Wird nicht mehr unterstützt.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**\_INTERNETFLAG \_ MUSS ANFORDERUNG \_ \_ ZWISCHENSPEICHERN**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Identisch mit dem bevorzugten Wert, **INTERNET \_ FLAG NEED \_ \_ FILE**. Bewirkt, dass eine temporäre Datei erstellt wird, wenn die Datei nicht zwischengespeichert werden kann. Dieses Flag kann von [**FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet werden.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) und [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**\_INTERNETFLAG: \_ DATEI ERFORDERLICH \_**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Bewirkt, dass eine temporäre Datei erstellt wird, wenn die Datei nicht zwischengespeichert werden kann. Dieses Flag kann von [**FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet werden.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) und [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**\_INTERNETFLAG \_ KEINE \_ AUTHENTIFIZIERUNG**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Versucht die Authentifizierung nicht automatisch. Dieses Flag kann von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**\_INTERNETFLAG \_ KEINE AUTOMATISCHE \_ \_ UMLEITUNG**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Verarbeitet die Umleitung in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)nicht automatisch. Dieses Flag kann auch von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) für HTTP-Anforderungen verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**\_INTERNETFLAG \_ KEIN \_ \_ CACHESCHREIBVORGANG**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Fügt die zurückgegebene Entität nicht dem Cache hinzu. Dieses Flag wird von , [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) und [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**\_INTERNETFLAG \_ KEINE \_ COOKIES**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Fügt Den Anforderungen nicht automatisch Cookieheader hinzu, und der Cookiedatenbank werden nicht automatisch zurückgegebene Cookies hinzugefügt. Dieses Flag kann von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (für HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**\_INTERNETFLAG \_ KEINE \_ BENUTZEROBERFLÄCHE**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Deaktiviert das Dialogfeld "Cookie". Dieses Flag kann von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (nur HTTP-Anforderungen) verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**\_INTERNETFLAG \_ OFFLINE**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Identisch mit **INTERNET \_ FLAG FROM \_ \_ CACHE**. Stellt keine Netzwerkanforderungen. Alle Entitäten werden aus dem Cache zurückgegeben. Wenn sich das angeforderte Element nicht im Cache befindet, wird ein geeigneter Fehler zurückgegeben, z. B. ERROR \_ FILE \_ NOT \_ FOUND. Nur die [**InternetOpen-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopena) verwendet dieses Flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**\_INTERNETFLAG \_ PASSIV**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Verwendet passive FTP-Semantik. Nur [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwenden dieses Flag. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet dieses Flag für FTP-Anforderungen, und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet dieses Flag für FTP-Dateien und -Verzeichnisse.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**\_INTERNETFLAG \_ PRAGMA \_ NOCACHE**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Erzwingt, dass die Anforderung vom Ursprungsserver aufgelöst wird, auch wenn eine zwischengespeicherte Kopie auf dem Proxy vorhanden ist. Die [**Funktion InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (nur bei HTTP- und HTTPS-Anforderungen) und [**die HttpOpenRequest-Funktion**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) verwenden dieses Flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**\_INTERNETFLAG- \_ \_ ROHDATEN**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Gibt die Daten beim Abrufen von FTP-Verzeichnisinformationen als [**WIN32 \_ FIND \_ DATA-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) zurück. Wenn dieses Flag nicht angegeben ist oder der Aufruf über einen CERN-Proxy erfolgt, gibt [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) die HTML-Version des Verzeichnisses zurück. Nur die [**InternetOpenUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet dieses Flag.

**Windows XP und Windows Server 2003 R2 und früher:** Gibt auch eine [**GOPHER \_ FIND \_ DATA-Struktur**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) zurück, wenn Gopher-Verzeichnisinformationen abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**\_INTERNETFLAG \_ READ \_ PREFETCH**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Dieses Flag ist derzeit deaktiviert.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**ERNEUTES \_ LADEN DES INTERNETFLAGS \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Erzwingt einen Download der angeforderten Datei, des angeforderten Objekts oder der angeforderten Verzeichnisliste vom ursprünglichen Server, nicht aus dem Cache. Die Funktionen [**FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwenden dieses Flag.

**Windows XP und Windows Server 2003 R2 und früher:** Wird auch von [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) und [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)verwendet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_ \_ EINGESCHRÄNKTE ZONE MIT INTERNETFLAG \_**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Gibt an, dass das festgelegte Cookie einer nicht vertrauenswürdigen Website zugeordnet ist.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**\_INTERNETFLAG \_ NEU SYNCHRONISIEREN**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Lädt HTTP-Ressourcen erneut, wenn die Ressource seit dem letzten Herunterladen geändert wurde. Alle FTP-Ressourcen werden neu geladen. Dieses Flag kann von [**FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet werden.

**Windows XP und Windows Server 2003 R2 und früher:** Auch von [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) und [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)verwendet, und Gopher-Ressourcen werden neu geladen.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**\_INTERNETFLAG \_ SICHER**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



Verwendung eine sichere Transaktionssemantik. Dies bedeutet die Verwendung Secure Sockets Layer/Private Communications Technology (SSL/PCT) und ist nur in HTTP-Anforderungen sinnvoll. Dieses Flag wird von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) und [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet. Dies ist jedoch redundant, wenn https:// in der URL angezeigt wird. Die [**InternetConnect-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet dieses Flag für HTTP-Verbindungen. alle Anforderungshandles, die unter dieser Verbindung erstellt wurden, erben dieses Flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**\_INTERNETFLAGÜBERTRAGUNG \_ \_ ASCII**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Überträgt die Datei als ASCII (nur FTP). Dieses Flag kann von [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)und [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_ \_ \_ INTERNETFLAGÜBERTRAGUNGSBINÄRDATEI**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Überträgt die Datei als Binärdatei (nur FTP). Dieses Flag kann von [**FtpOpenFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)und [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)verwendet werden.


</dt> </dl> </dd> <dt>

<span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET \_ OHNE \_ RÜCKRUF**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Gibt an, dass für diese API keine Rückrufe erfolgen sollen. Dies wird für den *dxContext-Parameter* der Funktionen verwendet, die asynchrone Vorgänge zulassen.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNETOPTION UNTERDRÜCKEN DER \_ \_ \_ \_ SERVERAUTHENTIFIZIERUNG**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Legt ein HTTP-Anforderungsobjekt so fest, dass es sich nicht bei Ursprungsservern anmeldet, sondern automatisch bei HTTP-Proxyservern anmeldet. Diese Option unterscheidet sich vom Anforderungsflag INTERNET \_ FLAG \_ NO \_ AUTH, das die Authentifizierung bei Proxyservern und Ursprungsservern verhindert. Wenn Sie diesen Modus festlegen, wird die Verwendung von Anmeldeinformationen (entweder zuvor bereitgestellter Benutzername/Kennwort oder CLIENT-SSL-Zertifikat) bei der Kommunikation mit einem Ursprungsserver unterdrückt. Wenn die Anforderung jedoch über einen Authentifizierungsproxy übertragen werden muss, führt WinINet weiterhin die automatische Authentifizierung beim HTTP-Proxy gemäß den Intranetzoneneinstellungen für den Benutzer durch. Die Standardeinstellung Intranetzone ist das Zulassen der automatischen Anmeldung mit den Standardanmeldeinformationen des Benutzers. Um die Unterdrückung aller identifizierenden Informationen sicherzustellen, sollte der Aufrufer INTERNET \_ OPTION \_ SUPPRESS SERVER \_ \_ AUTH mit dem \_ \_ Anforderungsflag INTERNET FLAG NO \_ COOKIES kombinieren. Diese Option kann nur für Anforderungsobjekte festgelegt werden, bevor sie gesendet wurden. Wenn versucht wird, diese Option festzulegen, nachdem die Anforderung gesendet wurde, wird ERROR \_ INTERNET INCORRECT HANDLE STATE \_ \_ \_ zurückgegeben. Für diese Option ist kein Puffer erforderlich. Dies wird von InternetSetOption nur für Handles verwendet, die von HttpOpenRequest zurückgegeben werden. Version: Erfordert Internet Explorer 8.0 oder höher.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**WININET \_ API \_ FLAG \_ ASYNC**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Erzwingt asynchrone Vorgänge.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**\_ \_ WININET-API-FLAGSYNCHRONISIERUNG \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Erzwingt synchrone Vorgänge.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**VERWENDUNGSKONTEXT DES \_ WININET-API-FLAGS \_ \_ \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Erzwingt, dass die API den Kontextwert verwendet, auch wenn er auf 0 (null) festgelegt ist.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



 

