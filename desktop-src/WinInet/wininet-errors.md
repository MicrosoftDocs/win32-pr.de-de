---
title: Fehlermeldungen (WinInet. h)
description: In den WinInet-Funktionen werden ggf. Fehlercodes zurückgegeben. Die folgenden Fehler sind spezifisch für die WinInet-Funktionen.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106460"
---
# <a name="error-messages-winineth"></a><span data-ttu-id="34b17-104">Fehlermeldungen (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="34b17-104">Error Messages (Wininet.h)</span></span>

<span data-ttu-id="34b17-105">In den WinInet-Funktionen werden ggf. Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34b17-105">The WinINet functions return error codes where appropriate.</span></span> <span data-ttu-id="34b17-106">Die folgenden Fehler sind spezifisch für die WinInet-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="34b17-106">The following errors are specific to the WinINet functions.</span></span>

<dl> <dt>

<span data-ttu-id="34b17-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**Fehler beim Löschen von \_ FTP \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERROR\_FTP\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-108">12111</span><span class="sxs-lookup"><span data-stu-id="34b17-108">12111</span></span>
</dt> <dt>



<span data-ttu-id="34b17-109">Der FTP-Vorgang wurde nicht abgeschlossen, da die Sitzung abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="34b17-109">The FTP operation was not completed because the session was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**Fehler " \_ FTP \_ nicht \_ passiv \_ "**</span><span class="sxs-lookup"><span data-stu-id="34b17-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERROR\_FTP\_NO\_PASSIVE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-111">12112</span><span class="sxs-lookup"><span data-stu-id="34b17-111">12112</span></span>
</dt> <dt>



<span data-ttu-id="34b17-112">Der passive Modus ist auf dem Server nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34b17-112">Passive mode is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**Fehler \_ bei FTP- \_ Übertragung wird \_ ausgeführt \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERROR\_FTP\_TRANSFER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-114">12110</span><span class="sxs-lookup"><span data-stu-id="34b17-114">12110</span></span>
</dt> <dt>



<span data-ttu-id="34b17-115">Der angeforderte Vorgang kann nicht für das FTP-Sitzungs handle ausgeführt werden, da bereits ein Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34b17-115">The requested operation cannot be made on the FTP session handle because an operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**Fehler \_ Gopher- \_ Attribut wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="34b17-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERROR\_GOPHER\_ATTRIBUTE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-117">12137</span><span class="sxs-lookup"><span data-stu-id="34b17-117">12137</span></span>
</dt> <dt>



<span data-ttu-id="34b17-118">Das angeforderte Attribut konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-118">The requested attribute could not be located.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-119">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-119">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**Fehler beim \_ Gopher- \_ Daten \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="34b17-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**ERROR\_GOPHER\_DATA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-121">12132</span><span class="sxs-lookup"><span data-stu-id="34b17-121">12132</span></span>
</dt> <dt>



<span data-ttu-id="34b17-122">Beim Empfangen von Daten vom Gopher-Server wurde ein Fehler festgestellt.</span><span class="sxs-lookup"><span data-stu-id="34b17-122">An error was detected while receiving data from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-123">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-123">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**Fehler beim \_ Gopher- \_ Ende \_ der \_ Daten.**</span><span class="sxs-lookup"><span data-stu-id="34b17-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERROR\_GOPHER\_END\_OF\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-125">12133</span><span class="sxs-lookup"><span data-stu-id="34b17-125">12133</span></span>
</dt> <dt>



<span data-ttu-id="34b17-126">Das Ende der Daten wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="34b17-126">The end of the data has been reached.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-127">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-127">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**Fehler bei \_ \_ fehlerhafter \_ Art von Locator \_ .**</span><span class="sxs-lookup"><span data-stu-id="34b17-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERROR\_GOPHER\_INCORRECT\_LOCATOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-129">12135</span><span class="sxs-lookup"><span data-stu-id="34b17-129">12135</span></span>
</dt> <dt>



<span data-ttu-id="34b17-130">Der Serverlocatorpunkt-Typ ist für diesen Vorgang nicht richtig.</span><span class="sxs-lookup"><span data-stu-id="34b17-130">The type of the locator is not correct for this operation.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-131">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-131">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**Fehler " \_ gopher" \_ ungültiger \_ Locator.**</span><span class="sxs-lookup"><span data-stu-id="34b17-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERROR\_GOPHER\_INVALID\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-133">12134</span><span class="sxs-lookup"><span data-stu-id="34b17-133">12134</span></span>
</dt> <dt>



<span data-ttu-id="34b17-134">Der angegebene Serverlocatorpunkt ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-134">The supplied locator is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-135">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-135">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**Fehler- \_ Gopher \_ nicht \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="34b17-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERROR\_GOPHER\_NOT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-137">12131</span><span class="sxs-lookup"><span data-stu-id="34b17-137">12131</span></span>
</dt> <dt>



<span data-ttu-id="34b17-138">Die Anforderung muss für einen Dateilocator erfolgen.</span><span class="sxs-lookup"><span data-stu-id="34b17-138">The request must be made for a file locator.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-139">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-139">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**Fehler \_ Gopher \_ nicht \_ Gopher \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="34b17-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERROR\_GOPHER\_NOT\_GOPHER\_PLUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-141">12136</span><span class="sxs-lookup"><span data-stu-id="34b17-141">12136</span></span>
</dt> <dt>



<span data-ttu-id="34b17-142">Der angeforderte Vorgang kann nur für einen Gopher +-Server oder mit einem Serverlocatorpunkt erfolgen, der einen Gopher +-Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="34b17-142">The requested operation can be made only against a Gopher+ server, or with a locator that specifies a Gopher+ operation.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-143">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-143">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**Fehler beim \_ Gopher- \_ Protokoll. \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**ERROR\_GOPHER\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-145">12130</span><span class="sxs-lookup"><span data-stu-id="34b17-145">12130</span></span>
</dt> <dt>



<span data-ttu-id="34b17-146">Fehler beim Übernehmen der vom Gopher-Server zurückgegebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="34b17-146">An error was detected while parsing data returned from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-147">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-147">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**Fehler \_ Gopher \_ unbekannter \_ Locator.**</span><span class="sxs-lookup"><span data-stu-id="34b17-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERROR\_GOPHER\_UNKNOWN\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-149">12138</span><span class="sxs-lookup"><span data-stu-id="34b17-149">12138</span></span>
</dt> <dt>



<span data-ttu-id="34b17-150">Der Locatortyp ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="34b17-150">The locator type is unknown.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-151">Nur Windows XP und Windows Server 2003 R2 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-151">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**Fehler \_ http- \_ Cookie \_ abgelehnt**</span><span class="sxs-lookup"><span data-stu-id="34b17-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERROR\_HTTP\_COOKIE\_DECLINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-153">12162</span><span class="sxs-lookup"><span data-stu-id="34b17-153">12162</span></span>
</dt> <dt>



<span data-ttu-id="34b17-154">Das HTTP-Cookie wurde vom Server abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="34b17-154">The HTTP cookie was declined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**Fehler \_ http- \_ Cookie \_ muss \_ bestätigt werden**</span><span class="sxs-lookup"><span data-stu-id="34b17-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERROR\_HTTP\_COOKIE\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-156">12161</span><span class="sxs-lookup"><span data-stu-id="34b17-156">12161</span></span>
</dt> <dt>



<span data-ttu-id="34b17-157">Das HTTP-Cookie erfordert eine Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="34b17-157">The HTTP cookie requires confirmation.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-158">Nur Windows Vista und Windows Server 2008 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-158">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**Fehler \_ http- \_ \_ Downlevelserver**</span><span class="sxs-lookup"><span data-stu-id="34b17-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERROR\_HTTP\_DOWNLEVEL\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-160">12151</span><span class="sxs-lookup"><span data-stu-id="34b17-160">12151</span></span>
</dt> <dt>



<span data-ttu-id="34b17-161">Der Server hat keine Header zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34b17-161">The server did not return any headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**HTTP-Fehler \_ \_ Header ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="34b17-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**ERROR\_HTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-163">12155</span><span class="sxs-lookup"><span data-stu-id="34b17-163">12155</span></span>
</dt> <dt>



<span data-ttu-id="34b17-164">Der Header konnte nicht hinzugefügt werden, da er bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="34b17-164">The header could not be added because it already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**HTTP-Fehler \_ \_ Header wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="34b17-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**ERROR\_HTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-166">12150</span><span class="sxs-lookup"><span data-stu-id="34b17-166">12150</span></span>
</dt> <dt>



<span data-ttu-id="34b17-167">Der angeforderte Header konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-167">The requested header could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**HTTP-Fehler bei \_ \_ ungültigem \_ Header**</span><span class="sxs-lookup"><span data-stu-id="34b17-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERROR\_HTTP\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-169">12153</span><span class="sxs-lookup"><span data-stu-id="34b17-169">12153</span></span>
</dt> <dt>



<span data-ttu-id="34b17-170">Der angegebene Header ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-170">The supplied header is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**HTTP-Fehler bei \_ \_ ungültiger \_ Abfrage \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="34b17-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERROR\_HTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-172">12154</span><span class="sxs-lookup"><span data-stu-id="34b17-172">12154</span></span>
</dt> <dt>



<span data-ttu-id="34b17-173">Die an [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) gestellte Anforderung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-173">The request made to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**Fehler \_ http \_ - \_ Antwort auf ungültige Server \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERROR\_HTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-175">12152</span><span class="sxs-lookup"><span data-stu-id="34b17-175">12152</span></span>
</dt> <dt>



<span data-ttu-id="34b17-176">Die Serverantwort konnte nicht analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-176">The server response could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**Fehler \_ http \_ nicht \_ umgeleitet**</span><span class="sxs-lookup"><span data-stu-id="34b17-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERROR\_HTTP\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-178">12160</span><span class="sxs-lookup"><span data-stu-id="34b17-178">12160</span></span>
</dt> <dt>



<span data-ttu-id="34b17-179">Die HTTP-Anforderung wurde nicht umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="34b17-179">The HTTP request was not redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**Fehler bei \_ http- \_ Umleitung. \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERROR\_HTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-181">12156</span><span class="sxs-lookup"><span data-stu-id="34b17-181">12156</span></span>
</dt> <dt>



<span data-ttu-id="34b17-182">Die Umleitung ist fehlgeschlagen, da entweder das Schema geändert wurde (z. b. http zu FTP) oder alle Versuche zum Umleiten fehlgeschlagen sind (der Standardwert ist fünf Versuche).</span><span class="sxs-lookup"><span data-stu-id="34b17-182">The redirection failed because either the scheme changed (for example, HTTP to FTP) or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**Fehler \_ http- \_ Umleitung \_ muss \_ bestätigt werden**</span><span class="sxs-lookup"><span data-stu-id="34b17-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERROR\_HTTP\_REDIRECT\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-184">12168</span><span class="sxs-lookup"><span data-stu-id="34b17-184">12168</span></span>
</dt> <dt>



<span data-ttu-id="34b17-185">Die Umleitung erfordert eine Bestätigung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="34b17-185">The redirection requires user confirmation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**Fehler beim asynchronen Thread für das \_ Internet. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERROR\_INTERNET\_ASYNC\_THREAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-187">12047</span><span class="sxs-lookup"><span data-stu-id="34b17-187">12047</span></span>
</dt> <dt>



<span data-ttu-id="34b17-188">Die Anwendung konnte keinen asynchronen Thread starten.</span><span class="sxs-lookup"><span data-stu-id="34b17-188">The application could not start an asynchronous thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**Fehler "Internet fehlerhaftes \_ \_ Auto- \_ \_ Proxy \_ Skript"**</span><span class="sxs-lookup"><span data-stu-id="34b17-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERROR\_INTERNET\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-190">12166</span><span class="sxs-lookup"><span data-stu-id="34b17-190">12166</span></span>
</dt> <dt>



<span data-ttu-id="34b17-191">Fehler beim automatischen Proxy Konfigurationsskript.</span><span class="sxs-lookup"><span data-stu-id="34b17-191">There was an error in the automatic proxy configuration script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**Fehler beim Internet mit fehlerhafter \_ \_ \_ options \_ Länge**</span><span class="sxs-lookup"><span data-stu-id="34b17-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERROR\_INTERNET\_BAD\_OPTION\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-193">12010</span><span class="sxs-lookup"><span data-stu-id="34b17-193">12010</span></span>
</dt> <dt>



<span data-ttu-id="34b17-194">Die Länge einer für [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) oder [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) angegebenen Option ist für den angegebenen Typ der Option falsch.</span><span class="sxs-lookup"><span data-stu-id="34b17-194">The length of an option supplied to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) is incorrect for the type of option specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**Fehler "Internet fehlerhafter \_ \_ \_ Registrierungs \_ Parameter"**</span><span class="sxs-lookup"><span data-stu-id="34b17-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERROR\_INTERNET\_BAD\_REGISTRY\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-196">12022</span><span class="sxs-lookup"><span data-stu-id="34b17-196">12022</span></span>
</dt> <dt>



<span data-ttu-id="34b17-197">Ein erforderlicher Registrierungs Wert wurde gefunden, weist aber einen falschen Typ auf oder weist einen ungültigen Wert auf.</span><span class="sxs-lookup"><span data-stu-id="34b17-197">A required registry value was located but is an incorrect type or has an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**Fehler \_ Internet \_ Verbindung kann nicht hergestellt werden \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERROR\_INTERNET\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-199">12029</span><span class="sxs-lookup"><span data-stu-id="34b17-199">12029</span></span>
</dt> <dt>



<span data-ttu-id="34b17-200">Fehler beim Versuch, eine Verbindung mit dem Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="34b17-200">The attempt to connect to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**Fehler \_ Internet- \_ CHG- \_ Post \_ ist \_ nicht \_ sicher**</span><span class="sxs-lookup"><span data-stu-id="34b17-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERROR\_INTERNET\_CHG\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-202">12042</span><span class="sxs-lookup"><span data-stu-id="34b17-202">12042</span></span>
</dt> <dt>



<span data-ttu-id="34b17-203">Die Anwendung stellt eine Bereitstellung durch und versucht, mehrere Textzeilen auf einem Server zu ändern, der nicht sicher ist.</span><span class="sxs-lookup"><span data-stu-id="34b17-203">The application is posting and attempting to change multiple lines of text on a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**Fehler " \_ Internet \_ Client Authentifizierungs \_ \_ Zertifikat \_ erforderlich"**</span><span class="sxs-lookup"><span data-stu-id="34b17-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-205">12044</span><span class="sxs-lookup"><span data-stu-id="34b17-205">12044</span></span>
</dt> <dt>



<span data-ttu-id="34b17-206">Der Server fordert die Client Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="34b17-206">The server is requesting client authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**Fehler \_ beim \_ Einrichten der Internet Client Authentifizierung \_ . \_ \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_NOT\_SETUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-208">12046</span><span class="sxs-lookup"><span data-stu-id="34b17-208">12046</span></span>
</dt> <dt>



<span data-ttu-id="34b17-209">Auf diesem Computer ist keine Client Autorisierung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="34b17-209">Client authorization is not set up on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**Fehler beim Abbrechen der \_ Internet \_ Verbindung. \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERROR\_INTERNET\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-211">12030</span><span class="sxs-lookup"><span data-stu-id="34b17-211">12030</span></span>
</dt> <dt>



<span data-ttu-id="34b17-212">Die Verbindung mit dem Server wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="34b17-212">The connection with the server has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**Fehler \_ beim \_ Zurücksetzen der Internet Verbindung \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERROR\_INTERNET\_CONNECTION\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-214">12031</span><span class="sxs-lookup"><span data-stu-id="34b17-214">12031</span></span>
</dt> <dt>



<span data-ttu-id="34b17-215">Die Verbindung mit dem Server wurde zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="34b17-215">The connection with the server has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**Fehler \_ beim \_ Decodieren des Internets. \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERROR\_INTERNET\_DECODING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-217">12175</span><span class="sxs-lookup"><span data-stu-id="34b17-217">12175</span></span>
</dt> <dt>



<span data-ttu-id="34b17-218">WinInet konnte die Decodierung von Inhalten für die Antwort nicht durchführen.</span><span class="sxs-lookup"><span data-stu-id="34b17-218">WinINet failed to perform content decoding on the response.</span></span> <span data-ttu-id="34b17-219">Weitere Informationen finden Sie im Thema [**Inhalts Codierung**](content-encoding.md) .</span><span class="sxs-lookup"><span data-stu-id="34b17-219">For more information, see the [**Content Encoding**](content-encoding.md) topic.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**Fehler beim \_ Internet \_ Dialogfeld \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**ERROR\_INTERNET\_DIALOG\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-221">12049</span><span class="sxs-lookup"><span data-stu-id="34b17-221">12049</span></span>
</dt> <dt>



<span data-ttu-id="34b17-222">Ein anderer Thread enthält ein Kennwort-Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="34b17-222">Another thread has a password dialog box in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**Fehler beim Internet Verbindung. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERROR\_INTERNET\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-224">12163</span><span class="sxs-lookup"><span data-stu-id="34b17-224">12163</span></span>
</dt> <dt>



<span data-ttu-id="34b17-225">Die Internet Verbindung ist verloren gegangen.</span><span class="sxs-lookup"><span data-stu-id="34b17-225">The Internet connection has been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**Fehler \_ beim \_ erweiterten \_ Internet Fehler**</span><span class="sxs-lookup"><span data-stu-id="34b17-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**ERROR\_INTERNET\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-227">12003</span><span class="sxs-lookup"><span data-stu-id="34b17-227">12003</span></span>
</dt> <dt>



<span data-ttu-id="34b17-228">Vom Server wurde ein erweiterter Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34b17-228">An extended error was returned from the server.</span></span> <span data-ttu-id="34b17-229">Dies ist in der Regel eine Zeichenfolge oder ein Puffer, der eine ausführliche Fehlermeldung enthält.</span><span class="sxs-lookup"><span data-stu-id="34b17-229">This is typically a string or buffer containing a verbose error message.</span></span> <span data-ttu-id="34b17-230">Rufen Sie [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) auf, um den Fehlertext abzurufen.</span><span class="sxs-lookup"><span data-stu-id="34b17-230">Call [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) to retrieve the error text.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**Fehler beim \_ Internet mit \_ \_ duetosecuritycheck.**</span><span class="sxs-lookup"><span data-stu-id="34b17-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERROR\_INTERNET\_FAILED\_DUETOSECURITYCHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-232">12171</span><span class="sxs-lookup"><span data-stu-id="34b17-232">12171</span></span>
</dt> <dt>



<span data-ttu-id="34b17-233">Die Funktion konnte aufgrund einer Sicherheitsüberprüfung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-233">The function failed due to a security check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**Fehler \_ beim \_ erneuten Versuch von Internet Force \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERROR\_INTERNET\_FORCE\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-235">12032</span><span class="sxs-lookup"><span data-stu-id="34b17-235">12032</span></span>
</dt> <dt>



<span data-ttu-id="34b17-236">Die Funktion muss die Anforderung wiederholen.</span><span class="sxs-lookup"><span data-stu-id="34b17-236">The function needs to redo the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**Fehler \_ Internet- \_ Fortezza- \_ Anmeldung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="34b17-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERROR\_INTERNET\_FORTEZZA\_LOGIN\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-238">12054</span><span class="sxs-lookup"><span data-stu-id="34b17-238">12054</span></span>
</dt> <dt>



<span data-ttu-id="34b17-239">Die angeforderte Ressource erfordert die Fortezza-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="34b17-239">The requested resource requires Fortezza authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**Fehler \_ Internet \_ handle \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="34b17-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERROR\_INTERNET\_HANDLE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-241">12036</span><span class="sxs-lookup"><span data-stu-id="34b17-241">12036</span></span>
</dt> <dt>



<span data-ttu-id="34b17-242">Die Anforderung ist fehlgeschlagen, da das Handle bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="34b17-242">The request failed because the handle already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**Fehler " \_ Internet \_ http \_ zu https" \_ \_ beim \_ redir**</span><span class="sxs-lookup"><span data-stu-id="34b17-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-244">12039</span><span class="sxs-lookup"><span data-stu-id="34b17-244">12039</span></span>
</dt> <dt>



<span data-ttu-id="34b17-245">Die Anwendung wechselt aufgrund einer Umleitung von einer nicht-SSL-zu einer SSL-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="34b17-245">The application is moving from a non-SSL to an SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**Fehler " \_ Internet \_ https \_ http \_ Submit \_ redir"**</span><span class="sxs-lookup"><span data-stu-id="34b17-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERROR\_INTERNET\_HTTPS\_HTTP\_SUBMIT\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-247">12052</span><span class="sxs-lookup"><span data-stu-id="34b17-247">12052</span></span>
</dt> <dt>



<span data-ttu-id="34b17-248">Die Daten, die an eine SSL-Verbindung übermittelt werden, werden an eine nicht-SSL-Verbindung umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="34b17-248">The data being submitted to an SSL connection is being redirected to a non-SSL connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**Fehler \_ \_ beim Internet HTTPS \_ zu \_ http \_ bei \_ redir.**</span><span class="sxs-lookup"><span data-stu-id="34b17-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-250">12040</span><span class="sxs-lookup"><span data-stu-id="34b17-250">12040</span></span>
</dt> <dt>



<span data-ttu-id="34b17-251">Die Anwendung wechselt aufgrund einer Umleitung von einer SSL-zu einer nicht-SSL-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="34b17-251">The application is moving from an SSL to an non-SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**Fehler \_ im Internet des \_ falschen \_ Formats**</span><span class="sxs-lookup"><span data-stu-id="34b17-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERROR\_INTERNET\_INCORRECT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-253">12027</span><span class="sxs-lookup"><span data-stu-id="34b17-253">12027</span></span>
</dt> <dt>



<span data-ttu-id="34b17-254">Das Format der Anforderung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-254">The format of the request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**Fehler beim \_ Internet \_ fehlerhafter \_ handle- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="34b17-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-256">12019</span><span class="sxs-lookup"><span data-stu-id="34b17-256">12019</span></span>
</dt> <dt>



<span data-ttu-id="34b17-257">Der angeforderte Vorgang kann nicht ausgeführt werden, da das angegebene Handle nicht den richtigen Status aufweist.</span><span class="sxs-lookup"><span data-stu-id="34b17-257">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**Fehler \_ im Internet \_ fehlerhafter \_ handle- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="34b17-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-259">12018</span><span class="sxs-lookup"><span data-stu-id="34b17-259">12018</span></span>
</dt> <dt>



<span data-ttu-id="34b17-260">Der angegebene Handlertyp ist für diesen Vorgang falsch.</span><span class="sxs-lookup"><span data-stu-id="34b17-260">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**\_ \_ Fehlerhaftes Internet \_ Kennwort**</span><span class="sxs-lookup"><span data-stu-id="34b17-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERROR\_INTERNET\_INCORRECT\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-262">12014</span><span class="sxs-lookup"><span data-stu-id="34b17-262">12014</span></span>
</dt> <dt>



<span data-ttu-id="34b17-263">Die Anforderung zum Verbinden und Anmelden bei einem FTP-Server konnte nicht abgeschlossen werden, da das angegebene Kennwort falsch ist.</span><span class="sxs-lookup"><span data-stu-id="34b17-263">The request to connect and log on to an FTP server could not be completed because the supplied password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**\_fehlerhafter \_ Internet \_ Benutzer \_ Name**</span><span class="sxs-lookup"><span data-stu-id="34b17-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERROR\_INTERNET\_INCORRECT\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-265">12013</span><span class="sxs-lookup"><span data-stu-id="34b17-265">12013</span></span>
</dt> <dt>



<span data-ttu-id="34b17-266">Die Anforderung zum Verbinden und Anmelden bei einem FTP-Server konnte nicht abgeschlossen werden, da der angegebene Benutzername falsch ist.</span><span class="sxs-lookup"><span data-stu-id="34b17-266">The request to connect and log on to an FTP server could not be completed because the supplied user name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**Fehler \_ beim \_ Einfügen der \_ Crom-Datei**</span><span class="sxs-lookup"><span data-stu-id="34b17-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERROR\_INTERNET\_INSERT\_CDROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-268">12053</span><span class="sxs-lookup"><span data-stu-id="34b17-268">12053</span></span>
</dt> <dt>



<span data-ttu-id="34b17-269">Die Anforderung erfordert, dass eine CD-ROM in das CD-ROM-Laufwerk eingefügt wird, um die angeforderte Ressource zu suchen.</span><span class="sxs-lookup"><span data-stu-id="34b17-269">The request requires a CD-ROM to be inserted in the CD-ROM drive to locate the resource requested.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-270">Nur Windows Vista und Windows Server 2008 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-270">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**\_Interner Fehler im Internet. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**ERROR\_INTERNET\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-272">12004</span><span class="sxs-lookup"><span data-stu-id="34b17-272">12004</span></span>
</dt> <dt>



<span data-ttu-id="34b17-273">Ein interner Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="34b17-273">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**Fehler beim \_ Internet \_ ungültige Zertifizierungsstelle \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERROR\_INTERNET\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-275">12045</span><span class="sxs-lookup"><span data-stu-id="34b17-275">12045</span></span>
</dt> <dt>



<span data-ttu-id="34b17-276">Die Funktion ist mit der Zertifizierungsstelle, die das Zertifikat des Servers generiert hat, nicht vertraut.</span><span class="sxs-lookup"><span data-stu-id="34b17-276">The function is unfamiliar with the Certificate Authority that generated the server's certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**Fehler beim \_ Internet \_ ungültiger \_ Vorgang.**</span><span class="sxs-lookup"><span data-stu-id="34b17-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERROR\_INTERNET\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-278">12016</span><span class="sxs-lookup"><span data-stu-id="34b17-278">12016</span></span>
</dt> <dt>



<span data-ttu-id="34b17-279">Der angeforderte Vorgang ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-279">The requested operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**Fehler beim \_ Internet \_ ungültige \_ Option**</span><span class="sxs-lookup"><span data-stu-id="34b17-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERROR\_INTERNET\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-281">12009</span><span class="sxs-lookup"><span data-stu-id="34b17-281">12009</span></span>
</dt> <dt>



<span data-ttu-id="34b17-282">Eine Anforderung an [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) oder [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) hat einen ungültigen Optionswert angegeben.</span><span class="sxs-lookup"><span data-stu-id="34b17-282">A request to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**Fehler beim \_ Internet \_ ungültige \_ Proxy \_ Anforderung.**</span><span class="sxs-lookup"><span data-stu-id="34b17-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERROR\_INTERNET\_INVALID\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-284">12033</span><span class="sxs-lookup"><span data-stu-id="34b17-284">12033</span></span>
</dt> <dt>



<span data-ttu-id="34b17-285">Die Anforderung an den Proxy war ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-285">The request to the proxy was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**Fehler beim \_ Internet \_ ungültige \_ URL.**</span><span class="sxs-lookup"><span data-stu-id="34b17-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERROR\_INTERNET\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-287">12005</span><span class="sxs-lookup"><span data-stu-id="34b17-287">12005</span></span>
</dt> <dt>



<span data-ttu-id="34b17-288">Die URL ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-288">The URL is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**Fehler beim \_ Internet \_ Element \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="34b17-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERROR\_INTERNET\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-290">12028</span><span class="sxs-lookup"><span data-stu-id="34b17-290">12028</span></span>
</dt> <dt>



<span data-ttu-id="34b17-291">Das angeforderte Element konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-291">The requested item could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**Fehler beim \_ Internet \_ Anmelde \_ Fehler.**</span><span class="sxs-lookup"><span data-stu-id="34b17-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-293">12015</span><span class="sxs-lookup"><span data-stu-id="34b17-293">12015</span></span>
</dt> <dt>



<span data-ttu-id="34b17-294">Fehler bei der Anforderung zum Verbinden und Anmelden bei einem FTP-Server.</span><span class="sxs-lookup"><span data-stu-id="34b17-294">The request to connect and log on to an FTP server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**Fehler beim \_ Internet Anmeldefehler beim \_ Anzeigen des \_ \_ \_ Entitäts \_ Texts.**</span><span class="sxs-lookup"><span data-stu-id="34b17-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-296">12174</span><span class="sxs-lookup"><span data-stu-id="34b17-296">12174</span></span>
</dt> <dt>



<span data-ttu-id="34b17-297">Der MS-Logoff Digest-Header wurde von der Website zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34b17-297">The MS-Logoff digest header has been returned from the website.</span></span> <span data-ttu-id="34b17-298">Dieser Header weist das Digest-Paket ausdrücklich an, Anmelde Informationen für den zugeordneten Bereich zu löschen.</span><span class="sxs-lookup"><span data-stu-id="34b17-298">This header specifically instructs the digest package to purge credentials for the associated realm.</span></span> <span data-ttu-id="34b17-299">Dieser Fehler wird nur zurückgegeben, wenn die Option zum [ \_ Anzeigen von \_ \_ \_ \_ \_ Entitäts \_ Text der Internet Fehler Maske angezeigt](option-flags.md) wird; andernfalls wird der **Fehler " \_ Internet \_ Login \_ Failure** " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34b17-299">This error will only be returned if [INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY](option-flags.md) option has been set; otherwise, **ERROR\_INTERNET\_LOGIN\_FAILURE** is returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**Fehler \_ im Internet mit \_ gemischter \_ Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="34b17-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERROR\_INTERNET\_MIXED\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-301">12041</span><span class="sxs-lookup"><span data-stu-id="34b17-301">12041</span></span>
</dt> <dt>



<span data-ttu-id="34b17-302">Der Inhalt ist nicht vollständig sicher.</span><span class="sxs-lookup"><span data-stu-id="34b17-302">The content is not entirely secure.</span></span> <span data-ttu-id="34b17-303">Einige der Inhalte, die angezeigt werden, stammen möglicherweise von nicht geschützten Servern.</span><span class="sxs-lookup"><span data-stu-id="34b17-303">Some of the content being viewed may have come from unsecured servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**Fehler beim Auflösen des \_ Internet \_ namens. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERROR\_INTERNET\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-305">12007</span><span class="sxs-lookup"><span data-stu-id="34b17-305">12007</span></span>
</dt> <dt>



<span data-ttu-id="34b17-306">Der Servername konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-306">The server name could not be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**Fehler \_ Internet \_ benötigt \_ MSN \_ SSPI \_ pkg**</span><span class="sxs-lookup"><span data-stu-id="34b17-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERROR\_INTERNET\_NEED\_MSN\_SSPI\_PKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-308">12173</span><span class="sxs-lookup"><span data-stu-id="34b17-308">12173</span></span>
</dt> <dt>



<span data-ttu-id="34b17-309">Derzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="34b17-309">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**Fehler \_ Internet \_ \_ Benutzeroberfläche erforderlich**</span><span class="sxs-lookup"><span data-stu-id="34b17-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERROR\_INTERNET\_NEED\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-311">12034</span><span class="sxs-lookup"><span data-stu-id="34b17-311">12034</span></span>
</dt> <dt>



<span data-ttu-id="34b17-312">Eine Benutzeroberfläche oder ein anderer Blockierungs Vorgang wurde angefordert.</span><span class="sxs-lookup"><span data-stu-id="34b17-312">A user interface or other blocking operation has been requested.</span></span>

> [!Note]  
> <span data-ttu-id="34b17-313">Nur Windows Vista und Windows Server 2008 und früher.</span><span class="sxs-lookup"><span data-stu-id="34b17-313">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**Fehler \_ Internet \_ kein \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="34b17-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERROR\_INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-315">12025</span><span class="sxs-lookup"><span data-stu-id="34b17-315">12025</span></span>
</dt> <dt>



<span data-ttu-id="34b17-316">Eine asynchrone Anforderung konnte nicht durchgeführt werden, da keine Rückruffunktion festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="34b17-316">An asynchronous request could not be made because a callback function has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**Fehler \_ Internet \_ ohne \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="34b17-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERROR\_INTERNET\_NO\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-318">12024</span><span class="sxs-lookup"><span data-stu-id="34b17-318">12024</span></span>
</dt> <dt>



<span data-ttu-id="34b17-319">Eine asynchrone Anforderung konnte nicht durchgeführt werden, da ein NULL-Kontextwert angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="34b17-319">An asynchronous request could not be made because a zero context value was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**Fehler \_ Internet \_ kein \_ direkter \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="34b17-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERROR\_INTERNET\_NO\_DIRECT\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-321">12023</span><span class="sxs-lookup"><span data-stu-id="34b17-321">12023</span></span>
</dt> <dt>



<span data-ttu-id="34b17-322">Zurzeit kann kein direkter Netzwerk Zugriff erfolgen.</span><span class="sxs-lookup"><span data-stu-id="34b17-322">Direct network access cannot be made at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**Fehler " \_ Internet" \_ nicht \_ Initialisiert**</span><span class="sxs-lookup"><span data-stu-id="34b17-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERROR\_INTERNET\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-324">12172</span><span class="sxs-lookup"><span data-stu-id="34b17-324">12172</span></span>
</dt> <dt>



<span data-ttu-id="34b17-325">Die Initialisierung der WinInet-API ist nicht erfolgt.</span><span class="sxs-lookup"><span data-stu-id="34b17-325">Initialization of the WinINet API has not occurred.</span></span> <span data-ttu-id="34b17-326">Gibt an, dass eine Funktion auf höherer Ebene, z. b. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), noch nicht aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="34b17-326">Indicates that a higher-level function, such as [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), has not been called yet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**Fehler " \_ Internet \_ nicht \_ Proxy \_ Anforderung"**</span><span class="sxs-lookup"><span data-stu-id="34b17-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERROR\_INTERNET\_NOT\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-328">12020</span><span class="sxs-lookup"><span data-stu-id="34b17-328">12020</span></span>
</dt> <dt>



<span data-ttu-id="34b17-329">Die Anforderung kann nicht über einen Proxy durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-329">The request cannot be made via a proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**Fehler beim \_ Internet \_ Vorgang. \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERROR\_INTERNET\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-331">12017</span><span class="sxs-lookup"><span data-stu-id="34b17-331">12017</span></span>
</dt> <dt>



<span data-ttu-id="34b17-332">Der Vorgang wurde abgebrochen, in der Regel, weil das Handle, für das die Anforderung ausgeführt wurde, vor dem Abschluss des Vorgangs geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="34b17-332">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**Fehler " \_ Internet \_ Option \_ nicht \_ feststellbar"**</span><span class="sxs-lookup"><span data-stu-id="34b17-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERROR\_INTERNET\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-334">12011</span><span class="sxs-lookup"><span data-stu-id="34b17-334">12011</span></span>
</dt> <dt>



<span data-ttu-id="34b17-335">Die angeforderte Option kann nicht festgelegt werden, sondern nur abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-335">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**Fehler beim \_ Internet \_ außerhalb \_ der \_ Handles**</span><span class="sxs-lookup"><span data-stu-id="34b17-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERROR\_INTERNET\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-337">12001</span><span class="sxs-lookup"><span data-stu-id="34b17-337">12001</span></span>
</dt> <dt>



<span data-ttu-id="34b17-338">Zu diesem Zeitpunkt können keine weiteren Handles generiert werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-338">No more handles could be generated at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**Fehler " \_ Internet \_ Post" \_ ist \_ nicht \_ sicher.**</span><span class="sxs-lookup"><span data-stu-id="34b17-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-340">12043</span><span class="sxs-lookup"><span data-stu-id="34b17-340">12043</span></span>
</dt> <dt>



<span data-ttu-id="34b17-341">Die Anwendung veröffentlicht Daten auf einem Server, der nicht sicher ist.</span><span class="sxs-lookup"><span data-stu-id="34b17-341">The application is posting data to a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**Fehler " \_ Internet \_ Protokoll \_ nicht \_ gefunden"**</span><span class="sxs-lookup"><span data-stu-id="34b17-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERROR\_INTERNET\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-343">12008</span><span class="sxs-lookup"><span data-stu-id="34b17-343">12008</span></span>
</dt> <dt>



<span data-ttu-id="34b17-344">Das angeforderte Protokoll konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-344">The requested protocol could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**Fehler \_ beim \_ Internet \_ Proxyserver \_ nicht erreichbar.**</span><span class="sxs-lookup"><span data-stu-id="34b17-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERROR\_INTERNET\_PROXY\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-346">12165</span><span class="sxs-lookup"><span data-stu-id="34b17-346">12165</span></span>
</dt> <dt>



<span data-ttu-id="34b17-347">Der angegebene Proxy Server kann nicht erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-347">The designated proxy server cannot be reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**Fehler beim \_ Ändern der Internet \_ Umleitungs \_ Schema \_**</span><span class="sxs-lookup"><span data-stu-id="34b17-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERROR\_INTERNET\_REDIRECT\_SCHEME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-349">12048</span><span class="sxs-lookup"><span data-stu-id="34b17-349">12048</span></span>
</dt> <dt>



<span data-ttu-id="34b17-350">Die Funktion konnte die Umleitung nicht verarbeiten, da das Schema geändert wurde (z. b. http zu FTP).</span><span class="sxs-lookup"><span data-stu-id="34b17-350">The function could not handle the redirection, because the scheme changed (for example, HTTP to FTP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**Fehler beim \_ Internet \_ Registrierungs \_ Wert \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="34b17-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERROR\_INTERNET\_REGISTRY\_VALUE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-352">12021</span><span class="sxs-lookup"><span data-stu-id="34b17-352">12021</span></span>
</dt> <dt>



<span data-ttu-id="34b17-353">Ein erforderlicher Registrierungs Wert wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="34b17-353">A required registry value could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**Fehler \_ Internet \_ Anforderung steht \_ aus.**</span><span class="sxs-lookup"><span data-stu-id="34b17-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERROR\_INTERNET\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-355">12026</span><span class="sxs-lookup"><span data-stu-id="34b17-355">12026</span></span>
</dt> <dt>



<span data-ttu-id="34b17-356">Der erforderliche Vorgang konnte nicht abgeschlossen werden, da eine oder mehrere Anforderungen ausstehen.</span><span class="sxs-lookup"><span data-stu-id="34b17-356">The required operation could not be completed because one or more requests are pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**Fehler beim \_ Internet- \_ Wiederholungs \_ Dialogfeld**</span><span class="sxs-lookup"><span data-stu-id="34b17-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**ERROR\_INTERNET\_RETRY\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-358">12050</span><span class="sxs-lookup"><span data-stu-id="34b17-358">12050</span></span>
</dt> <dt>



<span data-ttu-id="34b17-359">Das Dialogfeld sollte erneut versucht werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-359">The dialog box should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**Fehler \_ Internet \_ sec \_ CERT \_ CN ist \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="34b17-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-361">12038</span><span class="sxs-lookup"><span data-stu-id="34b17-361">12038</span></span>
</dt> <dt>



<span data-ttu-id="34b17-362">Der allgemeine Name des SSL-Zertifikats (Hostname) ist falsch, wenn Sie z. b. www.Server.com eingegeben haben und der allgemeine Name des Zertifikats www.different.com lautet.</span><span class="sxs-lookup"><span data-stu-id="34b17-362">SSL certificate common name (host name field) is incorrect for example, if you entered www.server.com and the common name on the certificate says www.different.com.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**Fehler \_ Internet \_ Sek. \_ CERT- \_ Datum \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="34b17-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-364">12037</span><span class="sxs-lookup"><span data-stu-id="34b17-364">12037</span></span>
</dt> <dt>



<span data-ttu-id="34b17-365">Das vom Server empfangene SSL-Zertifikat ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-365">SSL certificate date that was received from the server is bad.</span></span> <span data-ttu-id="34b17-366">Das Zertifikat ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="34b17-366">The certificate is expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**Fehler \_ Internet \_ Sek. \_ CERT- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="34b17-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-368">12055</span><span class="sxs-lookup"><span data-stu-id="34b17-368">12055</span></span>
</dt> <dt>



<span data-ttu-id="34b17-369">Das SSL-Zertifikat enthält Fehler.</span><span class="sxs-lookup"><span data-stu-id="34b17-369">The SSL certificate contains errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**Fehler \_ Internet \_ sec \_ CERT \_ No \_ Rev**</span><span class="sxs-lookup"><span data-stu-id="34b17-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERROR\_INTERNET\_SEC\_CERT\_NO\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-371">12056</span><span class="sxs-lookup"><span data-stu-id="34b17-371">12056</span></span>
</dt> <dt>



<span data-ttu-id="34b17-372">Das SSL-Zertifikat wurde nicht widerrufen.</span><span class="sxs-lookup"><span data-stu-id="34b17-372">The SSL certificate was not revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**Fehler beim \_ Internet \_ sec- \_ CERT \_ Rev \_ .**</span><span class="sxs-lookup"><span data-stu-id="34b17-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERROR\_INTERNET\_SEC\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-374">12057</span><span class="sxs-lookup"><span data-stu-id="34b17-374">12057</span></span>
</dt> <dt>



<span data-ttu-id="34b17-375">Die Sperrung des SSL-Zertifikats ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="34b17-375">Revocation of the SSL certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**Fehler \_ Internet \_ Sek. \_ Zertifikat \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="34b17-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERROR\_INTERNET\_SEC\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-377">12170</span><span class="sxs-lookup"><span data-stu-id="34b17-377">12170</span></span>
</dt> <dt>



<span data-ttu-id="34b17-378">Das SSL-Zertifikat wurde widerrufen.</span><span class="sxs-lookup"><span data-stu-id="34b17-378">The SSL certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**Fehler \_ Internet \_ Sek. \_ ungültiges \_ Zertifikat**</span><span class="sxs-lookup"><span data-stu-id="34b17-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERROR\_INTERNET\_SEC\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-380">12169</span><span class="sxs-lookup"><span data-stu-id="34b17-380">12169</span></span>
</dt> <dt>



<span data-ttu-id="34b17-381">Das SSL-Zertifikat ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="34b17-381">The SSL certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**Fehler beim \_ Internet \_ Sicherheits \_ Kanal \_ .**</span><span class="sxs-lookup"><span data-stu-id="34b17-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**ERROR\_INTERNET\_SECURITY\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-383">12157</span><span class="sxs-lookup"><span data-stu-id="34b17-383">12157</span></span>
</dt> <dt>



<span data-ttu-id="34b17-384">Bei der Anwendung ist ein interner Fehler beim Laden der SSL-Bibliotheken aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="34b17-384">The application experienced an internal error loading the SSL libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**Fehler " \_ Internet \_ Server \_ nicht erreichbar"**</span><span class="sxs-lookup"><span data-stu-id="34b17-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERROR\_INTERNET\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-386">12164</span><span class="sxs-lookup"><span data-stu-id="34b17-386">12164</span></span>
</dt> <dt>



<span data-ttu-id="34b17-387">Die angegebener Website oder der Server ist nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="34b17-387">The website or server indicated is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**Fehler beim \_ Internet \_ Herunterfahren**</span><span class="sxs-lookup"><span data-stu-id="34b17-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERROR\_INTERNET\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-389">12012</span><span class="sxs-lookup"><span data-stu-id="34b17-389">12012</span></span>
</dt> <dt>



<span data-ttu-id="34b17-390">Die WinInet-Unterstützung wird heruntergefahren oder entladen.</span><span class="sxs-lookup"><span data-stu-id="34b17-390">WinINet support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**Fehler \_ Internet \_ tcpip \_ nicht \_ installiert**</span><span class="sxs-lookup"><span data-stu-id="34b17-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERROR\_INTERNET\_TCPIP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-392">12159</span><span class="sxs-lookup"><span data-stu-id="34b17-392">12159</span></span>
</dt> <dt>



<span data-ttu-id="34b17-393">Der erforderliche Protokollstapel ist nicht geladen, und die Anwendung kann Winsock nicht starten.</span><span class="sxs-lookup"><span data-stu-id="34b17-393">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**Fehler beim \_ Internet \_ Timeout.**</span><span class="sxs-lookup"><span data-stu-id="34b17-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERROR\_INTERNET\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-395">12002</span><span class="sxs-lookup"><span data-stu-id="34b17-395">12002</span></span>
</dt> <dt>



<span data-ttu-id="34b17-396">Timeout für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="34b17-396">The request has timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**Fehler beim zwischen \_ \_ Speichern der \_ \_ \_ Datei durch das Internet.**</span><span class="sxs-lookup"><span data-stu-id="34b17-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERROR\_INTERNET\_UNABLE\_TO\_CACHE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-398">12158</span><span class="sxs-lookup"><span data-stu-id="34b17-398">12158</span></span>
</dt> <dt>



<span data-ttu-id="34b17-399">Die Funktion konnte die Datei nicht zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="34b17-399">The function was unable to cache the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**Fehler \_ beim \_ \_ \_ herunterladen des \_ Skripts durch das Internet**</span><span class="sxs-lookup"><span data-stu-id="34b17-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERROR\_INTERNET\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-401">12167</span><span class="sxs-lookup"><span data-stu-id="34b17-401">12167</span></span>
</dt> <dt>



<span data-ttu-id="34b17-402">Das Skript für die automatische Proxykonfiguration konnte nicht heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-402">The automatic proxy configuration script could not be downloaded.</span></span> <span data-ttu-id="34b17-403">Das kennflag für das Internet Kennzeichen \_ \_ muss zwischengespeichert werden \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="34b17-403">The INTERNET\_FLAG\_MUST\_CACHE\_REQUEST flag was set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**Fehler \_ im Internet \_ unbekannter \_ Schema**</span><span class="sxs-lookup"><span data-stu-id="34b17-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERROR\_INTERNET\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34b17-405">12006</span><span class="sxs-lookup"><span data-stu-id="34b17-405">12006</span></span>
</dt> <dt>



<span data-ttu-id="34b17-406">Das URL-Schema konnte nicht erkannt werden, oder es wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34b17-406">The URL scheme could not be recognized, or is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Fehler bei \_ ungültigem \_ handle**</span><span class="sxs-lookup"><span data-stu-id="34b17-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34b17-408">Das Handle, das an die API übermittelt wurde, wurde entweder ungültig oder wurde geschlossen.</span><span class="sxs-lookup"><span data-stu-id="34b17-408">The handle that was passed to the API has been either invalidated or closed.</span></span>

<span data-ttu-id="34b17-409">**Header:** In "Winerror. h" deklariert</span><span class="sxs-lookup"><span data-stu-id="34b17-409">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**Fehler \_ Weitere \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="34b17-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34b17-411">Weitere Daten sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34b17-411">More data is available.</span></span>

<span data-ttu-id="34b17-412">**Header:** In "Winerror. h" deklariert</span><span class="sxs-lookup"><span data-stu-id="34b17-412">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**Fehler \_ keine \_ weiteren \_ Dateien**</span><span class="sxs-lookup"><span data-stu-id="34b17-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34b17-414">Es wurden keine weiteren Dateien gefunden.</span><span class="sxs-lookup"><span data-stu-id="34b17-414">No more files have been found.</span></span>

<span data-ttu-id="34b17-415">**Header:** In "Winerror. h" deklariert</span><span class="sxs-lookup"><span data-stu-id="34b17-415">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="34b17-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**Fehler \_ keine \_ weiteren \_ Elemente**</span><span class="sxs-lookup"><span data-stu-id="34b17-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="34b17-417">Es wurden keine weiteren Elemente gefunden.</span><span class="sxs-lookup"><span data-stu-id="34b17-417">No more items have been found.</span></span>

<span data-ttu-id="34b17-418">**Header:** In "Winerror. h" deklariert</span><span class="sxs-lookup"><span data-stu-id="34b17-418">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34b17-419">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34b17-419">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="34b17-420">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="34b17-420">WinINet does not support server implementations.</span></span> <span data-ttu-id="34b17-421">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34b17-421">In addition, it should not be used from a service.</span></span> <span data-ttu-id="34b17-422">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="34b17-422">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="34b17-423">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34b17-423">Requirements</span></span>



| <span data-ttu-id="34b17-424">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34b17-424">Requirement</span></span> | <span data-ttu-id="34b17-425">Wert</span><span class="sxs-lookup"><span data-stu-id="34b17-425">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="34b17-426">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34b17-426">Minimum supported client</span></span><br/> | <span data-ttu-id="34b17-427">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34b17-427">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="34b17-428">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34b17-428">Minimum supported server</span></span><br/> | <span data-ttu-id="34b17-429">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34b17-429">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="34b17-430">Header</span><span class="sxs-lookup"><span data-stu-id="34b17-430">Header</span></span><br/>                   | <dl> <span data-ttu-id="34b17-431"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="34b17-431"><dt>Wininet.h</dt></span></span> </dl> |



 

