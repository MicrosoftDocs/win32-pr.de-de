---
description: Eine Gruppe von Methoden, die zum Bearbeiten von Sperren verwendet wird.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Csharelocknh-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344598"
---
# <a name="csharelocknh-methods"></a><span data-ttu-id="a4943-103">Csharelocknh-Methoden</span><span class="sxs-lookup"><span data-stu-id="a4943-103">CShareLockNH Methods</span></span>

<span data-ttu-id="a4943-104">Eine Gruppe von Methoden, die zum Bearbeiten von Sperren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4943-104">A group of methods that is used to manipulate locks.</span></span>

## <a name="methods"></a><span data-ttu-id="a4943-105">Methoden</span><span class="sxs-lookup"><span data-stu-id="a4943-105">Methods</span></span>

<span data-ttu-id="a4943-106">Die folgenden Methoden werden von Rwnh.dll exportiert.</span><span class="sxs-lookup"><span data-stu-id="a4943-106">The following are methods exported by Rwnh.dll.</span></span>



| <span data-ttu-id="a4943-107">Methode</span><span class="sxs-lookup"><span data-stu-id="a4943-107">Method</span></span>                                                                   | <span data-ttu-id="a4943-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4943-108">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="a4943-109">**Exclusivelock**</span><span class="sxs-lookup"><span data-stu-id="a4943-109">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)                     | <span data-ttu-id="a4943-110">Erhält eine Lese-/Schreibsperre.</span><span class="sxs-lookup"><span data-stu-id="a4943-110">Acquires a reader/writer lock.</span></span>                                  |
| [<span data-ttu-id="a4943-111">**Exclusivetopartial**</span><span class="sxs-lookup"><span data-stu-id="a4943-111">**ExclusiveToPartial**</span></span>](csharelocknh--exclusivetopartial.md)           | <span data-ttu-id="a4943-112">Ändert den Zustand.</span><span class="sxs-lookup"><span data-stu-id="a4943-112">Changes the state.</span></span>                                              |
| [<span data-ttu-id="a4943-113">**Exclusiveunlock**</span><span class="sxs-lookup"><span data-stu-id="a4943-113">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)                 | <span data-ttu-id="a4943-114">Gibt eine Sperre frei.</span><span class="sxs-lookup"><span data-stu-id="a4943-114">Releases a lock.</span></span>                                                |
| [<span data-ttu-id="a4943-115">**Firstpartialto Exclusive**</span><span class="sxs-lookup"><span data-stu-id="a4943-115">**FirstPartialToExclusive**</span></span>](csharelocknh--firstpartialtoexclusive.md) | <span data-ttu-id="a4943-116">Wird verwendet, um eine partielle Sperre in eine exklusive Sperre umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="a4943-116">Used in converting a partial lock to an exclusive lock.</span></span>         |
| [<span data-ttu-id="a4943-117">**Partitionier.**</span><span class="sxs-lookup"><span data-stu-id="a4943-117">**PartialLock**</span></span>](csharelocknh--partiallock.md)                         | <span data-ttu-id="a4943-118">Verhindert, dass mehr als ein Thread eine Sperre erhält.</span><span class="sxs-lookup"><span data-stu-id="a4943-118">Prevents more than one thread from completing acquiring a lock.</span></span> |
| [<span data-ttu-id="a4943-119">**Partialunlock**</span><span class="sxs-lookup"><span data-stu-id="a4943-119">**PartialUnlock**</span></span>](csharelocknh--partialunlock.md)                     | <span data-ttu-id="a4943-120">Gibt eine partielle Sperre frei.</span><span class="sxs-lookup"><span data-stu-id="a4943-120">Releases a partial lock.</span></span>                                        |
| [<span data-ttu-id="a4943-121">**Sharelock**</span><span class="sxs-lookup"><span data-stu-id="a4943-121">**ShareLock**</span></span>](csharelocknh--sharelock.md)                             | <span data-ttu-id="a4943-122">Erhält eine Sperre für den freigegebenen Modus.</span><span class="sxs-lookup"><span data-stu-id="a4943-122">Obtains a lock for shared mode.</span></span>                                 |
| [<span data-ttu-id="a4943-123">**Share Unlock**</span><span class="sxs-lookup"><span data-stu-id="a4943-123">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)                         | <span data-ttu-id="a4943-124">Gibt eine Sperre aus dem freigegebenen Modus frei.</span><span class="sxs-lookup"><span data-stu-id="a4943-124">Releases a lock from shared mode.</span></span>                               |
| [<span data-ttu-id="a4943-125">**Sharedtopartial**</span><span class="sxs-lookup"><span data-stu-id="a4943-125">**SharedToPartial**</span></span>](csharelocknh--sharedtopartial.md)                 | <span data-ttu-id="a4943-126">Ruft eine partielle Sperre ab.</span><span class="sxs-lookup"><span data-stu-id="a4943-126">Obtains a partial lock.</span></span>                                         |
| [<span data-ttu-id="a4943-127">**Tryexclusivelock**</span><span class="sxs-lookup"><span data-stu-id="a4943-127">**TryExclusiveLock**</span></span>](csharelocknh--tryexclusivelock.md)               | <span data-ttu-id="a4943-128">Erhält exklusiv eine Sperre.</span><span class="sxs-lookup"><span data-stu-id="a4943-128">Obtains a lock exclusively.</span></span>                                     |



 

 

 



