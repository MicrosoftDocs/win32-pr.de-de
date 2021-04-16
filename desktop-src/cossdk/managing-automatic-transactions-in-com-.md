---
description: Im COM+-Programmiermodell können Sie Ihre Komponenten so entwerfen, dass Sie die am besten&\# 8212, das Aktivieren von Geschäftslogik oder das Einrichten einer Datenbankverbindung&\# 8212 und das Transaktions Verarbeitungs Framework von Microsoft Windows zum Automatisieren von Transaktionen verwenden.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Verwalten von automatischen Transaktionen in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524056"
---
# <a name="managing-automatic-transactions-in-com"></a><span data-ttu-id="c0153-103">Verwalten von automatischen Transaktionen in com+</span><span class="sxs-lookup"><span data-stu-id="c0153-103">Managing Automatic Transactions in COM+</span></span>

<span data-ttu-id="c0153-104">Im COM+-Programmiermodell können Sie Ihre Komponenten so entwerfen, dass Sie Ihre Anforderungen optimal erledigen – indem Sie die Geschäftslogik aktivieren oder eine Datenbankverbindung herstellen – und sich auf das Transaktions Verarbeitungs Framework von Microsoft Windows verlassen, um Transaktionen zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="c0153-104">In the COM+ programming model, you can design your components to do what they do best—enabling business logic or establishing a database connection—and rely on the transaction processing framework of Microsoft Windows to automate transactions.</span></span>

## <a name="starting-a-transaction"></a><span data-ttu-id="c0153-105">Starten einer Transaktion</span><span class="sxs-lookup"><span data-stu-id="c0153-105">Starting a Transaction</span></span>

<span data-ttu-id="c0153-106">Com+ startet automatisch eine Transaktion, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="c0153-106">COM+ automatically begins a transaction when it encounters either of the following conditions:</span></span>

-   <span data-ttu-id="c0153-107">Wenn ein nicht transaktionaler Client eine Komponente aufruft, die eine Transaktion erfordert oder eine neue Transaktion erfordert.</span><span class="sxs-lookup"><span data-stu-id="c0153-107">When a non-transactional client calls a component that requires a transaction or requires a new transaction.</span></span>
-   <span data-ttu-id="c0153-108">Wenn ein transaktionaler Client eine Komponente aufruft, die eine neue Transaktion erfordert.</span><span class="sxs-lookup"><span data-stu-id="c0153-108">When a transactional client calls a component that requires a new transaction.</span></span>

<span data-ttu-id="c0153-109">Wenn com+ feststellt, dass ein Objekt über eine neue Transaktion verfügen soll, beginnt es zuerst mit der Transaktion und fügt dann das Objekt in das Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="c0153-109">If COM+ determines that an object should have a new transaction, it begins the transaction first and then places the object in it.</span></span> <span data-ttu-id="c0153-110">Der Vorgang umfasst folgende Schritte:</span><span class="sxs-lookup"><span data-stu-id="c0153-110">The process includes the following steps:</span></span>

1.  <span data-ttu-id="c0153-111">Com+ erstellt ein Kontext Objekt, legt sowohl die [JIT-Aktivierungs](com--just-in-time-activation.md) -als auch die- [Synchronisierungs](com--synchronization.md) Attribute auf Required fest und legt die [konsistenten und done-Flags](consistent-and-done-flags.md) auf true bzw. false fest.</span><span class="sxs-lookup"><span data-stu-id="c0153-111">COM+ creates a context object, sets both the [JIT activation](com--just-in-time-activation.md) and [Synchronization](com--synchronization.md) attributes to Required, and sets the [consistent and done flags](consistent-and-done-flags.md) to True and False, respectively.</span></span>
2.  <span data-ttu-id="c0153-112">Com+ kommuniziert mit dem Distributed Transaction Coordinator (DTC), um eine Transaktion zu starten.</span><span class="sxs-lookup"><span data-stu-id="c0153-112">COM+ communicates with the Distributed Transaction Coordinator (DTC) to begin a transaction.</span></span> <span data-ttu-id="c0153-113">Der DTC koordiniert die physische Transaktion.</span><span class="sxs-lookup"><span data-stu-id="c0153-113">The DTC coordinates the physical transaction.</span></span>
3.  <span data-ttu-id="c0153-114">Der DTC generiert einen Transaktions Bezeichner und übergibt ihn an com+ zurück.</span><span class="sxs-lookup"><span data-stu-id="c0153-114">The DTC generates a transaction identifier and passes it back to COM+.</span></span> <span data-ttu-id="c0153-115">Der Transaktions Bezeichner legt eine Transaktionsgrenze fest.</span><span class="sxs-lookup"><span data-stu-id="c0153-115">The transaction identifier establishes a transaction boundary.</span></span> <span data-ttu-id="c0153-116">Alle an der Transaktion beteiligten Objekte verwenden denselben Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c0153-116">All objects participating in the transaction share the same identifier.</span></span>
4.  <span data-ttu-id="c0153-117">Wenn der Client das Objekt erstellt, aktiviert com+ ihn innerhalb der Transaktionsgrenze.</span><span class="sxs-lookup"><span data-stu-id="c0153-117">When the client creates the object, COM+ activates it within the transaction boundary.</span></span>

## <a name="ending-a-transaction"></a><span data-ttu-id="c0153-118">Beenden einer Transaktion</span><span class="sxs-lookup"><span data-stu-id="c0153-118">Ending a Transaction</span></span>

<span data-ttu-id="c0153-119">Com+ beendet eine automatische Transaktion, indem ein Commit oder Abbruch ausgeführt wird, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="c0153-119">COM+ ends an automatic transaction by committing or aborting it when one of the following conditions occurs:</span></span>

-   <span data-ttu-id="c0153-120">Das Stamm Objekt der Transaktion schließt seine Arbeit ab, und com+ gibt es frei.</span><span class="sxs-lookup"><span data-stu-id="c0153-120">The root object of the transaction completes its work and COM+ releases it.</span></span> <span data-ttu-id="c0153-121">Nachdem das Stamm Objekt deaktiviert wurde, versucht die Transaktion, einen Commit durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c0153-121">After the root object deactivates, the transaction attempts to commit.</span></span>
-   <span data-ttu-id="c0153-122">Der Client gibt das Stamm Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="c0153-122">The client releases the root object.</span></span> <span data-ttu-id="c0153-123">Ohne einen Verweis wird das Stamm Objekt deaktiviert, und die Transaktion versucht, einen Commit durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c0153-123">Without a reference, the root object deactivates and the transaction attempts to commit.</span></span>
-   <span data-ttu-id="c0153-124">Die Transaktion überschreitet den Timeout Schwellenwert.</span><span class="sxs-lookup"><span data-stu-id="c0153-124">The transaction exceeds its time-out threshold.</span></span> <span data-ttu-id="c0153-125">Die Transaktion wird automatisch abgebrochen, wenn nicht innerhalb des Transaktions Timeout Zeitraums ein Commit ausgeführt wird, wobei alle der Transaktion zugeordneten Objekte deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c0153-125">The transaction aborts automatically if not committed within the transaction time-out period, deactivating all objects associated with the transaction.</span></span> <span data-ttu-id="c0153-126">Der Standardwert für das Transaktions Timeout beträgt 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c0153-126">The default transaction time-out period is 60 seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0153-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0153-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0153-128">Konsistente und done-Flags</span><span class="sxs-lookup"><span data-stu-id="c0153-128">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="c0153-129">Beschleunigen von Transaktionen durch Benachrichtigen des root-Objekts</span><span class="sxs-lookup"><span data-stu-id="c0153-129">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[<span data-ttu-id="c0153-130">Beenden einer automatischen Transaktion durch Aufrufen von SetComplete</span><span class="sxs-lookup"><span data-stu-id="c0153-130">Terminating an Automatic Transaction by Calling SetComplete</span></span>](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



