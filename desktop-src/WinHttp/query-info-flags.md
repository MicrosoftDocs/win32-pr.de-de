---
description: Diese Attribute und Modifizierer werden von WinHttpQueryHeaders verwendet.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Abfrageinformationsflags (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ba15c258a37627cdbdd79f13859761fd671385
ms.sourcegitcommit: df0933ad2b42f07031f4340330712c11cf712ff0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107385888"
---
# <a name="query-info-flags-winhttph"></a>Abfrageinformationsflags (Winhttp.h)

Diese Attribute und Modifizierer werden von [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders)verwendet.

Die Attributflags werden von [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) verwendet, um anzugeben, welche Informationen abgerufen werden sollen. Die meisten Attributflags werden direkt einem bestimmten HTTP-Header zugeordnet. Es gibt auch einige spezielle Flags, z. B. WINHTTP \_ QUERY \_ RAW \_ HEADERS, die nicht mit einem bestimmten Header verknüpft sind.

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WINHTTP \_ QUERY \_ ACCEPT**
</dt> <dd> <dl> <dt>



Ruft die zulässigen Medientypen für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ CHARSET**
</dt> <dd> <dl> <dt>



Ruft die zulässigen Zeichensätze für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ ENCODING**
</dt> <dd> <dl> <dt>



Ruft die zulässigen Werte für die Inhaltscodierung für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ LANGUAGE**
</dt> <dd> <dl> <dt>



Ruft die zulässigen natürlichen Sprachen für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ RANGES**
</dt> <dd> <dl> <dt>



Ruft die Typen von Bereichsanforderungen ab, die für eine Ressource akzeptiert werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**ALTER DER \_ WINHTTP-ABFRAGE \_**
</dt> <dd> <dl> <dt>



Ruft das Feld Age response-header ab, das die Schätzung des Absenders für den Zeitraum seit der Generierung der Antwort auf dem Ursprungsserver enthält.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WINHTTP \_ QUERY \_ ALLOW**
</dt> <dd> <dl> <dt>



Empfängt die [**vom Server unterstützten**](glossary.md) HTTP-Verben.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_ \_ WINHTTP-ABFRAGEAUTHENTIFIZIERUNGSINFORMATIONEN \_**
</dt> <dd> <dl> <dt>



Ruft den Authentication-Info ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**\_ \_ WINHTTP-ABFRAGEAUTORISIERUNG**
</dt> <dd> <dl> <dt>



Ruft die für eine Anforderung verwendeten Autorisierungsanmeldeinformationen ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**\_ \_ WINHTTP-ABFRAGECACHE-STEUERELEMENT \_**
</dt> <dd> <dl> <dt>



Ruft die Cachesteuerungs-Direktiven ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**\_WINHTTP-ABFRAGEVERBINDUNG \_**
</dt> <dd> <dl> <dt>



Ruft alle Optionen ab, die für eine bestimmte Verbindung angegeben sind und nicht von Proxys über weitere Verbindungen kommuniziert werden dürfen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSBASIS \_**
</dt> <dd> <dl> <dt>



Ruft den Basis-Uniform Resource Identifier (URI) ab, um relative URLs innerhalb der Entität aufzulösen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSBESCHREIBUNG \_**
</dt> <dd> <dl> <dt>



Veraltet. Wird aus Kompatibilitäts- und Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSDISPOSITION \_**
</dt> <dd> <dl> <dt>



Veraltet. Wird aus Kompatibilitäts- und Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSCODIERUNG \_**
</dt> <dd> <dl> <dt>



Ruft zusätzliche Inhaltscodierung ab, die auf die gesamte Ressource angewendet wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**\_ \_ WINHTTP-ABFRAGEINHALTS-ID \_**
</dt> <dd> <dl> <dt>



Ruft die Inhaltsidentifikation ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSSPRACHE \_**
</dt> <dd> <dl> <dt>



Ruft die Sprache ab, in der der Inhalt geschrieben wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**LÄNGE DES \_ WINHTTP-ABFRAGEINHALTS \_ \_**
</dt> <dd> <dl> <dt>



Ruft die Größe der Ressource in Bytes ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**SPEICHERORT DES \_ WINHTTP-ABFRAGEINHALTS \_ \_**
</dt> <dd> <dl> <dt>



Ruft den Ressourcenspeicherort für die Entität ab, die in der Nachricht eingeschlossen ist.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP \_ QUERY \_ CONTENT \_ MD5**
</dt> <dd> <dl> <dt>



Ruft einen MD5-Digest des Entitätstexts ab, um eine End-to-End-Überprüfung der Nachrichtenintegrität für den Entitätstext bereitzustellen. Weitere Informationen finden Sie unter [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSBEREICH \_**
</dt> <dd> <dl> <dt>



Ruft die Position im vollständigen Entitätstext ab, an der der Teilentitätstext eingefügt werden soll, und die Gesamtgröße des vollständigen Entitätstexts.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**CODIERUNG DER \_ WINHTTP-ABFRAGEINHALTSÜBERTRAGUNG \_ \_ \_**
</dt> <dd> <dl> <dt>



Ruft eine Codierungstransformation ab, die auf einen Entitätstext anwendbar ist. Sie wurde möglicherweise bereits angewendet, muss möglicherweise angewendet werden oder ist optional anwendbar.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**\_ \_ WINHTTP-ABFRAGEINHALTSTYP \_**
</dt> <dd> <dl> <dt>



Empfängt den Inhaltstyp der Ressource, z. B. text oder html.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**\_ \_ WINHTTP-ABFRAGECOOKIE**
</dt> <dd> <dl> <dt>



Ruft alle cookies ab, die der Anforderung zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**\_WINHTTP-ABFRAGEKOSTEN \_**
</dt> <dd> <dl> <dt>



Wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP \_ QUERY \_ CUSTOM**
</dt> <dd> <dl> <dt>



Bewirkt, dass [**WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) nach dem im *pwszName-Parameter angegebenen* Headernamen sucht und die Headerinformationen in *lpBuffer* speichert. Eine Anwendung kann **WINHTTP \_ OPTION RECEIVE \_ RESPONSE \_ \_ TIMEOUT** verwenden, um die maximale Zeit zu begrenzen, die diese Abfrage auf den Empfang aller Header wartet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**\_WINHTTP-ABFRAGEDATUM \_**
</dt> <dd> <dl> <dt>



Empfängt das Datum und die Uhrzeit, zu der die Nachricht stammt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**VON \_ \_ ABGELEITETE WINHTTP-ABFRAGE \_**
</dt> <dd> <dl> <dt>



Wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ \_ WINHTTP-ABFRAGE-ETAG**
</dt> <dd> <dl> <dt>



Ruft das Entitätstag für die zugeordnete Entität ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP \_ QUERY \_ EXPECT**
</dt> <dd> <dl> <dt>



Ruft den Expect-Header ab, der angibt, ob die Clientanwendung Antworten der Serie 100 erwarten soll.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**\_WINHTTP-ABFRAGE \_ LÄUFT AB**
</dt> <dd> <dl> <dt>



Empfängt das Datum und die Uhrzeit, nach der die Ressource als veraltet betrachtet werden soll.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**\_WINHTTP-ABFRAGE \_ WEITERGELEITET**
</dt> <dd> <dl> <dt>



Veraltet. Wird aus Kompatibilitäts- und Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WINHTTP \_ QUERY \_ FROM**
</dt> <dd> <dl> <dt>



Ruft die E-Mail-Adresse für den Benutzer ab, der den anfordernden [*Benutzer-Agent*](glossary.md) steuert, wenn der From-Header angegeben ist.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**\_WINHTTP-ABFRAGEHOST \_**
</dt> <dd> <dl> <dt>



Ruft den Internethost und die Portnummer der angeforderten Ressource ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP \_ QUERY \_ IF \_ MATCH**
</dt> <dd> <dl> <dt>



Ruft den Inhalt des If-Match Anforderungsheaderfelds ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**\_WINHTTP-ABFRAGE, \_ WENN \_ SIE GEÄNDERT \_ WURDE**
</dt> <dd> <dl> <dt>



Ruft den Inhalt des If-Modified-Since-Headers ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**\_WINHTTP-ABFRAGE, \_ WENN \_ KEINE ÜBEREINSTIMMUNG \_ BESTEHT**
</dt> <dd> <dl> <dt>



Ruft den Inhalt des Anforderungsheaderfelds If-None-Match ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WINHTTP \_ QUERY \_ IF \_ RANGE**
</dt> <dd> <dl> <dt>



Ruft den Inhalt des If-Range Anforderungsheaderfelds ab. Mit diesem Header kann die Clientanwendung überprüfen, ob die Entität, die mit einer Teilkopie der Entität im Cache der Clientanwendung verknüpft ist, nicht aktualisiert wurde. Wenn die Entität nicht aktualisiert wurde, senden Sie die Teile, die in der Clientanwendung fehlen. Wenn die Entität aktualisiert wurde, senden Sie die gesamte aktualisierte Entität.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**\_WINHTTP-ABFRAGE, \_ WENN SEIT NICHT \_ GEÄNDERT \_**
</dt> <dd> <dl> <dt>



Ruft den Inhalt des Anforderungsheaderfelds If-Unmodified-Since ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**\_WINHTTP-ABFRAGELINK \_**
</dt> <dd> <dl> <dt>



Veraltet. Wird aus Gründen der Kompatibilität von Legacyanwendungen beibehalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_WINHTTP-ABFRAGE \_ ZULETZT \_ GEÄNDERT**
</dt> <dd> <dl> <dt>



Empfängt das Datum und die Uhrzeit der letzten Änderung der Ressource. Datum und Uhrzeit werden vom Server bestimmt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**\_ \_ WINHTTP-ABFRAGESPEICHERORT**
</dt> <dd> <dl> <dt>



Ruft den absoluten URI ab, der in einem Location-Antwortheader verwendet wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**WINHTTP \_ QUERY \_ MAX**
</dt> <dd> <dl> <dt>



Gibt den maximalen Wert eines WINHTTP \_ \_ \* QUERY-Werts an. Kein Abfrageflag.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**WINHTTP \_ QUERY \_ MAX \_ FORWARDS**
</dt> <dd> <dl> <dt>



Ruft die Anzahl der Proxys oder Gateways ab, die die Anforderung an den nächsten eingehenden Server weitergeleitet werden können.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_ \_ WINHTTP-ABFRAGENACHRICHTEN-ID \_**
</dt> <dd> <dl> <dt>



Wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_ \_ WINHTTP-ABFRAGE-MIME-VERSION \_**
</dt> <dd> <dl> <dt>



Empfängt die Version des MULTIPURPOSE INTERNET MAIL EXTENSIONS (MIME), das zum Erstellen der Nachricht verwendet wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_ \_ WINHTTP-ABFRAGE-ORIG-URI \_**
</dt> <dd> <dl> <dt>



Veraltet. Wird aus Kompatibilitäts- und Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WINHTTP \_ QUERY \_ PRAGMA**
</dt> <dd> <dl> <dt>



Empfängt die implementierungsspezifischen Anweisungen, die für jeden Empfänger entlang der Anforderungs-/Antwortkette gelten können.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_ \_ WINHTTP-ABFRAGEPROXYAUTHENTIFIZIERUNG \_**
</dt> <dd> <dl> <dt>



Ruft das vom Proxy zurückgegebene Authentifizierungsschema und den Bereich ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_ \_ WINHTTP-ABFRAGEPROXYAUTORISIERUNG \_**
</dt> <dd> <dl> <dt>



Ruft den Header ab, mit dem der Benutzer bei einem Proxy identifiziert wird, für den eine Authentifizierung erforderlich ist. Dieser Header kann nur abgerufen werden, bevor die Anforderung an den Server gesendet wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_ \_ WINHTTP-ABFRAGEPROXYVERBINDUNG \_**
</dt> <dd> <dl> <dt>



Ruft den Proxy-Connection ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_ \_ WINHTTP-ABFRAGEPROXYUNTERSTÜTZUNG \_**
</dt> <dd> <dl> <dt>



Ruft den Proxy-Support ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP \_ QUERY \_ PUBLIC**
</dt> <dd> <dl> <dt>



Empfängt HTTP-Verben, die auf diesem Server verfügbar sind.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_WINHTTP-ABFRAGEBEREICH \_**
</dt> <dd> <dl> <dt>



Ruft den Bytebereich einer Entität ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_ \_ UNFORMATIERTE WINHTTP-ABFRAGEHEADER \_**
</dt> <dd> <dl> <dt>



Empfängt alle vom Server zurückgegebenen Header. Jeder Header wird mit \\ "0" beendet. Ein \\ zusätzliches "0" beendet die Liste der Header.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP \_ QUERY \_ RAW \_ HEADERS \_ CRLF**
</dt> <dd> <dl> <dt>



Empfängt alle vom Server zurückgegebenen Header. Jeder Header wird durch eine CR/LF-Sequenz (Wagenrücklauf/Zeilenvorschub) getrennt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**\_WINHTTP-ABFRAGEREFERENZ \_**
</dt> <dd> <dl> <dt>



Empfängt den URI der Ressource, in der der angeforderte URI abgerufen wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_WINHTTP-ABFRAGEAKTUALISIERUNG \_**
</dt> <dd> <dl> <dt>



Veraltet. Wird aus Gründen der Kompatibilität von Legacyanwendungen beibehalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_ \_ WINHTTP-ABFRAGEANFORDERUNGSMETHODE \_**
</dt> <dd> <dl> <dt>



Empfängt das HTTP-Verb, das in der Anforderung verwendet wird, in der Regel GET oder POST.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WINHTTP \_ QUERY \_ RETRY \_ AFTER**
</dt> <dd> <dl> <dt>



Ruft den Zeitraum ab, für den der Dienst voraussichtlich nicht verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_WINHTTP-ABFRAGESERVER \_**
</dt> <dd> <dl> <dt>



Ruft Informationen über die Software ab, die vom Ursprungsserver zum Verarbeiten der Anforderung verwendet wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_ \_ \_ WINHTTP-ABFRAGESATZCOOKIE**
</dt> <dd> <dl> <dt>



Empfängt den Wert des Für die Anforderung festgelegten Cookies.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**\_ \_ WINHTTP-ABFRAGESTATUSCODE \_**
</dt> <dd> <dl> <dt>



Empfängt den vom Server zurückgegebenen Statuscode. Eine Liste der möglichen Werte finden Sie unter [**HTTP-Statuscodes**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**\_ \_ WINHTTP-ABFRAGESTATUSTEXT \_**
</dt> <dd> <dl> <dt>



Empfängt zusätzlichen Text, der vom Server in der Antwortzeile zurückgegeben wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**\_WINHTTP-ABFRAGETITEL \_**
</dt> <dd> <dl> <dt>



Veraltet. Wird aus Kompatibilitäts- und Legacy-Anwendungskompatibilität verwaltet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**\_ \_ WINHTTP-ABFRAGEÜBERTRAGUNGSCODIERUNG \_**
</dt> <dd> <dl> <dt>



Ruft den Typ der Transformation ab, die auf den Nachrichtentext angewendet wurde, damit er sicher zwischen Absender und Empfänger übertragen werden kann.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_WINHTTP-ABFRAGE, \_ ES SEI \_ DENN, SIE WURDE \_ GEÄNDERT.**
</dt> <dd> <dl> <dt>



Ruft den Unless-Modified-Since-Header ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_ \_ WINHTTP-ABFRAGEUPGRADE**
</dt> <dd> <dl> <dt>



Ruft die zusätzlichen Kommunikationsprotokolle ab, die vom Server unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_ \_ WINHTTP-ABFRAGE-URI**
</dt> <dd> <dl> <dt>



Empfängt einen Teil oder den ganzen URI, mit dem die Request-URI-Ressource identifiziert werden kann.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_ \_ WINHTTP-ABFRAGEBENUTZER-AGENT \_**
</dt> <dd> <dl> <dt>



Ruft Informationen über den Benutzer-Agent ab, der die Anforderung gestellt hat.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**\_WINHTTP-ABFRAGE \_ VARIIERT**
</dt> <dd> <dl> <dt>



Ruft den Header ab, der angibt, dass die Entität mithilfe einer servergesteuerten Aushandlung aus einer Reihe verfügbarer Darstellungen der Antwort ausgewählt wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**\_WINHTTP-ABFRAGEVERSION \_**
</dt> <dd> <dl> <dt>



Ruft die HTTP-Version ab, die in der Statuszeile vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_WINHTTP-ABFRAGE \_ ÜBER**
</dt> <dd> <dl> <dt>



Ruft die Zwischenprotokolle und Empfänger zwischen dem Benutzer-Agent und dem Server bei Anforderungen sowie zwischen dem Ursprungsserver und dem Client bei Antworten ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_WINHTTP-ABFRAGEWARNUNG \_**
</dt> <dd> <dl> <dt>



Ruft zusätzliche Informationen zum Status einer Antwort ab, die möglicherweise nicht vom Antwortstatuscode widergespiegelt werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP \_ QUERY \_ WWW \_ AUTHENTICATE**
</dt> <dd> <dl> <dt>



Ruft das vom Server zurückgegebene Authentifizierungsschema und den vom Server zurückgegebenen Bereich ab.


</dt> </dl> </dd> </dl>

Die Modifiziererflags werden zusammen mit einem Attributflag verwendet, um die Anforderung zu ändern. Modifiziererflags ändern entweder das Format der zurückgegebenen Daten oder geben an, wo die [**WinHttpQueryHeaders-Funktion**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) nach den Informationen suchen soll.

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**\_ \_ WINHTTP-ABFRAGEFLAGNUMMER \_**
</dt> <dd> <dl> <dt>



Gibt die Daten als 32-Bit-Zahl für Header zurück, deren Wert eine Zahl ist, z. B. der Statuscode.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_ANFORDERUNGSHEADER FÜR WINHTTP-ABFRAGEFLAGS \_ \_ \_**
</dt> <dd> <dl> <dt>



Fragt nur Anforderungsheader ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**\_WINHTTP-ABFRAGEFLAG \_ \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>



Gibt den Headerwert als [**SYSTEMTIME-Struktur**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) zurück, die keine Analyse der Daten durch die Anwendung erfordert. Verwenden Sie für Header, deren Wert eine Datums-/Uhrzeitzeichenfolge ist, z. B. "Last-Modified-Time".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows XP, Windows 2000 Professional mit \[ SP3-Desktop-Apps\]      |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2003, Windows 2000 Server mit \[ SP3-Desktop-Apps\]   |
| Header                   | <dl> <dt>Winhttp.h</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

* [WinHTTP-Versionen](winhttp-versions.md)
