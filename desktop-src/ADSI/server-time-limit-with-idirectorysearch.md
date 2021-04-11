---
title: Server Zeit Limit bei idirector ysearch
description: Um zu vermeiden, dass die gesamte CPU-Zeit verwendet und andere Vorgänge nicht ausgeführt werden, geben Sie das Such Zeitlimit auf einen kleinen Wert an, und führen Sie die Anwendung dann später erneut aus, wenn der Bericht nicht generiert werden kann.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Server Zeit Limit mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, Server Zeit Limit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947328"
---
# <a name="server-time-limit-with-idirectorysearch"></a><span data-ttu-id="9658a-105">Server Zeit Limit bei idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="9658a-105">Server Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="9658a-106">Wenn Sie eine Suche auf einem ausgelasteten Server anfordern, möchten Sie möglicherweise anfordern, dass der Server die Suche auf ein angegebenes Zeitlimit beschränkt.</span><span class="sxs-lookup"><span data-stu-id="9658a-106">When you request a search on a busy server, you may want to request that the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="9658a-107">Sie möchten z. b. eine Anwendung ausführen, um einen wöchentlichen Bericht auf einem Server zu generieren, der in der Nähe seiner Kapazität ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9658a-107">For example, you want to run an application to generate a weekly report on a server that is running near its capacity.</span></span> <span data-ttu-id="9658a-108">Um zu vermeiden, dass die gesamte CPU-Zeit verwendet und andere Vorgänge nicht ausgeführt werden, geben Sie das Such Zeitlimit auf einen kleinen Wert an, und führen Sie die Anwendung dann später erneut aus, wenn der Bericht nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9658a-108">To avoid using all the CPU time and preventing other operations from running, specify the search time limit to a small value and then rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="9658a-109">Einige Server erzwingen möglicherweise eine eigene administrative Zeitbegrenzung.</span><span class="sxs-lookup"><span data-stu-id="9658a-109">Some servers might impose their own administrative time limit.</span></span> <span data-ttu-id="9658a-110">Wenn Sie in diesen Fällen einen Wert für das Such Zeitlimit angeben, der größer ist als das administrative Zeit Limit, ignoriert der Server Ihre Spezifikation und verwendet stattdessen den internen Wert des Zeitlimits.</span><span class="sxs-lookup"><span data-stu-id="9658a-110">In these cases, if you specify a search time limit value greater than the administrative time limit, the server will ignore your specification and use its internal time limit value instead.</span></span>

<span data-ttu-id="9658a-111">Der Standardwert für das Serverzeit Limit ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="9658a-111">The default for the server time limit is no limit.</span></span> <span data-ttu-id="9658a-112">Zum Festlegen eines Serverzeit Limits legen Sie eine Suchoption für die Suchoption " **ADS \_ searchpref \_ time \_ Limit** " mit einem **\_ ganzzahligen adstype** -Wert fest, der das Server Zeitlimit (in Sekunden) in dem an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode über gebenden [**ADS \_ \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) enthält.</span><span class="sxs-lookup"><span data-stu-id="9658a-112">To set a server time limit, set an **ADS\_SEARCHPREF\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the server time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="9658a-113">Dieser Vorgang wird im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9658a-113">This operation is shown in the following code example.</span></span> <span data-ttu-id="9658a-114">Ein Serverzeit Limit von 0 (null) gibt an, dass kein Zeit Limit</span><span class="sxs-lookup"><span data-stu-id="9658a-114">A server time limit of zero indicates no time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




