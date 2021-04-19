---
description: 'Weitere Informationen: WUA-Netzwerkfehler Codes'
ms.assetid: 07ff2ed7-09bc-4af7-84f9-66a921c0f53f
title: WUA-Netzwerkfehler Codes (wuerror. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fb2c027939afda3fe5817a8a860469fc90b766
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372622"
---
# <a name="wua-networking-error-codes"></a>WUA-Netzwerkfehler Codes

Die Windows Update-Agent-API (WUA) kann beim Ausführen von Netzwerk Vorgängen wie dem Suchen nach Updates die folgenden Fehlercodes zurückgeben:



| Konstante/Wert                                                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WU_E_WINHTTP_INVALID_FILE"></span><span id="wu_e_winhttp_invalid_file"></span><dl> <dt>**Wu \_ E \_ WinHTTP \_ ungültige \_ Datei**</dt> <dt>0x80240038</dt> </dl>                                  | Die heruntergeladene Datei weist einen unerwarteten Inhaltstyp auf.<br/>                                                                                                                               |
| <span id="WU_E_PT_HTTP_STATUS_BAD_REQUEST"></span><span id="wu_e_pt_http_status_bad_request"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ - \_ Status \_**</dt> ungültige Anforderung <dt>0x80244016</dt> </dl>              | Identisch mit HTTP-Status 400 – der Server konnte die Anforderung aufgrund einer ungültigen Syntax nicht verarbeiten.<br/>                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_DENIED"></span><span id="wu_e_pt_http_status_denied"></span><dl> <dt>**Wu \_ E \_ PT \_ http- \_ Status \_ verweigert**</dt> <dt>0x80244017</dt> </dl>                              | Identisch mit HTTP-Status 401 – für die angeforderte Ressource ist eine Benutzerauthentifizierung erforderlich.<br/>                                                                                                    |
| <span id="WU_E_PT_HTTP_STATUS_FORBIDDEN"></span><span id="wu_e_pt_http_status_forbidden"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ - \_ Status**</dt> unzulässig <dt>0x80244018</dt> </dl>                     | Identisch mit HTTP-Status 403 – der Server hat die Anforderung verstanden, lehnt aber dessen Erfüllung ab.<br/>                                                                                              |
| <span id="WU_E_PT_HTTP_STATUS_NOT_FOUND"></span><span id="wu_e_pt_http_status_not_found"></span><dl> <dt>**Wu \_ E \_ PT \_ http- \_ Status \_ nicht \_ gefunden**</dt> <dt>0x80244019</dt> </dl>                    | Identisch mit HTTP-Status 404 – der Server kann den angeforderten URI (Uniform Resource Identifier) nicht finden.<br/>                                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_BAD_METHOD"></span><span id="wu_e_pt_http_status_bad_method"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ - \_ Status \_**</dt> ungültige Methode <dt>0x8024401a</dt> </dl>                 | Identisch mit HTTP-Status 405 – die HTTP-Methode ist nicht zulässig.<br/>                                                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="wu_e_pt_http_status_proxy_auth_req"></span><dl> <dt>**Wu \_ E \_ PT \_ http- \_ Status \_ Proxy Authentifizierung \_ \_ req**</dt> <dt>0x8024401b</dt> </dl>    | Identisch mit HTTP-Status 407 – die Proxy Authentifizierung ist erforderlich.<br/>                                                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="wu_e_pt_http_status_request_timeout"></span><dl> <dt>**Wu \_ E \_ PT \_ http- \_ Status \_ Anforderung \_ Timeout**</dt> <dt>0x8024401c</dt> </dl>  | Identisch mit HTTP-Status 408 – Timeout des Servers beim Warten auf die Anforderung.<br/>                                                                                                           |
| <span id="WU_E_PT_HTTP_STATUS_CONFLICT"></span><span id="wu_e_pt_http_status_conflict"></span><dl> <dt>**Wu \_ E \_ PT \_ http- \_ Status \_ Konflikt**</dt> <dt>0x8024401d</dt> </dl>                        | Identisch mit HTTP-Status 409 – die Anforderung wurde aufgrund eines Konflikts mit dem aktuellen Zustand der Ressource nicht abgeschlossen.<br/>                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_GONE"></span><span id="wu_e_pt_http_status_gone"></span><dl> <dt>**Wu \_ \_Http- \_ \_ Status \_ "e PT**</dt> " ist <dt>0x8024401e</dt> </dl>                                    | Identisch mit HTTP-Status 410 – die angeforderte Ressource ist auf dem Server nicht mehr verfügbar.<br/>                                                                                                |
| <span id="WU_E_PT_HTTP_STATUS_SERVER_ERROR"></span><span id="wu_e_pt_http_status_server_error"></span><dl> <dt>**Wu \_ E \_ PT \_ http- \_ Status \_ Server \_ Fehler**</dt> <dt>0x8024401f</dt> </dl>           | Identisch mit HTTP-Status 500 – ein interner Fehler des Servers hat die Erfüllung der Anforderung verhindert.<br/>                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_NOT_SUPPORTED"></span><span id="wu_e_pt_http_status_not_supported"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ - \_ Status \_ wird nicht unterstützt**</dt> <dt>0x80244020</dt> </dl>        | Identisch mit HTTP-Status 501 – der Server unterstützt die Funktionalität, die zum erfüllen der Anforderung erforderlich ist, nicht. <br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_BAD_GATEWAY"></span><span id="wu_e_pt_http_status_bad_gateway"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ - \_ Status \_**</dt> ungültiges Gateway <dt>0x80244021</dt> </dl>              | Identisch mit HTTP-Status 502 – der Server hat beim fungieren als Gateway oder Proxy eine ungültige Antwort vom Upstreamserver empfangen, auf den er bei der Erfüllung der Anforderung zugegriffen hat.<br/> |
| <span id="WU_E_PT_HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="wu_e_pt_http_status_service_unavail"></span><dl> <dt>**Wu \_ E \_ PT \_ http- \_ Status \_ Dienst \_ nicht erreichbar**</dt> <dt>0x80244022</dt> </dl>  | Identisch mit HTTP-Status 503 – der Dienst ist vorübergehend überlastet.<br/>                                                                                                                  |
| <span id="WU_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="wu_e_pt_http_status_gateway_timeout"></span><dl> <dt>**Wu \_ E \_ PT \_ http- \_ Status \_ Gateway- \_ Timeout**</dt> <dt>0x80244023</dt> </dl>  | Identisch mit HTTP-Status 504 – bei der Anforderung ist beim Warten auf ein Gateway ein Timeout aufgetreten.<br/>                                                                                                        |
| <span id="WU_E_PT_HTTP_STATUS_VERSION_NOT_SUP"></span><span id="wu_e_pt_http_status_version_not_sup"></span><dl> <dt>**Wu \_ E \_ PT \_ http- \_ Status \_ Version \_ nicht \_ SUP**</dt> <dt>0x80244024</dt> </dl> | Identisch mit HTTP-Status 505 – die für die Anforderung verwendete HTTP-Protokollversion wird vom Server nicht unterstützt.<br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_NOT_MAPPED"></span><span id="wu_e_pt_http_status_not_mapped"></span><dl> <dt>**Wu \_ E \_ PT \_ http- \_ Status \_ nicht \_ zugeordnet**</dt> <dt>0x8024402b</dt> </dl>                 | Die Anforderung konnte nicht abgeschlossen werden, und der Grund entsprach keinem der Wu \_ E-http- \_ \_ \_ \* Fehlercodes.<br/>                                                               |
| <span id="WU_E_PT_WINHTTP_NAME_NOT_RESOLVED"></span><span id="wu_e_pt_winhttp_name_not_resolved"></span><dl> <dt>**Wu \_ E \_ PT- \_ WinHTTP- \_ Name \_ nicht \_ aufgelöst**</dt> <dt>0x8024402C</dt> </dl>        | Identisch mit \_ dem Fehler WinHTTP \_ -Name wurde nicht aufgelöst \_ \_ -der Proxy Server-oder Zielserver Name kann nicht aufgelöst werden.<br/>                                                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wuerror. h</dt> </dl> |



 

 




