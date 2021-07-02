---
description: In diesem Thema werden die Von WinHTTP verwendeten Strukturen identifiziert.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: WinHTTP-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ecf91702a2f49e2c0a754fcc69d9d34febf229
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174985"
---
# <a name="winhttp-structures"></a><span data-ttu-id="c11dd-103">WinHTTP-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c11dd-103">WinHTTP structures</span></span>

<span data-ttu-id="c11dd-104">WinHTTP verwendet die folgenden Strukturen:</span><span class="sxs-lookup"><span data-stu-id="c11dd-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="c11dd-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="c11dd-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="c11dd-106">Enthält die globale HTTP-Version.</span><span class="sxs-lookup"><span data-stu-id="c11dd-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="c11dd-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="c11dd-108">Enthält die Bestandteile einer URL.</span><span class="sxs-lookup"><span data-stu-id="c11dd-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="c11dd-109">Diese Struktur wird mit den [**Funktionen WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) und [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c11dd-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="c11dd-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="c11dd-111">Enthält das Ergebnis eines Aufrufs einer asynchronen Funktion.</span><span class="sxs-lookup"><span data-stu-id="c11dd-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="c11dd-112">Diese Struktur wird mit dem [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c11dd-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="c11dd-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="c11dd-114">Wird verwendet, um der [**WinHttpGetProxyForURL-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) anzugeben, ob die URL der PAC-Datei (Proxy Auto-Configuration) angegeben oder die URL mit DHCP- oder DNS-Abfragen an das Netzwerk automatisch gefunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="c11dd-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="c11dd-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="c11dd-116">Enthält zertifikatsinformationen, die vom Server zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c11dd-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="c11dd-117">Diese Struktur wird von der [**WinHttpQueryOption-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c11dd-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-118">**WINHTTP_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="c11dd-118">**WINHTTP_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

<span data-ttu-id="c11dd-119">Stellt eine Verbindungsgruppe dar.</span><span class="sxs-lookup"><span data-stu-id="c11dd-119">Represents a connection group.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-120">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="c11dd-120">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="c11dd-121">Enthält die Quell- und Ziel-IP-Adresse der Anforderung, die die Antwort generiert hat.</span><span class="sxs-lookup"><span data-stu-id="c11dd-121">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-122">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="c11dd-122">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="c11dd-123">Enthält Informationen zu Benutzer-Anmeldeinformationen, die für die Server- und Proxyauthentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c11dd-123">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="c11dd-124">Diese Struktur ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="c11dd-124">This structure has been deprecated.</span></span> <span data-ttu-id="c11dd-125">Stattdessen wird die Verwendung [**der**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) WINHTTP_CREDS_EX empfohlen.</span><span class="sxs-lookup"><span data-stu-id="c11dd-125">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-126">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="c11dd-126">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="c11dd-127">Enthält Informationen zu Benutzer-Anmeldeinformationen, die für die Server- und Proxyauthentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c11dd-127">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="c11dd-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="c11dd-129">Enthält die Internet Explorer Proxykonfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="c11dd-129">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-130">**WINHTTP_EXTENDED_HEADER**</span><span class="sxs-lookup"><span data-stu-id="c11dd-130">**WINHTTP_EXTENDED_HEADER**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header)
</dt> <dd>

<span data-ttu-id="c11dd-131">Stellt einen HTTP-Anforderungsheader als Name-Wert-Zeichenfolgenpaar dar.</span><span class="sxs-lookup"><span data-stu-id="c11dd-131">Represents an HTTP request header as a name/value string pair.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-132">**WINHTTP_HEADER_NAME**</span><span class="sxs-lookup"><span data-stu-id="c11dd-132">**WINHTTP_HEADER_NAME**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name)
</dt> <dd>

<span data-ttu-id="c11dd-133">Stellt einen HTTP-Anforderungsheadernamen dar.</span><span class="sxs-lookup"><span data-stu-id="c11dd-133">Represents an HTTP request header name.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-134">**WINHTTP_HOST_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="c11dd-134">**WINHTTP_HOST_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

<span data-ttu-id="c11dd-135">Stellt eine Auflistung von Verbindungsgruppen dar.</span><span class="sxs-lookup"><span data-stu-id="c11dd-135">Represents a collection of connection groups.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-136">**WINHTTP_MATCH_CONNECTION_GUID**</span><span class="sxs-lookup"><span data-stu-id="c11dd-136">**WINHTTP_MATCH_CONNECTION_GUID**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

<span data-ttu-id="c11dd-137">Stellt die GUID einer Verbindung für den Verbindungsabgleich dar.</span><span class="sxs-lookup"><span data-stu-id="c11dd-137">Represents the GUID of a connection, for purposes of connection-matching.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-138">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="c11dd-138">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="c11dd-139">Enthält die Sitzungs- oder Standardproxykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c11dd-139">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-140">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="c11dd-140">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="c11dd-141">Eine Auflistung von Proxyergebniseinträgen, die von [**WinHttpGetProxyResult bereitgestellt werden.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="c11dd-141">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-142">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="c11dd-142">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="c11dd-143">Ein Ergebniseintrag aus einem Aufruf von [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="c11dd-143">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-144">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span><span class="sxs-lookup"><span data-stu-id="c11dd-144">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

<span data-ttu-id="c11dd-145">Stellt eine Beschreibung des aktuellen Zustands der WinHttp-Verbindungen dar.</span><span class="sxs-lookup"><span data-stu-id="c11dd-145">Represents a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-146">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="c11dd-146">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="c11dd-147">Enthält Statistiken für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c11dd-147">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-148">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="c11dd-148">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="c11dd-149">Enthält Zeitsteuerungsinformationen für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c11dd-149">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-150">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="c11dd-150">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="c11dd-151">Enthält SChannel-Verbindungs- und Verschlüsselungsinformationen für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c11dd-151">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-152">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="c11dd-152">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="c11dd-153">Ergebnisstatus eines WebSocket-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c11dd-153">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="c11dd-154">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="c11dd-154">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="c11dd-155">Status eines WebSocket-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c11dd-155">Status of a WebSocket operation.</span></span>

</dd> </dl>
