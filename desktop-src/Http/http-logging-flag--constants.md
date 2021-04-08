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
# <a name="http_logging_flag_-constants"></a><span data-ttu-id="548c7-103">HTTP- \_ Protokollierungs Kennzeichen- \_ \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="548c7-103">HTTP\_LOGGING\_FLAG\_ Constants</span></span>

<span data-ttu-id="548c7-104">Die **http- \_ Protokollierungs \_ \_** Kennzeichen-Konstanten definieren die Optionen zum Konfigurieren der Protokollierung für die HTTP-Server-API.</span><span class="sxs-lookup"><span data-stu-id="548c7-104">The **HTTP\_LOGGING\_FLAG\_** constants define the options to configure logging on the HTTP Server API.</span></span>

<span data-ttu-id="548c7-105">Diese Konstanten werden in der [**http- \_ Protokollierungs \_ Informations**](/windows/desktop/api/Http/ns-http-http_logging_info) Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="548c7-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="548c7-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_ \_ \_ lokale \_ Zeit des \_ Rollovers der HTTP-Protokollierung**</span><span class="sxs-lookup"><span data-stu-id="548c7-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**HTTP\_LOGGING\_FLAG\_LOCAL\_TIME\_ROLLOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548c7-107">Der Protokoll Dateirollover basiert auf der lokalen Zeit.</span><span class="sxs-lookup"><span data-stu-id="548c7-107">The log file rollover is based on local time.</span></span> <span data-ttu-id="548c7-108">Standardmäßig basiert Protokoll Dateirollover auf der koordinierten Weltzeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="548c7-108">By default, log file rollovers is based on coordinated universal time (UTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548c7-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Http \_ \_ \_ \_ \_ Protokollierungsflag verwendet UTF8-Konvertierung**</span><span class="sxs-lookup"><span data-stu-id="548c7-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span> **HTTP\_LOGGING\_FLAG\_USE\_UTF8\_CONVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548c7-110">Die Unicode-Felder werden beim Schreiben in die Protokolldateien in UTF8-Multibytes konvertiert.</span><span class="sxs-lookup"><span data-stu-id="548c7-110">The unicode fields are converted to UTF8 multibytes when writting to the log files.</span></span> <span data-ttu-id="548c7-111">Standardmäßig werden die Protokolldateien mit der lokalen Code Page Konvertierung geschrieben.</span><span class="sxs-lookup"><span data-stu-id="548c7-111">By default, the log files are written with the local code page conversion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548c7-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP- \_ Protokollierungs Kennzeichen \_ \_ \_ nur Protokollfehler \_**</span><span class="sxs-lookup"><span data-stu-id="548c7-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548c7-113">Die Protokolldateien enthalten nur Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="548c7-113">The log files include error information only.</span></span> <span data-ttu-id="548c7-114">Standardmäßig werden sowohl Fehler-als auch Erfolgs Antworten protokolliert.</span><span class="sxs-lookup"><span data-stu-id="548c7-114">By default, both error and success responses are logged.</span></span> <span data-ttu-id="548c7-115">Wenn weder das **http \_ - \_ protokollierungsflag \_ \_ \_ nur Fehler protokollieren** oder das **http- \_ protokollierungsflag \_ \_ \_ \_ nur Erfolg** festlegen festgelegt ist, werden sowohl Fehler-als auch Erfolgs Informationen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="548c7-115">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="548c7-116">Dieses Flag kann nicht festgelegt werden, wenn das **http- \_ protokollierungsflag \_ nur " \_ \_ \_ nur erfolgreich" protokolliert** wird.</span><span class="sxs-lookup"><span data-stu-id="548c7-116">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** flag is also set.</span></span> <span data-ttu-id="548c7-117">Diese beiden Flags schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="548c7-117">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548c7-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Http \_ \_protokollierungsflag \_ \_ \_ nur Erfolg**</span><span class="sxs-lookup"><span data-stu-id="548c7-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span> **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548c7-119">Die Protokolldateien enthalten nur Erfolgs Informationen.</span><span class="sxs-lookup"><span data-stu-id="548c7-119">The log files include success information only.</span></span> <span data-ttu-id="548c7-120">Standardmäßig werden sowohl Fehler als auch Erfolgs Transaktionen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="548c7-120">By default, both errors and success transactions are logged.</span></span> <span data-ttu-id="548c7-121">Wenn weder das **http \_ - \_ protokollierungsflag \_ \_ \_ nur Fehler protokollieren** oder das **http- \_ protokollierungsflag \_ \_ \_ \_ nur Erfolg** festlegen festgelegt ist, werden sowohl Fehler-als auch Erfolgs Informationen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="548c7-121">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="548c7-122">Dieses Flag kann nicht festgelegt werden, wenn das Flag für das **http- \_ Protokollierungs Kennzeichen \_ \_ \_ \_ nur Protokollfehler** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="548c7-122">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** flag is also set.</span></span> <span data-ttu-id="548c7-123">Diese beiden Flags schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="548c7-123">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="548c7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="548c7-124">Requirements</span></span>



| <span data-ttu-id="548c7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="548c7-125">Requirement</span></span> | <span data-ttu-id="548c7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="548c7-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="548c7-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="548c7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="548c7-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="548c7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="548c7-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="548c7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="548c7-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="548c7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="548c7-131">Header</span><span class="sxs-lookup"><span data-stu-id="548c7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="548c7-132"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="548c7-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="548c7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="548c7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="548c7-134">HTTP-Server-API, Version 2,0, Konstanten</span><span class="sxs-lookup"><span data-stu-id="548c7-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="548c7-135">**HTTP- \_ Protokollierungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="548c7-135">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="548c7-136">**Httptarturlgroupproperty**</span><span class="sxs-lookup"><span data-stu-id="548c7-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="548c7-137">**Httpsetserversessionproperty**</span><span class="sxs-lookup"><span data-stu-id="548c7-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="548c7-138">**Httpqueryurlgroupproperty**</span><span class="sxs-lookup"><span data-stu-id="548c7-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="548c7-139">**Httpqueryserversessionproperty**</span><span class="sxs-lookup"><span data-stu-id="548c7-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





