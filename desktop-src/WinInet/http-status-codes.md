---
title: HTTP-Statuscodes (Wininet.h)
description: Die folgende Tabelle enthält die Konstanten und entsprechenden Werte für die HTTP-Statuscodes, die von Servern im Internet zurückgegeben werden.
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01c6a8fecf7d1c7b3f95c1d4ce8040b9ba25e7d72ee4a41c8cbbcd24cd0da4bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743808"
---
# <a name="http-status-codes-winineth"></a>HTTP-Statuscodes (Wininet.h)

Die folgende Tabelle enthält die Konstanten und entsprechenden Werte für die HTTP-Statuscodes, die von Servern im Internet zurückgegeben werden.

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP \_ STATUS \_ CONTINUE**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Die Anforderung kann fortgesetzt werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_ \_ HTTP-STATUSWECHSELPROTOKOLLE \_**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Der Server hat protokolle in einem Upgradeheader gewechselt.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**\_HTTP-STATUS \_ OK**
</dt> <dd> <dl> <dt>

200
</dt> <dt>



Die Anforderung wurde erfolgreich abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_HTTP-STATUS \_ ERSTELLT**
</dt> <dd> <dl> <dt>

201
</dt> <dt>



Die Anforderung wurde erfüllt und führte zur Erstellung einer neuen Ressource.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_HTTP-STATUS \_ AKZEPTIERT**
</dt> <dd> <dl> <dt>

202
</dt> <dt>



Die Anforderung wurde für die Verarbeitung akzeptiert, aber die Verarbeitung wurde nicht abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**\_HTTP-STATUS \_ PARTIAL**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



Die zurückgegebenen Metainformationen im Entitätsheader sind nicht der endgültige Satz, der vom Ursprungsserver verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**\_HTTP-STATUS \_ KEIN \_ INHALT**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



Der Server hat die Anforderung erfüllt, aber es gibt keine neuen Informationen, die zurückgesendet werden müssen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_HTTP STATUS RESET CONTENT \_ \_ (INHALT ZURÜCKSETZEN DES HTTP-STATUS)**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



Die Anforderung wurde abgeschlossen, und das Clientprogramm sollte die Dokumentansicht zurücksetzen, die dazu geführt hat, dass die Anforderung gesendet wurde, damit der Benutzer problemlos eine weitere Eingabeaktion initiieren kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**TEILINHALT \_ DES HTTP-STATUS \_ \_**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



Der Server hat die partielle GET-Anforderung für die Ressource erfüllt.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_HTTP-STATUS \_ MEHRDEUTIG**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



Der Server konnte nicht entscheiden, was zurückgegeben werden soll.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_HTTP-STATUS \_ VERSCHOBEN**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



Die angeforderte Ressource wurde einem neuen permanenten URI (Uniform Resource Identifier) zugewiesen, und alle zukünftigen Verweise auf diese Ressource sollten mithilfe einer der zurückgegebenen URIs erfolgen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**\_ \_ HTTP-STATUSUMLEITUNG**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



Die angeforderte Ressource befindet sich vorübergehend unter einem anderen URI (Uniform Resource Identifier).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**UMLEITUNGSMETHODE FÜR \_ HTTP-STATUS \_ \_**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



Die Antwort auf die Anforderung finden Sie unter einem anderen URI (Uniform Resource Identifier) und sollte mithilfe eines GET HTTP-Verbs für diese Ressource abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_HTTP-STATUS \_ NICHT \_ GEÄNDERT**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



Die angeforderte Ressource wurde nicht geändert.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_HTTP-STATUS \_ PROXY VERWENDEN \_**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



Der Zugriff auf die angeforderte Ressource muss über den Proxy erfolgen, der vom Feld location angegeben wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP \_ STATUS \_ REDIRECT \_ KEEP \_ VERB**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



Die umgeleitete Anforderung behält das gleiche HTTP-Verb bei. HTTP/1.1-Verhalten.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_ \_ HTTP-STATUS \_ UNGÜLTIGE ANFORDERUNG**
</dt> <dd> <dl> <dt>

400
</dt> <dt>



Die Anforderung konnte aufgrund einer ungültigen Syntax nicht vom Server verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**\_HTTP-STATUS \_ VERWEIGERT**
</dt> <dd> <dl> <dt>

401
</dt> <dt>



Für die angeforderte Ressource ist eine Benutzerauthentifizierung erforderlich.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP \_ STATUS \_ PAYMENT \_ REQ**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



Derzeit nicht im HTTP-Protokoll implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_HTTP-STATUS \_ VERBOTEN**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



Der Server hat die Anforderung verstanden, versucht jedoch, sie zu erfüllen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_HTTP-STATUS \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



Der Server hat nichts gefunden, das dem angeforderten URI (Uniform Resource Identifier) entspricht.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ UNGÜLTIGE \_ HTTP-STATUSMETHODE**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



Das verwendete HTTP-Verb ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_HTTP-STATUS \_ KEINE \_ AKZEPTABEL**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



Es wurden keine Antworten gefunden, die für den Client akzeptabel sind.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP \_ STATUS \_ PROXY \_ AUTH \_ REQ**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



Proxyauthentifizierung erforderlich.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ \_ HTTP-STATUSANFORDERUNGSTIMEOUT**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



Das Zeitlimit wurde beim Warten auf die Anforderung vom Server überschritten.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_ \_ HTTP-STATUSKONFLIKT**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



Die Anforderung konnte aufgrund eines Konflikts mit dem aktuellen Zustand der Ressource nicht abgeschlossen werden. Der Benutzer sollte weitere Informationen erneut übermitteln.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_HTTP-STATUS \_ NICHT MEHR**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



Die angeforderte Ressource ist auf dem Server nicht mehr verfügbar, und es ist keine Weiterleitungsadresse bekannt.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_HTTP-STATUSLÄNGE \_ \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



Der Server verweigert die Annahme der Anforderung ohne definierte Inhaltslänge.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_FEHLER BEI \_ HTTP-STATUS PRECOND \_**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



Die vorbedingung, die in einem oder mehreren Anforderungsheaderfeldern angegeben wurde, wurde beim Testen auf dem Server als FALSE ausgewertet.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_ \_ HTTP-STATUSANFORDERUNG \_ ZU \_ GROß**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



Der Server möchte eine Anforderung verarbeiten, da die Anforderungsentität größer ist als der Server bereit oder in der Lage ist, diese zu verarbeiten.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_HTTP-STATUS-URI \_ \_ ZU \_ LANG**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



Der Server versucht, die Anforderung zu bedienen, da der Anforderungs-URI (Uniform Resource Identifier) länger ist, als der Server interpretieren möchte.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_NICHT \_ UNTERSTÜTZTE \_ MEDIEN MIT HTTP-STATUS**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



Der Server kann die Anforderung nicht ausführen, da die Entität der Anforderung in einem Format vor liegt, das von der angeforderten Ressource für die angeforderte Methode nicht unterstützt wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**WIEDERHOLUNG \_ DES \_ HTTP-STATUS \_ MIT**
</dt> <dd> <dl> <dt>

449
</dt> <dt>



Die Anforderung sollte nach der entsprechenden Aktion wiederholt werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_ \_ HTTP-STATUSSERVERFEHLER \_**
</dt> <dd> <dl> <dt>

500
</dt> <dt>



Der Server hat eine unerwartete Bedingung festgestellt, die die Erfüllung der Anforderung verhindert hat.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_HTTP-STATUS \_ NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

501
</dt> <dt>



Der Server unterstützt nicht die Funktionalität, die zum Erfüllen der Anforderung erforderlich ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP \_ STATUS \_ BAD \_ GATEWAY**
</dt> <dd> <dl> <dt>

502
</dt> <dt>



Der Server hat als Gateway oder Proxy eine ungültige Antwort vom Upstreamserver erhalten, auf den er zugegriffen hat, um die Anforderung zu erfüllen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**\_HTTP-STATUSDIENST \_ NICHT \_ VERFÜGBAR**
</dt> <dd> <dl> <dt>

503
</dt> <dt>



Der Dienst ist zurzeit überlastet.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_ \_ \_ HTTP-STATUSGATEWAY-TIMEOUT**
</dt> <dd> <dl> <dt>

504
</dt> <dt>



Bei der Anforderung ist eine Zeitüberschreitung aufgetreten, während auf ein Gateway gewartet wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_HTTP-STATUSVERSION \_ NICHT \_ \_ SUP**
</dt> <dd> <dl> <dt>

505
</dt> <dt>



Der Server unterstützt die in der Anforderungsnachricht verwendete HTTP-Protokollversion nicht oder verweigert deren Unterstützung.


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



 

