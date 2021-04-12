---
description: Diese Konstanten und entsprechenden Werte geben die von Servern im Internet zurückgegebenen HTTP-Statuscodes an.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: HTTP-Status Codes (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf4103cdc382bd5ab0d582fe99212083e2780ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216710"
---
# <a name="http-status-codes-winhttph"></a>HTTP-Status Codes (WinHTTP. h)

Diese Konstanten und entsprechenden Werte geben die von Servern im Internet zurückgegebenen HTTP-Statuscodes an.

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP- \_ Status \_ fortsetzen**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Die Anforderung kann fortgesetzt werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP- \_ Status \_ Schalter \_ Protokolle**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Der Server hat die Protokolle in einem Upgradeheader geändert.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP- \_ Status \_ OK**
</dt> <dd> <dl> <dt>

200
</dt> <dt>



Die Anforderung wurde erfolgreich abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP- \_ Status \_ erstellt**
</dt> <dd> <dl> <dt>

201
</dt> <dt>



Die Anforderung wurde erfüllt und führte zur Erstellung einer neuen Ressource.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP- \_ Status \_ akzeptiert**
</dt> <dd> <dl> <dt>

202
</dt> <dt>



Die Anforderung wurde zur Verarbeitung angenommen, die Verarbeitung wurde jedoch noch nicht abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP- \_ Status \_ partiell**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



Die zurückgegebenen Meta-Informationen im Entitäts Header sind nicht die definitive Menge, die auf dem Ursprungsserver verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP- \_ Status " \_ kein \_ Inhalt"**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



Der Server hat die Anforderung erfüllt, aber es sind keine neuen Informationen zum Zurücksenden vorhanden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**Inhalt des HTTP- \_ Status \_ Zurücksetzen \_**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



Die Anforderung wurde abgeschlossen, und das Client Programm sollte die Dokument Ansicht zurücksetzen, die bewirkt hat, dass die Anforderung gesendet wurde, damit der Benutzer problemlos eine andere Eingabe Aktion initiieren kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ Teil \_ Inhalt des HTTP-Status**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



Der Server hat die partielle Get-Anforderung für die Ressource erfüllt.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP- \_ Status \_ WebDAV- \_ \_ Multistatus**
</dt> <dd> <dl> <dt>

207
</dt> <dt>



Während eines WebDAV-Vorgangs (World Wide Web verteilte Erstellung und Versionsverwaltung) gibt dies mehrere Statuscodes für eine einzelne Antwort an. Der Antworttext enthält Extensible Markup Language (XML), der die Statuscodes beschreibt. Weitere Informationen finden Sie unter [http Extensions for verteilte Authoring](../webdav/webdav-portal.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP- \_ Status \_ mehrdeutig**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



Die angeforderte Ressource ist an einem oder mehreren Standorten verfügbar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP- \_ Status \_ verschoben**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



Die angeforderte Ressource wurde einem neuen permanenten Uniform Resource Identifier (URI) zugewiesen, und zukünftige Verweise auf diese Ressource sollten mithilfe eines der zurückgegebenen URIs durchgeführt werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP- \_ Status \_ Umleitung**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



Die angeforderte Ressource befindet sich vorübergehend unter einem anderen URI.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP- \_ Status \_ Umleitungs \_ Methode**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



Die Antwort auf die Anforderung befindet sich unter einem anderen URI und sollte mit einem get [*http-Verb*](glossary.md) für diese Ressource abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP- \_ Status \_ nicht \_ geändert**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



Die angeforderte Ressource wurde nicht geändert.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP \_ - \_ Status \_ Proxy verwenden**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



Der Zugriff auf die angeforderte Ressource muss über den Proxy erfolgen, der durch das Feld Speicherort angegeben wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**Keep-Verb für HTTP- \_ Status \_ Umleitung \_ \_**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



Die umgeleitete Anforderung behält dasselbe [*http-Verb*](glossary.md)bei. HTTP/1.1-Verhalten.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP-Status ungültige \_ \_ \_ Anforderung**
</dt> <dd> <dl> <dt>

400
</dt> <dt>



Die Anforderung konnte vom Server aufgrund einer ungültigen Syntax nicht verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP- \_ Status \_ verweigert**
</dt> <dd> <dl> <dt>

401
</dt> <dt>



Für die angeforderte Ressource ist eine Benutzerauthentifizierung erforderlich.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP- \_ Status \_ Zahlung \_ req**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



Nicht im HTTP-Protokoll implementiert.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP- \_ Status unzulässig \_**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



Der Server hat die Anforderung verstanden, kann Sie aber nicht erfüllen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP- \_ Status \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



Der Server hat nichts gefunden, das mit dem angeforderten URI übereinstimmt.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP-Status fehlerhafter \_ \_ \_ Methode**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



Das verwendete [*http-Verb*](glossary.md) ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP- \_ Status \_ keine \_ akzeptabel**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



Es wurden keine für den Client akzeptablen Antworten gefunden.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP- \_ Status \_ Proxy Authentifizierung \_ \_ req**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



Proxy Authentifizierung erforderlich.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**Timeout für HTTP- \_ Status \_ Anforderung \_**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



Das Zeitlimit wurde beim Warten auf die Anforderung vom Server überschritten.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP- \_ Status \_ Konflikt**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



Die Anforderung konnte aufgrund eines Konflikts mit dem aktuellen Zustand der Ressource nicht abgeschlossen werden. Der Benutzer sollte erneut mit weiteren Informationen übermitteln.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP- \_ Status ist \_ abgelaufen**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



Die angeforderte Ressource ist auf dem Server nicht mehr verfügbar, und es ist keine Weiterleitungsadresse bekannt.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP- \_ Status \_ Länge \_ erforderlich**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



Der Server kann die Anforderung ohne definierte Inhalts Länge nicht akzeptieren.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**Fehler beim http \_ -Status " \_ pred". \_**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



Die Vorbedingung, die in mindestens einem Anforderungs Header Feld angegeben wurde, wurde beim Testen auf dem Server als "false" ausgewertet.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP- \_ Status \_ Anforderung \_ zu \_ groß**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



Der Server kann die Anforderung nicht verarbeiten, da die Anforderungs Entität größer ist, als der Server verarbeiten kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP- \_ Status- \_ URI \_ zu \_ lang**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



Der Server kann die Anforderung nicht verarbeiten, da der Anforderungs-URI länger ist, als vom Server interpretiert werden kann.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_ \_ nicht unterstützte HTTP-Status \_ Medien**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



Der Server kann die Anforderung nicht bedienen, weil die Entität der Anforderung in einem Format vorliegt, das von der angeforderten Ressource für die angeforderte Methode nicht unterstützt wird.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP- \_ Status \_ Wiederholung \_ mit**
</dt> <dd> <dl> <dt>

449
</dt> <dt>



Die Anforderung sollte erneut versucht werden, nachdem Sie die entsprechende Aktion ausgeführt hat.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP- \_ Status \_ Server \_ Fehler**
</dt> <dd> <dl> <dt>

500
</dt> <dt>



Der Server hat eine unerwartete Bedingung feststellen, die die Erfüllung der Anforderung verhindert hat.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP \_ - \_ Status \_ wird nicht unterstützt**
</dt> <dd> <dl> <dt>

501
</dt> <dt>



Der Server unterstützt die erforderliche Funktionalität zum erfüllen der Anforderung nicht.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP-Status ungültiges \_ \_ \_ Gateway**
</dt> <dd> <dl> <dt>

502
</dt> <dt>



Der Server hat beim fungieren als Gateway oder Proxy eine ungültige Antwort vom Upstreamserver empfangen, auf den er bei dem Versuch zugegriffen hat, die Anforderung zu erfüllen.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP- \_ Status \_ Dienst \_ nicht erreichbar**
</dt> <dd> <dl> <dt>

503
</dt> <dt>



Der Dienst ist zurzeit überlastet.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP- \_ Status \_ Gateway- \_ Timeout**
</dt> <dd> <dl> <dt>

504
</dt> <dt>



Bei der Anforderung ist eine Zeitüberschreitung aufgetreten, während auf ein Gateway gewartet wurde.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP- \_ Status \_ Version \_ nicht \_ SUP**
</dt> <dd> <dl> <dt>

505
</dt> <dt>



Die in der Anforderungs Nachricht verwendete HTTP-Protokollversion wird vom Server nicht unterstützt.


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

 

