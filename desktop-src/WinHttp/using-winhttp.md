---
description: In diesem Abschnitt wird beschrieben, wie Sie die C/C++-API für Microsoft Windows HTTP-Dienste (WinHTTP) und die COM-Schnittstelle verwenden, die vom WinHttpRequest-Objekt verfügbar gemacht wird.
ms.assetid: 16178bb8-5e95-46a5-825a-880edc402445
title: Verwenden von WinHTTP
ms.topic: article
ms.date: 07/22/2020
ms.openlocfilehash: cda0a7772b88dfd9c03675c522f4b7504ea00b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484998"
---
# <a name="using-winhttp"></a><span data-ttu-id="dca1a-103">Verwenden von WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dca1a-103">Using WinHTTP</span></span>

<span data-ttu-id="dca1a-104">In diesem Abschnitt wird beschrieben, wie Sie die C/C++-API für Microsoft Windows HTTP-Dienste (WinHTTP) und die COM-Schnittstelle verwenden, die vom **WinHttpRequest** -Objekt verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="dca1a-104">This section describes how to use both the C/C++ API for Microsoft Windows HTTP Services (WinHTTP) and the COM interface exposed by the **WinHttpRequest** Object.</span></span> <span data-ttu-id="dca1a-105">Einen Vergleich dieser Schnittstellen finden Sie unter [Auswählen einer WinHTTP-Schnittstelle](choosing-a-winhttp-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="dca1a-105">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span> <span data-ttu-id="dca1a-106">Außerdem wird beschrieben, wie die in WinHTTP enthaltenen Verwaltungs Tools verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dca1a-106">It also describes how to use the administrative tools included with WinHTTP.</span></span>

## <a name="how-to-topics"></a><span data-ttu-id="dca1a-107">Themen zur Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="dca1a-107">How-To Topics</span></span>

[<span data-ttu-id="dca1a-108">Verwenden der WinHTTP-C/C++-API</span><span class="sxs-lookup"><span data-stu-id="dca1a-108">Using the WinHTTP C/C++ API</span></span>](using-the-winhttp-c-c---api.md)

-   [<span data-ttu-id="dca1a-109">Übersicht über WinHTTP-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="dca1a-109">WinHTTP Sessions Overview</span></span>](winhttp-sessions-overview.md)
-   [<span data-ttu-id="dca1a-110">HINTERNET Handles in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dca1a-110">HINTERNET Handles in WinHTTP</span></span>](hinternet-handles-in-winhttp.md)
-   [<span data-ttu-id="dca1a-111">URL (Uniform Resource Locators) in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dca1a-111">Uniform Resource Locators (URLs) in WinHTTP</span></span>](uniform-resource-locators--urls--in-winhttp.md)
-   [<span data-ttu-id="dca1a-112">Authentifizierung in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dca1a-112">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
-   [<span data-ttu-id="dca1a-113">Passport-Authentifizierung in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dca1a-113">Passport Authentication in WinHTTP</span></span>](passport-authentication-in-winhttp.md)
-   [<span data-ttu-id="dca1a-114">SSL in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dca1a-114">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
-   [<span data-ttu-id="dca1a-115">Verwenden von WinHTTP als parallele Assembly</span><span class="sxs-lookup"><span data-stu-id="dca1a-115">Using WinHTTP as a Side-by-side Assembly</span></span>](using-winhttp-as-a-side-by-side-assembly.md)
-   [<span data-ttu-id="dca1a-116">Behandlung von Cookies in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dca1a-116">Cookie Handling in WinHTTP</span></span>](cookie-handling-in-winhttp.md)
-   [<span data-ttu-id="dca1a-117">Fehlerbehandlung in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dca1a-117">Error Handling in WinHTTP</span></span>](error-handling-in-winhttp.md)
-   [<span data-ttu-id="dca1a-118">WinHTTP-AutoProxy-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="dca1a-118">WinHTTP AutoProxy Support</span></span>](winhttp-autoproxy-support.md)

[<span data-ttu-id="dca1a-119">Verwenden des WinHttpRequest-com-Objekts</span><span class="sxs-lookup"><span data-stu-id="dca1a-119">Using the WinHttpRequest COM Object</span></span>](using-the-winhttprequest-com-object.md)

-   [<span data-ttu-id="dca1a-120">Abrufen von Daten mithilfe eines Skripts</span><span class="sxs-lookup"><span data-stu-id="dca1a-120">Retrieving Data Using Script</span></span>](retrieving-data-using-script.md)
-   [<span data-ttu-id="dca1a-121">Authentifizierung mithilfe eines Skripts</span><span class="sxs-lookup"><span data-stu-id="dca1a-121">Authentication Using Script</span></span>](authentication-using-script.md)

[<span data-ttu-id="dca1a-122">Verwenden von WinHTTP-Tools</span><span class="sxs-lookup"><span data-stu-id="dca1a-122">Using WinHTTP Tools</span></span>](using-winhttp-tools.md)

-   [<span data-ttu-id="dca1a-123">WinHttpCfg.exe, ein Zertifikat Konfigurations Tool</span><span class="sxs-lookup"><span data-stu-id="dca1a-123">WinHttpCfg.exe, a Certificate Configuration Tool</span></span>](winhttpcertcfg-exe--a-certificate-configuration-tool.md)
-   [<span data-ttu-id="dca1a-124">ProxyCfg.exe, ein Proxy Konfigurations Tool</span><span class="sxs-lookup"><span data-stu-id="dca1a-124">ProxyCfg.exe, a Proxy Configuration Tool</span></span>](proxycfg-exe--a-proxy-configuration-tool.md)
-   [<span data-ttu-id="dca1a-125">Winhttptracecfg, ein Konfigurations Tool für die Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="dca1a-125">WinHttpTraceCfg, a Trace Configuration Tool</span></span>](winhttptracecfg-exe--a-trace-configuration-tool.md)

 

 



