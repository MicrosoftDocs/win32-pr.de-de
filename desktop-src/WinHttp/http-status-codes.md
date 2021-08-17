---
description: Diese Konstanten und entsprechenden Werte geben HTTP-Statuscodes an, die von Servern im Internet zurückgegeben werden.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: HTTP-Statuscodes (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86f145a2a7b5f7e807d1b393d9c4fd9b4f71c81052f0f023a04f72e139842637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744571"
---
# <a name="http-status-codes-winhttph"></a>HTTP-Statuscodes (Winhttp.h)

Diese Konstanten und entsprechenden Werte geben HTTP-Statuscodes an, die von Servern im Internet zurückgegeben werden.

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_HTTP-STATUS \_ CONTINUE**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Die Anforderung kann fortgesetzt werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**PROTOKOLLE FÜR \_ \_ HTTP-STATUSWECHSEL \_**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Der Server hat protokolle in einem Upgradeheader umgeschaltet.


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



Die Anforderung wurde zur Verarbeitung akzeptiert, aber die Verarbeitung wurde nicht abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP \_ STATUS \_ PARTIAL**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



Die zurückgegebenen Metainformationen im Entitätsheader sind nicht die endgültige Menge, die vom Ursprungsserver verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**\_HTTP-STATUS \_ KEIN \_ INHALT**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



Der Server hat die Anforderung erfüllt, aber es gibt keine neuen Informationen, die zurück gesendet werden müssen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**INHALT DER \_ HTTP-STATUSZURÜCKSETZUNG \_ \_**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



Die Anforderung wurde abgeschlossen, und das Clientprogramm sollte die Dokumentansicht zurücksetzen, die dazu führte, dass die Anforderung gesendet wurde, damit der Benutzer problemlos eine weitere Eingabeaktion initiieren kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**TEILINHALT \_ DES \_ \_ HTTP-STATUS**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



Der Server hat die teilielle GET-Anforderung für die Ressource erfüllt.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP \_ STATUS \_ WEBDAV \_ MULTI \_ STATUS**
</dt> <dd> <dl> <dt>

207
</dt> <dt>



Während eines World Wide Web WebDAV-Vorgangs (Distributed Authoring and Versioning) gibt dies mehrere Statuscodes für eine einzelne Antwort an. Der Antwortkörper enthält Extensible Markup Language (XML), die die Statuscodes beschreibt. Weitere Informationen finden Sie unter [HTTP-Erweiterungen für die verteilte Erstellung.](../webdav/webdav-portal.md)


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_HTTP-STATUS \_ MEHRDEUTIG**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



Die angeforderte Ressource ist an einem oder mehreren Standorten verfügbar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_HTTP-STATUS \_ VERSCHOBEN**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



Die angeforderte Ressource wurde einem neuen permanenten Uniform Resource Identifier (URI) zugewiesen, und alle zukünftigen Verweise auf diese Ressource sollten mithilfe eines der zurückgegebenen URIs erfolgen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**UMLEITUNG DES \_ \_ HTTP-STATUS**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



Die angeforderte Ressource befindet sich vorübergehend unter einem anderen URI.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_ \_ HTTP-STATUSUMLEITUNGSMETHODE \_**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



Die Antwort auf die Anforderung kann unter einem anderen URI gefunden werden und sollte mithilfe eines [*GET-HTTP-Verbs*](glossary.md) für diese Ressource abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_HTTP-STATUS \_ NICHT \_ GEÄNDERT**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



Die angeforderte Ressource wurde nicht geändert.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_HTTP-STATUS– \_ PROXY \_ VERWENDEN**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



Auf die angeforderte Ressource muss über den Proxy zugegriffen werden, der durch das Feld location angegeben wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_ \_ HTTP-STATUSUMLEITUNG– \_ \_ KEEP-VERB**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



Die umgeleitete Anforderung behält das gleiche [*HTTP-Verb bei.*](glossary.md) HTTP/1.1-Verhalten.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_HTTP-STATUS \_ : ANFORDERUNG \_ "BAD"**
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

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**REQ \_ DER \_ \_ HTTP-STATUSZAHLUNG**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



Nicht im HTTP-Protokoll implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_HTTP-STATUS \_ VERBOTEN**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



Der Server hat die Anforderung verstanden, kann sie jedoch nicht erfüllen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_HTTP-STATUS \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



Der Server hat nichts gefunden, das dem angeforderten URI entspricht.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP \_ STATUS \_ BAD \_ METHOD**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



Das [*verwendete HTTP-Verb*](glossary.md) ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_HTTP-STATUS \_ KEINE \_ AKZEPTABEL**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



Es wurden keine antworten gefunden, die für den Client akzeptabel sind.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**\_ \_ \_ HTTP-STATUSPROXY-AUTHENTIFIZIERUNGS-REQ \_**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



Proxyauthentifizierung erforderlich.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**TIMEOUT \_ FÜR \_ \_ HTTP-STATUSANFORDERUNG**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



Das Zeitlimit wurde beim Warten auf die Anforderung vom Server überschritten.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_ \_ HTTP-STATUSKONFLIKT**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



Die Anforderung konnte aufgrund eines Konflikts mit dem aktuellen Zustand der Ressource nicht abgeschlossen werden. Der Benutzer sollte weitere Informationen erneut senden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_HTTP-STATUS \_ NICHT MEHR VERFÜGBAR**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



Die angeforderte Ressource ist auf dem Server nicht mehr verfügbar, und es ist keine Weiterleitungsadresse bekannt.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_HTTP-STATUSLÄNGE \_ \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



Der Server kann die Anforderung nicht ohne eine definierte Inhaltslänge akzeptieren.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**FEHLER \_ BEIM \_ HTTP-STATUS "PRECOND" \_**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



Die in einem oder mehr der Anforderungsheaderfelder gegebene Vorbedingung wurde beim Testen auf dem Server als FALSE ausgewertet.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_HTTP-STATUSANFORDERUNG \_ ZU \_ \_ GROß**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



Der Server kann die Anforderung nicht verarbeiten, da die Anforderungsentität größer ist, als der Server verarbeiten kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_ \_ HTTP-STATUS-URI \_ ZU \_ LANG**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



Der Server kann die Anforderung nicht warten, da der Anforderungs-URI länger ist, als der Server interpretieren kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**NICHT \_ UNTERSTÜTZTE \_ \_ HTTP-STATUSMEDIEN**
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



Der Server unterstützt nicht die HTTP-Protokollversion, die in der Anforderungsnachricht verwendet wurde.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional nur mit \[ SP3-Desktop-Apps\]<br/>      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000 Server nur mit \[ SP3-Desktop-Apps\]<br/>   |
| Header<br/>                   | <dl> <dt>Winhttp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WinHTTP-Versionen](winhttp-versions.md)
</dt> </dl>

 

