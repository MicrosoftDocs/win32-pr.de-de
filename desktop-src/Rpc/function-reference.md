---
title: Funktionsreferenz
description: In diesem Abschnitt werden die Remote Prozedur Aufrufe (RPC)-Lauf Zeitfunktionen beschrieben, die in Microsoft RPC unterstützt werden.
ms.assetid: 135bef8d-1794-420e-a111-604d02dbcc06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163c68f56a483d3eb7f62596c4a3d78ba2b5774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471317"
---
# <a name="function-reference"></a><span data-ttu-id="9909d-103">Funktionsreferenz</span><span class="sxs-lookup"><span data-stu-id="9909d-103">Function Reference</span></span>

<span data-ttu-id="9909d-104">In diesem Abschnitt werden die Remote Prozedur Aufrufe (RPC)-Lauf Zeitfunktionen beschrieben, die in Microsoft RPC unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9909d-104">This section documents the Remote Procedure Call (RPC) run-time functions supported in Microsoft RPC.</span></span> <span data-ttu-id="9909d-105">In diesem Abschnitt werden der Zweck, die Syntax, die Eingabeparameter und die Rückgabewerte der einzelnen Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9909d-105">This section describes each function's purpose, syntax, input parameters, and return values.</span></span> <span data-ttu-id="9909d-106">Außerdem werden zusätzliche Informationen bereitstellt, die Sie bei der Verwendung von RPC-Funktionen in einer Anwendung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9909d-106">It also provides additional information to help you use RPC functions in an application.</span></span>

<span data-ttu-id="9909d-107">Alle Zeiger, die an RPC-Funktionen weitergegeben werden, müssen das **\_ \_ RPC- \_ weite** Attribut enthalten</span><span class="sxs-lookup"><span data-stu-id="9909d-107">All pointers passed to RPC functions must include the **\_ \_RPC\_FAR** attribute.</span></span> <span data-ttu-id="9909d-108">Beispielsweise wird das RPC-Zeiger **\_ Bindungs \_ \* handle** zu **RPC- \_ Bindungs \_ handle RPC- \_ \_ \_ weit \*** , und **Char \* \*** *ptr* wird zu **char RPC Far \_ \_ \_ \* \_ \_ RPC \_ Far \*** *ptr*.</span><span class="sxs-lookup"><span data-stu-id="9909d-108">For example, the pointer **RPC\_BINDING\_HANDLE \*** becomes **RPC\_BINDING\_HANDLE \_ \_RPC\_FAR \*** and **char \* \*** *Ptr* becomes **char \_ \_RPC\_FAR \* \_ \_RPC\_FAR \*** *Ptr*.</span></span>

<span data-ttu-id="9909d-109">In diesem Abschnitt werden die Funktions Verweise in den folgenden Gruppen dargestellt:</span><span class="sxs-lookup"><span data-stu-id="9909d-109">This section presents the function references in the following groups:</span></span>

-   [<span data-ttu-id="9909d-110">RPC-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9909d-110">RPC Functions</span></span>](rpc-functions.md)
-   [<span data-ttu-id="9909d-111">RPC-Rückruf-und Benachrichtigungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="9909d-111">RPC Callback and Notification Functions</span></span>](rpc-callback-and-notification-functions.md)

 

 




