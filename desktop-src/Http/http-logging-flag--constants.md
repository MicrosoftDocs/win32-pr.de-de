---
title: HTTP_LOGGING_FLAG_ Konstanten (http. h)
description: Definieren Sie die Optionen zum Konfigurieren der Protokollierung für die HTTP-Server-API.
ms.assetid: b6afef7a-5426-4ccd-9785-169e83812c07
topic_type:
- apiref
api_name:
- HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER
- HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION
- HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY
- HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c501fc3ab646ab65fa039a5ff5e7d2dc0578002a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742504"
---
# <a name="http_logging_flag_-constants"></a>HTTP- \_ Protokollierungs Kennzeichen- \_ \_ Konstanten

Die **http- \_ Protokollierungs \_ \_** Kennzeichen-Konstanten definieren die Optionen zum Konfigurieren der Protokollierung für die HTTP-Server-API.

Diese Konstanten werden in der [**http- \_ Protokollierungs \_ Informations**](/windows/desktop/api/Http/ns-http-http_logging_info) Struktur verwendet.

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_ \_ \_ lokale \_ Zeit des \_ Rollovers der HTTP-Protokollierung**
</dt> <dd> <dl> <dt>



Der Protokoll Dateirollover basiert auf der lokalen Zeit. Standardmäßig basiert Protokoll Dateirollover auf der koordinierten Weltzeit (UTC).


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Http \_ \_ \_ \_ \_ Protokollierungsflag verwendet UTF8-Konvertierung**
</dt> <dd> <dl> <dt>



Die Unicode-Felder werden beim Schreiben in die Protokolldateien in UTF8-Multibytes konvertiert. Standardmäßig werden die Protokolldateien mit der lokalen Code Page Konvertierung geschrieben.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP- \_ Protokollierungs Kennzeichen \_ \_ \_ nur Protokollfehler \_**
</dt> <dd> <dl> <dt>



Die Protokolldateien enthalten nur Fehlerinformationen. Standardmäßig werden sowohl Fehler-als auch Erfolgs Antworten protokolliert. Wenn weder das **http \_ - \_ protokollierungsflag \_ \_ \_ nur Fehler protokollieren** oder das **http- \_ protokollierungsflag \_ \_ \_ \_ nur Erfolg** festlegen festgelegt ist, werden sowohl Fehler-als auch Erfolgs Informationen protokolliert.

Dieses Flag kann nicht festgelegt werden, wenn das **http- \_ protokollierungsflag \_ nur " \_ \_ \_ nur erfolgreich" protokolliert** wird. Diese beiden Flags schließen sich gegenseitig aus.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Http \_ \_protokollierungsflag \_ \_ \_ nur Erfolg**
</dt> <dd> <dl> <dt>



Die Protokolldateien enthalten nur Erfolgs Informationen. Standardmäßig werden sowohl Fehler als auch Erfolgs Transaktionen protokolliert. Wenn weder das **http \_ - \_ protokollierungsflag \_ \_ \_ nur Fehler protokollieren** oder das **http- \_ protokollierungsflag \_ \_ \_ \_ nur Erfolg** festlegen festgelegt ist, werden sowohl Fehler-als auch Erfolgs Informationen protokolliert.

Dieses Flag kann nicht festgelegt werden, wenn das Flag für das **http- \_ Protokollierungs Kennzeichen \_ \_ \_ \_ nur Protokollfehler** festgelegt ist. Diese beiden Flags schließen sich gegenseitig aus.


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

 

 





