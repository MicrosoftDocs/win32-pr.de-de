---
description: Eine Transaktion ist ein Objekt, das eine logische Arbeitseinheit definiert.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transaktionen (Kerneltransaktions-Manager)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350187"
---
# <a name="transactions"></a><span data-ttu-id="9531f-103">Transaktionen</span><span class="sxs-lookup"><span data-stu-id="9531f-103">Transactions</span></span>

<span data-ttu-id="9531f-104">Eine Transaktion ist ein Objekt, das eine logische Arbeitseinheit definiert.</span><span class="sxs-lookup"><span data-stu-id="9531f-104">A transaction is an object that defines a logical unit of work.</span></span> <span data-ttu-id="9531f-105">Die Transaktion ist aktiv, solange ein Handle auf die Transaktion verweist, und Sie gilt als aktiv, wenn für die Transaktion noch kein Commit oder Rollback ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9531f-105">The transaction is alive as long as there is a handle referencing the transaction and it is considered active if the transaction has not yet been committed or rolled back.</span></span> <span data-ttu-id="9531f-106">Wenn eine Transaktion erstellt wird und alle Handles vor einem Commit oder Rollback geschlossen wurden, wird für die Transaktion ein Rollback ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9531f-106">If a transaction is created and all handles to it have been closed before a commit or rollback occurs, the transaction will be rolled back.</span></span>

<span data-ttu-id="9531f-107">Stellen Sie sich vor, dass ein transaktionaler Client im Benutzermodus eine Transaktion erstellt, um deren Vorgänge zu begrenzen, und dann Updates für einen oder mehrere Ressourcen-Manager ausführt.</span><span class="sxs-lookup"><span data-stu-id="9531f-107">Consider the case of a user-mode transactional client that creates a transaction to scope its operations, then performs updates on one or more resource managers.</span></span> <span data-ttu-id="9531f-108">Folgendes passiert:</span><span class="sxs-lookup"><span data-stu-id="9531f-108">The following occurs:</span></span>

1.  <span data-ttu-id="9531f-109">Der Client ruft die Funktion "up [**Transaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) " auf, um die Transaktion zu erstellen, und empfängt ein Handle für diese Transaktion als Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="9531f-109">The client calls the [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) function to create the transaction and receives a handle to that transaction as the return value.</span></span>

    <span data-ttu-id="9531f-110">Die Transaktion kann von einer beliebigen Anzahl von Prozessen geöffnet oder geerbt werden. Jeder Prozess ist daher an der Transaktion beteiligt.</span><span class="sxs-lookup"><span data-stu-id="9531f-110">The transaction can be opened or inherited by any number of processes; each process is thus involved in the transaction.</span></span> <span data-ttu-id="9531f-111">Der Fehler bei einem dieser Prozesse bewirkt, dass die Transaktion abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="9531f-111">The failure of any of these processes will cause the transaction to abort.</span></span>

    <span data-ttu-id="9531f-112">Diese Transaktion ist möglicherweise noch nicht persistent.</span><span class="sxs-lookup"><span data-stu-id="9531f-112">This transaction may not yet be persistent.</span></span> <span data-ttu-id="9531f-113">Nur Transaktionen, die den vorbereiteten Zustand erreicht haben, müssen über Systemfehler hinweg wieder hergestellt werden, wenn die Transaktion die vermutete Abbruch Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9531f-113">Only transactions that have reached the prepared state must be recovered across system failures if the transaction uses presumed-abort logging.</span></span>

2.  <span data-ttu-id="9531f-114">Der Client muss eine Transaktion explizit an den Ressourcen-Manager übergeben.</span><span class="sxs-lookup"><span data-stu-id="9531f-114">The client must pass a transaction to the resource manager explicitly.</span></span>
3.  <span data-ttu-id="9531f-115">Der Client führt alle Transaktions Vorgänge mit einem oder mehreren RMS aus, z. b. transaktiven Dateisystemen.</span><span class="sxs-lookup"><span data-stu-id="9531f-115">The client performs all its transactional operations with one or more RMs, such as transacted file systems.</span></span>
4.  <span data-ttu-id="9531f-116">Der Client ruft die [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9531f-116">The client calls the [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) function.</span></span>
5.  <span data-ttu-id="9531f-117">Der Resource Manager empfängt Benachrichtigungen von KTM, um seine Daten vorzubereiten und zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="9531f-117">The resource manager receives notifications from KTM to prepare and commit its data.</span></span>

## <a name="transactions-and-threads"></a><span data-ttu-id="9531f-118">Transaktionen und Threads</span><span class="sxs-lookup"><span data-stu-id="9531f-118">Transactions and Threads</span></span>

<span data-ttu-id="9531f-119">Transaktionen sind nicht identisch mit Threads.</span><span class="sxs-lookup"><span data-stu-id="9531f-119">Transactions are not the same as threads.</span></span> <span data-ttu-id="9531f-120">Mehrere Threads oder Prozesse können Teil einer einzelnen Transaktion sein.</span><span class="sxs-lookup"><span data-stu-id="9531f-120">Multiple threads or processes can be a part of a single transaction.</span></span> <span data-ttu-id="9531f-121">Umgekehrt kann ein Thread zu unterschiedlichen Zeitpunkten Teil mehrerer verschiedener Transaktionen sein.</span><span class="sxs-lookup"><span data-stu-id="9531f-121">Conversely, a thread can be a part of several different transactions at different times.</span></span>

## <a name="transaction-functions"></a><span data-ttu-id="9531f-122">Transaktionsfunktionen</span><span class="sxs-lookup"><span data-stu-id="9531f-122">Transaction Functions</span></span>

<span data-ttu-id="9531f-123">Die folgenden Funktionen werden mit Transaktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9531f-123">The following functions are used with transactions.</span></span>



| <span data-ttu-id="9531f-124">Funktion</span><span class="sxs-lookup"><span data-stu-id="9531f-124">Function</span></span>                                                            | <span data-ttu-id="9531f-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9531f-125">Description</span></span>                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9531f-126">**CommitTransaction**</span><span class="sxs-lookup"><span data-stu-id="9531f-126">**CommitTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | <span data-ttu-id="9531f-127">Fordert an, dass die angegebene Transaktion ein Commit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9531f-127">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="9531f-128">**Committransaktionasync**</span><span class="sxs-lookup"><span data-stu-id="9531f-128">**CommitTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | <span data-ttu-id="9531f-129">Fordert an, dass die angegebene Transaktion ein Commit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9531f-129">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="9531f-130">**CreateTransaction**</span><span class="sxs-lookup"><span data-stu-id="9531f-130">**CreateTransaction**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | <span data-ttu-id="9531f-131">Erstellt ein neues Transaktions Objekt.</span><span class="sxs-lookup"><span data-stu-id="9531f-131">Creates a new transaction object.</span></span>                                                             |
| [<span data-ttu-id="9531f-132">**Gettransaktioninformation**</span><span class="sxs-lookup"><span data-stu-id="9531f-132">**GetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | <span data-ttu-id="9531f-133">Gibt die angeforderten Informationen zur angegebenen Transaktion zurück.</span><span class="sxs-lookup"><span data-stu-id="9531f-133">Returns the requested information about the specified transaction.</span></span>                            |
| [<span data-ttu-id="9531f-134">**Opentransaction**</span><span class="sxs-lookup"><span data-stu-id="9531f-134">**OpenTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | <span data-ttu-id="9531f-135">Öffnet eine vorhandene Transaktion.</span><span class="sxs-lookup"><span data-stu-id="9531f-135">Opens an existing transaction.</span></span>                                                                |
| [<span data-ttu-id="9531f-136">**RollbackTransaction**</span><span class="sxs-lookup"><span data-stu-id="9531f-136">**RollbackTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | <span data-ttu-id="9531f-137">Fordert an, dass für die angegebene Transaktion ein Rollback ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9531f-137">Requests that the specified transaction be rolled back.</span></span>                                       |
| [<span data-ttu-id="9531f-138">**Rollbacktransaktionasync**</span><span class="sxs-lookup"><span data-stu-id="9531f-138">**RollbackTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | <span data-ttu-id="9531f-139">Fordert an, dass für die angegebene Transaktion ein Rollback ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9531f-139">Requests that the specified transaction be rolled back.</span></span> <span data-ttu-id="9531f-140">Diese Funktion gibt asynchron zurück.</span><span class="sxs-lookup"><span data-stu-id="9531f-140">This function returns asynchronously.</span></span> |
| [<span data-ttu-id="9531f-141">**Settransaktioninformation**</span><span class="sxs-lookup"><span data-stu-id="9531f-141">**SetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | <span data-ttu-id="9531f-142">Legt die Transaktionsinformationen für die angegebene Transaktion fest.</span><span class="sxs-lookup"><span data-stu-id="9531f-142">Sets the transaction information for the specified transaction.</span></span>                               |



 

 

 



