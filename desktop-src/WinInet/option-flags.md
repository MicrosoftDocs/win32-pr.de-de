---
title: Optionsflags (WinInet. h)
description: Die folgenden Optionsflags werden mit den Funktionen InternetQueryOption und InternetSetOption verwendet. Alle gültigen Optionsflags haben einen Wert größer oder gleich der Internet \_ First \_ -Option und kleiner oder gleich der Internet \_ Last- \_ Option.
ms.assetid: 708510b8-468a-4287-849b-cba3d7001ea8
topic_type:
- apiref
api_name:
- INTERNET_OPTION_ALTER_IDENTITY
- INTERNET_OPTION_ASYNC
- INTERNET_OPTION_ASYNC_ID
- INTERNET_OPTION_ASYNC_PRIORITY
- INTERNET_OPTION_BYPASS_EDITED_ENTRY
- INTERNET_OPTION_CACHE_STREAM_HANDLE
- INTERNET_OPTION_CACHE_TIMESTAMPS
- INTERNET_OPTION_CALLBACK
- INTERNET_OPTION_CALLBACK_FILTER
- INTERNET_OPTION_CLIENT_CERT_CONTEXT
- INTERNET_OPTION_CODEPAGE
- INTERNET_OPTION_CODEPAGE_PATH
- INTERNET_OPTION_CODEPAGE_EXTRA
- INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH
- INTERNET_OPTION_CONNECT_BACKOFF
- INTERNET_OPTION_CONNECT_RETRIES
- INTERNET_OPTION_CONNECT_TIME
- INTERNET_OPTION_CONNECT_TIMEOUT
- INTERNET_OPTION_CONNECTED_STATE
- INTERNET_OPTION_CONTEXT_VALUE
- INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT
- INTERNET_OPTION_CONTROL_SEND_TIMEOUT
- INTERNET_OPTION_DATA_RECEIVE_TIMEOUT
- INTERNET_OPTION_DATA_SEND_TIMEOUT
- INTERNET_OPTION_DATAFILE_NAME
- INTERNET_OPTION_DATAFILE_EXT
- INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO
- INTERNET_OPTION_DIGEST_AUTH_UNLOAD
- INTERNET_OPTION_DISABLE_AUTODIAL
- INTERNET_OPTION_DISCONNECTED_TIMEOUT
- INTERNET_OPTION_ENABLE_HTTP_PROTOCOL
- INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ
- INTERNET_OPTION_ENCODE_EXTRA
- INTERNET_OPTION_END_BROWSER_SESSION
- INTERNET_OPTION_ERROR_MASK
- INTERNET_OPTION_ENTERPRISE_CONTEXT
- INTERNET_OPTION_EXTENDED_ERROR
- INTERNET_OPTION_FROM_CACHE_TIMEOUT
- INTERNET_OPTION_HANDLE_TYPE
- INTERNET_OPTION_HSTS
- INTERNET_OPTION_HTTP_DECODING
- INTERNET_OPTION_HTTP_PROTOCOL_USED
- INTERNET_OPTION_HTTP_VERSION
- INTERNET_OPTION_IDENTITY
- INTERNET_OPTION_IDLE_STATE
- INTERNET_OPTION_IDN
- INTERNET_OPTION_IGNORE_OFFLINE
- INTERNET_OPTION_KEEP_CONNECTION
- INTERNET_OPTION_LISTEN_TIMEOUT
- INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER
- INTERNET_OPTION_MAX_CONNS_PER_PROXY
- INTERNET_OPTION_MAX_CONNS_PER_SERVER
- INTERNET_OPTION_OFFLINE_MODE
- INTERNET_OPTION_OFFLINE_SEMANTICS
- INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE
- INTERNET_OPTION_PARENT_HANDLE
- INTERNET_OPTION_PASSWORD
- INTERNET_OPTION_PER_CONNECTION_OPTION
- INTERNET_OPTION_POLICY
- INTERNET_OPTION_PROXY
- INTERNET_OPTION_PROXY_PASSWORD
- INTERNET_OPTION_PROXY_SETTINGS_CHANGED
- INTERNET_OPTION_PROXY_USERNAME
- INTERNET_OPTION_READ_BUFFER_SIZE
- INTERNET_OPTION_RECEIVE_THROUGHPUT
- INTERNET_OPTION_RECEIVE_TIMEOUT
- INTERNET_OPTION_REFRESH
- INTERNET_OPTION_REMOVE_IDENTITY
- INTERNET_OPTION_REQUEST_FLAGS
- INTERNET_OPTION_REQUEST_PRIORITY
- INTERNET_OPTION_RESET_URLCACHE_SESSION
- INTERNET_OPTION_SECONDARY_CACHE_KEY
- INTERNET_OPTION_SECURITY_CERTIFICATE
- INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT
- INTERNET_OPTION_SECURITY_FLAGS
- INTERNET_OPTION_SECURITY_KEY_BITNESS
- INTERNET_OPTION_SEND_THROUGHPUT
- INTERNET_OPTION_SEND_TIMEOUT
- INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT
- INTERNET_OPTION_SETTINGS_CHANGED
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- INTERNET_OPTION_SUPPRESS_BEHAVIOR
- INTERNET_OPTION_URL
- INTERNET_OPTION_USER_AGENT
- INTERNET_OPTION_USERNAME
- INTERNET_OPTION_VERSION
- INTERNET_OPTION_WRITE_BUFFER_SIZE
api_location:
- Wininet.h
- Winineti.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c99ca6f12836c620ed7c952e0ceb1844aee3b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343893"
---
# <a name="option-flags-winineth"></a><span data-ttu-id="f8462-104">Optionsflags (WinInet. h)</span><span class="sxs-lookup"><span data-stu-id="f8462-104">Option Flags (Wininet.h)</span></span>

<span data-ttu-id="f8462-105">Die folgenden Optionsflags werden mit den Funktionen [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-105">The following option flags are used with the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) functions.</span></span> <span data-ttu-id="f8462-106">Alle gültigen Optionsflags haben einen Wert größer oder gleich der **Internet \_ First- \_ Option** und kleiner oder gleich der **Internet \_ Last- \_ Option**.</span><span class="sxs-lookup"><span data-stu-id="f8462-106">All valid option flags have a value greater than or equal to **INTERNET\_FIRST\_OPTION** and less than or equal to **INTERNET\_LAST\_OPTION**.</span></span>

<dl> <dt>

<span data-ttu-id="f8462-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**Internet \_ Option \_ \_ Identität ändern**</span><span class="sxs-lookup"><span data-stu-id="f8462-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**INTERNET\_OPTION\_ALTER\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-108">80</span><span class="sxs-lookup"><span data-stu-id="f8462-108">80</span></span>
</dt> <dt>



<span data-ttu-id="f8462-109">Nicht implementiert</span><span class="sxs-lookup"><span data-stu-id="f8462-109">Not implemented</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**Internet \_ Option " \_ Async"**</span><span class="sxs-lookup"><span data-stu-id="f8462-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**INTERNET\_OPTION\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-111">30</span><span class="sxs-lookup"><span data-stu-id="f8462-111">30</span></span>
</dt> <dt>



<span data-ttu-id="f8462-112">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-112">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**Internet \_ Option \_ Async- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="f8462-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**INTERNET\_OPTION\_ASYNC\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-114">15</span><span class="sxs-lookup"><span data-stu-id="f8462-114">15</span></span>
</dt> <dt>



<span data-ttu-id="f8462-115">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-115">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**Internet \_ Option \_ Async- \_ Priorität**</span><span class="sxs-lookup"><span data-stu-id="f8462-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**INTERNET\_OPTION\_ASYNC\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-117">16</span><span class="sxs-lookup"><span data-stu-id="f8462-117">16</span></span>
</dt> <dt>



<span data-ttu-id="f8462-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-118">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**Internet \_ Option \_ " \_ bearbeiteten \_ Eintrag umgehen"**</span><span class="sxs-lookup"><span data-stu-id="f8462-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**INTERNET\_OPTION\_BYPASS\_EDITED\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-120">64</span><span class="sxs-lookup"><span data-stu-id="f8462-120">64</span></span>
</dt> <dt>



<span data-ttu-id="f8462-121">Legt den booleschen Wert fest, der bestimmt, ob das System das Netzwerk auf neueren Inhalt überprüfen und bearbeitete Cache Einträge überschreiben soll, wenn eine neuere Version gefunden wird, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-121">Sets or retrieves the Boolean value that determines if the system should check the network for newer content and overwrite edited cache entries if a newer version is found.</span></span> <span data-ttu-id="f8462-122">Wenn diese Einstellung auf " **true**" festgelegt ist, überprüft das System das Netzwerk auf neueren Inhalt und überschreibt den bearbeiteten Cache Eintrag mit der neueren Version.</span><span class="sxs-lookup"><span data-stu-id="f8462-122">If set to **True**, the system checks the network for newer content and overwrites the edited cache entry with the newer version.</span></span> <span data-ttu-id="f8462-123">Der Standardwert ist **false**. er gibt an, dass der bearbeitete Cache Eintrag ohne Überprüfung des Netzwerks verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8462-123">The default is **False**, which indicates that the edited cache entry should be used without checking the network.</span></span> <span data-ttu-id="f8462-124">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-124">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="f8462-125">Er ist nur in Microsoft Internet Explorer 5 oder höher gültig.</span><span class="sxs-lookup"><span data-stu-id="f8462-125">It is valid only in Microsoft Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**Internet- \_ options \_ Cache- \_ \_ Streamhandle**</span><span class="sxs-lookup"><span data-stu-id="f8462-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**INTERNET\_OPTION\_CACHE\_STREAM\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-127">27</span><span class="sxs-lookup"><span data-stu-id="f8462-127">27</span></span>
</dt> <dt>



<span data-ttu-id="f8462-128">Wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-128">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**Internet \_ Option \_ Cache- \_ Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="f8462-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**INTERNET\_OPTION\_CACHE\_TIMESTAMPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-130">69</span><span class="sxs-lookup"><span data-stu-id="f8462-130">69</span></span>
</dt> <dt>



<span data-ttu-id="f8462-131">Ruft eine [**Internet Cache-Zeit \_ \_ Stempel**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) Struktur ab, die die LastModified-Zeit enthält und die Zeit bis zum Ablauf der im Internet Cache gespeicherten Ressource abläuft.</span><span class="sxs-lookup"><span data-stu-id="f8462-131">Retrieves an [**INTERNET\_CACHE\_TIMESTAMPS**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) structure that contains the LastModified time and Expires time from the resource stored in the Internet cache.</span></span> <span data-ttu-id="f8462-132">Dieser Wert wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-132">This value is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**Rückruf der Internet \_ Option \_**</span><span class="sxs-lookup"><span data-stu-id="f8462-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**INTERNET\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-134">1</span><span class="sxs-lookup"><span data-stu-id="f8462-134">1</span></span>
</dt> <dt>



<span data-ttu-id="f8462-135">Legt die Adresse der Rückruffunktion fest, die für dieses Handle definiert ist, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-135">Sets or retrieves the address of the callback function defined for this handle.</span></span> <span data-ttu-id="f8462-136">Diese Option kann für alle [**HINTERNET**](appendix-a-hinternet-handles.md) -Handles verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-136">This option can be used on all [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="f8462-137">Wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-137">Used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**\_ \_ Rückruf \_ Filter für Internet Optionen**</span><span class="sxs-lookup"><span data-stu-id="f8462-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**INTERNET\_OPTION\_CALLBACK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-139">54</span><span class="sxs-lookup"><span data-stu-id="f8462-139">54</span></span>
</dt> <dt>



<span data-ttu-id="f8462-140">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-140">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**Internet \_ Option \_ Client \_ Zertifikat \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="f8462-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**INTERNET\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-142">84</span><span class="sxs-lookup"><span data-stu-id="f8462-142">84</span></span>
</dt> <dt>



<span data-ttu-id="f8462-143">Dieses Flag wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-143">This flag is not supported by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="f8462-144">Der *lpBuffer* -Parameter muss ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Struktur und kein Zeiger auf einen **CERT- \_ Kontext** Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="f8462-144">The *lpBuffer* parameter must be a pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure and not a pointer to a **CERT\_CONTEXT** pointer.</span></span> <span data-ttu-id="f8462-145">Wenn eine Anwendung ein **fehlerhafter \_ Internet \_ Client \_ \_ \_** Authentifizierungszertifikat erhält, muss Sie " [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) " anrufen oder " [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) " verwenden, um ein Zertifikat anzugeben, bevor Sie die Anforderung wiederholen.</span><span class="sxs-lookup"><span data-stu-id="f8462-145">If an application receives **ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**, it must call [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or use [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="f8462-146">[**Certduplikatecertifisprotext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) wird dann aufgerufen, sodass der übergebenen Zertifikat Kontext unabhängig von der Anwendung freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f8462-146">[**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) is then called so that the certificate context passed can be independently released by the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**Codepage für Internet- \_ Optionen \_**</span><span class="sxs-lookup"><span data-stu-id="f8462-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**INTERNET\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-148">68</span><span class="sxs-lookup"><span data-stu-id="f8462-148">68</span></span>
</dt> <dt>



<span data-ttu-id="f8462-149">Standardmäßig wird der Host-oder Autoritäts Teil der Unicode-URL gemäß der IDN-Spezifikation codiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-149">By default, the host or authority portion of the Unicode URL is encoded according to the IDN specification.</span></span> <span data-ttu-id="f8462-150">Wenn diese Option für die Anforderung oder das Verbindungs Handle festgelegt wird, wenn IDN deaktiviert ist, wird ein Code Page-Codierungsschema für den Hostteil der URL angegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-150">Setting this option on the request, or connection handle, when IDN is disabled, specifies a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="f8462-151">Der *lpBuffer* -Parameter im [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) -aufrufen enthält die gewünschte DBCS-Codepage.</span><span class="sxs-lookup"><span data-stu-id="f8462-151">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS code page.</span></span> <span data-ttu-id="f8462-152">Wenn in *lpBuffer* keine Codepage angegeben ist, verwendet Wininet die standardmäßige System Codepage (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="f8462-152">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span> <span data-ttu-id="f8462-153">Hinweis: diese Option wird ignoriert, wenn IDN nicht deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f8462-153">Note: This option is ignored if IDN is not disabled.</span></span> <span data-ttu-id="f8462-154">Weitere Informationen zum Deaktivieren von IDN finden Sie unter der Option " **Internet \_ Option \_ IDN** ".</span><span class="sxs-lookup"><span data-stu-id="f8462-154">For more information about how to disable IDN, see the **INTERNET\_OPTION\_IDN** option.</span></span>

<span data-ttu-id="f8462-155">**Windows XP mit SP2 und Windows Server 2003 mit SP1:** Dieses Flag wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-155">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="f8462-156">**Version:** Erfordert Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="f8462-156">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**Internet \_ Option \_ Codepage- \_ Pfad**</span><span class="sxs-lookup"><span data-stu-id="f8462-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**INTERNET\_OPTION\_CODEPAGE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-158">100</span><span class="sxs-lookup"><span data-stu-id="f8462-158">100</span></span>
</dt> <dt>



<span data-ttu-id="f8462-159">Standardmäßig ist der Pfadteil der URL UTF8-codiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-159">By default, the path portion of the URL is UTF8 encoded.</span></span> <span data-ttu-id="f8462-160">Die WinInet-API führt Escapezeichen (%) aus. Codierung der High-Bit-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f8462-160">The WinINet API performs escape character (%) encoding on the high-bit characters.</span></span> <span data-ttu-id="f8462-161">Wenn diese Option für die Anforderung oder das Verbindungs Handle festgelegt wird, wird die UTF8-Codierung deaktiviert und eine bestimmte Codepage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8462-161">Setting this option on the request, or connection handle, disables the UTF8 encoding and sets a specific code page.</span></span> <span data-ttu-id="f8462-162">Der *lpBuffer* -Parameter im [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) -aufrufen enthält die gewünschte DBCS-Codepage für den Pfad.</span><span class="sxs-lookup"><span data-stu-id="f8462-162">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the path.</span></span> <span data-ttu-id="f8462-163">Wenn in *lpBuffer* keine Codepage angegeben ist, verwendet Wininet die Standard-CP \_ UTF8.</span><span class="sxs-lookup"><span data-stu-id="f8462-163">If no code page is specified in *lpBuffer*, WinINet uses the default CP\_UTF8.</span></span>

<span data-ttu-id="f8462-164">**Windows XP mit SP2 und Windows Server 2003 mit SP1:** Dieses Flag wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-164">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="f8462-165">**Version:** Erfordert Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="f8462-165">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**Internet \_ Option \_ Codepage \_ extra**</span><span class="sxs-lookup"><span data-stu-id="f8462-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**INTERNET\_OPTION\_CODEPAGE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-167">101</span><span class="sxs-lookup"><span data-stu-id="f8462-167">101</span></span>
</dt> <dt>



<span data-ttu-id="f8462-168">Standardmäßig ist der Pfadteil der URL die standardmäßige System Codepage (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="f8462-168">By default, the path portion of the URL is the default system code page (CP\_ACP).</span></span> <span data-ttu-id="f8462-169">Das Escapezeichen (%) für den zusätzlichen Teil werden keine Konvertierungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8462-169">The escape character (%) conversions are not performed on the extra portion.</span></span> <span data-ttu-id="f8462-170">Wenn Sie diese Option für die Anforderung oder das Verbindungs Handle festlegen, wird die CP \_ ACP-Codierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f8462-170">Setting this option on the request, or connection handle disables the CP\_ACP encoding.</span></span> <span data-ttu-id="f8462-171">Der *lpBuffer* -Parameter im Aufrufen von [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) enthält die gewünschte DBCS-Codepage für den zusätzlichen Teil der URL.</span><span class="sxs-lookup"><span data-stu-id="f8462-171">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the extra portion of the URL.</span></span> <span data-ttu-id="f8462-172">Wenn in *lpBuffer* keine Codepage angegeben ist, verwendet Wininet die standardmäßige System Codepage (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="f8462-172">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="f8462-173">**Windows XP mit SP2 und Windows Server 2003 mit SP1:** Dieses Flag wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-173">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="f8462-174">**Version:** Erfordert Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="f8462-174">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**\_ \_ komprimierte \_ Inhalts \_ Länge für Internet Option**</span><span class="sxs-lookup"><span data-stu-id="f8462-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**INTERNET\_OPTION\_COMPRESSED\_CONTENT\_LENGTH**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-176">147</span><span class="sxs-lookup"><span data-stu-id="f8462-176">147</span></span>
</dt> <dt>



<span data-ttu-id="f8462-177">Bei einer Anforderung, bei der WinInet die von Server bereitgestellte Inhalts Codierung decodiert hat, ruft die vom Server gemeldete Inhalts Länge des Antwort Texts als ULONGLONG ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-177">For a request where WinInet decompressed the server s supplied Content-Encoding, retrieves the server-reported Content-Length of the response body as a ULONGLONG.</span></span> <span data-ttu-id="f8462-178">Unterstützt in Windows 10, Version 1507 und höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-178">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**Internet \_ Option \_ Connect- \_ Backoff**</span><span class="sxs-lookup"><span data-stu-id="f8462-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**INTERNET\_OPTION\_CONNECT\_BACKOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-180">4</span><span class="sxs-lookup"><span data-stu-id="f8462-180">4</span></span>
</dt> <dt>



<span data-ttu-id="f8462-181">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-181">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**Internet \_ Option \_ Connect- \_ Wiederholungs Versuche**</span><span class="sxs-lookup"><span data-stu-id="f8462-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**INTERNET\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-183">3</span><span class="sxs-lookup"><span data-stu-id="f8462-183">3</span></span>
</dt> <dt>



<span data-ttu-id="f8462-184">Legt einen ganz Zahl Wert ohne Vorzeichen fest oder ruft ihn ab, der angibt, wie oft WinInet versucht, aufzulösen und eine Verbindung mit einem Host herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f8462-184">Sets or retrieves an unsigned long integer value that contains the number of times WinINet attempts to resolve and connect to a host.</span></span> <span data-ttu-id="f8462-185">Es wird nur einmal pro IP-Adresse versucht.</span><span class="sxs-lookup"><span data-stu-id="f8462-185">It only attempts once per IP address.</span></span> <span data-ttu-id="f8462-186">Wenn Sie z. b. versuchen, eine Verbindung mit einem multithosthost herzustellen, der über zehn IP-Adressen verfügt, und \_ die Internet Option \_ Connect- \_ Wiederholungen auf sieben festgelegt ist, versucht WinInet nur, die ersten sieben IP-Adressen aufzulösen und eine Verbindung damit herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f8462-186">For example, if you attempt to connect to a multihome host that has ten IP addresses and INTERNET\_OPTION\_CONNECT\_RETRIES is set to seven, WinINet only attempts to resolve and connect to the first seven IP addresses.</span></span> <span data-ttu-id="f8462-187">Wenn hingegen die gleichen zehn IP-Adressen festgelegt sind, \_ \_ versucht WinInet, wenn die Verbindungs Wiederholungen für die Internet Option \_ auf 20 festgelegt sind, jede der zehn nur einmal.</span><span class="sxs-lookup"><span data-stu-id="f8462-187">Conversely, given the same set of ten IP addresses, if INTERNET\_OPTION\_CONNECT\_RETRIES is set to 20, WinINet attempts each of the ten only once.</span></span> <span data-ttu-id="f8462-188">Wenn ein Host nur über eine IP-Adresse verfügt und der erste Verbindungsversuch fehlschlägt, gibt es keine weiteren Versuche.</span><span class="sxs-lookup"><span data-stu-id="f8462-188">If a host has only one IP address and the first connection attempt fails, there are no further attempts.</span></span> <span data-ttu-id="f8462-189">Wenn nach der angegebenen Anzahl von versuchen nach wie vor ein Verbindungsversuch fehlschlägt, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f8462-189">If a connection attempt still fails after the specified number of attempts, the request is canceled.</span></span> <span data-ttu-id="f8462-190">Der Standardwert für die Internet \_ Option \_ Connect- \_ Wiederholungen sind fünf Versuche.</span><span class="sxs-lookup"><span data-stu-id="f8462-190">The default value for INTERNET\_OPTION\_CONNECT\_RETRIES is five attempts.</span></span> <span data-ttu-id="f8462-191">Diese Option kann für ein beliebiges [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet werden, einschließlich eines **null** -Handles.</span><span class="sxs-lookup"><span data-stu-id="f8462-191">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="f8462-192">Sie wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-192">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**\_ \_ Verbindungs \_ Zeit für Internet Option**</span><span class="sxs-lookup"><span data-stu-id="f8462-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**INTERNET\_OPTION\_CONNECT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-194">55</span><span class="sxs-lookup"><span data-stu-id="f8462-194">55</span></span>
</dt> <dt>



<span data-ttu-id="f8462-195">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-195">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**Internet \_ Option \_ Verbindungs \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="f8462-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**INTERNET\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-197">2</span><span class="sxs-lookup"><span data-stu-id="f8462-197">2</span></span>
</dt> <dt>



<span data-ttu-id="f8462-198">Legt einen ganz Zahl Wert ohne Vorzeichen fest oder ruft ihn ab, der den für Internet Verbindungsanforderungen zu verwendenden Timeout Wert in Millisekunden enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-198">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to use for Internet connection requests.</span></span> <span data-ttu-id="f8462-199">Wenn Sie diese Option auf unendlich (0xFFFFFFFF) festlegen, wird dieser Timer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f8462-199">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="f8462-200">Wenn eine Verbindungsanforderung länger dauert als dieser Timeout Wert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f8462-200">If a connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="f8462-201">Wenn Sie versuchen, eine Verbindung mit mehreren IP-Adressen für einen einzelnen Host (einen Host mit mehreren Heim Häusern) herzustellen, ist das Timeout Limit für alle IP-Adressen kumulativ.</span><span class="sxs-lookup"><span data-stu-id="f8462-201">When attempting to connect to multiple IP addresses for a single host (a multihome host), the timeout limit is cumulative for all of the IP addresses.</span></span> <span data-ttu-id="f8462-202">Diese Option kann für ein beliebiges [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet werden, einschließlich eines **null** -Handles.</span><span class="sxs-lookup"><span data-stu-id="f8462-202">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="f8462-203">Sie wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-203">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**\_ \_ verbundener Internet Options \_ Status**</span><span class="sxs-lookup"><span data-stu-id="f8462-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**INTERNET\_OPTION\_CONNECTED\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-205">50</span><span class="sxs-lookup"><span data-stu-id="f8462-205">50</span></span>
</dt> <dt>



<span data-ttu-id="f8462-206">Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der den verbundenen Zustand enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-206">Sets or retrieves an unsigned long integer value that contains the connected state.</span></span> <span data-ttu-id="f8462-207">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-207">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**Internet \_ options- \_ Kontext \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="f8462-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**INTERNET\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-209">45</span><span class="sxs-lookup"><span data-stu-id="f8462-209">45</span></span>
</dt> <dt>



<span data-ttu-id="f8462-210">Legt ein DWORD- \_ ptr fest, das die Adresse des Kontext Werts enthält, der diesem [**HINTERNET**](appendix-a-hinternet-handles.md) -Handle zugeordnet ist, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-210">Sets or retrieves a DWORD\_PTR that contains the address of the context value associated with this [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="f8462-211">Diese Option kann für ein beliebiges [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-211">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="f8462-212">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-212">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="f8462-213">Zuvor wurde der Kontextwert auf die Adresse festgelegt, die im **lpBuffer** -Zeiger gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f8462-213">Previously, this set the context value to the address stored in the **lpBuffer** pointer.</span></span> <span data-ttu-id="f8462-214">Dies wurde korrigiert, sodass der im Puffer gespeicherte Wert verwendet wird und dem [Internet Option- \_ \_ Kontext \_ Wert](/windows) Flag ein neuer Wert zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f8462-214">This has been corrected so that the value stored in the buffer is used and the [INTERNET\_OPTION\_CONTEXT\_VALUE](/windows) flag is assigned a new value.</span></span> <span data-ttu-id="f8462-215">Der alte Wert 10 wurde beibehalten, sodass für das alte Verhalten geschriebene Anwendungen weiterhin unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-215">The old value, 10, has been preserved so that applications written for the old behavior are still supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**Empfangs Timeout für das Internet \_ options \_ Steuerelement \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f8462-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**INTERNET\_OPTION\_CONTROL\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-217">6</span><span class="sxs-lookup"><span data-stu-id="f8462-217">6</span></span>
</dt> <dt>



<span data-ttu-id="f8462-218">Identisch mit [dem \_ \_ Empfangs \_ Timeout der Internet Option](/windows).</span><span class="sxs-lookup"><span data-stu-id="f8462-218">Identical to [INTERNET\_OPTION\_RECEIVE\_TIMEOUT](/windows).</span></span> <span data-ttu-id="f8462-219">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-219">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**\_ \_ \_ Sende Timeout für Internet Options Steuerung \_**</span><span class="sxs-lookup"><span data-stu-id="f8462-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**INTERNET\_OPTION\_CONTROL\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-221">5</span><span class="sxs-lookup"><span data-stu-id="f8462-221">5</span></span>
</dt> <dt>



<span data-ttu-id="f8462-222">Identisch mit [dem \_ \_ Sende \_ Timeout der Internet Option](/windows).</span><span class="sxs-lookup"><span data-stu-id="f8462-222">Identical to [INTERNET\_OPTION\_SEND\_TIMEOUT](/windows).</span></span> <span data-ttu-id="f8462-223">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-223">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**\_Timeout für \_ Daten \_ Empfangs \_ Timeout der Internet Option**</span><span class="sxs-lookup"><span data-stu-id="f8462-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**INTERNET\_OPTION\_DATA\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-225">8</span><span class="sxs-lookup"><span data-stu-id="f8462-225">8</span></span>
</dt> <dt>



<span data-ttu-id="f8462-226">Legt einen ganz Zahl Wert ohne Vorzeichen fest, der den Timeout Wert (in Millisekunden) enthält, um eine Antwort auf eine Anforderung für den Datenkanal einer FTP-Transaktion zu erhalten, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-226">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="f8462-227">Wenn die Antwort länger dauert als dieser Timeout Wert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f8462-227">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="f8462-228">Diese Option kann für ein beliebiges [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet werden, einschließlich eines **null** -Handles.</span><span class="sxs-lookup"><span data-stu-id="f8462-228">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="f8462-229">Sie wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-229">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="f8462-230">Dieses Flag hat keine Auswirkung auf die HTTP-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="f8462-230">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**Timeout für die Internet \_ Option- \_ Daten \_ Übermittlung \_**</span><span class="sxs-lookup"><span data-stu-id="f8462-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**INTERNET\_OPTION\_DATA\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-232">7</span><span class="sxs-lookup"><span data-stu-id="f8462-232">7</span></span>
</dt> <dt>



<span data-ttu-id="f8462-233">Legt einen langen ganzzahligen Wert ohne Vorzeichen (in Millisekunden) fest oder ruft ihn ab, der den Timeout Wert für das Senden einer Anforderung für den Datenkanal einer FTP-Transaktion enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-233">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="f8462-234">Wenn der Sendevorgang länger dauert als dieser Timeout Wert, wird der Sendevorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f8462-234">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="f8462-235">Diese Option kann für ein beliebiges [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet werden, einschließlich eines **null** -Handles.</span><span class="sxs-lookup"><span data-stu-id="f8462-235">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="f8462-236">Sie wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-236">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="f8462-237">Dieses Flag hat keine Auswirkung auf die HTTP-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="f8462-237">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**Internet \_ Option \_ DataFile- \_ Name**</span><span class="sxs-lookup"><span data-stu-id="f8462-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**INTERNET\_OPTION\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-239">33</span><span class="sxs-lookup"><span data-stu-id="f8462-239">33</span></span>
</dt> <dt>



<span data-ttu-id="f8462-240">Ruft einen Zeichen folgen Wert ab, der den Namen der Datei enthält, die eine heruntergeladene Entität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-240">Retrieves a string value that contains the name of the file backing a downloaded entity.</span></span> <span data-ttu-id="f8462-241">Dieses Flag ist gültig, nachdem [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)oder [**httpopererequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f8462-241">This flag is valid after [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) has completed.</span></span> <span data-ttu-id="f8462-242">Diese Option kann nur von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-242">This option can only be queried by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**Internet \_ Option \_ DataFile-Datei \_**</span><span class="sxs-lookup"><span data-stu-id="f8462-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**INTERNET\_OPTION\_DATAFILE\_EXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-244">96</span><span class="sxs-lookup"><span data-stu-id="f8462-244">96</span></span>
</dt> <dt>



<span data-ttu-id="f8462-245">Legt einen Zeichen folgen Wert fest, der die Erweiterung der Datei enthält, die eine heruntergeladene Entität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-245">Sets a string value that contains the extension of the file backing a downloaded entity.</span></span> <span data-ttu-id="f8462-246">Dieses Flag sollte vor dem Aufrufen von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**ftpopenfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-246">This flag should be set before calling [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="f8462-247">Diese Option kann nur von [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-247">This option can only be set by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**Internet \_ Option \_ Diagnose \_ - \_ Socketinformationen**</span><span class="sxs-lookup"><span data-stu-id="f8462-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**INTERNET\_OPTION\_DIAGNOSTIC\_SOCKET\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-249">67</span><span class="sxs-lookup"><span data-stu-id="f8462-249">67</span></span>
</dt> <dt>



<span data-ttu-id="f8462-250">Ruft eine [**Internet \_ Diagnose \_ Socket \_ Info**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) -Struktur ab, die Daten über eine angegebene HTTP-Anforderung enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-250">Retrieves an [**INTERNET\_DIAGNOSTIC\_SOCKET\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) structure that contains data about a specified HTTP Request.</span></span> <span data-ttu-id="f8462-251">Dieses Flag wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-251">This flag is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

<span data-ttu-id="f8462-252">**Windows 7:** Diese Option wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-252">**Windows 7:** This option is no longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**Internet \_ Option \_ Digest-Authentifizierung \_ \_ entladen**</span><span class="sxs-lookup"><span data-stu-id="f8462-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**INTERNET\_OPTION\_DIGEST\_AUTH\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-254">76</span><span class="sxs-lookup"><span data-stu-id="f8462-254">76</span></span>
</dt> <dt>



<span data-ttu-id="f8462-255">Veranlasst das System, das SSPI-Paket für die Digest-Authentifizierung abzumelden und alle für den Prozess erstellten Anmelde Informationen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f8462-255">Causes the system to log off the Digest authentication SSPI package, purging all of the credentials created for the process.</span></span> <span data-ttu-id="f8462-256">Für diese Option ist kein Puffer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8462-256">No buffer is required for this option.</span></span> <span data-ttu-id="f8462-257">Sie wird von [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-257">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**Internet \_ Option \_ \_ AutoDial deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="f8462-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**INTERNET\_OPTION\_DISABLE\_AUTODIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-259">70</span><span class="sxs-lookup"><span data-stu-id="f8462-259">70</span></span>
</dt> <dt>



<span data-ttu-id="f8462-260">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-260">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**Internet \_ Option \_ - \_ Timeout für getrennte Verbindung**</span><span class="sxs-lookup"><span data-stu-id="f8462-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**INTERNET\_OPTION\_DISCONNECTED\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-262">49</span><span class="sxs-lookup"><span data-stu-id="f8462-262">49</span></span>
</dt> <dt>



<span data-ttu-id="f8462-263">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-263">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**Internet \_ Option \_ \_ http- \_ Protokoll aktivieren**</span><span class="sxs-lookup"><span data-stu-id="f8462-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**INTERNET\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-265">148</span><span class="sxs-lookup"><span data-stu-id="f8462-265">148</span></span>
</dt> <dt>



<span data-ttu-id="f8462-266">Legt eine DWORD-Bitmaske von zulässigen erweiterten HTTP-Versionen fest.</span><span class="sxs-lookup"><span data-stu-id="f8462-266">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="f8462-267">Kann für beliebige handle-Typen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-267">May be set on any handle type.</span></span> <span data-ttu-id="f8462-268">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="f8462-268">Possible values are:</span></span>

-   <span data-ttu-id="f8462-269">HTTP \_ - \_ protokollflag \_ HTTP2 (0x2).</span><span class="sxs-lookup"><span data-stu-id="f8462-269">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="f8462-270">Unterstützt unter Windows 10, Version 1507 und höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-270">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="f8462-271">Ältere Versionen von http (1,1 und früher) können mit dieser Option nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-271">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="f8462-272">Der Standardwert ist 0x0.</span><span class="sxs-lookup"><span data-stu-id="f8462-272">The default is 0x0.</span></span> <span data-ttu-id="f8462-273">Unterstützt in Windows 10, Version 1507 und höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-273">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**Internet \_ Option \_ \_ Umleitungs \_ Cache \_ Lesen aktivieren**</span><span class="sxs-lookup"><span data-stu-id="f8462-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**INTERNET\_OPTION\_ENABLE\_REDIRECT\_CACHE\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-275">122</span><span class="sxs-lookup"><span data-stu-id="f8462-275">122</span></span>
</dt> <dt>



<span data-ttu-id="f8462-276">Legt bei einem Anforderungs handle einen booleschen Wert fest, der steuert, ob für eine bestimmte Anforderung Umleitungen aus dem WinInet-Cache zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-276">On a request handle, sets a Boolean controlling whether redirects will be returned from the WinInet cache for a given request.</span></span> <span data-ttu-id="f8462-277">Der Standardwert lautet FALSE.</span><span class="sxs-lookup"><span data-stu-id="f8462-277">The default is FALSE.</span></span> <span data-ttu-id="f8462-278">In Windows 8 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-278">Supported in Windows 8 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**Internet \_ Option " \_ \_ zusätzliche Codierung"**</span><span class="sxs-lookup"><span data-stu-id="f8462-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**INTERNET\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-280">155</span><span class="sxs-lookup"><span data-stu-id="f8462-280">155</span></span>
</dt> <dt>



<span data-ttu-id="f8462-281">Gibt einen booleschen Wert zurück, der angibt, ob nicht-ASCII-Zeichen in der Abfrage Zeichenfolge Prozent codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f8462-281">Gets/sets a BOOL indicating whether non-ASCII characters in the query string should be percent-encoded.</span></span> <span data-ttu-id="f8462-282">Der Standardwert lautet FALSE.</span><span class="sxs-lookup"><span data-stu-id="f8462-282">The default is FALSE.</span></span> <span data-ttu-id="f8462-283">Wird in Windows 8.1 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-283">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**Internet \_ Option \_ End \_ Browser \_ Sitzung**</span><span class="sxs-lookup"><span data-stu-id="f8462-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**INTERNET\_OPTION\_END\_BROWSER\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-285">42</span><span class="sxs-lookup"><span data-stu-id="f8462-285">42</span></span>
</dt> <dt>



<span data-ttu-id="f8462-286">Leert Einträge, die nicht aus dem Kenn Wort Cache auf dem Festplattenlaufwerk verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-286">Flushes entries not in use from the password cache on the hard disk drive.</span></span> <span data-ttu-id="f8462-287">Setzt auch die Cache Zeit zurück, die verwendet wird, wenn der Synchronisierungs Modus einmal pro Sitzung ist.</span><span class="sxs-lookup"><span data-stu-id="f8462-287">Also resets the cache time used when the synchronization mode is once-per-session.</span></span> <span data-ttu-id="f8462-288">Für diese Option ist kein Puffer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8462-288">No buffer is required for this option.</span></span> <span data-ttu-id="f8462-289">Diese wird von [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-289">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**Internet \_ Option- \_ Fehler \_ Maske**</span><span class="sxs-lookup"><span data-stu-id="f8462-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**INTERNET\_OPTION\_ERROR\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-291">62</span><span class="sxs-lookup"><span data-stu-id="f8462-291">62</span></span>
</dt> <dt>



<span data-ttu-id="f8462-292">Legt einen langen ganzzahligen Wert ohne Vorzeichen fest, der die Fehler Masken enthält, die von der Client Anwendung behandelt werden können.</span><span class="sxs-lookup"><span data-stu-id="f8462-292">Sets an unsigned long integer value that contains the error masks that can be handled by the client application.</span></span> <span data-ttu-id="f8462-293">Dies kann eine Kombination der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="f8462-293">This can be a combination of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f8462-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>Internet \_ Fehler \_ Maske \_ kombiniertes \_ Sek. \_ Zertifikat</span><span class="sxs-lookup"><span data-stu-id="f8462-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>INTERNET\_ERROR\_MASK\_COMBINED\_SEC\_CERT</span></span>
</dt> <dd>

<span data-ttu-id="f8462-295">0x2</span><span class="sxs-lookup"><span data-stu-id="f8462-295">0x2</span></span>

<span data-ttu-id="f8462-296">Gibt an, dass alle Zertifikat Fehler mit der gleichen Fehlerrückgabe gemeldet werden sollen, und zwar mit dem **Fehler \_ Internet \_ Sek. cert- \_ \_ Fehler**.</span><span class="sxs-lookup"><span data-stu-id="f8462-296">Indicates that all certificate errors are to be reported using the same error return, namely **ERROR\_INTERNET\_SEC\_CERT\_ERRORS**.</span></span> <span data-ttu-id="f8462-297">Wenn dieses Flag festgelegt ist, wenden Sie bei Empfang des **Fehlers " \_ Internet \_ sec \_ CERT \_ Errors** " den Fehler " **internetterrordlg** " an, damit der Benutzer auf ein bekanntes Dialogfeld reagieren kann, das das Problem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f8462-297">If this flag is set, call **InternetErrorDlg** upon receiving the **ERROR\_INTERNET\_SEC\_CERT\_ERRORS** error, so that the user can respond to a familiar dialog describing the problem.</span></span>

> [!Caution]  
> <span data-ttu-id="f8462-298">Wenn Sie den Benutzer nicht über diesen Fehler informieren, macht der Benutzer potenzielle Spoofingangriffe.</span><span class="sxs-lookup"><span data-stu-id="f8462-298">Failing to inform the user of this error exposes the user to potential spoofing attacks.</span></span>

 

</dd> <dt>

<span data-ttu-id="f8462-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>Internet \_ Fehler \_ Maske \_ Insert- \_ CDROM</span><span class="sxs-lookup"><span data-stu-id="f8462-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>INTERNET\_ERROR\_MASK\_INSERT\_CDROM</span></span>
</dt> <dd>

<span data-ttu-id="f8462-300">0x1</span><span class="sxs-lookup"><span data-stu-id="f8462-300">0x1</span></span>

<span data-ttu-id="f8462-301">Gibt an, dass die Client Anwendung den Fehlercode für den **Fehler \_ Internet \_ Insert- \_ CDROM** verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="f8462-301">Indicates that the client application can handle the **ERROR\_INTERNET\_INSERT\_CDROM** error code.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>Fehler beim Anmelden der Internet \_ Fehler \_ Maske \_ Anzeige des \_ \_ \_ Entitäts \_ Texts</span><span class="sxs-lookup"><span data-stu-id="f8462-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY</span></span>
</dt> <dd>

<span data-ttu-id="f8462-303">0x8</span><span class="sxs-lookup"><span data-stu-id="f8462-303">0x8</span></span>

<span data-ttu-id="f8462-304">Gibt an, dass die Client Anwendung den Fehlercode für die **Fehlermeldung der \_ Internet \_ Anmeldung \_ \_ anzeigen \_ \_** kann.</span><span class="sxs-lookup"><span data-stu-id="f8462-304">Indicates that the client application can handle the **ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY** error code.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>Internet \_ Fehler \_ Maske \_ benötigt \_ MSN \_ SSPI \_ pkg</span><span class="sxs-lookup"><span data-stu-id="f8462-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>INTERNET\_ERROR\_MASK\_NEED\_MSN\_SSPI\_PKG</span></span>
</dt> <dd>

<span data-ttu-id="f8462-306">0x4</span><span class="sxs-lookup"><span data-stu-id="f8462-306">0x4</span></span>

<span data-ttu-id="f8462-307">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-307">Not implemented.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="f8462-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**Internet \_ Option \_ Enterprise \_ context**</span><span class="sxs-lookup"><span data-stu-id="f8462-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**INTERNET\_OPTION\_ENTERPRISE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-309">159</span><span class="sxs-lookup"><span data-stu-id="f8462-309">159</span></span>
</dt> <dt>



<span data-ttu-id="f8462-310">Legt einen pwstr mit der Unternehmens-ID fest (siehe https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) , was für die Anforderung gilt).</span><span class="sxs-lookup"><span data-stu-id="f8462-310">Sets a PWSTR containing the Enterprise ID (see https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) which applies to the request.</span></span> <span data-ttu-id="f8462-311">Unterstützt in Windows 10, Version 1507 und höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-311">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**\_Erweiterte Internet Option- \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="f8462-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**INTERNET\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-313">24</span><span class="sxs-lookup"><span data-stu-id="f8462-313">24</span></span>
</dt> <dt>



<span data-ttu-id="f8462-314">Ruft den Wert einer langen ganzen Zahl ohne Vorzeichen ab, der einen Winsock-Fehlercode enthält, der den **Fehlern \_ \_** angezeigt wird, die zuletzt in diesem Thread Kontext zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="f8462-314">Retrieves an unsigned long integer value that contains a Winsock error code mapped to the **ERROR\_INTERNET\_** error messages last returned in this thread context.</span></span> <span data-ttu-id="f8462-315">Diese Option wird für ein **null**-[**HINTERNET**](appendix-a-hinternet-handles.md) Handle von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-315">This option is used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**Internet \_ Option \_ von \_ Cache \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="f8462-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**INTERNET\_OPTION\_FROM\_CACHE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-317">63</span><span class="sxs-lookup"><span data-stu-id="f8462-317">63</span></span>
</dt> <dt>



<span data-ttu-id="f8462-318">Legt den Wert A1n Long Integer ohne Vorzeichen fest oder ruft ihn ab, der die Zeitspanne enthält, die das System auf eine Antwort auf eine Netzwerk Anforderung warten soll, bevor der Cache auf eine Kopie der Ressource überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="f8462-318">Sets or retrieves a1n unsigned long integer value that contains the amount of time the system should wait for a response to a network request before checking the cache for a copy of the resource.</span></span> <span data-ttu-id="f8462-319">Wenn eine Netzwerk Anforderung länger als die angegebene Zeit dauert und die angeforderte Ressource im Cache verfügbar ist, wird die Ressource aus dem Cache abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f8462-319">If a network request takes longer than the time specified and the requested resource is available in the cache, the resource is retrieved from the cache.</span></span> <span data-ttu-id="f8462-320">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-320">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**Internet- \_ options \_ handle- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="f8462-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**INTERNET\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-322">9</span><span class="sxs-lookup"><span data-stu-id="f8462-322">9</span></span>
</dt> <dt>



<span data-ttu-id="f8462-323">Ruft einen ganzzahligen langen ganzzahligen Wert ohne Vorzeichen ab, der den Typ der weiter gegebenen [**hinternethandles**](appendix-a-hinternet-handles.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-323">Retrieves an unsigned long integer value that contains the type of the [**HINTERNET**](appendix-a-hinternet-handles.md) handles passed in.</span></span> <span data-ttu-id="f8462-324">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) für beliebige [hinternethandles](appendix-a-hinternet-handles.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-324">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) on any [HINTERNET](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="f8462-325">Folgende Rückgabewerte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="f8462-325">Possible return values include the following.</span></span>

<dl> <dt>

<span data-ttu-id="f8462-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>Internet \_ handle \_ - \_ Typ \_ FTP-Verbindung</span><span class="sxs-lookup"><span data-stu-id="f8462-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_FTP</span></span>
</dt> <dd>

<span data-ttu-id="f8462-327">2</span><span class="sxs-lookup"><span data-stu-id="f8462-327">2</span></span>

</dd> <dt>

<span data-ttu-id="f8462-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>Internet \_ handle- \_ Typ \_ Connect \_ gopher</span><span class="sxs-lookup"><span data-stu-id="f8462-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_GOPHER</span></span>
</dt> <dd>

<span data-ttu-id="f8462-329">3</span><span class="sxs-lookup"><span data-stu-id="f8462-329">3</span></span>

</dd> <dt>

<span data-ttu-id="f8462-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>Internet \_ handle \_ - \_ Typ \_ http verbinden</span><span class="sxs-lookup"><span data-stu-id="f8462-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="f8462-331">4</span><span class="sxs-lookup"><span data-stu-id="f8462-331">4</span></span>

</dd> <dt>

<span data-ttu-id="f8462-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>\_ \_ \_ Datei Anforderung des Typs "Internet Handle" \_</span><span class="sxs-lookup"><span data-stu-id="f8462-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>INTERNET\_HANDLE\_TYPE\_FILE\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="f8462-333">14</span><span class="sxs-lookup"><span data-stu-id="f8462-333">14</span></span>

</dd> <dt>

<span data-ttu-id="f8462-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>FTP-Datei für Internet Handle- \_ \_ Typ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f8462-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="f8462-335">7</span><span class="sxs-lookup"><span data-stu-id="f8462-335">7</span></span>

</dd> <dt>

<span data-ttu-id="f8462-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>Internet \_ handle- \_ Typ \_ FTP- \_ Datei \_ HTML</span><span class="sxs-lookup"><span data-stu-id="f8462-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="f8462-337">8</span><span class="sxs-lookup"><span data-stu-id="f8462-337">8</span></span>

</dd> <dt>

<span data-ttu-id="f8462-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>\_FTP- \_ \_ \_ Suche mit Internet Handle-Typ</span><span class="sxs-lookup"><span data-stu-id="f8462-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="f8462-339">5</span><span class="sxs-lookup"><span data-stu-id="f8462-339">5</span></span>

</dd> <dt>

<span data-ttu-id="f8462-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>Internet \_ handle \_ Typ \_ FTP- \_ Suche- \_ HTML</span><span class="sxs-lookup"><span data-stu-id="f8462-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="f8462-341">6</span><span class="sxs-lookup"><span data-stu-id="f8462-341">6</span></span>

</dd> <dt>

<span data-ttu-id="f8462-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>\_Typ- \_ \_ Gopher- \_ Datei des Internet Handles</span><span class="sxs-lookup"><span data-stu-id="f8462-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="f8462-343">11</span><span class="sxs-lookup"><span data-stu-id="f8462-343">11</span></span>

</dd> <dt>

<span data-ttu-id="f8462-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>Internet \_ handle \_ Type \_ Gopher \_ file \_ HTML</span><span class="sxs-lookup"><span data-stu-id="f8462-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="f8462-345">12</span><span class="sxs-lookup"><span data-stu-id="f8462-345">12</span></span>

</dd> <dt>

<span data-ttu-id="f8462-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>Art der Internet \_ handle- \_ \_ \_ Suche</span><span class="sxs-lookup"><span data-stu-id="f8462-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="f8462-347">9</span><span class="sxs-lookup"><span data-stu-id="f8462-347">9</span></span>

</dd> <dt>

<span data-ttu-id="f8462-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>Internet \_ handle \_ Type \_ Gopher \_ Find \_ HTML</span><span class="sxs-lookup"><span data-stu-id="f8462-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="f8462-349">10</span><span class="sxs-lookup"><span data-stu-id="f8462-349">10</span></span>

</dd> <dt>

<span data-ttu-id="f8462-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>HTTP-Anforderung für Internet Handle- \_ \_ Typ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f8462-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>INTERNET\_HANDLE\_TYPE\_HTTP\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="f8462-351">13</span><span class="sxs-lookup"><span data-stu-id="f8462-351">13</span></span>

</dd> <dt>

<span data-ttu-id="f8462-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>Internet \_ handle \_ Type \_ Internet</span><span class="sxs-lookup"><span data-stu-id="f8462-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>INTERNET\_HANDLE\_TYPE\_INTERNET</span></span>
</dt> <dd>

<span data-ttu-id="f8462-353">1</span><span class="sxs-lookup"><span data-stu-id="f8462-353">1</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="f8462-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**Internet \_ Option \_ hsts**</span><span class="sxs-lookup"><span data-stu-id="f8462-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**INTERNET\_OPTION\_HSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-355">157</span><span class="sxs-lookup"><span data-stu-id="f8462-355">157</span></span>
</dt> <dt>



<span data-ttu-id="f8462-356">Dient zum Abrufen oder Festlegen eines booleschen Werts, der angibt, ob WinInet http-hsts-Direktiven (Strict Transport Security) von Servern folgen soll</span><span class="sxs-lookup"><span data-stu-id="f8462-356">Gets/sets a BOOL indicating whether WinInet should follow HTTP Strict Transport Security (HSTS) directives from servers.</span></span> <span data-ttu-id="f8462-357">Wenn diese Option aktiviert ist, werden https://-Schemas für Domänen, die eine hsts-Richtlinie aufweisen, die von WinInet zwischengespeichert wird, zu übereinstimmenden</span><span class="sxs-lookup"><span data-stu-id="f8462-357">If enabled, https:// schemed requests to domains which have an HSTS policy cached by WinInet will be redirected to matching https:// URLs.</span></span> <span data-ttu-id="f8462-358">Der Standardwert lautet FALSE.</span><span class="sxs-lookup"><span data-stu-id="f8462-358">The default is FALSE.</span></span> <span data-ttu-id="f8462-359">Wird in Windows 8.1 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-359">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**Internet \_ Option \_ http- \_ Decodierung**</span><span class="sxs-lookup"><span data-stu-id="f8462-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**INTERNET\_OPTION\_HTTP\_DECODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-361">65</span><span class="sxs-lookup"><span data-stu-id="f8462-361">65</span></span>
</dt> <dt>



<span data-ttu-id="f8462-362">Ermöglicht WinInet das Ausführen von Decodierung für die gzip-und Deflate-Codierungs Schemas.</span><span class="sxs-lookup"><span data-stu-id="f8462-362">Enables WinINet to perform decoding for the gzip and deflate encoding schemes.</span></span> <span data-ttu-id="f8462-363">Weitere Informationen finden Sie unter [**Content Encoding**](content-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="f8462-363">For more information, see [**Content Encoding**](content-encoding.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**Internet \_ Option \_ http- \_ Protokoll \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="f8462-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**INTERNET\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-365">149</span><span class="sxs-lookup"><span data-stu-id="f8462-365">149</span></span>
</dt> <dt>



<span data-ttu-id="f8462-366">Ruft ein DWORD ab, das angibt, welche erweiterte http-Version für eine bestimmte Anforderung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f8462-366">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="f8462-367">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="f8462-367">Possible values are:</span></span>

-   <span data-ttu-id="f8462-368">HTTP \_ - \_ protokollflag \_ HTTP2 (0x2).</span><span class="sxs-lookup"><span data-stu-id="f8462-368">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="f8462-369">Unterstützt unter Windows 10, Version 1507 und höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-369">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="f8462-370">0x0 gibt HTTP/1.1 oder früher an; \_ \_ \_ Wenn mehr Genauigkeit erforderlich ist, um zu erfahren, welche Legacy Version verwendet wurde, finden Sie weitere Informationen unter http-Version</span><span class="sxs-lookup"><span data-stu-id="f8462-370">0x0 indicates HTTP/1.1 or earlier; see INTERNET\_OPTION\_HTTP\_VERSION if more precision is needed about which legacy version was used.</span></span> <span data-ttu-id="f8462-371">Unterstützt unter Windows 10, Version 1507 und höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-371">Supported on Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**Internet \_ Option \_ http- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="f8462-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**INTERNET\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-373">59</span><span class="sxs-lookup"><span data-stu-id="f8462-373">59</span></span>
</dt> <dt>



<span data-ttu-id="f8462-374">Legt eine [**http- \_ Versions \_ Informations**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) Struktur fest, die die unterstützte HTTP-Version enthält, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-374">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure that contains the supported HTTP version.</span></span> <span data-ttu-id="f8462-375">Dies muss für ein **null** -Handle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-375">This must be used on a **NULL** handle.</span></span> <span data-ttu-id="f8462-376">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-376">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="f8462-377">Unter Windows 7, Windows Server 2008 R2 und höher wird der Wert des Members **dwMinorVersion** in der HTTP- [**\_ Versions \_ Informations**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) Struktur von Internet Explorer-Einstellungen überschrieben.</span><span class="sxs-lookup"><span data-stu-id="f8462-377">On Windows 7, Windows Server 2008 R2, and later, the value of the **dwMinorVersion** member in the [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure is overridden by Internet Explorer settings.</span></span> <span data-ttu-id="f8462-378">**EnableHttp1 \_ 1** ist ein Registrierungs Wert unter " **HKLM \\ Software \\ Microsoft \\ InternetExplorer \\ advacnedoptions \\ http \\ Genable** by Internet Options", der in Internet Explorer für das System festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f8462-378">**EnableHttp1\_1** is a registry value under **HKLM\\Software\\Microsoft\\InternetExplorer\\AdvacnedOptions\\HTTP\\GENABLE** controlled by Internet Options set in Internet Explorer for the system.</span></span> <span data-ttu-id="f8462-379">Der Wert **EnableHttp1 \_ 1** ist standardmäßig 1.</span><span class="sxs-lookup"><span data-stu-id="f8462-379">The **EnableHttp1\_1** value defaults to 1.</span></span> <span data-ttu-id="f8462-380">Die **http- \_ Versions \_ Informations** Struktur wird für jede HTTP-Version, die kleiner als 1,1 ist, ignoriert, wenn **EnableHttp1 \_ 1** auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f8462-380">The **HTTP\_VERSION\_INFO** structure is ignored for any HTTP version less than 1.1 if **EnableHttp1\_1** is set to 1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**Internet \_ options \_ Identität**</span><span class="sxs-lookup"><span data-stu-id="f8462-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**INTERNET\_OPTION\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-382">78</span><span class="sxs-lookup"><span data-stu-id="f8462-382">78</span></span>
</dt> <dt>



<span data-ttu-id="f8462-383">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-383">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**Internet \_ Option im \_ Leerlauf \_ Zustand**</span><span class="sxs-lookup"><span data-stu-id="f8462-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**INTERNET\_OPTION\_IDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-385">51</span><span class="sxs-lookup"><span data-stu-id="f8462-385">51</span></span>
</dt> <dt>



<span data-ttu-id="f8462-386">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-386">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**Internet \_ Option \_ IDN**</span><span class="sxs-lookup"><span data-stu-id="f8462-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**INTERNET\_OPTION\_IDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-388">102</span><span class="sxs-lookup"><span data-stu-id="f8462-388">102</span></span>
</dt> <dt>



<span data-ttu-id="f8462-389">Standardmäßig wird der Host-oder Autoritäts Teil der URL gemäß der IDN-Spezifikation sowohl für direkte als auch für Proxy Verbindungen codiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-389">By default, the host or authority portion of the URL is encoded according to the IDN specification for both direct and proxy connections.</span></span> <span data-ttu-id="f8462-390">Diese Option kann für die Anforderung oder das Verbindungs Handle verwendet werden, um IDN zu aktivieren bzw. zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f8462-390">This option can be used on the request, or connection handle to enable or disable IDN.</span></span> <span data-ttu-id="f8462-391">Wenn IDN deaktiviert ist, verwendet Wininet die System Codepage, um den Host-oder Autoritäts Teil der URL zu codieren.</span><span class="sxs-lookup"><span data-stu-id="f8462-391">When IDN is disabled, WinINet uses the system codepage to encode the host or authority portion of the URL.</span></span> <span data-ttu-id="f8462-392">Um die IDN-Host Konvertierung zu deaktivieren, legen Sie den *lpBuffer* -Parameter im-Rückruf auf " [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) " auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="f8462-392">To disable IDN host conversion, set the *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to zero.</span></span> <span data-ttu-id="f8462-393">Um die IDN-Konvertierung nur für die direkte Verbindung zu aktivieren, geben Sie **Internet Kennzeichen \_ \_ IDN \_ Direct** im *lpBuffer* -Parameter des Aufrufes **internettoption** an.</span><span class="sxs-lookup"><span data-stu-id="f8462-393">To enable IDN conversion on only the direct connection, specify **INTERNET\_FLAG\_IDN\_DIRECT** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span> <span data-ttu-id="f8462-394">Um die IDN-Konvertierung nur für die Proxy Verbindung zu aktivieren, geben Sie **Internet Kennzeichen \_ \_ IDN- \_ Proxy** im " *lpBuffer* "-Parameter im " **InternetSetOption**"-Aufrufen an.</span><span class="sxs-lookup"><span data-stu-id="f8462-394">To enable IDN conversion on only the proxy connection, specify **INTERNET\_FLAG\_IDN\_PROXY** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span>

<span data-ttu-id="f8462-395">**Windows XP mit SP2 und Windows Server 2003 mit SP1:** Dieses Flag wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8462-395">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="f8462-396">**Version:** Erfordert Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="f8462-396">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**Internet \_ Option \_ \_ Offline ignorieren**</span><span class="sxs-lookup"><span data-stu-id="f8462-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**INTERNET\_OPTION\_IGNORE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-398">77</span><span class="sxs-lookup"><span data-stu-id="f8462-398">77</span></span>
</dt> <dt>



<span data-ttu-id="f8462-399">Legt fest oder Ruft ab, ob das globale Offline-Flag für das angegebene Anforderungs handle ignoriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8462-399">Sets or retrieves whether the global offline flag should be ignored for the specified request handle.</span></span> <span data-ttu-id="f8462-400">Für diese Option ist kein Puffer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8462-400">No buffer is required for this option.</span></span> <span data-ttu-id="f8462-401">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) mit einem Anforderungs Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-401">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with a request handle.</span></span> <span data-ttu-id="f8462-402">Diese Option ist nur in Internet Explorer 5 oder höher gültig.</span><span class="sxs-lookup"><span data-stu-id="f8462-402">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**Internet \_ Option \_ \_ Verbindung beibehalten**</span><span class="sxs-lookup"><span data-stu-id="f8462-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**INTERNET\_OPTION\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-404">22</span><span class="sxs-lookup"><span data-stu-id="f8462-404">22</span></span>
</dt> <dt>



<span data-ttu-id="f8462-405">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-405">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**Internet- \_ Option- \_ \_ timeout Timeout**</span><span class="sxs-lookup"><span data-stu-id="f8462-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**INTERNET\_OPTION\_LISTEN\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-407">11</span><span class="sxs-lookup"><span data-stu-id="f8462-407">11</span></span>
</dt> <dt>



<span data-ttu-id="f8462-408">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-408">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**Internet \_ Option max. Anzahl der \_ \_ \_ pro \_ 1 \_ 0 \_ Server**</span><span class="sxs-lookup"><span data-stu-id="f8462-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-410">74</span><span class="sxs-lookup"><span data-stu-id="f8462-410">74</span></span>
</dt> <dt>



<span data-ttu-id="f8462-411">Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der die maximale Anzahl von Verbindungen pro HTTP/1.0-Server enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-411">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="f8462-412">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-412">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="f8462-413">Diese Option ist nur in Internet Explorer 5 oder höher gültig.</span><span class="sxs-lookup"><span data-stu-id="f8462-413">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**Internet Option max. Anzahl von Verbindungs- \_ \_ \_ \_ und \_ Proxy Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="f8462-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-415">103</span><span class="sxs-lookup"><span data-stu-id="f8462-415">103</span></span>
</dt> <dt>



<span data-ttu-id="f8462-416">Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der die maximale Anzahl von Verbindungen pro CERN-Proxy enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-416">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per CERN proxy.</span></span> <span data-ttu-id="f8462-417">Wenn diese Option festgelegt oder abgerufen wird, muss der *HINTERNET* -Parameter auf einen **null** -handle-Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-417">When this option is set or retrieved, the *hInternet* parameter must set to a **null** handle value.</span></span> <span data-ttu-id="f8462-418">Ein **null** -handle-Wert gibt an, dass die Option für den aktuellen Prozess festgelegt oder abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8462-418">A **null** handle value indicates that the option should be set or queried for the current process.</span></span> <span data-ttu-id="f8462-419">Wenn Sie " [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) " mit dieser Option aufrufen, erhalten alle vorhandenen Proxy Objekte den neuen Wert.</span><span class="sxs-lookup"><span data-stu-id="f8462-419">When calling [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with this option, all existing proxy objects will receive the new value.</span></span> <span data-ttu-id="f8462-420">Dieser Wert ist auf einen Bereich von 2 bis 128 (einschließlich) beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f8462-420">This value is limited to a range of 2 to 128, inclusive.</span></span>

<span data-ttu-id="f8462-421">**Version:** Erfordert Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="f8462-421">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**Internet Option max. Anzahl von Verbindungs \_ \_ \_ \_ \_ Servern pro Server**</span><span class="sxs-lookup"><span data-stu-id="f8462-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-423">73</span><span class="sxs-lookup"><span data-stu-id="f8462-423">73</span></span>
</dt> <dt>



<span data-ttu-id="f8462-424">Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der die maximale Anzahl der pro Server zulässigen Verbindungen enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-424">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="f8462-425">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-425">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="f8462-426">Diese Option ist nur in Internet Explorer 5 oder höher gültig.</span><span class="sxs-lookup"><span data-stu-id="f8462-426">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**Internet \_ Option ( \_ Offline \_ Modus)**</span><span class="sxs-lookup"><span data-stu-id="f8462-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**INTERNET\_OPTION\_OFFLINE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-428">26</span><span class="sxs-lookup"><span data-stu-id="f8462-428">26</span></span>
</dt> <dt>



<span data-ttu-id="f8462-429">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-429">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**\_ \_ Offline \_ Semantik der Internet Option**</span><span class="sxs-lookup"><span data-stu-id="f8462-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**INTERNET\_OPTION\_OFFLINE\_SEMANTICS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-431">52</span><span class="sxs-lookup"><span data-stu-id="f8462-431">52</span></span>
</dt> <dt>



<span data-ttu-id="f8462-432">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-432">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**Internet \_ Option \_ zur Auswahl einer \_ \_ schwachen \_ Signatur**</span><span class="sxs-lookup"><span data-stu-id="f8462-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**INTERNET\_OPTION\_OPT\_IN\_WEAK\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-434">176</span><span class="sxs-lookup"><span data-stu-id="f8462-434">176</span></span>
</dt> <dt>



<span data-ttu-id="f8462-435">Abonnieren Sie schwache Signaturen (z. b. SHA-1) als unsicher behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-435">Opt-in for weak signatures (e.g. SHA-1) to be treated as insecure.</span></span> <span data-ttu-id="f8462-436">Dies weist WinInet an, [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) mithilfe des Parameters " **CERT \_ Chain \_ opt \_ in \_ Weak \_ Signature** " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f8462-436">This will instruct WinInet to call [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) using the **CERT\_CHAIN\_OPT\_IN\_WEAK\_SIGNATURE** parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**über \_ \_ geordnetes \_ Handle der Internet Option**</span><span class="sxs-lookup"><span data-stu-id="f8462-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**INTERNET\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-438">21</span><span class="sxs-lookup"><span data-stu-id="f8462-438">21</span></span>
</dt> <dt>



<span data-ttu-id="f8462-439">Ruft das übergeordnete Handle für dieses Handle ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-439">Retrieves the parent handle to this handle.</span></span> <span data-ttu-id="f8462-440">Diese Option kann für ein beliebiges [**hinternethandle**](appendix-a-hinternet-handles.md) von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-440">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**Internet \_ options \_ Kennwort**</span><span class="sxs-lookup"><span data-stu-id="f8462-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**INTERNET\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-442">29</span><span class="sxs-lookup"><span data-stu-id="f8462-442">29</span></span>
</dt> <dt>



<span data-ttu-id="f8462-443">Legt einen Zeichen folgen Wert fest oder ruft ihn ab, der das Kennwort enthält, das einem von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zurückgegebenen Handle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f8462-443">Sets or retrieves a string value that contains the password associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="f8462-444">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-444">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**Option "Internet \_ Option \_ pro \_ Verbindung \_ "**</span><span class="sxs-lookup"><span data-stu-id="f8462-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-446">75</span><span class="sxs-lookup"><span data-stu-id="f8462-446">75</span></span>
</dt> <dt>



<span data-ttu-id="f8462-447">Legt eine [**Internet \_ pro \_ conn- \_ options \_ Listen**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) Struktur fest oder ruft Sie ab, die eine Liste von Optionen für eine bestimmte Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="f8462-447">Sets or retrieves an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure that specifies a list of options for a particular connection.</span></span> <span data-ttu-id="f8462-448">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-448">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="f8462-449">Diese Option ist nur in Internet Explorer 5 oder höher gültig.</span><span class="sxs-lookup"><span data-stu-id="f8462-449">This option is only valid in Internet Explorer 5 and later.</span></span>

> [!Note]  
> <span data-ttu-id="f8462-450">**Internet \_ Die \_ Option \_ pro \_ Verbindung** bewirkt, dass die Einstellungen auf systemweite Weise geändert werden, wenn ein **null** -Handle beim [**Internet-toption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8462-450">**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION** causes the settings to be changed on a system-wide basis when a **NULL** handle is used in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="f8462-451">Um die globalen Proxy Einstellungen zu aktualisieren, müssen Sie **InternetSetOption** mit dem Flag "Option aktualisieren" der **Internet \_ Option \_** abrufen.</span><span class="sxs-lookup"><span data-stu-id="f8462-451">To refresh the global proxy settings, you must call **InternetSetOption** with the **INTERNET\_OPTION\_REFRESH** option flag.</span></span>

 

> [!Note]  
> <span data-ttu-id="f8462-452">Verwenden Sie diese Option für das Handle, das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)zurückgegeben wird, um die Proxy Informationen für den gesamten Prozess zu ändern, ohne dass sich dies auf die globalen Einstellungen in Internet Explorer 5 oder höher auswirkt.</span><span class="sxs-lookup"><span data-stu-id="f8462-452">To change proxy information for the entire process without affecting the global settings in Internet Explorer 5 and later, use this option on the handle that is returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="f8462-453">Im folgenden Codebeispiel wird der Proxy für den gesamten Prozess geändert, obwohl das [**HINTERNET**](appendix-a-hinternet-handles.md) -Handle geschlossen ist und nicht von Anforderungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f8462-453">The following code example changes the proxy for the whole process even though the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is closed and is not used by any requests.</span></span>

 

<span data-ttu-id="f8462-454">Weitere Informationen und Codebeispiele finden Sie im [KB-Artikel 226473](https://support.microsoft.com/kb/226473).</span><span class="sxs-lookup"><span data-stu-id="f8462-454">For more information and code examples, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**Internet \_ options \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="f8462-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**INTERNET\_OPTION\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-456">48</span><span class="sxs-lookup"><span data-stu-id="f8462-456">48</span></span>
</dt> <dt>



<span data-ttu-id="f8462-457">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-457">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**Internet \_ options \_ Proxy**</span><span class="sxs-lookup"><span data-stu-id="f8462-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**INTERNET\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-459">38</span><span class="sxs-lookup"><span data-stu-id="f8462-459">38</span></span>
</dt> <dt>



<span data-ttu-id="f8462-460">Legt eine [**Internet \_ Proxy \_ Info**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) -Struktur fest oder ruft Sie ab, die die Proxy Daten für ein vorhandenes [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Handle enthält, wenn das [**hinternethandle**](appendix-a-hinternet-handles.md) nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="f8462-460">Sets or retrieves an [**INTERNET\_PROXY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) structure that contains the proxy data for an existing [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) handle when the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is not **NULL**.</span></span> <span data-ttu-id="f8462-461">Wenn das [**hinternethandle**](appendix-a-hinternet-handles.md) **null** ist, legt die Funktion die globalen Proxy Daten fest oder fragt Sie ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-461">If the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is **NULL**, the function sets or queries the global proxy data.</span></span> <span data-ttu-id="f8462-462">Diese Option kann für das von **InternetOpen** zurückgegebene Handle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-462">This option can be used on the handle returned by **InternetOpen**.</span></span> <span data-ttu-id="f8462-463">Sie wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-463">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

> [!Note]  
> <span data-ttu-id="f8462-464">Es wird empfohlen, \_ \_ \_ \_ anstelle des Internet \_ options Proxys die Option Internet Option pro Verbindung zu verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="f8462-464">It is recommended that INTERNET\_OPTION\_PER\_CONNECTION\_OPTION be used instead of INTERNET\_OPTION\_PROXY.</span></span> <span data-ttu-id="f8462-465">Weitere Informationen finden Sie im [KB-Artikel 226473](https://support.microsoft.com/kb/226473).</span><span class="sxs-lookup"><span data-stu-id="f8462-465">For more information, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**Internet \_ Option \_ Proxy \_ Kennwort**</span><span class="sxs-lookup"><span data-stu-id="f8462-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**INTERNET\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-467">44</span><span class="sxs-lookup"><span data-stu-id="f8462-467">44</span></span>
</dt> <dt>



<span data-ttu-id="f8462-468">Legt einen Zeichen folgen Wert fest, der das Kennwort für den Zugriff auf den Proxy enthält, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-468">Sets or retrieves a string value that contains the password used to access the proxy.</span></span> <span data-ttu-id="f8462-469">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-469">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="f8462-470">Diese Option kann für das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)zurückgegebene Handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-470">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**\_Proxy Einstellungen für Internet Option \_ \_ \_ geändert**</span><span class="sxs-lookup"><span data-stu-id="f8462-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**INTERNET\_OPTION\_PROXY\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-472">95</span><span class="sxs-lookup"><span data-stu-id="f8462-472">95</span></span> 
</dt> <dt>



<span data-ttu-id="f8462-473">Benachrichtigt die aktuelle WinInet-Instanz, dass die Proxy Einstellungen geändert wurden und dass Sie mit den neuen Einstellungen aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f8462-473">Alerts the current WinInet instance that proxy settings have changed and that they must update with the new settings.</span></span> <span data-ttu-id="f8462-474">Legen Sie den *buffer* -Parameter von [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) auf **null** und *BufferLength* auf 0 fest, wenn Sie diese Option übergeben, um alle verfügbaren WinInet-Instanzen zu warnen.</span><span class="sxs-lookup"><span data-stu-id="f8462-474">To alert all available WinInet instances, set the *Buffer* parameter of [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to **NULL** and *BufferLength* to 0 when passing this option.</span></span> <span data-ttu-id="f8462-475">Diese Option kann für das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)zurückgegebene Handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-475">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**Internet \_ Option \_ Proxy \_ Benutzername**</span><span class="sxs-lookup"><span data-stu-id="f8462-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**INTERNET\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-477">43</span><span class="sxs-lookup"><span data-stu-id="f8462-477">43</span></span>
</dt> <dt>



<span data-ttu-id="f8462-478">Legt einen Zeichen folgen Wert fest, der den für den Zugriff auf den Proxy verwendeten Benutzernamen enthält, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-478">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span> <span data-ttu-id="f8462-479">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-479">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="f8462-480">Diese Option kann für das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) oder [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)zurückgegebene Handle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-480">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**Internet \_ Option- \_ Lese \_ Puffer \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="f8462-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**INTERNET\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-482">12</span><span class="sxs-lookup"><span data-stu-id="f8462-482">12</span></span>
</dt> <dt>



<span data-ttu-id="f8462-483">Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der die Größe des Lese Puffers enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-483">Sets or retrieves an unsigned long integer value that contains the size of the read buffer.</span></span> <span data-ttu-id="f8462-484">Diese Option kann für [**hinternethandles**](appendix-a-hinternet-handles.md) verwendet werden, die von [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)und [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (nur FTP-Sitzung) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-484">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="f8462-485">Diese Option wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-485">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**Durchsatz der Internet \_ Option- \_ Empfangs \_ Durchsatz**</span><span class="sxs-lookup"><span data-stu-id="f8462-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**INTERNET\_OPTION\_RECEIVE\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-487">57</span><span class="sxs-lookup"><span data-stu-id="f8462-487">57</span></span>
</dt> <dt>



<span data-ttu-id="f8462-488">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-488">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**\_ \_ Empfangs \_ Timeout für Internet Option**</span><span class="sxs-lookup"><span data-stu-id="f8462-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**INTERNET\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-490">6</span><span class="sxs-lookup"><span data-stu-id="f8462-490">6</span></span>
</dt> <dt>



<span data-ttu-id="f8462-491">Legt einen ganz Zahl Wert ohne Vorzeichen fest, der den Timeout Wert in Millisekunden enthält, um eine Antwort auf eine Anforderung zu empfangen, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-491">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request.</span></span> <span data-ttu-id="f8462-492">Wenn die Antwort länger dauert als dieser Timeout Wert, wird die Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f8462-492">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="f8462-493">Diese Option kann für ein beliebiges [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet werden, einschließlich eines **null** -Handles.</span><span class="sxs-lookup"><span data-stu-id="f8462-493">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="f8462-494">Sie wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-494">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="f8462-495">Diese Option ist nicht für die Darstellung eines differenzierten, unmittelbaren Timeouts vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f8462-495">This option is not intended to represent a fine-grained, immediate timeout.</span></span> <span data-ttu-id="f8462-496">Sie können davon ausgehen, dass das Timeout bis zu sechs Sekunden nach dem festgelegten Timeout Wert liegt.</span><span class="sxs-lookup"><span data-stu-id="f8462-496">You can expect the timeout to occur up to six seconds after the set timeout value.</span></span>

<span data-ttu-id="f8462-497">Bei Verwendung als Verweis auf eine FTP-Transaktion bezieht sich diese Option auf den Steuer Kanal.</span><span class="sxs-lookup"><span data-stu-id="f8462-497">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**Internet \_ Option \_ Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="f8462-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**INTERNET\_OPTION\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-499">37</span><span class="sxs-lookup"><span data-stu-id="f8462-499">37</span></span>
</dt> <dt>



<span data-ttu-id="f8462-500">Bewirkt, dass die Proxy Daten aus der Registrierung für ein Handle erneut angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-500">Causes the proxy data to be reread from the registry for a handle.</span></span> <span data-ttu-id="f8462-501">Es ist kein Puffer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8462-501">No buffer is required.</span></span> <span data-ttu-id="f8462-502">Diese Option kann für das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)zurückgegebene [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-502">This option can be used on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="f8462-503">Sie wird von [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-503">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**Internet \_ Option \_ \_ Identität entfernen**</span><span class="sxs-lookup"><span data-stu-id="f8462-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**INTERNET\_OPTION\_REMOVE\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-505">79</span><span class="sxs-lookup"><span data-stu-id="f8462-505">79</span></span>
</dt> <dt>



<span data-ttu-id="f8462-506">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-506">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**Internet \_ options- \_ anforderungsflags \_**</span><span class="sxs-lookup"><span data-stu-id="f8462-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**INTERNET\_OPTION\_REQUEST\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-508">23</span><span class="sxs-lookup"><span data-stu-id="f8462-508">23</span></span>
</dt> <dt>



<span data-ttu-id="f8462-509">Ruft den Wert einer langen ganzen Zahl ohne Vorzeichen ab, der die speziellen Statusflags enthält, die den Status des laufenden Downloads angeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-509">Retrieves an unsigned long integer value that contains the special status flags that indicate the status of the download in progress.</span></span> <span data-ttu-id="f8462-510">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-510">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="f8462-511">Die Option " [ \_ \_ Anforderungs \_ Flags" für Internet Optionen](/windows) kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="f8462-511">The [INTERNET\_OPTION\_REQUEST\_FLAGS](/windows) option can be one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f8462-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>Internet- \_ reqflag \_ Async</span><span class="sxs-lookup"><span data-stu-id="f8462-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET\_REQFLAG\_ASYNC</span></span>
</dt> <dd>

<span data-ttu-id="f8462-513">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f8462-513">0x00000002</span></span>

<span data-ttu-id="f8462-514">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-514">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>Internet- \_ reqflag- \_ Cache \_ Schreibvorgang \_ deaktiviert</span><span class="sxs-lookup"><span data-stu-id="f8462-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>INTERNET\_REQFLAG\_CACHE\_WRITE\_DISABLED</span></span>
</dt> <dd>

<span data-ttu-id="f8462-516">0x00000040</span><span class="sxs-lookup"><span data-stu-id="f8462-516">0x00000040</span></span>

<span data-ttu-id="f8462-517">Internet Anforderung kann nicht zwischengespeichert werden (z. b. eine HTTPS-Anforderung).</span><span class="sxs-lookup"><span data-stu-id="f8462-517">Internet request cannot be cached (an HTTPS request, for example).</span></span>

</dd> <dt>

<span data-ttu-id="f8462-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>Internet- \_ reqflag \_ aus dem \_ Cache</span><span class="sxs-lookup"><span data-stu-id="f8462-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET\_REQFLAG\_FROM\_CACHE</span></span>
</dt> <dd>

<span data-ttu-id="f8462-519">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f8462-519">0x00000001</span></span>

<span data-ttu-id="f8462-520">Die Antwort stammt aus dem Cache.</span><span class="sxs-lookup"><span data-stu-id="f8462-520">Response came from the cache.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>Internet- \_ reqflag- \_ Netto \_ Timeout</span><span class="sxs-lookup"><span data-stu-id="f8462-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>INTERNET\_REQFLAG\_NET\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="f8462-522">0x00000080</span><span class="sxs-lookup"><span data-stu-id="f8462-522">0x00000080</span></span>

<span data-ttu-id="f8462-523">Timeout bei der Internet Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f8462-523">Internet request timed out.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>Internet- \_ reqflag \_ keine \_ Header</span><span class="sxs-lookup"><span data-stu-id="f8462-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET\_REQFLAG\_NO\_HEADERS</span></span>
</dt> <dd>

<span data-ttu-id="f8462-525">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f8462-525">0x00000008</span></span>

<span data-ttu-id="f8462-526">Die ursprüngliche Antwort enthielt keine Header.</span><span class="sxs-lookup"><span data-stu-id="f8462-526">Original response contained no headers.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>Internet- \_ reqflag \_ passiv</span><span class="sxs-lookup"><span data-stu-id="f8462-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET\_REQFLAG\_PASSIVE</span></span>
</dt> <dd>

<span data-ttu-id="f8462-528">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8462-528">0x00000010</span></span>

<span data-ttu-id="f8462-529">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-529">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>Internet- \_ reqflag \_ über \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="f8462-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET\_REQFLAG\_VIA\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="f8462-531">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f8462-531">0x00000004</span></span>

<span data-ttu-id="f8462-532">Die Anforderung wurde über einen Proxy durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8462-532">Request was made through a proxy.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="f8462-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**Internet \_ Option- \_ Anforderungs \_ Priorität**</span><span class="sxs-lookup"><span data-stu-id="f8462-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**INTERNET\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-534">58</span><span class="sxs-lookup"><span data-stu-id="f8462-534">58</span></span>
</dt> <dt>



<span data-ttu-id="f8462-535">Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der die Priorität von Anforderungen enthält, die für eine Verbindung mit einem http-handle konkurrieren.</span><span class="sxs-lookup"><span data-stu-id="f8462-535">Sets or retrieves an unsigned long integer value that contains the priority of requests that compete for a connection on an HTTP handle.</span></span> <span data-ttu-id="f8462-536">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-536">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**Internet \_ Option \_ " \_ Urlcache- \_ Sitzung zurücksetzen"**</span><span class="sxs-lookup"><span data-stu-id="f8462-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**INTERNET\_OPTION\_RESET\_URLCACHE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-538">60</span><span class="sxs-lookup"><span data-stu-id="f8462-538">60</span></span>
</dt> <dt>



<span data-ttu-id="f8462-539">Startet eine neue Cache Sitzung für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="f8462-539">Starts a new cache session for the process.</span></span> <span data-ttu-id="f8462-540">Es ist kein Puffer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8462-540">No buffer is required.</span></span> <span data-ttu-id="f8462-541">Diese wird von [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-541">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="f8462-542">Diese Option ist nur für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f8462-542">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**Internet \_ Option \_ Sekundär \_ Cache \_ Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="f8462-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**INTERNET\_OPTION\_SECONDARY\_CACHE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-544">53</span><span class="sxs-lookup"><span data-stu-id="f8462-544">53</span></span>
</dt> <dt>



<span data-ttu-id="f8462-545">Legt einen Zeichen folgen Wert fest, der den sekundären Cache Schlüssel enthält, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-545">Sets or retrieves a string value that contains the secondary cache key.</span></span> <span data-ttu-id="f8462-546">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-546">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="f8462-547">Diese Option ist nur für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f8462-547">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**Internet \_ Option- \_ Sicherheits \_ Zertifikat**</span><span class="sxs-lookup"><span data-stu-id="f8462-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-549">35</span><span class="sxs-lookup"><span data-stu-id="f8462-549">35</span></span>
</dt> <dt>



<span data-ttu-id="f8462-550">Ruft das Zertifikat für einen SSL/PCT-Server (Secure Sockets Layer/private Communications Technology) in eine formatierte Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-550">Retrieves the certificate for an SSL/PCT (Secure Sockets Layer/Private Communications Technology) server into a formatted string.</span></span> <span data-ttu-id="f8462-551">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-551">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**\_ \_ Sicherheits \_ Zertifikat \_ Struktur "Internet Option"**</span><span class="sxs-lookup"><span data-stu-id="f8462-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-553">32</span><span class="sxs-lookup"><span data-stu-id="f8462-553">32</span></span>
</dt> <dt>



<span data-ttu-id="f8462-554">Ruft das Zertifikat für einen SSL/PCT-Server in die Internet \_ Certificate \_ Info-Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-554">Retrieves the certificate for an SSL/PCT server into the INTERNET\_CERTIFICATE\_INFO structure.</span></span> <span data-ttu-id="f8462-555">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-555">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**Internet \_ Option \_ - \_ sicherheitsflags**</span><span class="sxs-lookup"><span data-stu-id="f8462-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**INTERNET\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-557">31</span><span class="sxs-lookup"><span data-stu-id="f8462-557">31</span></span>
</dt> <dt>



<span data-ttu-id="f8462-558">Ruft einen ganzzahligen langen ganzzahligen Wert ohne Vorzeichen ab, der die sicherheitsflags für ein Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-558">Retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="f8462-559">Diese Option wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-559">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="f8462-560">Dies kann eine Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="f8462-560">It can be a combination of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f8462-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>\_Sicherheitsflag \_ 128 Bit</span><span class="sxs-lookup"><span data-stu-id="f8462-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>SECURITY\_FLAG\_128BIT</span></span>
</dt> <dd>

<span data-ttu-id="f8462-562">0x20000000</span><span class="sxs-lookup"><span data-stu-id="f8462-562">0x20000000</span></span>

<span data-ttu-id="f8462-563">Identisch mit dem bevorzugten Wert [ \_ sicherheitsflag \_ für \_ hohe Sicherheit](/windows).</span><span class="sxs-lookup"><span data-stu-id="f8462-563">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_STRONG](/windows).</span></span> <span data-ttu-id="f8462-564">Dies wird nur bei einem [**Internet QueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)-Rückruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-564">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="f8462-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>\_Sicherheitsflag \_ 40 Bit</span><span class="sxs-lookup"><span data-stu-id="f8462-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>SECURITY\_FLAG\_40BIT</span></span>
</dt> <dd>

<span data-ttu-id="f8462-566">0x10000000</span><span class="sxs-lookup"><span data-stu-id="f8462-566">0x10000000</span></span>

<span data-ttu-id="f8462-567">Identisch mit dem bevorzugten Wert [ \_ sicherheitsflag \_ \_ ](/windows)für die Stärke.</span><span class="sxs-lookup"><span data-stu-id="f8462-567">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="f8462-568">Dies wird nur bei einem [**Internet QueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)-Rückruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-568">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="f8462-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>Sicherheitsflag ( \_ \_ 56bit)</span><span class="sxs-lookup"><span data-stu-id="f8462-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>SECURITY\_FLAG\_56BIT</span></span>
</dt> <dd>

<span data-ttu-id="f8462-570">0x40000000</span><span class="sxs-lookup"><span data-stu-id="f8462-570">0x40000000</span></span>

<span data-ttu-id="f8462-571">Identisch mit dem bevorzugten Wert [ \_ sicherheitsflag- \_ Stärke \_ Mittel](/windows).</span><span class="sxs-lookup"><span data-stu-id="f8462-571">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_MEDIUM](/windows).</span></span> <span data-ttu-id="f8462-572">Dies wird nur bei einem [**Internet QueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)-Rückruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-572">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="f8462-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>\_sicherheitsflag \_ Fortezza</span><span class="sxs-lookup"><span data-stu-id="f8462-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>SECURITY\_FLAG\_FORTEZZA</span></span>
</dt> <dd>

<span data-ttu-id="f8462-574">0x08000000</span><span class="sxs-lookup"><span data-stu-id="f8462-574">0x08000000</span></span>

<span data-ttu-id="f8462-575">Gibt an, dass Fortezza verwendet wurde, um Geheimnisse, Authentifizierung und/oder Integrität für die angegebene Verbindung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f8462-575">Indicates Fortezza has been used to provide secrecy, authentication, and/or integrity for the specified connection.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>\_Sicherheitsflag \_ IETFSSL4</span><span class="sxs-lookup"><span data-stu-id="f8462-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>SECURITY\_FLAG\_IETFSSL4</span></span>
</dt> <dd>

<span data-ttu-id="f8462-577">0x00000020</span><span class="sxs-lookup"><span data-stu-id="f8462-577">0x00000020</span></span>

<span data-ttu-id="f8462-578">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-578">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>sicherheitsflag zum \_ \_ Ignorieren von \_ Zertifikat \_ CN \_ ungültig</span><span class="sxs-lookup"><span data-stu-id="f8462-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="f8462-580">0x00001000</span><span class="sxs-lookup"><span data-stu-id="f8462-580">0x00001000</span></span>

<span data-ttu-id="f8462-581">Ignoriert die [Fehlermeldung \_ Internet \_ sec \_ CERT \_ CN \_ ungültige](wininet-errors.md) Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="f8462-581">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>sicherheitsflag " \_ \_ Zertifikat mit \_ \_ \_ ungültigem Zertifikat ignorieren"</span><span class="sxs-lookup"><span data-stu-id="f8462-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="f8462-583">0x00002000</span><span class="sxs-lookup"><span data-stu-id="f8462-583">0x00002000</span></span>

<span data-ttu-id="f8462-584">Ignoriert die Fehlermeldung [ \_ Internet \_ sec \_ CERT \_ Date \_ ungültige](wininet-errors.md) Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="f8462-584">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>\_sicherheitsflag \_ " \_ Umleitung \_ an \_ http ignorieren"</span><span class="sxs-lookup"><span data-stu-id="f8462-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="f8462-586">0x00008000</span><span class="sxs-lookup"><span data-stu-id="f8462-586">0x00008000</span></span>

<span data-ttu-id="f8462-587">Ignoriert die [Fehlermeldung \_ Internet \_ https \_ an \_ http \_ bei \_ redir](wininet-errors.md) -Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="f8462-587">Ignores the [ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>\_sicherheitsflag \_ " \_ Umleitung \_ an \_ https ignorieren"</span><span class="sxs-lookup"><span data-stu-id="f8462-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS</span></span>
</dt> <dd>

<span data-ttu-id="f8462-589">0x00004000</span><span class="sxs-lookup"><span data-stu-id="f8462-589">0x00004000</span></span>

<span data-ttu-id="f8462-590">Ignoriert die [Fehlermeldung \_ Internet \_ http \_ to \_ https \_ bei \_ redir](wininet-errors.md) -Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="f8462-590">Ignores the [ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>sicherheitsflag "Sperrung \_ \_ ignorieren" \_</span><span class="sxs-lookup"><span data-stu-id="f8462-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>SECURITY\_FLAG\_IGNORE\_REVOCATION</span></span>
</dt> <dd>

<span data-ttu-id="f8462-592">0x00000080</span><span class="sxs-lookup"><span data-stu-id="f8462-592">0x00000080</span></span>

<span data-ttu-id="f8462-593">Ignoriert Probleme bei der Zertifikats Sperrung.</span><span class="sxs-lookup"><span data-stu-id="f8462-593">Ignores certificate revocation problems.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_sicherheitsflag \_ ignoriert \_ unbekannte \_ Zertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="f8462-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span>
</dt> <dd>

<span data-ttu-id="f8462-595">0x00000100</span><span class="sxs-lookup"><span data-stu-id="f8462-595">0x00000100</span></span>

<span data-ttu-id="f8462-596">Ignoriert unbekannte Probleme bei der Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="f8462-596">Ignores unknown certificate authority problems.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_sicherheitsflag \_ ignoriert \_ schwache \_ Signatur</span><span class="sxs-lookup"><span data-stu-id="f8462-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span>
</dt> <dd>

<span data-ttu-id="f8462-598">0x00010000</span><span class="sxs-lookup"><span data-stu-id="f8462-598">0x00010000</span></span>

<span data-ttu-id="f8462-599">Ignoriert schwache Probleme bei der Zertifikat Signatur.</span><span class="sxs-lookup"><span data-stu-id="f8462-599">Ignores weak certificate signature problems.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>\_sicherheitsflag \_ \_ falsche \_ Verwendung ignorieren</span><span class="sxs-lookup"><span data-stu-id="f8462-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_WRONG\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="f8462-601">0x00000200</span><span class="sxs-lookup"><span data-stu-id="f8462-601">0x00000200</span></span>

<span data-ttu-id="f8462-602">Ignoriert falsche Verwendungs Probleme.</span><span class="sxs-lookup"><span data-stu-id="f8462-602">Ignores incorrect usage problems.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>sicherheitsflag- \_ \_ normalbitheit</span><span class="sxs-lookup"><span data-stu-id="f8462-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>SECURITY\_FLAG\_NORMALBITNESS</span></span>
</dt> <dd>

<span data-ttu-id="f8462-604">0x10000000</span><span class="sxs-lookup"><span data-stu-id="f8462-604">0x10000000</span></span>

<span data-ttu-id="f8462-605">Identisch mit dem Wert [ \_ sicherheitsflag \_ \_ ](/windows)für die Stärke.</span><span class="sxs-lookup"><span data-stu-id="f8462-605">Identical to the value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="f8462-606">Dies wird nur bei einem [**Internet QueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)-Rückruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-606">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="f8462-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>\_sicherheitsflag \_ PCT</span><span class="sxs-lookup"><span data-stu-id="f8462-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>SECURITY\_FLAG\_PCT</span></span>
</dt> <dd>

<span data-ttu-id="f8462-608">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f8462-608">0x00000008</span></span>

<span data-ttu-id="f8462-609">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-609">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>\_Sicherheitsflag \_ PCT4</span><span class="sxs-lookup"><span data-stu-id="f8462-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>SECURITY\_FLAG\_PCT4</span></span>
</dt> <dd>

<span data-ttu-id="f8462-611">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8462-611">0x00000010</span></span>

<span data-ttu-id="f8462-612">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-612">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_sicherheitsflag \_ sicher</span><span class="sxs-lookup"><span data-stu-id="f8462-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span>
</dt> <dd>

<span data-ttu-id="f8462-614">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f8462-614">0x00000001</span></span>

<span data-ttu-id="f8462-615">Verwendet sichere Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="f8462-615">Uses secure transfers.</span></span> <span data-ttu-id="f8462-616">Dies wird nur bei einem [**Internet QueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)-Rückruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-616">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="f8462-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>sicherheitsflag für \_ \_ SSL</span><span class="sxs-lookup"><span data-stu-id="f8462-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>SECURITY\_FLAG\_SSL</span></span>
</dt> <dd>

<span data-ttu-id="f8462-618">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f8462-618">0x00000002</span></span>

<span data-ttu-id="f8462-619">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-619">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>\_Sicherheitsflag \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="f8462-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>SECURITY\_FLAG\_SSL3</span></span>
</dt> <dd>

<span data-ttu-id="f8462-621">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f8462-621">0x00000004</span></span>

<span data-ttu-id="f8462-622">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-622">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>sicherheitsflag- \_ \_ Stärke \_ Mittel</span><span class="sxs-lookup"><span data-stu-id="f8462-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span>
</dt> <dd>

<span data-ttu-id="f8462-624">0x40000000</span><span class="sxs-lookup"><span data-stu-id="f8462-624">0x40000000</span></span>

<span data-ttu-id="f8462-625">Verwendet die mittlere Verschlüsselung (56-Bit).</span><span class="sxs-lookup"><span data-stu-id="f8462-625">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="f8462-626">Dies wird nur bei einem [**Internet QueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)-Rückruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-626">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="f8462-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>sicherheitsflag- \_ \_ Stärke \_ stark</span><span class="sxs-lookup"><span data-stu-id="f8462-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span>
</dt> <dd>

<span data-ttu-id="f8462-628">0x20000000</span><span class="sxs-lookup"><span data-stu-id="f8462-628">0x20000000</span></span>

<span data-ttu-id="f8462-629">Verwendet die starke Verschlüsselung (128-Bit).</span><span class="sxs-lookup"><span data-stu-id="f8462-629">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="f8462-630">Dies wird nur bei einem [**Internet QueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)-Rückruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-630">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="f8462-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>sicherheitsflag- \_ \_ Stärke \_ schwach</span><span class="sxs-lookup"><span data-stu-id="f8462-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span>
</dt> <dd>

<span data-ttu-id="f8462-632">0x10000000</span><span class="sxs-lookup"><span data-stu-id="f8462-632">0x10000000</span></span>

<span data-ttu-id="f8462-633">Verwendet die schwache Verschlüsselung (40-Bit).</span><span class="sxs-lookup"><span data-stu-id="f8462-633">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="f8462-634">Dies wird nur bei einem [**Internet QueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)-Rückruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-634">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="f8462-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>\_sicherheitsflag \_ unknownbit</span><span class="sxs-lookup"><span data-stu-id="f8462-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>SECURITY\_FLAG\_UNKNOWNBIT</span></span>
</dt> <dd>

<span data-ttu-id="f8462-636">0x80000000</span><span class="sxs-lookup"><span data-stu-id="f8462-636">0x80000000</span></span>

<span data-ttu-id="f8462-637">Die in der Verschlüsselung verwendete bitgröße ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f8462-637">The bit size used in the encryption is unknown.</span></span> <span data-ttu-id="f8462-638">Dies wird nur bei einem [**Internet QueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)-Rückruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-638">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> </dl>

<span data-ttu-id="f8462-639">Beachten Sie, dass die auf diese Weise abgerufenen Daten auf eine Transaktion bezogen sind, die aufgetreten ist, deren Sicherheitsstufe nicht mehr geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f8462-639">Be aware that the data retrieved this way relates to a transaction that has occurred, whose security level can no longer be changed.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="f8462-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**Internet \_ Option- \_ Sicherheits \_ Schlüssel \_ Bitness**</span><span class="sxs-lookup"><span data-stu-id="f8462-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**INTERNET\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-641">36</span><span class="sxs-lookup"><span data-stu-id="f8462-641">36</span></span>
</dt> <dt>



<span data-ttu-id="f8462-642">Ruft den Wert einer langen ganzen Zahl ohne Vorzeichen ab, der die bitgröße des Verschlüsselungsschlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-642">Retrieves an unsigned long integer value that contains the bit size of the encryption key.</span></span> <span data-ttu-id="f8462-643">Je größer die Zahl, desto größer ist die verwendete Verschlüsselungsstärke.</span><span class="sxs-lookup"><span data-stu-id="f8462-643">The larger the number, the greater the encryption strength used.</span></span> <span data-ttu-id="f8462-644">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-644">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="f8462-645">Beachten Sie, dass die auf diese Weise abgerufenen Daten auf eine Transaktion bezogen sind, die bereits aufgetreten ist, deren Sicherheitsstufe nicht mehr geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f8462-645">Be aware that the data retrieved this way relates to a transaction that has already occurred, whose security level can no longer be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**Internet \_ Option \_ Send \_ Durchsatz**</span><span class="sxs-lookup"><span data-stu-id="f8462-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**INTERNET\_OPTION\_SEND\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-647">56</span><span class="sxs-lookup"><span data-stu-id="f8462-647">56</span></span>
</dt> <dt>



<span data-ttu-id="f8462-648">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8462-648">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**Internet \_ Option \_ Send \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="f8462-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**INTERNET\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-650">5</span><span class="sxs-lookup"><span data-stu-id="f8462-650">5</span></span>
</dt> <dt>



<span data-ttu-id="f8462-651">Legt einen langen ganzzahligen Wert ohne Vorzeichen (in Millisekunden) fest oder ruft ihn ab, der den Timeout Wert für das Senden einer Anforderung enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-651">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request.</span></span> <span data-ttu-id="f8462-652">Wenn der Sendevorgang länger dauert als dieser Timeout Wert, wird der Sendevorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="f8462-652">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="f8462-653">Diese Option kann für ein beliebiges [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet werden, einschließlich eines **null** -Handles.</span><span class="sxs-lookup"><span data-stu-id="f8462-653">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="f8462-654">Sie wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-654">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="f8462-655">Bei Verwendung als Verweis auf eine FTP-Transaktion bezieht sich diese Option auf den Steuer Kanal.</span><span class="sxs-lookup"><span data-stu-id="f8462-655">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**Internet \_ Option \_ Server \_ CERT- \_ Ketten \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="f8462-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**INTERNET\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-657">105</span><span class="sxs-lookup"><span data-stu-id="f8462-657">105</span></span>
</dt> <dt>



<span data-ttu-id="f8462-658">Ruft den Server s-Zertifikat Ketten Kontext als duplizierten [pccert- \_ Ketten \_ Kontext](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-658">Retrieves the server s certificate-chain context as a duplicated [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="f8462-659">Sie können diesen duplizierten Kontext an eine beliebige kryptografieapi-Funktion übergeben, die einen [pccert- \_ Ketten \_ Kontext](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)annimmt.</span><span class="sxs-lookup"><span data-stu-id="f8462-659">You may pass this duplicated context to any Crypto API function which takes a [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="f8462-660">Sie müssen [**certfreecertificatechain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) für den zurückgegebenen [pccert- \_ Ketten \_ Kontext](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) abrufen, wenn Sie mit dem Zertifikat Ketten Kontext abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="f8462-660">You must call [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) on the returned [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) when you are done with the certificate-chain context.</span></span>

<span data-ttu-id="f8462-661">**Version:** Erfordert Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="f8462-661">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**Internet \_ options \_ Einstellungen \_ geändert**</span><span class="sxs-lookup"><span data-stu-id="f8462-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**INTERNET\_OPTION\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-663">39</span><span class="sxs-lookup"><span data-stu-id="f8462-663">39</span></span>
</dt> <dt>



<span data-ttu-id="f8462-664">Benachrichtigt das System, dass die Registrierungs Einstellungen geändert wurden, sodass die Einstellungen beim nächsten [**Internet Connect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)-Rückruf überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-664">Notifies the system that the registry settings have been changed so that it verifies the settings on the next call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="f8462-665">Diese wird von [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-665">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**Internet \_ Option \_ Server Authentifizierung unterdrücken \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f8462-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-667">104</span><span class="sxs-lookup"><span data-stu-id="f8462-667">104</span></span>
</dt> <dt>



<span data-ttu-id="f8462-668">Legt ein HTTP-Anforderungs Objekt so fest, dass es sich nicht bei Ursprungs Servern anmelden, sondern die automatische Anmeldung bei http-Proxy Servern ausführt.</span><span class="sxs-lookup"><span data-stu-id="f8462-668">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="f8462-669">Diese Option unterscheidet sich vom anwendungsflag **Internet \_ Flag \_ No \_ auth**, das die Authentifizierung bei Proxy Servern und Ursprungs Servern verhindert.</span><span class="sxs-lookup"><span data-stu-id="f8462-669">This option differs from the Request flag **INTERNET\_FLAG\_NO\_AUTH**, which prevents authentication to both proxy servers and origin servers.</span></span>

<span data-ttu-id="f8462-670">Wenn Sie diesen Modus festlegen, wird bei der Kommunikation mit einem Ursprungsserver die Verwendung von Anmelde Informationsmaterial (entweder zuvor bereitgestellter Benutzername/Kennwort oder Client-SSL-Zertifikat) unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="f8462-670">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="f8462-671">Wenn die Anforderung jedoch über einen authentifizier enden Proxy übertragen werden muss, führt WinInet weiterhin eine automatische Authentifizierung für den HTTP-Proxy Gemäß den Intranet-Zonen Einstellungen für den Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="f8462-671">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="f8462-672">Die Standardeinstellung für die Intranetzone besteht darin, die automatische Anmeldung mithilfe der Standard Anmelde Informationen des Benutzers zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="f8462-672">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span>

<span data-ttu-id="f8462-673">Um die Unterdrückung aller identifizierenden Informationen sicherzustellen, sollte der Aufrufer die **Internet \_ Option \_ \_ Server \_** Authentifizierung unterdrücken mit dem Anforderungs Kennzeichen **Internet \_ Flag \_ No \_ Cookies** kombinieren.</span><span class="sxs-lookup"><span data-stu-id="f8462-673">To ensure suppression of all identifying information, the caller should combine **INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH** with the **INTERNET\_FLAG\_NO\_COOKIES** request flag.</span></span>

<span data-ttu-id="f8462-674">Diese Option kann nur für Anforderungs Objekte festgelegt werden, bevor Sie gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="f8462-674">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="f8462-675">Wenn versucht wird, diese Option festzulegen, nachdem die Anforderung gesendet wurde, wird der **Fehler " \_ Internet \_ fehlerhafter \_ handle \_**" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8462-675">Attempts to set this option after the request has been sent will return **ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**.</span></span>

<span data-ttu-id="f8462-676">Für diese Option ist kein Puffer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8462-676">No buffer is required for this option.</span></span> <span data-ttu-id="f8462-677">Diese wird von [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) bei Handles verwendet, die nur von [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-677">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) on handles returned by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) only.</span></span>

<span data-ttu-id="f8462-678">**Version:** Erfordert Internet Explorer 8,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-678">**Version:** Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**Internet \_ Option \_ Verhalten unterdrücken \_**</span><span class="sxs-lookup"><span data-stu-id="f8462-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**INTERNET\_OPTION\_SUPPRESS\_BEHAVIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-680">81</span><span class="sxs-lookup"><span data-stu-id="f8462-680">81</span></span>
</dt> <dt>



<span data-ttu-id="f8462-681">Eine Option für allgemeine Zwecke, die verwendet wird, um Verhalten auf Prozess weite Basis zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="f8462-681">A general purpose option that is used to suppress behaviors on a process-wide basis.</span></span> <span data-ttu-id="f8462-682">Der *lpBuffer* -Parameter der Funktion muss ein Zeiger auf ein DWORD sein, das das zu unterdrückende Verhalten enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-682">The *lpBuffer* parameter of the function must be a pointer to a DWORD containing the specific behavior to suppress.</span></span> <span data-ttu-id="f8462-683">Diese Option kann nicht mit [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-683">This option cannot be queried with [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="f8462-684">Zulässige Werte:</span><span class="sxs-lookup"><span data-stu-id="f8462-684">The permitted values are:</span></span>

<dl> <dt>

<span data-ttu-id="f8462-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>Internet \_ Unterdrückung \_ Alle zurücksetzen \_</span><span class="sxs-lookup"><span data-stu-id="f8462-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET\_SUPPRESS\_RESET\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="f8462-686">0</span><span class="sxs-lookup"><span data-stu-id="f8462-686">0</span></span>

<span data-ttu-id="f8462-687">Deaktiviert alle Unterdrückungen und aktiviert das standardmäßige und konfigurierte Verhalten erneut.</span><span class="sxs-lookup"><span data-stu-id="f8462-687">Disables all suppressions, re-enabling default and configured behavior.</span></span> <span data-ttu-id="f8462-688">Bei dieser Option handelt es sich um das Festlegen der zurück Setzung von **\_ \_ \_ Richtlinien \_** für das Internet unterdrücken von Cookies und das **\_ \_ \_ \_ Zurücksetzen des Cookies**</span><span class="sxs-lookup"><span data-stu-id="f8462-688">This option is the equivalent of setting **INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET** and **INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET** individually.</span></span>

<span data-ttu-id="f8462-689">**Version:** Erfordert Internet Explorer 6,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-689">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>\_Cookie- \_ \_ Richtlinie zum Internet Unterdrückung</span><span class="sxs-lookup"><span data-stu-id="f8462-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY</span></span> 
</dt> <dd>

<span data-ttu-id="f8462-691">1</span><span class="sxs-lookup"><span data-stu-id="f8462-691">1</span></span>

<span data-ttu-id="f8462-692">Ignoriert alle konfigurierten cookierichtlinien und ermöglicht die Festlegung von Cookies.</span><span class="sxs-lookup"><span data-stu-id="f8462-692">Ignores any configured cookie policies and allows cookies to be set.</span></span>

<span data-ttu-id="f8462-693">**Version:** Erfordert Internet Explorer 6,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-693">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>\_ \_ \_ Zurücksetzen von Cookies durch Internet Unterdrückung \_</span><span class="sxs-lookup"><span data-stu-id="f8462-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET</span></span> 
</dt> <dd>

<span data-ttu-id="f8462-695">2</span><span class="sxs-lookup"><span data-stu-id="f8462-695">2</span></span>

<span data-ttu-id="f8462-696">Deaktiviert die Unterdrückung **der \_ \_ Cookie- \_ Richtlinie im Internet** und ermöglicht so die Auswertung von Cookies gemäß der konfigurierten cookierichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f8462-696">Disables the **INTERNET\_SUPPRESS\_COOKIE\_POLICY** suppression, permitting the evaluation of cookies according to the configured cookie policy.</span></span>

<span data-ttu-id="f8462-697">**Version:** Erfordert Internet Explorer 6,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-697">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span>Cookie für Internet \_ Unterdrückung \_ \_</span><span class="sxs-lookup"><span data-stu-id="f8462-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> INTERNET\_SUPPRESS\_COOKIE\_PERSIST</span></span>
</dt> <dd>

<span data-ttu-id="f8462-699">3</span><span class="sxs-lookup"><span data-stu-id="f8462-699">3</span></span>

<span data-ttu-id="f8462-700">Unterdrückt die Persistenz von Cookies, auch wenn Sie vom Server als persistent angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="f8462-700">Suppresses the persistence of cookies, even if the server has specified them as persistent.</span></span>

<span data-ttu-id="f8462-701">**Version:** Erfordert Internet Explorer 8,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-701">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="f8462-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>\_ \_ \_ Zurücksetzen des Cookies durch Internet Unterdrückung \_</span><span class="sxs-lookup"><span data-stu-id="f8462-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="f8462-703">4</span><span class="sxs-lookup"><span data-stu-id="f8462-703">4</span></span>

<span data-ttu-id="f8462-704">Deaktiviert die Unterdrückung **des \_ \_ Cookies \_** zum Unterdrücken von Cookies, wodurch die Persistenz von Cookies wieder aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f8462-704">Disables the **INTERNET\_SUPPRESS\_COOKIE\_PERSIST** suppression, re-enabling the persistence of cookies.</span></span> <span data-ttu-id="f8462-705">Alle zuvor unterdrückten Cookies werden nicht persistent.</span><span class="sxs-lookup"><span data-stu-id="f8462-705">Any previously suppressed cookies will not become persistent.</span></span>

<span data-ttu-id="f8462-706">**Version:** Erfordert Internet Explorer 8,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f8462-706">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="f8462-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**Internet \_ options- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="f8462-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**INTERNET\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-708">34</span><span class="sxs-lookup"><span data-stu-id="f8462-708">34</span></span>
</dt> <dt>



<span data-ttu-id="f8462-709">Ruft einen Zeichen folgen Wert ab, der die vollständige URL einer heruntergeladenen Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-709">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="f8462-710">Wenn die ursprüngliche URL zusätzliche Daten enthielt, z. b. Such Zeichenfolgen oder Anker, oder wenn der-Rückruf umgeleitet wurde, unterscheidet sich die zurückgegebene URL vom ursprünglichen.</span><span class="sxs-lookup"><span data-stu-id="f8462-710">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="f8462-711">Diese Option gilt für [**hinternethandles**](appendix-a-hinternet-handles.md) , die von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**gopheropenfile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)oder [**httpopererequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-711">This option is valid on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="f8462-712">Sie wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-712">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**Internet \_ Option- \_ Benutzer- \_ Agent**</span><span class="sxs-lookup"><span data-stu-id="f8462-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**INTERNET\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-714">41</span><span class="sxs-lookup"><span data-stu-id="f8462-714">41</span></span>
</dt> <dt>



<span data-ttu-id="f8462-715">Legt die Benutzer-Agent-Zeichenfolge für Handles fest, die von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) bereitgestellt werden, und wird in nachfolgenden [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) -Funktionen verwendet, sofern Sie nicht durch einen durch [**httpadrequestheaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) oder [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)hinzugefügten Header überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f8462-715">Sets or retrieves the user agent string on handles supplied by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) and used in subsequent [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions, as long as it is not overridden by a header added by [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) or [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="f8462-716">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-716">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**Internet \_ options \_ Name**</span><span class="sxs-lookup"><span data-stu-id="f8462-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**INTERNET\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-718">28</span><span class="sxs-lookup"><span data-stu-id="f8462-718">28</span></span>
</dt> <dt>



<span data-ttu-id="f8462-719">Legt eine Zeichenfolge fest, die den Benutzernamen enthält, der einem von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zurückgegebenen Handle zugeordnet ist, oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="f8462-719">Sets or retrieves a string that contains the user name associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="f8462-720">Diese wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-720">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**Internet \_ options \_ Version**</span><span class="sxs-lookup"><span data-stu-id="f8462-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**INTERNET\_OPTION\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-722">40</span><span class="sxs-lookup"><span data-stu-id="f8462-722">40</span></span>
</dt> <dt>



<span data-ttu-id="f8462-723">Ruft eine **Internet \_ Version \_ Info** -Struktur ab, die die Versionsnummer Wininet.dll enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-723">Retrieves an **INTERNET\_VERSION\_INFO** structure that contains the version number of Wininet.dll.</span></span> <span data-ttu-id="f8462-724">Diese Option kann für ein NULL- [**HINTERNET**](appendix-a-hinternet-handles.md) Handle von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-724">This option can be used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8462-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**\_Größe des \_ Schreib \_ Puffers für Internet Optionen \_**</span><span class="sxs-lookup"><span data-stu-id="f8462-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**INTERNET\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8462-726">13</span><span class="sxs-lookup"><span data-stu-id="f8462-726">13</span></span>
</dt> <dt>



<span data-ttu-id="f8462-727">Legt einen langen ganzzahligen Wert ohne Vorzeichen fest oder ruft ihn ab, der die Größe des Schreib Puffers in Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="f8462-727">Sets or retrieves an unsigned long integer value that contains the size, in bytes, of the write buffer.</span></span> <span data-ttu-id="f8462-728">Diese Option kann für [**hinternethandles**](appendix-a-hinternet-handles.md) verwendet werden, die von [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) und [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) zurückgegeben werden (nur FTP-Sitzung).</span><span class="sxs-lookup"><span data-stu-id="f8462-728">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="f8462-729">Sie wird von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) und [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8462-729">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8462-730">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8462-730">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8462-731">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="f8462-731">WinINet does not support server implementations.</span></span> <span data-ttu-id="f8462-732">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8462-732">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f8462-733">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f8462-733">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8462-734">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8462-734">Requirements</span></span>



| <span data-ttu-id="f8462-735">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8462-735">Requirement</span></span> | <span data-ttu-id="f8462-736">Wert</span><span class="sxs-lookup"><span data-stu-id="f8462-736">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8462-737">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8462-737">Minimum supported client</span></span><br/> | <span data-ttu-id="f8462-738">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8462-738">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="f8462-739">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8462-739">Minimum supported server</span></span><br/> | <span data-ttu-id="f8462-740">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8462-740">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                   |
| <span data-ttu-id="f8462-741">Header</span><span class="sxs-lookup"><span data-stu-id="f8462-741">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8462-742"><dt>Wininet. h; </dt> <dt>Winineti. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8462-742"><dt>Wininet.h; </dt> <dt>Winineti.h</dt></span></span> </dl> |



 

