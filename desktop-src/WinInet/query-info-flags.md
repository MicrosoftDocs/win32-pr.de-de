---
title: Abfrageinformationsflags (Wininet.h)
description: Die folgenden Listen enthalten die Attribute und Modifizierer, die von HttpQueryInfo und QueryInfo verwendet werden.
ms.assetid: b1613193-ae03-411e-bf05-de42f471cd8c
topic_type:
- apiref
api_name:
- HTTP_QUERY_ACCEPT
- HTTP_QUERY_ACCEPT_CHARSET
- HTTP_QUERY_ACCEPT_ENCODING
- HTTP_QUERY_ACCEPT_LANGUAGE
- HTTP_QUERY_ACCEPT_RANGES
- HTTP_QUERY_AGE
- HTTP_QUERY_ALLOW
- HTTP_QUERY_AUTHORIZATION
- HTTP_QUERY_CACHE_CONTROL
- HTTP_QUERY_CONNECTION
- HTTP_QUERY_CONTENT_BASE
- HTTP_QUERY_CONTENT_DESCRIPTION
- HTTP_QUERY_CONTENT_DISPOSITION
- HTTP_QUERY_CONTENT_ENCODING
- HTTP_QUERY_CONTENT_ID
- HTTP_QUERY_CONTENT_LANGUAGE
- HTTP_QUERY_CONTENT_LENGTH
- HTTP_QUERY_CONTENT_LOCATION
- HTTP_QUERY_CONTENT_MD5
- HTTP_QUERY_CONTENT_RANGE
- HTTP_QUERY_CONTENT_TRANSFER_ENCODING
- HTTP_QUERY_CONTENT_TYPE
- HTTP_QUERY_COOKIE
- HTTP_QUERY_COST
- HTTP_QUERY_CUSTOM
- HTTP_QUERY_DATE
- HTTP_QUERY_DERIVED_FROM
- HTTP_QUERY_ECHO_HEADERS
- HTTP_QUERY_ECHO_HEADERS_CRLF
- HTTP_QUERY_ECHO_REPLY
- HTTP_QUERY_ECHO_REQUEST
- HTTP_QUERY_ETAG
- HTTP_QUERY_EXPECT
- HTTP_QUERY_EXPIRES
- HTTP_QUERY_FORWARDED
- HTTP_QUERY_FROM
- HTTP_QUERY_HOST
- HTTP_QUERY_IF_MATCH
- HTTP_QUERY_IF_MODIFIED_SINCE
- HTTP_QUERY_IF_NONE_MATCH
- HTTP_QUERY_IF_RANGE
- HTTP_QUERY_IF_UNMODIFIED_SINCE
- HTTP_QUERY_LAST_MODIFIED
- HTTP_QUERY_LINK
- HTTP_QUERY_LOCATION
- HTTP_QUERY_MAX
- HTTP_QUERY_MAX_FORWARDS
- HTTP_QUERY_MESSAGE_ID
- HTTP_QUERY_MIME_VERSION
- HTTP_QUERY_ORIG_URI
- HTTP_QUERY_PRAGMA
- HTTP_QUERY_PROXY_AUTHENTICATE
- HTTP_QUERY_PROXY_AUTHORIZATION
- HTTP_QUERY_PROXY_CONNECTION
- HTTP_QUERY_PUBLIC
- HTTP_QUERY_RANGE
- HTTP_QUERY_RAW_HEADERS
- HTTP_QUERY_RAW_HEADERS_CRLF
- HTTP_QUERY_REFERER
- HTTP_QUERY_REFRESH
- HTTP_QUERY_REQUEST_METHOD
- HTTP_QUERY_RETRY_AFTER
- HTTP_QUERY_SERVER
- HTTP_QUERY_SET_COOKIE
- HTTP_QUERY_STATUS_CODE
- HTTP_QUERY_STATUS_TEXT
- HTTP_QUERY_TITLE
- HTTP_QUERY_TRANSFER_ENCODING
- HTTP_QUERY_UNLESS_MODIFIED_SINCE
- HTTP_QUERY_UPGRADE
- HTTP_QUERY_URI
- HTTP_QUERY_USER_AGENT
- HTTP_QUERY_VARY
- HTTP_QUERY_VERSION
- HTTP_QUERY_VIA
- HTTP_QUERY_WARNING
- HTTP_QUERY_WWW_AUTHENTICATE
- HTTP_QUERY_X_CONTENT_TYPE_OPTIONS
- HTTP_QUERY_P3P
- HTTP_QUERY_X_P2P_PEERDIST
- HTTP_QUERY_TRANSLATE
- HTTP_QUERY_X_UA_COMPATIBLE
- HTTP_QUERY_DEFAULT_STYLE
- HTTP_QUERY_X_FRAME_OPTIONS
- HTTP_QUERY_X_XSS_PROTECTION
- HTTP_QUERY_FLAG_COALESCE
- HTTP_QUERY_FLAG_NUMBER
- HTTP_QUERY_FLAG_REQUEST_HEADERS
- HTTP_QUERY_FLAG_SYSTEMTIME
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb2e52a30aa10161963f215e9045db006a82fee482a67947017d20372cefbdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955550"
---
# <a name="query-info-flags-winineth"></a>Abfrageinformationsflags (Wininet.h)

Die folgenden Listen enthalten die Attribute und Modifizierer, die von [**HttpQueryInfo und**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) [**QueryInfo verwendet werden.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))

Die Attributflags werden von [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (oder [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) verwendet, um anzugeben, welche Daten abgerufen werden sollen. Die meisten Attributflags werden direkt einem bestimmten HTTP-Header zuordnen. Es gibt auch einige spezielle Flags, z. B. [HTTP \_ QUERY RAW \_ \_ HEADERS,](/windows)die nicht mit einem bestimmten Header verknüpft sind.

<dl> <dt>

<span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**HTTP \_ QUERY \_ ACCEPT**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Ruft die zulässigen Medientypen für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**HTTP \_ QUERY \_ ACCEPT \_ CHARSET**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Ruft die zulässigen Zeichensätze für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**HTTP \_ QUERY ACCEPT ENCODING (HTTP-ABFRAGE AKZEPTIERT \_ \_ CODIERUNG)**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Ruft die zulässigen Werte für die Inhaltscodierung für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP \_ QUERY \_ ACCEPT \_ LANGUAGE**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Ruft die zulässigen natürlichen Sprachen für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**AKZEPTIEREN \_ VON \_ HTTP-ABFRAGEBEREICHEN \_**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Ruft die Typen von Bereichsanforderungen ab, die für eine Ressource akzeptiert werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP \_ QUERY \_ AGE**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Ruft das Feld Age response-header ab, das die Schätzung des Absenders für die Zeit seit dem Erstellen der Antwort auf dem Ursprungsserver enthält.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP \_ QUERY \_ ALLOW**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Empfängt die vom Server unterstützten HTTP-Verben.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_ \_ HTTP-ABFRAGEAUTORISIERUNG**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Ruft die für eine Anforderung verwendeten Autorisierungsanmeldeinformationen ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_ \_ \_ HTTP-ABFRAGECACHE-STEUERELEMENT**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Ruft die Cachesteuersteuer direktiven ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**\_ \_ HTTP-ABFRAGEVERBINDUNG**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Ruft alle Optionen ab, die für eine bestimmte Verbindung angegeben sind und nicht von Proxys über weitere Verbindungen kommuniziert werden dürfen.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**\_ \_ HTTP-ABFRAGEINHALTSBASIS \_**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Ruft den Basis-URI (Uniform Resource Identifier) zum Auflösen relativer URLs innerhalb der Entität ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**BESCHREIBUNG DES \_ \_ HTTP-ABFRAGEINHALTS \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Veraltet. Wird nur aus Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**\_ \_ HTTP-ABFRAGEINHALTSDISPOSITION \_**
</dt> <dd> <dl> <dt>

47
</dt> <dt>



Veraltet. Wird nur aus Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**\_ \_ HTTP-ABFRAGEINHALTSCODIERUNG \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Ruft alle zusätzlichen Inhaltscodierungen ab, die auf die gesamte Ressource angewendet wurden.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**\_INHALTS-ID DER \_ \_ HTTP-ABFRAGE**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Ruft die Inhaltsidentifikation ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**\_ \_ HTTP-ABFRAGEINHALTSSPRACHE \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Ruft die Sprache ab, in der sich der Inhalt befindet.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**LÄNGE \_ DES \_ HTTP-ABFRAGEINHALTS \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Ruft die Größe der Ressource in Bytes ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**SPEICHERORT DES \_ \_ HTTP-ABFRAGEINHALTS \_**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Ruft den Ressourcenspeicherort für die in der Nachricht eingeschlossene Entität ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**\_HTTP-ABFRAGEINHALT \_ \_ MD5**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Ruft einen MD5-Digest des Entitätstexts ab, um eine End-to-End-Nachrichtenintegritätsprüfung (End-to-End Message Integrity Check, MIC) für den Entitätstext zu bieten. Weitere Informationen finden Sie unter RFC1864, The Content-MD5 Header Field, at [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_ \_ HTTP-ABFRAGEINHALTSBEREICH \_**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Ruft die Position im vollständigen Entitätskörper ab, an der der partielle Entitätskörper eingefügt werden soll, und die Gesamtgröße des vollständigen Entitätskörpers.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**\_ÜBERTRAGUNGSCODIERUNG \_ VON \_ HTTP-ABFRAGEINHALTEN \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Empfängt die zusätzliche Inhaltscodierung, die auf die Ressource angewendet wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_ \_ HTTP-ABFRAGEINHALTSTYP \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Empfängt den Inhaltstyp der Ressource (z. B. text/html).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_ \_ HTTP-ABFRAGECOOKIE**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Ruft alle Cookies ab, die der Anforderung zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**\_ \_ HTTP-ABFRAGEKOSTEN**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Wird nicht mehr unterstützt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**BENUTZERDEFINIERTE \_ \_ HTTP-ABFRAGE**
</dt> <dd> <dl> <dt>

65.535
</dt> <dt>



Bewirkt, [**dass HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) nach dem in *lpvBuffer* angegebenen Headernamen sucht und die Headerdaten in *lpvBuffer gespeichert.*


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**\_ \_ HTTP-ABFRAGEDATUM**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Empfängt das Datum und die Uhrzeit, zu der die Nachricht stammt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**VON \_ \_ ABGELEITETE \_ HTTP-ABFRAGE**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Wird nicht mehr unterstützt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_ \_ HTTP-ABFRAGE-ECHOHEADER \_**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP \_ QUERY \_ ECHO \_ HEADERS \_ CRLF**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP \_ QUERY \_ ECHO \_ REPLY**
</dt> <dd> <dl> <dt>

72
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**HTTP \_ QUERY \_ ECHO \_ REQUEST**
</dt> <dd> <dl> <dt>

71
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP \_ QUERY \_ ETAG**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Ruft das Entitätstag für die zugeordnete Entität ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_HTTP-ABFRAGE \_ ERWARTET**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Ruft den Expect-Header ab, der angibt, ob die Clientanwendung Antworten der Serie 100 erwarten soll.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**\_HTTP-ABFRAGE \_ LÄUFT AB**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Empfängt das Datum und die Uhrzeit, nach der die Ressource als veraltet betrachtet werden soll.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**WEITERGELEITETE \_ \_ HTTP-ABFRAGE**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Veraltet. Wird nur aus Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**\_HTTP-ABFRAGE \_ VON**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Ruft die E-Mail-Adresse für den menschlichen Benutzer ab, der den anfordernden Benutzer-Agent steuert, wenn der From-Header angegeben ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**\_ \_ HTTP-ABFRAGEHOST**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Ruft den Internethost und die Portnummer der angeforderten Ressource ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP \_ QUERY \_ IF \_ MATCH**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Ruft den Inhalt des If-Match Anforderungsheaderfelds ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**\_ \_ HTTP-ABFRAGE, WENN \_ SIE GEÄNDERT \_ WURDE, DA**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Ruft den Inhalt des If-Modified-Since-Headers ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**\_HTTP-ABFRAGE, \_ WENN KEINE \_ \_ ÜBEREINSTIMMUNG**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Ruft den Inhalt des Anforderungsheaderfelds If-None-Match ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP \_ QUERY \_ IF \_ RANGE**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Ruft den Inhalt des If-Range Anforderungsheaderfelds ab. Mit diesem Header kann die Clientanwendung überprüfen, ob die Entität im Zusammenhang mit einer Teilkopie der Entität im Clientanwendungscache nicht aktualisiert wurde. Wenn die Entität nicht aktualisiert wurde, senden Sie die Teile, in denen die Clientanwendung fehlt. Wenn die Entität aktualisiert wurde, senden Sie die gesamte aktualisierte Entität.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**\_ \_ HTTP-ABFRAGE, \_ WENN SIE NICHT GEÄNDERT \_ WURDE, DA**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Ruft den Inhalt des Anforderungsheaderfelds If-Unmodified-Since ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_HTTP-ABFRAGE \_ ZULETZT \_ GEÄNDERT**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Empfängt das Datum und die Uhrzeit, zu der der Server der Meinung ist, dass die Ressource zuletzt geändert wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**\_ \_ HTTP-ABFRAGELINK**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Veraltet. Wird nur aus Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**\_ \_ HTTP-ABFRAGESPEICHERORT**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Ruft den absoluten Uniform Resource Identifier (URI) ab, der in einem Location-Antwortheader verwendet wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**HTTP \_ QUERY \_ MAX**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



Kein Abfrageflag. Gibt den Höchstwert eines HTTP \_ QUERY-Werts \_ \* an.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**MAXIMALE \_ \_ FORWARDS FÜR \_ HTTP-ABFRAGEN**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Ruft die Anzahl der Proxys oder Gateways ab, die die Anforderung an den nächsten eingehenden Server weitergeleitet werden können.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_ \_ \_ HTTP-ABFRAGENACHRICHTEN-ID**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Wird nicht mehr unterstützt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_ \_ HTTP-ABFRAGE-MIME-VERSION \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Empfängt die Version des MIME-Protokolls, das zum Erstellen der Nachricht verwendet wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**\_ \_ HTTP-ABFRAGE-ORIG-URI \_**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Veraltet. Wird nur aus Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP \_ QUERY \_ PRAGMA**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Empfängt die implementierungsspezifischen Anweisungen, die für jeden Empfänger entlang der Anforderungs-/Antwortkette gelten können.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_ \_ HTTP-ABFRAGEPROXYAUTHENTIFIZIERUNG \_**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Ruft das vom Proxy zurückgegebene Authentifizierungsschema und den Bereich ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**AUTORISIERUNG DES \_ \_ HTTP-ABFRAGEPROXYS \_**
</dt> <dd> <dl> <dt>

61
</dt> <dt>



Ruft den Header ab, mit dem der Benutzer bei einem Proxy identifiziert wird, für den eine Authentifizierung erforderlich ist. Dieser Header kann nur abgerufen werden, bevor die Anforderung an den Server gesendet wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_ \_ HTTP-ABFRAGEPROXYVERBINDUNG \_**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Ruft den Proxy-Connection ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**HTTP \_ QUERY \_ PUBLIC**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Empfängt methoden, die auf diesem Server verfügbar sind.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**\_ \_ HTTP-ABFRAGEBEREICH**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Ruft den Bytebereich einer Entität ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_UNFORMATTE \_ \_ HTTP-ABFRAGEHEADER**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Empfängt alle vom Server zurückgegebenen Header. Jeder Header wird mit \\ "0" beendet. Ein zusätzliches \\ "0" beendet die Liste der Header.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP \_ QUERY \_ RAW \_ HEADERS \_ CRLF**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Empfängt alle vom Server zurückgegebenen Header. Jeder Header wird durch eine CR/LF-Sequenz (Wagenrücklauf/Zeilenfeed) getrennt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**\_ \_ HTTP-ABFRAGE-REFERER**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Empfängt Uniform Resource Identifier (URI) der Ressource, in der der angeforderte URI erhalten wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**\_ \_ HTTP-ABFRAGEAKTUALISIERUNG**
</dt> <dd> <dl> <dt>

46
</dt> <dt>



Veraltet. Wird nur aus Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**\_ \_ HTTP-ABFRAGEANFORDERUNGSMETHODE \_**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Empfängt das HTTP-Verb, das in der Anforderung verwendet wird, in der Regel GET oder POST.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**WIEDERHOLUNG \_ DER \_ \_ HTTP-ABFRAGE NACH**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Ruft die Zeit ab, für die der Dienst voraussichtlich nicht verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**\_ \_ HTTP-ABFRAGESERVER**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Ruft Daten über die Software ab, die vom Ursprungsserver zur Verarbeitung der Anforderung verwendet wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP \_ QUERY \_ SET \_ COOKIE**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Empfängt den Wert des für die Anforderung festgelegten Cookies.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_ \_ HTTP-ABFRAGESTATUSCODE \_**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Empfängt den vom Server zurückgegebenen Statuscode. Weitere Informationen und eine Liste der möglichen Werte finden Sie unter [**HTTP-Statuscodes**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**\_ \_ HTTP-ABFRAGESTATUSTEXT \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Empfängt zusätzlichen Text, der vom Server in der Antwortzeile zurückgegeben wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**\_ \_ HTTP-ABFRAGETITEL**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Veraltet. Wird nur aus Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**\_ \_ HTTP-ABFRAGEÜBERTRAGUNGSCODIERUNG \_**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Ruft den Typ der Transformation ab, die auf den Nachrichtentext angewendet wurde, damit er sicher zwischen Absender und Empfänger übertragen werden kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**\_HTTP-ABFRAGE, \_ ES SEI \_ DENN, SIE WURDE \_ GEÄNDERT.**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Ruft den Unless-Modified-Since-Header ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**\_ \_ HTTP-ABFRAGEUPGRADE**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Ruft die zusätzlichen Kommunikationsprotokolle ab, die vom Server unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**\_ \_ HTTP-ABFRAGE-URI**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Empfängt einige oder alle URIs (Uniform Resource Identifiers), anhand derer die Request-URI-Ressource identifiziert werden kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_ \_ HTTP-ABFRAGEBENUTZER-AGENT \_**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Ruft Daten über den Benutzer-Agent ab, der die Anforderung gestellt hat.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**\_HTTP-ABFRAGE \_ VARIIERT**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Ruft den Header ab, der angibt, dass die Entität mithilfe einer servergesteuerten Aushandlung aus einer Reihe verfügbarer Darstellungen der Antwort ausgewählt wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**\_ \_ HTTP-ABFRAGEVERSION**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Empfängt den letzten Antwortcode, der vom Server zurückgegeben wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**\_ \_ HTTP-ABFRAGE ÜBER**
</dt> <dd> <dl> <dt>

66
</dt> <dt>



Ruft die Zwischenprotokolle und Empfänger zwischen dem Benutzer-Agent und dem Server bei Anforderungen sowie zwischen dem Ursprungsserver und dem Client bei Antworten ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**\_ \_ HTTP-ABFRAGEWARNUNG**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Ruft zusätzliche Daten zum Status einer Antwort ab, die möglicherweise nicht im Antwortstatuscode widergespiegelt werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP \_ QUERY \_ WWW \_ AUTHENTICATE**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Ruft das vom Server zurückgegebene Authentifizierungsschema und den Bereich ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**OPTIONEN FÜR \_ DEN \_ HTTP-ABFRAGE-X-INHALTSTYP \_ \_ \_**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Ruft den Headerwert X-Content-Type-Options ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**\_HTTP-ABFRAGE \_ P3P**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Ruft den P3P-Headerwert ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP \_ QUERY \_ X \_ P2P \_ PEERDIST**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Ruft den X-P2P-PeerDist-Headerwert ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP \_ QUERY \_ TRANSLATE**
</dt> <dd> <dl> <dt>

82
</dt> <dt>



Ruft den Translate-Headerwert ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**\_HTTP-ABFRAGE \_ X \_ \_ UA-KOMPATIBEL**
</dt> <dd> <dl> <dt>

83
</dt> <dt>



Ruft den X-UA-kompatiblen Headerwert ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**STANDARDSTIL \_ DER \_ \_ HTTP-ABFRAGE**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Ruft den Default-Style-Headerwert ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**HTTP \_ QUERY \_ X \_ FRAME \_ OPTIONS**
</dt> <dd> <dl> <dt>

85
</dt> <dt>



Ruft den Headerwert X-Frame-Options ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP \_ QUERY \_ X \_ XSS \_ PROTECTION**
</dt> <dd> <dl> <dt>

86
</dt> <dt>



Ruft den X-XSS-Protection-Headerwert ab.


</dt> </dl> </dd> </dl>

Die Modifiziererflags werden in Verbindung mit einem Attributflag verwendet, um die Anforderung zu ändern. Modifiziererflags ändern entweder das Format der zurückgegebenen Daten oder geben an, wo [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (oder [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) nach den Daten suchen soll.

<dl> <dt>

<span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**\_ \_ HTTP-ABFRAGEFLAG \_ COALESCE**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**\_ \_ HTTP-ABFRAGEFLAGNUMMER \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Gibt die Daten als 32-Bit-Zahl für Header zurück, deren Wert eine Zahl ist, z. B. der Statuscode.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_ANFORDERUNGSHEADER \_ DES \_ \_ HTTP-ABFRAGEFLAGS**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Fragt nur Anforderungsheader ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**\_ \_ HTTP-ABFRAGEFLAG \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Gibt den Headerwert als [**SYSTEMTIME-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) zurück, für die die Anwendung die Daten nicht analysieren muss. Wird für Header verwendet, deren Wert eine Datums-/Uhrzeitzeichenfolge ist, z. B. "Last-Modified-Time".


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



 

