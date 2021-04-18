---
title: HTTP_LOG_FIELD_ Konstanten (http. h)
description: Definieren Sie die Felder im W3C-Protokoll und in den Fehlerprotokollen.
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340992"
---
# <a name="http_log_field_-constants"></a>HTTP- \_ Protokoll \_ Feld \_ Konstanten

Die **http \_ - \_ Protokoll \_ Feld** Konstanten definieren die Felder im W3C-Protokoll und die Fehlerprotokolle.

Diese Konstanten werden in der [**http- \_ Protokollierungs \_ Informations**](/windows/desktop/api/Http/ns-http-http_logging_info) Struktur verwendet.

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_ \_ Feld \_ Datum des HTTP-Protokolls**
</dt> <dd> <dl> <dt>



Das Datum, an dem die Aktivität aufgetreten ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_ \_ Feld \_ Zeit für HTTP-Protokoll**
</dt> <dd> <dl> <dt>



Die Uhrzeit in koordinierter Weltzeit (UTC), zu der die Aktivität aufgetreten ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP \_ \_ -Protokollfeld \_ Client \_ -IP**
</dt> <dd> <dl> <dt>



Die IP-Adresse des Clients, der die Anforderung gestellt hat.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**Benutzer Name für das HTTP- \_ Protokoll \_ Feld \_ \_**
</dt> <dd> <dl> <dt>



Der Name des authentifizierten Benutzers, der auf den Server zugegriffen hat. Anonyme Benutzer werden durch einen Bindestrich gekennzeichnet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP- \_ Protokoll \_ Feld- \_ Website \_ Name**
</dt> <dd> <dl> <dt>



Der Name der Website, auf der der Protokolldatei Eintrag generiert wurde.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Http \_ \_ \_ Computer \_ Name für Protokollfeld**
</dt> <dd> <dl> <dt>



Der Name des Computers, auf dem der Protokolldatei Eintrag generiert wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP \_ \_ -Protokollfeld \_ Server \_ -IP**
</dt> <dd> <dl> <dt>



Die IP-Adresse des Servers, auf dem der Protokolldatei Eintrag generiert wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP- \_ Protokoll \_ Feld \_ Methode**
</dt> <dd> <dl> <dt>



Die angeforderte Aktion, z. b. eine Get-Methode.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Http \_ \_URI- \_ \_ Stamm des Protokoll Felds**
</dt> <dd> <dl> <dt>



Das Ziel der Aktion, z. b. Default.htm.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**URI-Abfrage für HTTP- \_ Protokoll \_ Feld \_ \_**
</dt> <dd> <dl> <dt>



Die Abfrage, die der Client auszuführen versucht hat, falls vorhanden. Eine Abfrage-URI (Universal Resource Identifier) ist nur für dynamische Seiten erforderlich.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**Status des HTTP- \_ Protokoll \_ Felds \_**
</dt> <dd> <dl> <dt>



Der HTTP-Statuscode.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**Win32-Status des HTTP- \_ Protokoll \_ Felds \_ \_**
</dt> <dd> <dl> <dt>



Der Windows-Statuscode.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_gesendete HTTP-Protokoll \_ Feld \_ Bytes \_**
</dt> <dd> <dl> <dt>



Die Nummer in Bytes, die vom Server gesendet wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP- \_ Protokoll \_ Feld ( \_ Bytes \_ )**
</dt> <dd> <dl> <dt>



Die Nummer in Bytes, die vom Server empfangen wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**Zeit für das HTTP- \_ Protokoll \_ Feld \_ \_**
</dt> <dd> <dl> <dt>



Die Zeit (in Millisekunden) der Aktion.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP- \_ Protokoll \_ Feld- \_ \_ Serverport**
</dt> <dd> <dl> <dt>



Die für den Dienst konfigurierte Server Portnummer.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Http \_ Protokoll \_ Feld \_ Benutzer- \_ Agent**
</dt> <dd> <dl> <dt>



Die Anwendung, die vom Client verwendet wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP- \_ Protokoll \_ Feld \_ Cookie**
</dt> <dd> <dl> <dt>



Der Inhalt des gesendeten oder empfangenen Cookies, sofern vorhanden.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP- \_ Protokoll \_ Feld \_ Verweis**
</dt> <dd> <dl> <dt>



Die Website, die der Benutzer zuletzt besucht hat. Diese Website stellte eine Verknüpfung zur aktuellen Website her.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP- \_ Protokoll \_ Feld \_ Version**
</dt> <dd> <dl> <dt>



Die vom Client verwendete HTTP-Protokollversion.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP- \_ Protokoll \_ Feld \_ Host**
</dt> <dd> <dl> <dt>



Der Host Header Name (sofern vorhanden).


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**unter Status des HTTP- \_ Protokoll \_ Felds \_ \_**
</dt> <dd> <dl> <dt>



Der unter Status-Fehlercode.


</dt> </dl> </dd> </dl>

Die folgenden Konstanten werden für die HTTP-Fehler Protokollierung verwendet.

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP- \_ Protokoll \_ Feld- \_ \_ ClientPort**
</dt> <dd> <dl> <dt>



Die Client Portnummer, von der die Anforderung empfangen wird. Dieses Protokollfeld wird nur für die Fehler Protokollierung verwendet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**URI für HTTP- \_ Protokoll \_ Feld \_**
</dt> <dd> <dl> <dt>



Der in der Anforderung empfangene URI, einschließlich des Abfrage Teils. Dieses Protokollfeld wird nur für die Fehler Protokollierung verwendet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**Website-ID für HTTP- \_ Protokoll \_ Feld \_ \_**
</dt> <dd> <dl> <dt>



Die anwendungsspezifische numerische ID der URL-Gruppe, an die die Anforderung weitergeleitet wird. Dieses Protokollfeld wird nur für die Fehler Protokollierung verwendet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**Grund für HTTP- \_ Protokoll \_ Feld \_**
</dt> <dd> <dl> <dt>



Der Fehlerursachen Ausdruck. Dieses Protokollfeld wird nur für die Fehler Protokollierung verwendet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**\_ \_ \_ Warteschlangen \_ Name für http-Protokollfeld**
</dt> <dd> <dl> <dt>



Der Name der Anforderungs Warteschlange, an die die Anforderung gesendet wird. Dieses Protokollfeld wird nur für die Fehler Protokollierung verwendet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP- \_ Protokoll \_ Feld- \_ streamid**
</dt> <dd> <dl> <dt>



Die Datenstrom-ID.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[HTTP-Server-API, Version 2,0, Konstanten](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**HTTP- \_ Protokollierungs \_ Informationen**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**Httptarturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**Httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**Httpqueryurlgroupproperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**Httpqueryserversessionproperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





