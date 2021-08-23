---
title: HTTP_LOG_FIELD_ Konstanten (Http.h)
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
ms.openlocfilehash: 616caaed9829c7f926f95f8982033457e1835a6beccfcad8313f6624d68195db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950829"
---
# <a name="http_log_field_-constants"></a>HTTP \_ LOG \_ \_ FIELD-Konstanten

Die **HTTP \_ LOG \_ \_ FIELD-Konstanten** definieren die Felder im W3C-Protokoll und in den Fehlerprotokollen.

Diese Konstanten werden in der [**HTTP \_ LOGGING \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_logging_info) verwendet.

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_DATUM DES HTTP-PROTOKOLLFELDS \_ \_**
</dt> <dd> <dl> <dt>



Das Datum, an dem die Aktivität aufgetreten ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**FELDZEIT \_ DES HTTP-PROTOKOLLS \_ \_**
</dt> <dd> <dl> <dt>



Die Zeit in koordinierter Weltzeit (UTC), zu der die Aktivität aufgetreten ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**CLIENT-IP DES \_ HTTP-PROTOKOLLFELDS \_ \_ \_**
</dt> <dd> <dl> <dt>



Die IP-Adresse des Clients, der die Anforderung gestellt hat.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_BENUTZERNAME DES HTTP-PROTOKOLLFELDS \_ \_ \_**
</dt> <dd> <dl> <dt>



Der Name des authentifizierten Benutzers, der auf Ihren Server zugegriffen hat. Anonyme Benutzer werden durch einen Bindestrich gekennzeichnet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**WEBSITENAME \_ DES HTTP-PROTOKOLLFELDS \_ \_ \_**
</dt> <dd> <dl> <dt>



Der Name des Standorts, an dem der Protokolldateieintrag generiert wurde.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**HTTP \_ COMPUTERNAME \_ DES \_ PROTOKOLLFELDS \_**
</dt> <dd> <dl> <dt>



Der Name des Computers, auf dem der Protokolldateieintrag generiert wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**IP DES \_ HTTP-PROTOKOLLFELDSERVERS \_ \_ \_**
</dt> <dd> <dl> <dt>



Die IP-Adresse des Servers, auf dem der Protokolldateieintrag generiert wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP \_ LOG \_ \_ FIELD-METHODE**
</dt> <dd> <dl> <dt>



Die angeforderte Aktion, z. B. eine get-Methode.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**HTTP \_ LOG \_ FIELD \_ URI \_ STEM**
</dt> <dd> <dl> <dt>



Das Ziel der Aktion, z. B. Default.htm.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**HTTP \_ LOG \_ FIELD \_ URI \_ QUERY**
</dt> <dd> <dl> <dt>



Die Abfrage, sofern vorhanden, die der Client ausführen wollte. Eine Abfrage-URI (Universal Resource Identifier) ist nur für dynamische Seiten erforderlich.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_STATUS DES HTTP-PROTOKOLLFELDS \_ \_**
</dt> <dd> <dl> <dt>



Der HTTP-Statuscode.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_HTTP-PROTOKOLLFELD \_ \_ WIN32-STATUS \_**
</dt> <dd> <dl> <dt>



Der Windows Statuscode.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_GESENDETE BYTES DES HTTP-PROTOKOLLFELDS \_ \_ \_**
</dt> <dd> <dl> <dt>



Die Zahl in Bytes, die vom Server gesendet wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP \_ LOG \_ FIELD \_ BYTES \_ RECV**
</dt> <dd> <dl> <dt>



Die Zahl in Bytes, die vom Server empfangen wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**\_DAUER DES HTTP-PROTOKOLLFELDS \_ \_ \_**
</dt> <dd> <dl> <dt>



Die Zeit der Aktion in Millisekunden.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP \_ LOG \_ FIELD \_ SERVER \_ PORT**
</dt> <dd> <dl> <dt>



Die Serverportnummer, die für den Dienst konfiguriert ist.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**HTTP \_ \_ \_ \_ PROTOKOLLFELDBENUTZER-AGENT**
</dt> <dd> <dl> <dt>



Die Anwendung, die vom Client verwendet wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP \_ LOG \_ FIELD \_ COOKIE**
</dt> <dd> <dl> <dt>



Der Inhalt des gesendeten oder empfangenen Cookies, sofern vorhanden.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP \_ LOG \_ FIELD \_ REFERER**
</dt> <dd> <dl> <dt>



Die Website, die der Benutzer zuletzt besucht hat. Diese Website stellte eine Verknüpfung zur aktuellen Website her.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**VERSION \_ DES HTTP-PROTOKOLLFELDS \_ \_**
</dt> <dd> <dl> <dt>



Die vom Client verwendete HTTP-Protokollversion.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP \_ LOG \_ FIELD \_ HOST**
</dt> <dd> <dl> <dt>



Der Hostheadername, falls vorhanden.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**\_ \_ UNTERSTATUS DES HTTP-PROTOKOLLFELDS \_ \_**
</dt> <dd> <dl> <dt>



Der Unterstatusfehlercode.


</dt> </dl> </dd> </dl>

Die folgenden Konstanten werden für die HTTP-Fehlerprotokollierung verwendet.

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**CLIENTPORT \_ DES HTTP-PROTOKOLLFELDS \_ \_ \_**
</dt> <dd> <dl> <dt>



Die Clientportnummer, von der die Anforderung empfangen wird. Dieses Protokollfeld wird nur für die Fehlerprotokollierung verwendet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**HTTP \_ LOG \_ FIELD \_ URI**
</dt> <dd> <dl> <dt>



Der in der Anforderung empfangene URI einschließlich des Abfrageteils. Dieses Protokollfeld wird nur für die Fehlerprotokollierung verwendet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_WEBSITE-ID DES HTTP-PROTOKOLLFELDS \_ \_ \_**
</dt> <dd> <dl> <dt>



Die anwendungsspezifische numerische ID der URL-Gruppe, an die die Anforderung weitergeleitet wird. Dieses Protokollfeld wird nur für die Fehlerprotokollierung verwendet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**GRUND FÜR DAS \_ HTTP-PROTOKOLLFELD \_ \_**
</dt> <dd> <dl> <dt>



Die Fehlerursachenphrase. Dieses Protokollfeld wird nur für die Fehlerprotokollierung verwendet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**HTTP \_ LOG \_ FIELD \_ QUEUE \_ NAME**
</dt> <dd> <dl> <dt>



Der Name der Anforderungswarteschlange, an die die Anforderung gesendet wird. Dieses Protokollfeld wird nur für die Fehlerprotokollierung verwendet.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP \_ LOG \_ FIELD \_ STREAMID**
</dt> <dd> <dl> <dt>



Die Stream-ID.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[HTTP-Server-API- Version 2.0-Konstanten](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_HTTP-PROTOKOLLIERUNGSINFORMATIONEN \_**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





