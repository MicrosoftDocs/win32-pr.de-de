---
description: In der folgenden Liste sind die TAPI-MSP-Entwurfs Ziele enthalten.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Allgemeine Entwurfs Ziele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345154"
---
# <a name="general-design-goals"></a><span data-ttu-id="bb8f5-103">Allgemeine Entwurfs Ziele</span><span class="sxs-lookup"><span data-stu-id="bb8f5-103">General Design Goals</span></span>

<span data-ttu-id="bb8f5-104">In der folgenden Liste sind die TAPI-MSP-Entwurfs Ziele enthalten.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-104">The following list contains the TAPI MSP design goals.</span></span>

-   <span data-ttu-id="bb8f5-105">Basisklassen wurden einfach gehalten, wobei Member und Methoden nur bei Bedarf eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-105">Base classes have been kept simple, with members and methods introduced only when absolutely necessary.</span></span>
-   <span data-ttu-id="bb8f5-106">Einfache Vererbung.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-106">Simple inheritance.</span></span> <span data-ttu-id="bb8f5-107">Keine mehrfache Vererbung zwischen Klassen, obwohl mehrere Vererbung für die Schnittstellen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-107">No multiple inheritance among classes, although multiple inheritance is used for the interfaces.</span></span>
-   <span data-ttu-id="bb8f5-108">Das Sperren erfolgt nur in einer Richtung, um einen Deadlock zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-108">Locking happens only in one direction to prevent deadlock.</span></span> <span data-ttu-id="bb8f5-109">Methoden für das-Objekt, die die Sperre des Aufrufes erfordern, können Methoden für den Stream aufzurufen, die die Sperre für den Stream erfordern.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-109">Methods on the call object that require the lock on the call might call methods on the stream that require the lock on the stream.</span></span> <span data-ttu-id="bb8f5-110">Methoden im Datenstrom, die die Sperre für den Stream erfordern, werden jedoch nie eine Methode für den-Befehl aufruft, der eine Sperre für den-Befehl erfordert.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-110">However, methods on the stream that require the lock on the stream will never call a method on the call that requires a lock on the call.</span></span>
-   <span data-ttu-id="bb8f5-111">RefCounts werden verwendet, um den Zugriff zu schützen.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-111">Refcounts are used to protect access.</span></span> <span data-ttu-id="bb8f5-112">Alle Rückrufe, die an den Thread Pool gesendet werden, enthalten refCounts.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-112">All callbacks posted to the thread pool hold refcounts.</span></span> <span data-ttu-id="bb8f5-113">Der Ref count wird abgebrochen, wenn der Warte Vorgang abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-113">The refcount is canceled when the wait is canceled.</span></span> <span data-ttu-id="bb8f5-114">Das Adress Objekt hat eine Ref-Anzahl an Terminals.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-114">The Address object has refcounts on Terminals.</span></span> <span data-ttu-id="bb8f5-115">Calltobjekte haben refcount für die Adresse und für Datenströme.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-115">Call objects have refcounts on the Address and on Streams.</span></span> <span data-ttu-id="bb8f5-116">Stream-Objekte haben rebcounts bei aufrufen und Terminals.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-116">Stream objects have refcounts on Calls and Terminals.</span></span> <span data-ttu-id="bb8f5-117">Die Terminals haben Ref-Werte für Streams.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-117">The Terminals have refcounts on Streams.</span></span> <span data-ttu-id="bb8f5-118">Die zirkuläre refCounts unterbrechen, wenn die Shutdown-Methode für die Address-und calltobjekte aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bb8f5-118">The circular refcounts break when the shutdown method on the Address and Call objects is called.</span></span>

 

 



