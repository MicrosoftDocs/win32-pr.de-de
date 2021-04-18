---
title: IDN-Unterstützung in WinInet
description: Ab Windows Server 2008 und Windows Vista wird der Hostteil der Unicode-URL in den internationalisierten Domänen Namen (IDN) konvertiert.
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390880"
---
# <a name="idn-support-in-wininet"></a><span data-ttu-id="ec080-103">IDN-Unterstützung in WinInet</span><span class="sxs-lookup"><span data-stu-id="ec080-103">IDN Support in WinINet</span></span>

<span data-ttu-id="ec080-104">Ab Windows Server 2008 und Windows Vista wird der Hostteil der Unicode-URL in den internationalisierten Domänen Namen (IDN) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ec080-104">Starting in Windows Server 2008 and Windows Vista, the host portion of the Unicode URL is converted to the Internationalized Domain Name (IDN).</span></span> <span data-ttu-id="ec080-105">Separate Teile der Unicode-URL-Codierung können auch von Konfigurationen geändert werden, die von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ec080-105">Separate portions of the Unicode URL encoding can also be modified by configurations set by the application.</span></span> <span data-ttu-id="ec080-106">Die ANSI-Versionen der WinInet-API senden die URL weiterhin über das Netzwerk, wie Sie von der Anwendung eingegeben wurde, aber die WinInet-Unicode-Versionen der API entsprechen jetzt dem IDN-Standard (RFC3490) für URL-Codierungen.</span><span class="sxs-lookup"><span data-stu-id="ec080-106">The ANSI versions of the WinINet API continue to send the URL over the wire as entered by the application, however the WinINet Unicode versions of the API now conform to the IDN standard (RFC3490) for URL encodings.</span></span>

<span data-ttu-id="ec080-107">Wenn eine URL als Unicode-Parameter eingegeben wird, wird der Hostteil standardmäßig in das IDN-Format konvertiert, sowohl für Proxy-als auch für direkte Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="ec080-107">By default, when a URL is entered as a Unicode parameter, the host portion, for both proxy and direct connections, is converted to IDN format.</span></span> <span data-ttu-id="ec080-108">Die Anwendung hat die Möglichkeit, die IDN-Host Formatierung zu deaktivieren, indem Sie die Option " **Internet \_ Option \_ IDN** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="ec080-108">The application has the option to disable IDN host formatting by setting the **INTERNET\_OPTION\_IDN** option.</span></span> <span data-ttu-id="ec080-109">Die IDN-Host Konvertierung kann nur für die direkt-oder Proxy Verbindungen mithilfe der **Internet-Flag IDN \_ \_ \_ Direct** oder **Internet \_ Flag \_ IDN- \_ proxyflags** mit **Internet- \_ Option \_ IDN** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ec080-109">IDN host conversion can be enabled on only the direct or proxy connections by using the **INTERNET\_FLAG\_IDN\_DIRECT** or **INTERNET\_FLAG\_IDN\_PROXY** flags with **INTERNET\_OPTION\_IDN**.</span></span>

<span data-ttu-id="ec080-110">Im folgenden Codebeispiel wird veranschaulicht, wie die IDN-Host Konvertierung sowohl für den Proxy als auch für die direkte Verbindung deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ec080-110">The following code example shows how to disable IDN host conversion for both the proxy and direct connections.</span></span>

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

<span data-ttu-id="ec080-111">Wenn die IDN-Host Formatierung deaktiviert ist, kann die Anwendung die gewünschte Codepage mithilfe der **Internet \_ Option \_ Codepage** angeben.</span><span class="sxs-lookup"><span data-stu-id="ec080-111">If IDN host formatting is disabled, the application has the option to specify the desired codepage using **INTERNET\_OPTION\_CODEPAGE**.</span></span>

<span data-ttu-id="ec080-112">Im folgenden Codebeispiel wird gezeigt, wie die japanische Codepage angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec080-112">The following code example shows how to specify the Japanese code page.</span></span>

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

<span data-ttu-id="ec080-113">Der Pfadteil der URL ist standardmäßig UTF8-codiert, und die restlichen Segmente der URL, die Abfrage oder das Fragment, werden in die standardmäßige System Codepage (CP \_ ACP) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ec080-113">The path portion of the URL is UTF8 encoded by default, and the remaining segments of the URL, the query or fragment, are converted to the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="ec080-114">Im folgenden Beispiel wird gezeigt, wie die Codepages Koreanisch für den Pfadteil der URL angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec080-114">The following example shows how to specify the Korean language code page for the path portion of the URL.</span></span>

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

<span data-ttu-id="ec080-115">In der folgenden Tabelle werden die Optionen für die Unterstützung von IDN definiert.</span><span class="sxs-lookup"><span data-stu-id="ec080-115">The following table defines the options that support IDN.</span></span> <span data-ttu-id="ec080-116">Weitere Informationen finden Sie im Thema [Optionsflags](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="ec080-116">For more information, see the [Option Flags](option-flags.md) topic.</span></span>



| <span data-ttu-id="ec080-117">Option</span><span class="sxs-lookup"><span data-stu-id="ec080-117">Option</span></span>                            | <span data-ttu-id="ec080-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec080-118">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec080-119">Codepage für Internet- \_ Optionen \_</span><span class="sxs-lookup"><span data-stu-id="ec080-119">INTERNET\_OPTION\_CODEPAGE</span></span>        | <span data-ttu-id="ec080-120">Diese Option wird für die Anforderung oder das Verbindungs Handle festgelegt, um ein Code Page-Codierungsschema für den Hostteil der URL anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ec080-120">This option is set on the request, or connection handle, to specify a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="ec080-121">Diese Option wird ignoriert, wenn IDN aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ec080-121">This option is ignored if IDN is enabled.</span></span>                                                      |
| <span data-ttu-id="ec080-122">Internet \_ Option \_ Codepage- \_ Pfad</span><span class="sxs-lookup"><span data-stu-id="ec080-122">INTERNET\_OPTION\_CODEPAGE\_PATH</span></span>  | <span data-ttu-id="ec080-123">Diese Option wird für die Anforderung festgelegt, oder das Verbindungs Handle aktiviert das angegebene Codierungsschema für den Pfadteil der URL.</span><span class="sxs-lookup"><span data-stu-id="ec080-123">This option is set on the request, or connection handle enables the specified encoding scheme for the path portion of the URL.</span></span> <span data-ttu-id="ec080-124">Standardmäßig ist der Pfadteil der URL UTF8-codiert.</span><span class="sxs-lookup"><span data-stu-id="ec080-124">By default, the path portion of the URL is UTF8 encoded.</span></span>                                         |
| <span data-ttu-id="ec080-125">Internet \_ Option \_ Codepage \_ extra</span><span class="sxs-lookup"><span data-stu-id="ec080-125">INTERNET\_OPTION\_CODEPAGE\_EXTRA</span></span> | <span data-ttu-id="ec080-126">Das Festlegen dieser Option für die Anforderung oder das Verbindungs Handle ermöglicht das angegebene Codierungsschema für den zusätzlichen Teil der URL.</span><span class="sxs-lookup"><span data-stu-id="ec080-126">Setting this option on the request, or connection handle enables the specified encoding scheme for the extra portion of the URL.</span></span> <span data-ttu-id="ec080-127">Standardmäßig wird der zusätzliche Teil der URL in der standardmäßigen System Codepage (CP \_ ACP) codiert.</span><span class="sxs-lookup"><span data-stu-id="ec080-127">By default, the extra portion of the URL is encoded in the default system code page (CP\_ACP).</span></span> |
| <span data-ttu-id="ec080-128">Internet \_ Option \_ IDN</span><span class="sxs-lookup"><span data-stu-id="ec080-128">INTERNET\_OPTION\_IDN</span></span>             | <span data-ttu-id="ec080-129">Diese Option kann für die Anforderung oder das Verbindungs Handle zum Aktivieren oder Deaktivieren der IDN-Host Konvertierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec080-129">This option can be used on the request, or connection handle to enable or disable IDN host conversion.</span></span> <span data-ttu-id="ec080-130">Wenn IDN deaktiviert ist, verwendet Wininet die standardmäßige System Codepage, um den Host-oder Autoritäts Teil der URL zu codieren.</span><span class="sxs-lookup"><span data-stu-id="ec080-130">When IDN is disabled, WinINet uses the default system codepage to encode the host or authority portion of the URL.</span></span>       |



 

> [!Note]  
> <span data-ttu-id="ec080-131">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="ec080-131">WinINet does not support server implementations.</span></span> <span data-ttu-id="ec080-132">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec080-132">In addition, it should not be used from a service.</span></span> <span data-ttu-id="ec080-133">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="ec080-133">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 