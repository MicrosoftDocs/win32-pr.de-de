---
description: In diesem Thema werden die Strukturen beschrieben, die von WinHTTP verwendet werden.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: WinHTTP-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f09615e721b9d34243bd20074e83837e48a6803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214610"
---
# <a name="winhttp-structures"></a><span data-ttu-id="06830-103">WinHTTP-Strukturen</span><span class="sxs-lookup"><span data-stu-id="06830-103">WinHTTP structures</span></span>

<span data-ttu-id="06830-104">WinHTTP verwendet die folgenden Strukturen:</span><span class="sxs-lookup"><span data-stu-id="06830-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="06830-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="06830-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="06830-106">Enthält die globale HTTP-Version.</span><span class="sxs-lookup"><span data-stu-id="06830-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="06830-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="06830-108">Enthält die Bestandteile einer URL.</span><span class="sxs-lookup"><span data-stu-id="06830-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="06830-109">Diese Struktur wird mit den Funktionen [**winhttpknackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) und [**winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) verwendet.</span><span class="sxs-lookup"><span data-stu-id="06830-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="06830-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="06830-111">Enthält das Ergebnis eines Aufrufes einer asynchronen Funktion.</span><span class="sxs-lookup"><span data-stu-id="06830-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="06830-112">Diese Struktur wird mit dem [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) Prototyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="06830-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="06830-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="06830-114">Wird verwendet, um der [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Funktion anzugeben, ob die URL der PAC-Datei (Proxy Auto-Configuration) angegeben werden soll oder ob die URL mit DHCP-oder DNS-Abfragen automatisch im Netzwerk gefunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="06830-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="06830-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="06830-116">Enthält Zertifikat Informationen, die vom Server zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06830-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="06830-117">Diese Struktur wird von der [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="06830-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-118">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="06830-118">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="06830-119">Enthält die Quell-und Ziel-IP-Adresse der Anforderung, die die Antwort generiert hat.</span><span class="sxs-lookup"><span data-stu-id="06830-119">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-120">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="06830-120">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="06830-121">Enthält Benutzer Anmelde Informationen, die für die Server-und Proxy Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06830-121">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="06830-122">Diese Struktur ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="06830-122">This structure has been deprecated.</span></span> <span data-ttu-id="06830-123">Stattdessen wird die Verwendung der [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) Struktur empfohlen.</span><span class="sxs-lookup"><span data-stu-id="06830-123">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-124">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="06830-124">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="06830-125">Enthält Benutzer Anmelde Informationen, die für die Server-und Proxy Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06830-125">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-126">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="06830-126">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="06830-127">Enthält die Internet Explorer-Proxy Konfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="06830-127">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-128">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="06830-128">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="06830-129">Enthält die Sitzungs-oder Standard Proxykonfiguration.</span><span class="sxs-lookup"><span data-stu-id="06830-129">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-130">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="06830-130">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="06830-131">Eine Auflistung von Proxy Ergebnis Einträgen, die von [**winhttpgetproxyresult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="06830-131">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="06830-132">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="06830-132">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="06830-133">Ein Ergebniseintrag aus einem Aufrufen von [**winhttpgetproxyresult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="06830-133">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="06830-134">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="06830-134">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="06830-135">Enthält Statistiken für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="06830-135">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-136">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="06830-136">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="06830-137">Enthält Zeit Steuerungsinformationen für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="06830-137">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-138">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="06830-138">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="06830-139">Enthält SChannel-Verbindung und Chiffre Informationen für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="06830-139">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-140">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="06830-140">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="06830-141">Ergebnis Status eines WebSocket-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="06830-141">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="06830-142">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="06830-142">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="06830-143">Status eines WebSocket-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="06830-143">Status of a WebSocket operation.</span></span>

</dd> </dl>
