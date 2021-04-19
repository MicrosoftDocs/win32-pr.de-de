---
title: Abfrageinfoflags (WinInet. h)
description: Die folgenden Listen enthalten die von "HttpQueryInfo" und "queryInfo" verwendeten Attribute und modifiziererer.
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
ms.openlocfilehash: 5f3a6166c59e158d041e730d2198f6e1b066a8b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344111"
---
# <a name="query-info-flags-winineth"></a>Abfrageinfoflags (WinInet. h)

Die folgenden Listen enthalten die von " [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) " und " [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))" verwendeten Attribute und modifiziererer.

Die Attributflags werden von [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (oder [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) verwendet, um anzugeben, welche Daten abgerufen werden sollen. Die meisten Attributflags werden direkt einem bestimmten HTTP-Header zugeordnet. Es gibt auch einige spezielle Flags, wie z. b. [http- \_ Abfrage \_ \_ rohheader](/windows), die nicht mit einem bestimmten Header verknüpft sind.

<dl> <dt>

<span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**akzeptieren der HTTP- \_ Abfrage \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Ruft die zulässigen Medientypen für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**Zeichensatz für HTTP- \_ Abfrage \_ Annahme \_**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Ruft die zulässigen Zeichensätze für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**Codierung der HTTP- \_ Abfrage \_ Annahme \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Ruft die zulässigen Content-Coding-Werte für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**HTTP- \_ Abfrage \_ Accept- \_ Sprache**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Ruft die zulässigen natürlichen Sprachen für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**Accept-Bereiche der HTTP- \_ Abfrage \_ \_**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Ruft die Typen von Bereichs Anforderungen ab, die für eine Ressource akzeptiert werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**HTTP- \_ Abfrage \_ Alter**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Ruft das Feld "Age Response-Header" ab, das die Schätzung des Absenders der Zeitspanne enthält, seit die Antwort auf dem Ursprungsserver generiert wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**HTTP- \_ Abfrage \_ zulassen**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Empfängt die vom Server unterstützten HTTP-Verben.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**HTTP- \_ Abfrage \_ Autorisierung**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Ruft die Autorisierungs Anmelde Informationen ab, die für eine Anforderung verwendet werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**HTTP- \_ Abfrage \_ Cache- \_ Steuerelement**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Ruft die Cache Steuerungs Direktiven ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**HTTP- \_ Abfrage \_ Verbindung**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Ruft alle Optionen ab, die für eine bestimmte Verbindung angegeben werden und nicht von Proxys über weitere Verbindungen kommuniziert werden dürfen.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**Basis für HTTP- \_ Abfrage \_ Inhalt \_**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Ruft den Basis-URI (Uniform Resource Identifier) zum Auflösen relativer URLs innerhalb der Entität ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**Beschreibung der HTTP- \_ Abfrage \_ Inhalte \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Veraltet. Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**HTTP- \_ Abfrage \_ Inhalts \_ Disposition**
</dt> <dd> <dl> <dt>

47
</dt> <dt>



Veraltet. Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**Codierung von http- \_ Abfrage \_ Inhalten \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Ruft alle zusätzlichen Inhalts Codierungen ab, die auf die gesamte Ressource angewendet wurden.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**Inhalts-ID der HTTP- \_ Abfrage \_ \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Ruft die Inhalts Identifikation ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**Sprache für HTTP- \_ Abfrage \_ Inhalt \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Ruft die Sprache ab, in der sich der Inhalt befindet.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**Länge der HTTP- \_ Abfrage \_ Inhalte \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Ruft die Größe der Ressource in Bytes ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**Speicherort der HTTP- \_ Abfrage \_ Inhalte \_**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Ruft den Ressourcen Speicherort für die in der Nachricht eingeschlossene Entität ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**HTTP- \_ Abfrage \_ Inhalt \_ MD5**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Ruft einen MD5-Digest des Entitäts Texts ab, um eine End-to-End-Nachrichten Integritätsprüfung (MIC) für den Entitäts Text bereitzustellen. Weitere Informationen finden Sie unter RFC1864, dem Content-MD5-Header Feld unter [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_ \_ Inhalts \_ Bereich der HTTP-Abfrage**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Ruft den Speicherort im vollständigen Entitäts Text ab, in den der partielle Entitäts Text eingefügt werden soll, und die Gesamtgröße des vollständigen Entitäts Texts.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**Codierung der HTTP- \_ Abfrage \_ Inhalts \_ Übertragung \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Empfängt die zusätzliche Inhalts Codierung, die auf die Ressource angewendet wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_Inhaltstyp für http-Abfragen \_ \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Empfängt den Inhaltstyp der Ressource (z. b. Text/HTML).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**HTTP- \_ Abfrage \_ Cookie**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Ruft alle Cookies ab, die der Anforderung zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**Kosten der HTTP- \_ Abfrage \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Wird nicht mehr unterstützt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_ \_ benutzerdefinierte HTTP-Abfrage**
</dt> <dd> <dl> <dt>

65.535
</dt> <dt>



Bewirkt, dass [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) nach dem in *lpvbuffer* angegebenen Header Namen sucht und die Header Daten in *lpvbuffer* speichert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**Datum der HTTP- \_ Abfrage \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Empfängt das Datum und die Uhrzeit, zu der die Nachricht stammt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_ \_ von abgeleitete HTTP-Abfrage \_**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Wird nicht mehr unterstützt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_ \_ Echo \_ Header der HTTP-Abfrage**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**HTTP- \_ Abfrage \_ Echo \_ Header \_ CRLF**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**HTTP- \_ Abfrage- \_ Echo \_ Antwort**
</dt> <dd> <dl> <dt>

72
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**\_ \_ Echo \_ Anforderung der HTTP-Abfrage**
</dt> <dd> <dl> <dt>

71
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**HTTP- \_ Abfrage- \_ ETag**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Ruft das Entitätstag der zugeordneten Entität ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**erwartete http- \_ Abfrage \_**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Ruft den erwarteten Header ab, der angibt, ob die Client Anwendung Antworten auf 100-Reihen erwarten soll.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**HTTP- \_ Abfrage \_ läuft ab**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Empfängt das Datum und die Uhrzeit, nach der die Ressource als veraltet betrachtet werden soll.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**\_ \_ weitergeleitete HTTP-Abfrage**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Veraltet. Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**HTTP- \_ Abfrage \_ aus**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Ruft die e-Mail-Adresse für den Benutzer ab, der den anfordernden Benutzer-Agent steuert, wenn der from-Header angegeben ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**HTTP- \_ Abfrage \_ Host**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Ruft den Internet Host und die Portnummer der angeforderten Ressource ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**HTTP- \_ Abfrage \_ bei Übereinstimmung \_**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Ruft den Inhalt des If-Match Anforderungs Header Felds ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**HTTP- \_ Abfrage \_ bei \_ Änderung \_ seit**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Ruft den Inhalt des If-modified-since-Headers ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**HTTP- \_ Abfrage, \_ Wenn keiner gefunden wird \_ \_**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Ruft den Inhalt des Felds "If-None-Match Request-Header" ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**HTTP- \_ Abfrage, \_ Wenn \_ Bereich**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Ruft den Inhalt des If-Range Anforderungs Header Felds ab. Dieser Header ermöglicht der Client Anwendung, zu überprüfen, ob die Entität, die sich auf eine partielle Kopie der Entität im Client Anwendungscache bezieht, nicht aktualisiert wurde. Wenn die Entität nicht aktualisiert wurde, senden Sie die Teile, die die Client Anwendung fehlt. Wenn die Entität aktualisiert wurde, senden Sie die gesamte aktualisierte Entität.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**HTTP- \_ Abfrage, \_ Wenn \_ nicht geändert \_ seit**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Ruft den Inhalt des Felds "If-Unmodified-Since" des Anforderungs Headers ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ Letzte \_ Änderung der HTTP-Abfrage**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Empfängt das Datum und die Uhrzeit, zu denen der Server glaubt, dass die Ressource zuletzt geändert wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**HTTP- \_ Abfrage \_ Link**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Veraltet. Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**HTTP- \_ Abfrage \_ Speicherort**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Ruft den absoluten Uniform Resource Identifier (URI) ab, der in einem "Location"-Antwortheader verwendet wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**Max. http- \_ Abfrage \_**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



Kein abfrageflag. Gibt den maximalen Wert eines HTTP- \_ Abfrage \_ \* Werts an.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**maximale HTTP-Abfrage-Weiterleitung \_ \_ \_**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Ruft die Anzahl von Proxys oder Gateways ab, die die Anforderung an den nächsten eingehenden Server weiterleiten können.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**ID der HTTP- \_ Abfrage \_ Nachricht \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Wird nicht mehr unterstützt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**MIME-Version der HTTP- \_ Abfrage \_ \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Empfängt die Version des MIME-Protokolls, das zum Erstellen der Nachricht verwendet wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**URI der HTTP- \_ Abfrage- \_ \_ URI**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Veraltet. Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**HTTP- \_ Abfrage- \_ pragma**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Empfängt die Implementierungs spezifischen Direktiven, die ggf. für jeden Empfänger in der Anforderungs-/Antwortkette gelten.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**HTTP- \_ Abfrage \_ Proxy \_ authentifizieren**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Ruft das vom Proxy zurückgegebene Authentifizierungsschema und den Bereich ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**HTTP- \_ Abfrage \_ Proxy- \_ Autorisierung**
</dt> <dd> <dl> <dt>

61
</dt> <dt>



Ruft den Header ab, der verwendet wird, um den Benutzer für einen Proxy zu identifizieren, für den eine Authentifizierung erforderlich ist. Dieser Header kann nur abgerufen werden, bevor die Anforderung an den Server gesendet wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**HTTP- \_ Abfrage \_ Proxy \_ Verbindung**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Ruft den Proxy-Connection-Header ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**öffentliche http- \_ Abfrage \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Empfängt Methoden, die auf diesem Server verfügbar sind.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**HTTP- \_ Abfrage \_ Bereich**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Ruft den Byte Bereich einer Entität ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_ \_ Rohdaten \_ Header der HTTP-Abfrage**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Empfängt alle vom Server zurückgegebenen Header. Jeder Header wird durch " \\ 0" beendet. Eine zusätzliche " \\ 0" beendet die Liste der Header.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**HTTP \_ - \_ Abfrage \_ rohheader \_ CRLF**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Empfängt alle vom Server zurückgegebenen Header. Jeder Header wird durch eine Wagen Rücklauf/Zeilenvorschub-Sequenz (CR/LF) getrennt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**HTTP- \_ Abfrage \_ Verweis**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Empfängt den Uniform Resource Identifier (URI) der Ressource, in der der angeforderte URI abgerufen wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**Aktualisierung der HTTP- \_ Abfrage \_**
</dt> <dd> <dl> <dt>

46
</dt> <dt>



Veraltet. Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**HTTP- \_ Abfrage \_ Anforderungs \_ Methode**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Empfängt das HTTP-Verb, das in der Anforderung verwendet wird, in der Regel Get oder Post.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**Wiederholung der HTTP- \_ Abfrage \_ \_ nach**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Ruft die Zeitspanne ab, die erwartet wird, dass der Dienst nicht verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**HTTP- \_ Abfrage \_ Server**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Ruft Daten über die Software ab, die vom Ursprungsserver verwendet wird, um die Anforderung zu verarbeiten.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**HTTP- \_ Abfrage \_ Satz \_ Cookie**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Empfängt den Wert des Cookies, der für die Anforderung festgelegt ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_ \_ Status \_ Code der HTTP-Abfrage**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Empfängt den vom Server zurückgegebenen Statuscode. Weitere Informationen und eine Liste möglicher Werte finden Sie unter [**http-Status Codes**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**Text der HTTP- \_ Abfrage \_ Status \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Empfängt jeden zusätzlichen Text, der vom Server in der Antwort Zeile zurückgegeben wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**HTTP- \_ Abfrage \_ Titel**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Veraltet. Wird nur für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**HTTP- \_ Abfrage \_ Übertragungs \_ Codierung**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Ruft den Typ der Transformation ab, die auf den Nachrichtentext angewendet wurde, sodass er sicher zwischen dem Absender und dem Empfänger übertragen werden kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**HTTP- \_ Abfrage, \_ sofern nicht \_ geändert \_ seit**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Ruft den-nicht-Modified-Since-Header ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**Upgrade der HTTP- \_ Abfrage \_**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Ruft die zusätzlichen Kommunikationsprotokolle ab, die vom Server unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**HTTP- \_ Abfrage- \_ URI**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Empfängt einige oder alle URIs (Uniform Resource Identifier), durch die die Request-URI-Ressource identifiziert werden kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**Benutzer-Agent für HTTP- \_ Abfragen \_ \_**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Ruft Daten über den Benutzer-Agent ab, von dem die Anforderung stammt.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**HTTP- \_ Abfrage \_ variiert**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Ruft den Header ab, der angibt, dass die Entität mithilfe einer servergesteuerten Aushandlung aus einer Reihe von verfügbaren Darstellungen der Antwort ausgewählt wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**HTTP- \_ Abfrage \_ Version**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Empfängt den letzten Antwort Code, der vom Server zurückgegeben wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**HTTP- \_ Abfrage \_ über**
</dt> <dd> <dl> <dt>

66
</dt> <dt>



Ruft die zwischen Protokolle und Empfänger zwischen dem Benutzer-Agent und dem Server bei Anforderungen sowie zwischen dem Ursprungsserver und dem Client bei Antworten ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**HTTP- \_ Abfrage \_ Warnung**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Ruft zusätzliche Daten über den Status einer Antwort ab, die möglicherweise nicht durch den Antwortstatus Code reflektiert werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**HTTP- \_ Abfrage \_ www- \_ Authentifizierung**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Ruft das vom Server zurückgegebene Authentifizierungsschema und den Bereich ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**Optionen für HTTP- \_ Abfrage \_ X- \_ \_ Inhaltstyp \_**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Ruft den Header Wert "X-Content-Type-Options" ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**HTTP- \_ Abfrage \_ P3P**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Ruft den P3P-Header Wert ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**HTTP- \_ Abfrage \_ X P2P- \_ \_ Peer**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Ruft den X-P2P-Peer--Header Wert ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**HTTP- \_ Abfrage Übersetzung \_**
</dt> <dd> <dl> <dt>

82
</dt> <dt>



Ruft den Wert des Translation-Headers ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**HTTP- \_ Abfrage \_ X UA- \_ \_ kompatibel**
</dt> <dd> <dl> <dt>

83
</dt> <dt>



Ruft den X-UA-kompatiblen Header Wert ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**\_ \_ Standard \_ Stil der HTTP-Abfrage**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Ruft den Default-Style-Header Wert ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**Optionen für HTTP- \_ Abfrage \_ X- \_ Frame \_**
</dt> <dd> <dl> <dt>

85
</dt> <dt>



Ruft den X-Frame-Options-Header Wert ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**HTTP- \_ Abfrage \_ X- \_ XSS- \_ Schutz**
</dt> <dd> <dl> <dt>

86
</dt> <dt>



Ruft den X-XSS-Protection-Header Wert ab.


</dt> </dl> </dd> </dl>

Die Modifiziererflags werden zusammen mit einem attributflag verwendet, um die Anforderung zu ändern. Modifiziererflags ändern entweder das Format der zurückgegebenen Daten oder geben an, wo [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (oder [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) nach den Daten suchen soll.

<dl> <dt>

<span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**HTTP \_ - \_ abfrageflag- \_ COALESCE**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**HTTP \_ - \_ abfrageflagnummer \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Gibt die Daten als 32-Bit-Zahl für Header zurück, deren Wert eine Zahl ist, z. b. der Statuscode.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**HTTP-Abfrage Kennzeichen- \_ \_ \_ Anforderungs \_ Header**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Fragt nur Anforderungs Header ab.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**HTTP \_ - \_ abfrageflag \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Gibt den Header Wert als [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur zurück, die die Anwendung nicht benötigt, um die Daten zu analysieren. Verwenden Sie für Header, deren Wert eine Datums-/uhrzeitzeile ist, z. b. "Last-modified-time".


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



 

