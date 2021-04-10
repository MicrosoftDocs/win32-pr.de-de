---
description: Internet Schemas, die von WinHTTP unterstützt werden.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867792"
---
# <a name="internet_scheme"></a><span data-ttu-id="51612-103">Internet \_ Schema</span><span class="sxs-lookup"><span data-stu-id="51612-103">INTERNET\_SCHEME</span></span>

<span data-ttu-id="51612-104">Internet Schemas, die von WinHTTP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="51612-104">Internet schemes supported by WinHTTP.</span></span>

<dl> <dt>

<span data-ttu-id="51612-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**Internet- \_ Schema \_ http**</span><span class="sxs-lookup"><span data-stu-id="51612-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**INTERNET\_SCHEME\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51612-106">1</span><span class="sxs-lookup"><span data-stu-id="51612-106">1</span></span>
</dt> <dt>



<span data-ttu-id="51612-107">Ein HTTP-Internet Schema.</span><span class="sxs-lookup"><span data-stu-id="51612-107">An HTTP internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51612-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**Internet \_ Schema \_ https**</span><span class="sxs-lookup"><span data-stu-id="51612-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**INTERNET\_SCHEME\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51612-109">2</span><span class="sxs-lookup"><span data-stu-id="51612-109">2</span></span>
</dt> <dt>



<span data-ttu-id="51612-110">Ein HTTPS-Internet Schema (SSL).</span><span class="sxs-lookup"><span data-stu-id="51612-110">An HTTPS (SSL) internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51612-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**Internet- \_ Schema- \_ FTP**</span><span class="sxs-lookup"><span data-stu-id="51612-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**INTERNET\_SCHEME\_FTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51612-112">3</span><span class="sxs-lookup"><span data-stu-id="51612-112">3</span></span>
</dt> <dt>



<span data-ttu-id="51612-113">Ein FTP-Internet Schema.</span><span class="sxs-lookup"><span data-stu-id="51612-113">An FTP internet scheme.</span></span> <span data-ttu-id="51612-114">Dieses Schema wird nur für die Verwendung in [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) und [**winhttpgetproxyforurlex**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51612-114">This scheme is only supported for use in [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) and [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51612-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**Internet- \_ Schema- \_ SOCKS**</span><span class="sxs-lookup"><span data-stu-id="51612-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**INTERNET\_SCHEME\_SOCKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51612-116">4</span><span class="sxs-lookup"><span data-stu-id="51612-116">4</span></span>
</dt> <dt>



<span data-ttu-id="51612-117">Ein SOCKS-Internet-Schema.</span><span class="sxs-lookup"><span data-stu-id="51612-117">A SOCKS internet scheme.</span></span> <span data-ttu-id="51612-118">Dieses Schema wird nur für die Verwendung im [**\_ \_ Ergebnis \_ Eintrag des WinHTTP-Proxys**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51612-118">This scheme is only supported for use in [**WINHTTP\_PROXY\_RESULT\_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51612-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51612-119">Requirements</span></span>



| <span data-ttu-id="51612-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51612-120">Requirement</span></span> | <span data-ttu-id="51612-121">Wert</span><span class="sxs-lookup"><span data-stu-id="51612-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="51612-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51612-122">Minimum supported client</span></span><br/> | <span data-ttu-id="51612-123">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51612-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="51612-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51612-124">Minimum supported server</span></span><br/> | <span data-ttu-id="51612-125">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51612-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="51612-126">Header</span><span class="sxs-lookup"><span data-stu-id="51612-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="51612-127"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="51612-127"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51612-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51612-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51612-129">**Eintrag für WinHTTP- \_ Proxy \_ Ergebnis \_**</span><span class="sxs-lookup"><span data-stu-id="51612-129">**WINHTTP\_PROXY\_RESULT\_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




