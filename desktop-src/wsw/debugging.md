---
title: Debuggen (Windows-Webdienste)
description: Eine Reihe von Funktionen ist nur im Debugbuild verfügbar und zum Testen und Debuggen vorgesehen.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Debuggen von Webdiensten für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341571"
---
# <a name="debugging-windows-web-services"></a><span data-ttu-id="1dd32-106">Debuggen (Windows-Webdienste)</span><span class="sxs-lookup"><span data-stu-id="1dd32-106">Debugging (Windows Web Services)</span></span>

<span data-ttu-id="1dd32-107">Eine Reihe von Funktionen ist nur im Debugbuild verfügbar und zum Testen und Debuggen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="1dd32-107">A set of functions is only available in the DEBUG build, and are intended for testing and debugging.</span></span>


<span data-ttu-id="1dd32-108">Eine Reihe von Funktionen und Umgebungsvariablen sind nur im Debugmodus verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1dd32-108">There are a number of functions and environment variables available in the DEBUG mode only.</span></span> <span data-ttu-id="1dd32-109">Sie können zum Testen und Debuggen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dd32-109">They can be used to help with testing and debugging.</span></span>

-   <span data-ttu-id="1dd32-110">Durch Festlegen von wstimeout = 0 werden alle Timeouts unendlich.</span><span class="sxs-lookup"><span data-stu-id="1dd32-110">Setting WsTimeout=0 will cause all timeouts to be INFINITE.</span></span> <span data-ttu-id="1dd32-111">Dies ist nützlich, wenn der Debugger bei zeitsensiblen Vorgängen durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="1dd32-111">This is useful when stepping through the debugger during time sensitive operations.</span></span>
-   <span data-ttu-id="1dd32-112">Das Festlegen von wsfailcount hat denselben Effekt wie das Aufrufen von wssetautofail.</span><span class="sxs-lookup"><span data-stu-id="1dd32-112">Setting WsFailCount has the same effect as calling WsSetAutoFail.</span></span>
-   <span data-ttu-id="1dd32-113">Mit wsflags können Sie verschiedene Flags festlegen, die das Laufzeitverhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="1dd32-113">WsFlags allows you to set various flags that modify the runtime behavior.</span></span> <span data-ttu-id="1dd32-114">Die Syntax ist wsflags = a, b, c.</span><span class="sxs-lookup"><span data-stu-id="1dd32-114">The syntax is WsFlags=a,b,c.</span></span> <span data-ttu-id="1dd32-115">Die unterstützten Flags sind modifytimestamp, modifyinclusiveprefixes, modifytimestampdigest, modifyyheaderdigest und modifysignaturevalue.</span><span class="sxs-lookup"><span data-stu-id="1dd32-115">The supported flags are ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest and ModifySignatureValue.</span></span>

<span data-ttu-id="1dd32-116">Die folgenden Funktionen werden beim Debuggen verwendet:</span><span class="sxs-lookup"><span data-stu-id="1dd32-116">The following functions are used with debugging:</span></span>

-   [<span data-ttu-id="1dd32-117">**Wsdumpmemory**</span><span class="sxs-lookup"><span data-stu-id="1dd32-117">**WsDumpMemory**</span></span>](wsdumpmemory.md)
-   [<span data-ttu-id="1dd32-118">**Wssetauentfail**</span><span class="sxs-lookup"><span data-stu-id="1dd32-118">**WsSetAutoFail**</span></span>](wssetautofail.md)

 

 




