---
title: HTTP_LOGGING_FLAG_ Konstanten (Http.h)
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
ms.openlocfilehash: 6ae84697d84295d137f929bcf0d65c2e49fc6754aa7c1110d3b341bb471cbcb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981440"
---
# <a name="http_logging_flag_-constants"></a>HTTP \_ LOGGING \_ \_ FLAG-Konstanten

Die **HTTP \_ LOGGING \_ \_ FLAG-Konstanten** definieren die Optionen zum Konfigurieren der Protokollierung für die HTTP-Server-API.

Diese Konstanten werden in der [**HTTP \_ LOGGING \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_logging_info) verwendet.

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**ROLLOVER \_ DER LOKALEN ZEIT DES \_ \_ \_ HTTP-PROTOKOLLIERUNGSFLAGS \_**
</dt> <dd> <dl> <dt>



Das Rollover der Protokolldatei basiert auf der Ortszeit. Standardmäßig basieren Protokolldateirollover auf koordinierter Weltzeit (UTC).


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**HTTP \_ \_ \_ PROTOKOLLIERUNGSFLAG: \_ UTF8-KONVERTIERUNG \_ VERWENDEN**
</dt> <dd> <dl> <dt>



Die Unicode-Felder werden beim Schreiben in die Protokolldateien in UTF8-Multibyte konvertiert. Standardmäßig werden die Protokolldateien mit der Konvertierung der lokalen Codepage geschrieben.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**NUR \_ PROTOKOLLFEHLER DES \_ \_ \_ \_ HTTP-PROTOKOLLIERUNGSFLAGS**
</dt> <dd> <dl> <dt>



Die Protokolldateien enthalten nur Fehlerinformationen. Standardmäßig werden sowohl Fehler- als auch Erfolgsantworten protokolliert. Wenn weder **DAS HTTP LOGGING FLAG LOG ERRORS \_ \_ \_ \_ \_ ONLY** noch das **HTTP LOGGING FLAG LOG SUCCESS \_ \_ \_ \_ \_ ONLY** festgelegt ist, werden sowohl Fehler- als auch Erfolgsinformationen protokolliert.

Dieses Flag kann nicht festgelegt werden, wenn auch das **FLAG HTTP LOGGING FLAG LOG SUCCESS \_ \_ \_ \_ \_ ONLY** festgelegt ist. Diese beiden Flags schließen sich gegenseitig aus.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**HTTP \_ \_PROTOKOLLIERUNGSFLAG \_ PROTOKOLL NUR \_ \_ ERFOLGREICH**
</dt> <dd> <dl> <dt>



Die Protokolldateien enthalten nur Erfolgsinformationen. Standardmäßig werden sowohl Fehler als auch Erfolgstransaktionen protokolliert. Wenn weder **DAS HTTP LOGGING FLAG LOG ERRORS \_ \_ \_ \_ \_ ONLY** noch das **HTTP LOGGING FLAG LOG SUCCESS \_ \_ \_ \_ \_ ONLY** festgelegt ist, werden sowohl Fehler- als auch Erfolgsinformationen protokolliert.

Dieses Flag kann nicht festgelegt werden, wenn auch das **Flag HTTP LOGGING FLAG LOG ERRORS \_ \_ \_ \_ \_ ONLY** festgelegt ist. Diese beiden Flags schließen sich gegenseitig aus.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[HTTP Server API Version 2.0-Konstanten](http-server-api-version-2-0-constants.md)
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

 

 





