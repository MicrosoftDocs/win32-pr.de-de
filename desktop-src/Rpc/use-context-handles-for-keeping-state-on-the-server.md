---
title: Verwenden von Kontext Handles zum Beibehalten des Zustands auf dem Server
description: Verwenden von Kontext Handles zum Beibehalten des Zustands auf dem Server
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90bf14632ed1821a1a097a64951f6ca9aef751d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206818"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a><span data-ttu-id="2f38a-103">Verwenden von Kontext Handles zum Beibehalten des Zustands auf dem Server</span><span class="sxs-lookup"><span data-stu-id="2f38a-103">Use Context Handles for Keeping State on the Server</span></span>

<span data-ttu-id="2f38a-104">**Bewährte Methoden:** Verwenden Sie Kontext Handles, wenn der Zustand zwischen Aufrufen auf dem Server beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="2f38a-104">**Best practice:** Whenever state is kept on the server between calls, use context handles.</span></span>

<span data-ttu-id="2f38a-105">Kontext Handles sind häufig für neue RPC-Programmierer einschüchternd, und der Aufwand für Lernkontext Handles wird möglicherweise nicht als Wert für den Aufwand angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f38a-105">Context handles are often intimidating for new RPC programmers, and the overhead of learning context handles may not initially appear worth the effort.</span></span> <span data-ttu-id="2f38a-106">Es lohnt sich, da Kontext Handles über integrierte Lösungen für viele gängige Fehler bei der Netzwerk Programmierung verfügen, die andernfalls von Grund auf neu implementiert werden müssten.</span><span class="sxs-lookup"><span data-stu-id="2f38a-106">It is worth it because context handles have built-in solutions for many common pitfalls encountered in network programming that otherwise would have to be implemented from scratch.</span></span> <span data-ttu-id="2f38a-107">Das verstehen von Kontext Handles zahlt später die Dividenden.</span><span class="sxs-lookup"><span data-stu-id="2f38a-107">Understanding context handles pays dividends later.</span></span>

 

 




