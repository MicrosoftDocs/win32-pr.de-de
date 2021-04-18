---
description: Erben von manuellen Transaktionen
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Erben von manuellen Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340110"
---
# <a name="inheriting-manual-transactions"></a><span data-ttu-id="37eb7-103">Erben von manuellen Transaktionen</span><span class="sxs-lookup"><span data-stu-id="37eb7-103">Inheriting Manual Transactions</span></span>

<span data-ttu-id="37eb7-104">Wenn ein Objekt mit einer BYOT-Transaktion im Kontext ein zweites Objekt erstellt, kann das Downstream-Objekt die BYOT-Transaktion erben (sofern diese zum Erben von Transaktionen konfiguriert ist).</span><span class="sxs-lookup"><span data-stu-id="37eb7-104">If an object with a BYOT transaction in its context creates a second object, the downstream object can inherit the BYOT transaction (if configured to inherit transactions).</span></span> <span data-ttu-id="37eb7-105">Das erste mit dem BYOT-Gateway erstellte Objekt muss für "anfordern" oder "Support"-Transaktionen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="37eb7-105">The first object created using the BYOT gateway needs to be configured to "require" or "support" transactions.</span></span> <span data-ttu-id="37eb7-106">Nachfolgende Objekte in der Aktivität können basierend auf den Anwendungsanforderungen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="37eb7-106">Subsequent objects in the activity could be configured based on application requirements.</span></span>

<span data-ttu-id="37eb7-107">Für automatische Transaktionen versucht die com+-Laufzeit nicht, einen Commit für die Transaktion auszuführen, bis das Stamm Objekt angibt, dass Sie bereit ist (durch Aufrufen von [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) vor der Rückgabe von einem Aufruf).</span><span class="sxs-lookup"><span data-stu-id="37eb7-107">For automatic transactions, the COM+ runtime does not attempt to commit the transaction until the root object indicates that it is ready (by calling [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) before returning from a call).</span></span> <span data-ttu-id="37eb7-108">Benutzer sollten sich bewusst sein, dass ein Commit für eine BYOT-Transaktion vorzeitig ausgeführt werden kann (da die Arbeit von untergeordneten Objekten noch nicht abgeschlossen wurde), da der Stamm nicht in der com+-Laufzeitumgebung ausgeführt wird und die Commit-Semantik nicht an die Lebensdauer des Objekts gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="37eb7-108">Users should be aware that a BYOT transaction could commit prematurely (in that the work of child objects has not been completed), because the "root" is not running under the COM+ runtime environment, and the commit semantics are not tied to the lifetime of the object.</span></span> <span data-ttu-id="37eb7-109">Im Allgemeinen sollte der Benutzer darauf achten, dass die Synchronisierungs Grenze der Transaktion nicht verletzt wird.</span><span class="sxs-lookup"><span data-stu-id="37eb7-109">In general, the user should take care to not violate the synchronization boundary of the transaction.</span></span>

<span data-ttu-id="37eb7-110">Andernfalls wird die com+-Commit-Semantik angewendet.</span><span class="sxs-lookup"><span data-stu-id="37eb7-110">Otherwise, COM+ commit semantics apply.</span></span> <span data-ttu-id="37eb7-111">Com+ versucht nicht, einen Commit für eine Transaktion durchführen, während ein Objekt innerhalb einer Synchronisierungs Grenze aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="37eb7-111">COM+ will not attempt to commit a transaction while an object within a synchronization boundary is in call.</span></span> <span data-ttu-id="37eb7-112">Außerdem können-Objekte ihre Konsistenz mithilfe von [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)angeben.</span><span class="sxs-lookup"><span data-stu-id="37eb7-112">Also, objects can indicate their consistency using [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span></span> <span data-ttu-id="37eb7-113">Wenn versucht wird, einen Commit für eine Transaktion durchzusetzen, die die Arbeit eines Objekts mit dem Namen **DisableCommit** einschließt, wird die Transaktion abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="37eb7-113">If an attempt is made to commit a transaction which includes the work of an object that has called **DisableCommit**, the transaction will abort.</span></span>

 

 



