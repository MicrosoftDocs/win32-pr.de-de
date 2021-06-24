---
description: In diesem Thema werden die Von WinHTTP verwendeten Strukturen identifiziert.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: WinHTTP-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d6f0cdbb467e916b1a6ac54b90491cbee9efdb
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587976"
---
# <a name="winhttp-structures"></a><span data-ttu-id="96074-103">WinHTTP-Strukturen</span><span class="sxs-lookup"><span data-stu-id="96074-103">WinHTTP structures</span></span>

<span data-ttu-id="96074-104">WinHTTP verwendet die folgenden Strukturen:</span><span class="sxs-lookup"><span data-stu-id="96074-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="96074-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="96074-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="96074-106">Enthält die globale HTTP-Version.</span><span class="sxs-lookup"><span data-stu-id="96074-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="96074-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="96074-108">Enthält die Bestandteile einer URL.</span><span class="sxs-lookup"><span data-stu-id="96074-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="96074-109">Diese Struktur wird mit den [**Funktionen WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) und [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) verwendet.</span><span class="sxs-lookup"><span data-stu-id="96074-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="96074-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="96074-111">Enthält das Ergebnis eines Aufrufs einer asynchronen Funktion.</span><span class="sxs-lookup"><span data-stu-id="96074-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="96074-112">Diese Struktur wird mit dem [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) Prototyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="96074-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="96074-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="96074-114">Wird verwendet, um der [**WinHttpGetProxyForURL-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) anzugeben, ob die URL der PAC-Datei (Proxy Auto-Configuration) angegeben oder die URL mit DHCP- oder DNS-Abfragen automatisch im Netzwerk gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="96074-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="96074-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="96074-116">Enthält vom Server zurückgegebene Zertifikatinformationen.</span><span class="sxs-lookup"><span data-stu-id="96074-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="96074-117">Diese Struktur wird von der [**WinHttpQueryOption-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) verwendet.</span><span class="sxs-lookup"><span data-stu-id="96074-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-118">**WINHTTP_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="96074-118">**WINHTTP_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

<span data-ttu-id="96074-119">Stellt eine Verbindungsgruppe dar.</span><span class="sxs-lookup"><span data-stu-id="96074-119">Represents a connection group.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-120">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="96074-120">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="96074-121">Enthält die Quell- und Ziel-IP-Adresse der Anforderung, die die Antwort generiert hat.</span><span class="sxs-lookup"><span data-stu-id="96074-121">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-122">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="96074-122">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="96074-123">Enthält Informationen zu Benutzeranmeldeinformationen, die für die Server- und Proxyauthentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96074-123">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="96074-124">Diese Struktur ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="96074-124">This structure has been deprecated.</span></span> <span data-ttu-id="96074-125">Stattdessen wird die Verwendung der [**WINHTTP_CREDS_EX-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) empfohlen.</span><span class="sxs-lookup"><span data-stu-id="96074-125">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-126">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="96074-126">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="96074-127">Enthält Informationen zu Benutzeranmeldeinformationen, die für die Server- und Proxyauthentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96074-127">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="96074-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="96074-129">Enthält die Internet Explorer Proxykonfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="96074-129">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-130">**WINHTTP_HOST_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="96074-130">**WINHTTP_HOST_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

<span data-ttu-id="96074-131">Stellt eine Auflistung von Verbindungsgruppen dar.</span><span class="sxs-lookup"><span data-stu-id="96074-131">Represents a collection of connection groups.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-132">**WINHTTP_MATCH_CONNECTION_GUID**</span><span class="sxs-lookup"><span data-stu-id="96074-132">**WINHTTP_MATCH_CONNECTION_GUID**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

<span data-ttu-id="96074-133">Stellt die GUID einer Verbindung zum Zweck des Verbindungsabgleichs dar.</span><span class="sxs-lookup"><span data-stu-id="96074-133">Represents the GUID of a connection, for purposes of connection-matching.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-134">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="96074-134">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="96074-135">Enthält die Sitzungs- oder Standardproxykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="96074-135">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-136">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="96074-136">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="96074-137">Eine Auflistung von Proxyergebniseinträgen, die von [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="96074-137">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="96074-138">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="96074-138">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="96074-139">Ein Ergebniseintrag aus einem Aufruf von [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="96074-139">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="96074-140">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span><span class="sxs-lookup"><span data-stu-id="96074-140">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

<span data-ttu-id="96074-141">Stellt eine Beschreibung des aktuellen Status der WinHttp-Verbindungen dar.</span><span class="sxs-lookup"><span data-stu-id="96074-141">Represents a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-142">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="96074-142">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="96074-143">Enthält Statistiken für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="96074-143">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-144">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="96074-144">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="96074-145">Enthält Zeitsteuerungsinformationen für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="96074-145">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-146">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="96074-146">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="96074-147">Enthält SChannel-Verbindungs- und Verschlüsselungsinformationen für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="96074-147">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-148">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="96074-148">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="96074-149">Ergebnisstatus eines WebSocket-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="96074-149">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="96074-150">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="96074-150">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="96074-151">Status eines WebSocket-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="96074-151">Status of a WebSocket operation.</span></span>

</dd> </dl>
