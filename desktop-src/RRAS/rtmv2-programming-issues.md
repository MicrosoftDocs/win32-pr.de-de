---
title: RTMv2-Programmierprobleme
description: RTMv2-Funktionen werden mit den folgenden Annahmen geschrieben.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Programmierprobleme, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309963"
---
# <a name="rtmv2-programming-issues"></a><span data-ttu-id="ae1b5-104">RTMv2-Programmierprobleme</span><span class="sxs-lookup"><span data-stu-id="ae1b5-104">RTMv2 Programming Issues</span></span>

<span data-ttu-id="ae1b5-105">RTMv2-Funktionen werden mit den folgenden Annahmen geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ae1b5-105">RTMv2 functions are written with the following assumptions.</span></span>

-   <span data-ttu-id="ae1b5-106">RTMv2-Funktionen weisen keinen Arbeitsspeicher für den Client zu.</span><span class="sxs-lookup"><span data-stu-id="ae1b5-106">RTMv2 functions do not allocate memory for the client.</span></span> <span data-ttu-id="ae1b5-107">Der Client muss immer Arbeitsspeicher zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ae1b5-107">The client must always allocate memory.</span></span>
-   <span data-ttu-id="ae1b5-108">Wenn die Registrierung eines Clients aufgehoben wird, muss er Bereinigungs Vorgänge selbst durchführen, z. b. den gesamten zugeordneten Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="ae1b5-108">When a client is unregistering, it must perform clean-up operations itself, such as releasing all memory allocated.</span></span>
-   <span data-ttu-id="ae1b5-109">Clients müssen Handles ordnungsgemäß freigeben. Speicher Verluste können auftreten, wenn ein Client diese Vorgehensweise nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="ae1b5-109">Clients must release handles correctly; memory leaks can occur if a client does not observe this practice.</span></span>

 

 




