---
title: url
description: Die wwsapi-URL-API-Elemente stellen Mechanismen bereit, mit denen Sie URLs in Komponenten Teile aufteilen und aus Escapezeichen versehen und Komponenten Teile wieder in eine URL umwandeln können.
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- URL-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8511bf755f80f124071f658a65249243dc2f2af
ms.sourcegitcommit: 6f8c895f4d43c4463f6f33fa8014c5de413ece1f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2020
ms.locfileid: "106339050"
---
# <a name="url"></a><span data-ttu-id="6918d-106">url</span><span class="sxs-lookup"><span data-stu-id="6918d-106">Url</span></span>

<span data-ttu-id="6918d-107">Die wwsapi-URL-API-Elemente stellen Mechanismen bereit, mit denen Sie URLs in Komponenten Teile aufteilen und aus Escapezeichen versehen und Komponenten Teile wieder in eine URL umwandeln können.</span><span class="sxs-lookup"><span data-stu-id="6918d-107">The WWSAPI URL API elements provide mechanisms to split and unescape URLs into component parts, and to escape and combine component parts back into a URL.</span></span>

-   <span data-ttu-id="6918d-108">Verwenden Sie die [**wsdecodeurl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) -Funktion, um URLs zu teilen und in Komponenten Teile zu entweichen.</span><span class="sxs-lookup"><span data-stu-id="6918d-108">To split and unescape URLs into component parts, use the [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) function.</span></span>
-   <span data-ttu-id="6918d-109">Verwenden Sie zum Escapezeichen und zum Kombinieren von Komponenten teilen in einer URL die [**wsencodeurl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6918d-109">To escape and combine component parts back into a URL, use the [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) function.</span></span>
-   <span data-ttu-id="6918d-110">Um relative URLs mit einer absoluten Basis-URL zu kombinieren, die eine absolute URL bildet, verwenden Sie die [**wscombineurl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6918d-110">To combine relative URLs with an absolute base URL forming an absolute URL, use the [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) function.</span></span>

<span data-ttu-id="6918d-111">Die folgenden Enumerationen sind Teil der URL:</span><span class="sxs-lookup"><span data-stu-id="6918d-111">The following enumerations are part of the URL:</span></span>

-   [<span data-ttu-id="6918d-112">**WS- \_ URL- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="6918d-112">**WS\_URL\_FLAGS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="6918d-113">**WS- \_ URL- \_ \_ schematentyp**</span><span class="sxs-lookup"><span data-stu-id="6918d-113">**WS\_URL\_SCHEME\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

<span data-ttu-id="6918d-114">Die folgenden Funktionen sind Teil der URL:</span><span class="sxs-lookup"><span data-stu-id="6918d-114">The following functions are part of the URL:</span></span>

-   [<span data-ttu-id="6918d-115">**Wscombineurl**</span><span class="sxs-lookup"><span data-stu-id="6918d-115">**WsCombineUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [<span data-ttu-id="6918d-116">**Wsdecodeurl**</span><span class="sxs-lookup"><span data-stu-id="6918d-116">**WsDecodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [<span data-ttu-id="6918d-117">**Wsencodeurl**</span><span class="sxs-lookup"><span data-stu-id="6918d-117">**WsEncodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

<span data-ttu-id="6918d-118">Die folgenden Strukturen sind Teil der URL:</span><span class="sxs-lookup"><span data-stu-id="6918d-118">The following structures are part of the URL:</span></span>

-   [<span data-ttu-id="6918d-119">**WS- \_ https- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="6918d-119">**WS\_HTTPS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [<span data-ttu-id="6918d-120">**WS- \_ http- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="6918d-120">**WS\_HTTP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [<span data-ttu-id="6918d-121">**WS \_ netpipe- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="6918d-121">**WS\_NETPIPE\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="6918d-122">**WS \_ NetTcp- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="6918d-122">**WS\_NETTCP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [<span data-ttu-id="6918d-123">**WS \_ soapudp- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="6918d-123">**WS\_SOAPUDP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [<span data-ttu-id="6918d-124">**WS- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="6918d-124">**WS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




