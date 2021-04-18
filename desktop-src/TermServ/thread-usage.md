---
title: Verwendung von Threads
description: Sie sollten die Anwendungs Thread Verwendung für eine mehr Benutzer-, multiprozessorRemotedesktopdienste Umgebung optimieren und ausgleichen.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337146"
---
# <a name="thread-usage"></a><span data-ttu-id="d6fdb-103">Verwendung von Threads</span><span class="sxs-lookup"><span data-stu-id="d6fdb-103">Thread usage</span></span>

<span data-ttu-id="d6fdb-104">Threads bieten eine bequeme Möglichkeit, eine Anwendung zu ermöglichen, die Nutzung von CPU-Ressourcen in einem System zu maximieren, insbesondere in einer Konfiguration mit mehreren Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="d6fdb-104">Threads provide a convenient way of allowing an application to maximize its usage of CPU resources in a system, especially in a multiple processor configuration.</span></span> <span data-ttu-id="d6fdb-105">In einer Remotedesktopdienste Umgebung können allerdings mehrere Benutzer Multithreadanwendungen ausführen, und alle Threads für alle Benutzer konkurrieren mit den zentralen CPU-Ressourcen dieses Systems.</span><span class="sxs-lookup"><span data-stu-id="d6fdb-105">In a Remote Desktop Services environment, however, multiple users can be running multithreaded applications, and all of the threads for all of the users compete for the central CPU resources of that system.</span></span> <span data-ttu-id="d6fdb-106">Vor diesem Hintergrund sollten Sie die Anwendungs Thread Verwendung für eine mehr Benutzer-, multiprozessorRemotedesktopdienste Umgebung optimieren und ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="d6fdb-106">With this in mind, you should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span> <span data-ttu-id="d6fdb-107">Obwohl eine schlecht entwickelte Multithreadanwendung mit Leerlauf-oder verschwendeten Threads auf einem Client Computer ausreichend funktionieren kann, kann die gleiche Anwendung auf einem mehr Benutzer-Remotedesktopdienste Server nicht gut funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d6fdb-107">While a poorly designed multithreaded application with idle or wasted threads might perform adequately on a client computer, the same application might not perform well on a multiuser Remote Desktop Services server.</span></span>

 

 




