---
description: Diese Attribute und modifiziererer werden von WinHttpQueryHeaders verwendet.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Abfrageinfoflags (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9ffc8f4ba4a947fe6fb277617c99460c43ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042479"
---
# <a name="query-info-flags-winhttph"></a>Abfrageinfoflags (WinHTTP. h)

Diese Attribute und modifiziererer werden von [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)verwendet.

Die Attributflags werden von [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) verwendet, um anzugeben, welche Informationen abgerufen werden sollen. Die meisten Attributflags werden direkt einem bestimmten HTTP-Header zugeordnet. Außerdem gibt es einige spezielle Flags, z. b. WinHTTP- \_ Abfrage \_ Rohdaten \_ Header, die nicht mit einem bestimmten Header verknüpft sind.

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**WinHTTP- \_ Abfrage \_ Annahme**
</dt> <dd> <dl> <dt>



Ruft die zulässigen Medientypen für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**Zeichensatz für WinHTTP- \_ Abfrage \_ Annahme \_**
</dt> <dd> <dl> <dt>



Ruft die zulässigen Zeichensätze für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**WinHTTP- \_ Abfrage \_ Accept- \_ Codierung**
</dt> <dd> <dl> <dt>



Ruft die zulässigen Content-Coding-Werte für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**WinHTTP \_ Query \_ Accept- \_ Sprache**
</dt> <dd> <dl> <dt>



Ruft die zulässigen natürlichen Sprachen für die Antwort ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**Accept-Bereiche der WinHTTP- \_ Abfrage \_ \_**
</dt> <dd> <dl> <dt>



Ruft die Typen von Bereichs Anforderungen ab, die für eine Ressource akzeptiert werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**WinHTTP- \_ Abfrage \_ Alter**
</dt> <dd> <dl> <dt>



Ruft das Feld "Age Response-Header" ab, das die Schätzung des Absenders der Zeitspanne enthält, seit die Antwort auf dem Ursprungsserver generiert wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**WinHTTP- \_ Abfrage \_ zulassen**
</dt> <dd> <dl> <dt>



Empfängt die vom Server unterstützten [*http-Verb*](glossary.md)s.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_ \_ Authentifizierungs \_ Informationen für die WinHTTP-Abfrage**
</dt> <dd> <dl> <dt>



Ruft den Authentication-Info-Header ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**WinHTTP- \_ Abfrage \_ Autorisierung**
</dt> <dd> <dl> <dt>



Ruft die Autorisierungs Anmelde Informationen ab, die für eine Anforderung verwendet werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**WinHTTP- \_ Abfrage \_ Cache- \_ Steuerelement**
</dt> <dd> <dl> <dt>



Ruft die Cache Steuerungs Direktiven ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**WinHTTP- \_ Abfrage \_ Verbindung**
</dt> <dd> <dl> <dt>



Ruft alle Optionen ab, die für eine bestimmte Verbindung angegeben werden und nicht von Proxys über weitere Verbindungen kommuniziert werden dürfen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**Basis für WinHTTP- \_ Abfrage \_ Inhalt \_**
</dt> <dd> <dl> <dt>



Ruft den Basis Uniform Resource Identifier (URI) ab, um relative URLs innerhalb der Entität aufzulösen.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**Beschreibung der WinHTTP- \_ Abfrage \_ Inhalte \_**
</dt> <dd> <dl> <dt>



Veraltet. Wird für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**\_ \_ Inhalts \_ Disposition für WinHTTP-Abfrage**
</dt> <dd> <dl> <dt>



Veraltet. Wird für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**Codierung von WinHTTP- \_ Abfrage \_ Inhalten \_**
</dt> <dd> <dl> <dt>



Ruft zusätzliche Inhalts Codierungen ab, die auf die gesamte Ressource angewendet wurden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**WinHTTP- \_ Abfrage \_ Inhalts- \_ ID**
</dt> <dd> <dl> <dt>



Ruft die Inhalts Identifikation ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**\_ \_ Inhalts \_ Sprache für WinHTTP-Abfrage**
</dt> <dd> <dl> <dt>



Ruft die Sprache ab, in der der Inhalt geschrieben wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**\_ \_ Inhalts \_ Länge der WinHTTP-Abfrage**
</dt> <dd> <dl> <dt>



Ruft die Größe der Ressource in Bytes ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**Speicherort für WinHTTP- \_ Abfrage \_ Inhalt \_**
</dt> <dd> <dl> <dt>



Ruft den Ressourcen Speicherort für die in der Nachricht eingeschlossene Entität ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**Inhalt der WinHTTP- \_ Abfrage \_ \_ MD5**
</dt> <dd> <dl> <dt>



Ruft einen MD5-Digest des Entitäts Texts ab, um eine End-to-End-Nachrichten Integritätsprüfung für den Entitäts Text bereitzustellen. Weitere Informationen finden Sie unter [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**\_ \_ Inhalts \_ Bereich der WinHTTP-Abfrage**
</dt> <dd> <dl> <dt>



Ruft den Speicherort im vollständigen Entitäts Text ab, in den der partielle Entitäts Text eingefügt werden soll, und die Gesamtgröße des vollständigen Entitäts Texts.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**Codierung der \_ \_ Inhalts \_ Übertragung \_ mit WinHTTP-Abfragen**
</dt> <dd> <dl> <dt>



Ruft eine Codierungs Transformation ab, die auf einen Entitäts Text anwendbar ist. Möglicherweise wurde Sie bereits angewendet, muss ggf. angewendet werden, oder Sie kann optional sein.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**WinHTTP \_ - \_ Abfrage \_ Inhaltstyp**
</dt> <dd> <dl> <dt>



Empfängt den Inhaltstyp der Ressource, z. b. Text oder HTML.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**WinHTTP- \_ Abfrage \_ Cookie**
</dt> <dd> <dl> <dt>



Ruft alle Cookies ab, die der Anforderung zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**WinHTTP- \_ Abfrage \_ Kosten**
</dt> <dd> <dl> <dt>



Wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WinHTTP- \_ Abfrage \_ Benutzer definiert**
</dt> <dd> <dl> <dt>



Bewirkt, dass [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) nach dem im *pwszName* -Parameter angegebenen Header Namen sucht und die Header Informationen in *lpBuffer* speichert. Eine Anwendung kann das **Timeout für \_ das \_ empfangen \_ \_ der WinHTTP-Option** verwenden, um die maximale Zeit zu begrenzen, die diese Abfrage auf den Empfang aller Header wartet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**Datum der WinHTTP- \_ Abfrage \_**
</dt> <dd> <dl> <dt>



Empfängt das Datum und die Uhrzeit, zu der die Nachricht stammt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**\_ \_ von abgeleitete WinHTTP-Abfrage \_**
</dt> <dd> <dl> <dt>



Wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**WinHTTP- \_ Abfrage- \_ ETag**
</dt> <dd> <dl> <dt>



Ruft das Entitätstag der zugeordneten Entität ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WinHTTP- \_ Abfrage \_ erwartet**
</dt> <dd> <dl> <dt>



Ruft den erwarteten Header ab, der angibt, ob die Client Anwendung Antworten auf 100-Reihen erwarten soll.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**WinHTTP- \_ Abfrage \_ läuft ab**
</dt> <dd> <dl> <dt>



Empfängt das Datum und die Uhrzeit, nach der die Ressource als veraltet betrachtet werden soll.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**weitergeleitete WinHTTP- \_ Abfrage \_**
</dt> <dd> <dl> <dt>



Veraltet. Wird für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**WinHTTP- \_ Abfrage \_ aus**
</dt> <dd> <dl> <dt>



Ruft die e-Mail-Adresse für den Benutzer ab, der den anfordernden [*Benutzer-Agent*](glossary.md) steuert, wenn der from-Header angegeben ist.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**WinHTTP- \_ Abfrage \_ Host**
</dt> <dd> <dl> <dt>



Ruft den Internet Host und die Portnummer der angeforderten Ressource ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WinHTTP- \_ Abfrage \_ bei \_ Treffer**
</dt> <dd> <dl> <dt>



Ruft den Inhalt des If-Match Anforderungs Header Felds ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**WinHTTP- \_ Abfrage \_ bei \_ Änderung \_ seit**
</dt> <dd> <dl> <dt>



Ruft den Inhalt des If-modified-since-Headers ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**WinHTTP- \_ Abfrage, \_ Wenn \_ keine \_ Entsprechung vorliegt**
</dt> <dd> <dl> <dt>



Ruft den Inhalt des Felds "If-None-Match Request-Header" ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**WinHTTP- \_ Abfrage, \_ Wenn \_ Bereich**
</dt> <dd> <dl> <dt>



Ruft den Inhalt des If-Range Anforderungs Header Felds ab. Dieser Header ermöglicht der Client Anwendung, zu überprüfen, ob die Entität, die sich auf eine partielle Kopie der Entität im Cache der Client Anwendung bezieht, nicht aktualisiert wurde. Wenn die Entität nicht aktualisiert wurde, senden Sie die Teile, die die Client Anwendung fehlt. Wenn die Entität aktualisiert wurde, senden Sie die gesamte aktualisierte Entität.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**WinHTTP- \_ Abfrage, \_ Wenn \_ nicht geändert \_ seit**
</dt> <dd> <dl> <dt>



Ruft den Inhalt des Felds "If-Unmodified-Since" des Anforderungs Headers ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**WinHTTP- \_ Abfrage \_ Link**
</dt> <dd> <dl> <dt>



Veraltet. Wird für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ Letzte \_ Änderung der WinHTTP-Abfrage**
</dt> <dd> <dl> <dt>



Empfängt das Datum und die Uhrzeit der letzten Änderung der Ressource. Das Datum und die Uhrzeit werden vom Server bestimmt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**WinHTTP- \_ Abfrage \_ Speicherort**
</dt> <dd> <dl> <dt>



Ruft den absoluten URI ab, der in einem "Location"-Antwortheader verwendet wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**Max. WinHTTP- \_ Abfrage \_**
</dt> <dd> <dl> <dt>



Gibt den maximalen Wert eines WinHTTP- \_ Abfrage \_ \* Werts an. Kein abfrageflag.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**maximale WinHTTP-Abfrage-Weiterleitung \_ \_ \_**
</dt> <dd> <dl> <dt>



Ruft die Anzahl von Proxys oder Gateways ab, die die Anforderung an den nächsten eingehenden Server weiterleiten können.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**WinHTTP- \_ Abfrage nach \_ richten- \_ ID**
</dt> <dd> <dl> <dt>



Wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**WinHTTP \_ Query- \_ MIME- \_ Version**
</dt> <dd> <dl> <dt>



Empfängt die Version des Multipurpose Internet Mail Extensions (MIME)-Protokolls, das zum Erstellen der Nachricht verwendet wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**URI für WinHTTP- \_ Abfrage- \_ \_ URI**
</dt> <dd> <dl> <dt>



Veraltet. Wird für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**WinHTTP- \_ Abfrage- \_ pragma**
</dt> <dd> <dl> <dt>



Empfängt die Implementierungs spezifischen Direktiven, die ggf. für jeden Empfänger in der Anforderungs-/Antwortkette gelten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**Authentifizieren des WinHTTP- \_ Abfrage \_ Proxys \_**
</dt> <dd> <dl> <dt>



Ruft das vom Proxy zurückgegebene Authentifizierungsschema und den Bereich ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**WinHTTP- \_ Abfrage \_ Proxy- \_ Autorisierung**
</dt> <dd> <dl> <dt>



Ruft den Header ab, der verwendet wird, um den Benutzer für einen Proxy zu identifizieren, für den eine Authentifizierung erforderlich ist. Dieser Header kann nur abgerufen werden, bevor die Anforderung an den Server gesendet wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**WinHTTP- \_ Abfrage \_ Proxy \_ Verbindung**
</dt> <dd> <dl> <dt>



Ruft den Proxy-Connection-Header ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**Unterstützung für WinHTTP- \_ Abfrage \_ Proxy \_**
</dt> <dd> <dl> <dt>



Ruft den Proxy-Support-Header ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WinHTTP- \_ Abfrage \_ öffentlich**
</dt> <dd> <dl> <dt>



Empfängt auf diesem Server verfügbare HTTP-Verben.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**WinHTTP- \_ Abfrage \_ Bereich**
</dt> <dd> <dl> <dt>



Ruft den Byte Bereich einer Entität ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**unformatierte WinHTTP- \_ Abfrage \_ \_ Header**
</dt> <dd> <dl> <dt>



Empfängt alle vom Server zurückgegebenen Header. Jeder Header wird durch " \\ 0" beendet. Eine zusätzliche " \\ 0" beendet die Liste der Header.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**unformatierte WinHTTP- \_ Abfrage \_ \_ Header \_ CRLF**
</dt> <dd> <dl> <dt>



Empfängt alle vom Server zurückgegebenen Header. Jeder Header wird durch eine Wagen Rücklauf/Zeilenvorschub-Sequenz (CR/LF) getrennt.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**WinHTTP- \_ Abfrage \_ Verweis**
</dt> <dd> <dl> <dt>



Empfängt den URI der Ressource, in der der angeforderte URI abgerufen wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**WinHTTP- \_ Abfrage \_ Aktualisierung**
</dt> <dd> <dl> <dt>



Veraltet. Wird für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**WinHTTP- \_ Abfrage \_ Anforderungs \_ Methode**
</dt> <dd> <dl> <dt>



Empfängt das HTTP-Verb, das in der Anforderung verwendet wird, in der Regel Get oder Post.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**WinHTTP- \_ Abfrage \_ Wiederholung \_ nach**
</dt> <dd> <dl> <dt>



Ruft die Zeitspanne ab, die erwartet wird, dass der Dienst nicht verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**WinHTTP- \_ Abfrage \_ Server**
</dt> <dd> <dl> <dt>



Ruft Informationen über die Software ab, die vom Ursprungsserver zum Verarbeiten der Anforderung verwendet wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**WinHTTP- \_ Abfrage \_ Satz \_ Cookie**
</dt> <dd> <dl> <dt>



Empfängt den Wert des Cookies, der für die Anforderung festgelegt ist.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**WinHTTP- \_ Abfrage \_ Status \_ Code**
</dt> <dd> <dl> <dt>



Empfängt den vom Server zurückgegebenen Statuscode. Eine Liste möglicher Werte finden Sie unter [**http-Status Codes**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**Text des WinHTTP- \_ Abfrage \_ Status \_**
</dt> <dd> <dl> <dt>



Empfängt zusätzlichen Text, der vom Server in der Antwort Zeile zurückgegeben wird.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**WinHTTP- \_ Abfrage \_ Titel**
</dt> <dd> <dl> <dt>



Veraltet. Wird für die Legacy Anwendungs Kompatibilität beibehalten.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**Codieren von WinHTTP- \_ Abfrage \_ Übertragungen \_**
</dt> <dd> <dl> <dt>



Ruft den Typ der Transformation ab, die auf den Nachrichtentext angewendet wurde, sodass er sicher zwischen dem Absender und dem Empfänger übertragen werden kann.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**WinHTTP- \_ Abfrage, \_ sofern nicht \_ geändert \_ seit**
</dt> <dd> <dl> <dt>



Ruft den-nicht-Modified-Since-Header ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**WinHTTP- \_ Abfrage \_ Upgrade**
</dt> <dd> <dl> <dt>



Ruft die zusätzlichen Kommunikationsprotokolle ab, die vom Server unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**WinHTTP- \_ Abfrage- \_ URI**
</dt> <dd> <dl> <dt>



Empfängt einen oder alle der URI, mit dem die Request-URI-Ressource identifiziert werden kann.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**WinHTTP- \_ Abfrage \_ Benutzer- \_ Agent**
</dt> <dd> <dl> <dt>



Ruft Informationen über den Benutzer-Agent ab, der die Anforderung vorgenommen hat.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WinHTTP- \_ Abfrage \_ variiert**
</dt> <dd> <dl> <dt>



Ruft den Header ab, der angibt, dass die Entität mithilfe einer servergesteuerten Aushandlung aus einer Reihe von verfügbaren Darstellungen der Antwort ausgewählt wurde.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**WinHTTP- \_ Abfrage \_ Version**
</dt> <dd> <dl> <dt>



Ruft die HTTP-Version ab, die in der Statuszeile vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**WinHTTP- \_ Abfrage \_ über**
</dt> <dd> <dl> <dt>



Ruft die zwischen Protokolle und Empfänger zwischen dem Benutzer-Agent und dem Server bei Anforderungen sowie zwischen dem Ursprungsserver und dem Client bei Antworten ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**WinHTTP- \_ Abfrage \_ Warnung**
</dt> <dd> <dl> <dt>



Ruft zusätzliche Informationen über den Status einer Antwort ab, die möglicherweise nicht durch den Antwortstatus Code reflektiert werden.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WinHTTP- \_ Abfrage \_ www- \_ Authentifizierung**
</dt> <dd> <dl> <dt>



Ruft das vom Server zurückgegebene Authentifizierungsschema und den Bereich ab.


</dt> </dl> </dd> </dl>

Die Modifiziererflags werden zusammen mit einem attributflag verwendet, um die Anforderung zu ändern. Modifiziererflags ändern entweder das Format der zurückgegebenen Daten oder geben an, wo die [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) -Funktion nach den Informationen suchen soll.

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**WinHTTP \_ - \_ abfrageflagnummer \_**
</dt> <dd> <dl> <dt>



Gibt die Daten als 32-Bit-Zahl für Header zurück, deren Wert eine Zahl ist, z. b. der Statuscode.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**WinHTTP \_ - \_ abfrageflag- \_ Anforderungs \_ Header**
</dt> <dd> <dl> <dt>



Fragt nur Anforderungs Header ab.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WinHTTP \_ - \_ abfrageflag \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>



Gibt den Header Wert als [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur zurück, die die Anwendung nicht benötigt, um die Daten zu analysieren. Verwenden Sie für Header, deren Wert eine Datums-/uhrzeitzeile ist, z. b. "Last-modified-time".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>   |
| Header<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

