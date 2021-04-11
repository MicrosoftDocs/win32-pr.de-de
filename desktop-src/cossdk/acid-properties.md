---
description: Das von den kernelverarbeitungs-pionikern geprägt ist, die Akronym ACID steht für atomarisch, konsistent, isoliert und dauerhaft.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: ACID-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126601"
---
# <a name="acid-properties"></a><span data-ttu-id="ab508-103">ACID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab508-103">ACID Properties</span></span>

<span data-ttu-id="ab508-104">Das von den kernelverarbeitungs-pionikern geprägt ist, die Akronym ACID steht für atomarisch, konsistent, isoliert und dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="ab508-104">Coined by transaction processing pioneers, the acronym ACID stands for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="ab508-105">Um ein vorhersagbares Verhalten zu gewährleisten, müssen alle Transaktionen diese grundlegenden Eigenschaften besitzen, um die Rolle Unternehmens kritischer Transaktionen als all-oder-None-Vorschläge zu verstärken.</span><span class="sxs-lookup"><span data-stu-id="ab508-105">To ensure predictable behavior, all transactions must possess these basic properties, reinforcing the role of mission-critical transactions as all-or-none propositions.</span></span>

<span data-ttu-id="ab508-106">Die folgende Liste enthält eine Definition und eine Beschreibung der einzelnen ACID-Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ab508-106">The following list contains a definition and a description of each ACID property:</span></span>

<dl> <dt>

<span data-ttu-id="ab508-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic</span><span class="sxs-lookup"><span data-stu-id="ab508-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic</span></span>
</dt> <dd>

<span data-ttu-id="ab508-108">Eine Transaktion muss genau einmal ausgeführt werden und muss atomarisch sein – entweder ist entweder die gesamte Arbeit abgeschlossen, oder es ist kein Vorgang erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ab508-108">A transaction must execute exactly once and must be atomic—either all of the work is done or none of it is.</span></span> <span data-ttu-id="ab508-109">Vorgänge innerhalb einer Transaktion teilen sich in der Regel eine allgemeine Absicht und sind unabhängig.</span><span class="sxs-lookup"><span data-stu-id="ab508-109">Operations within a transaction usually share a common intent and are interdependent.</span></span> <span data-ttu-id="ab508-110">Wenn nur eine Teilmenge dieser Vorgänge durchgeführt wird, könnte das System die allgemeine Absicht der Transaktion kompromittieren.</span><span class="sxs-lookup"><span data-stu-id="ab508-110">By performing only a subset of these operations, the system could compromise the overall intent of the transaction.</span></span> <span data-ttu-id="ab508-111">Atomicity eliminiert nicht nur die Möglichkeit, nur eine Teilmenge der Vorgänge zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ab508-111">Atomicity eliminates the chance of processing only a subset of operations.</span></span>

</dd> <dt>

<span data-ttu-id="ab508-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Sten</span><span class="sxs-lookup"><span data-stu-id="ab508-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Consistent</span></span>
</dt> <dd>

<span data-ttu-id="ab508-113">Eine Transaktion muss die Konsistenz der Daten beibehalten und einen konsistenten Zustand von Daten in einen anderen konsistenten Zustand von Daten umwandeln.</span><span class="sxs-lookup"><span data-stu-id="ab508-113">A transaction must preserve the consistency of data, transforming one consistent state of data into another consistent state of data.</span></span> <span data-ttu-id="ab508-114">Ein Großteil der Verantwortung für die Aufrechterhaltung der Konsistenz fällt dem Anwendungsentwickler.</span><span class="sxs-lookup"><span data-stu-id="ab508-114">Much of the responsibility for maintaining consistency falls to the application developer.</span></span>

</dd> <dt>

<span data-ttu-id="ab508-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolation</span><span class="sxs-lookup"><span data-stu-id="ab508-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolated</span></span>
</dt> <dd>

<span data-ttu-id="ab508-116">Eine Transaktion muss eine Isolationseinheit sein, was bedeutet, dass sich gleichzeitige Transaktionen so verhalten sollten, als ob es sich um die einzige Transaktion handelt, die im System ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab508-116">A transaction must be a unit of isolation, which means that concurrent transactions should behave as if each were the only transaction running in the system.</span></span> <span data-ttu-id="ab508-117">Da die Anzahl gleichzeitiger Transaktionen durch einen hohen Grad an Isolation eingeschränkt werden kann, verringern einige Anwendungen die Isolationsstufe in Exchange, um einen besseren Durchsatz zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="ab508-117">Because a high degree of isolation can limit the number of concurrent transactions, some applications reduce the isolation level in exchange for better throughput.</span></span> <span data-ttu-id="ab508-118">Weitere Informationen finden Sie unter [Konfigurieren von Transaktions Isolations Stufen](configuring-transaction-isolation-levels.md) .</span><span class="sxs-lookup"><span data-stu-id="ab508-118">See [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="ab508-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Bar</span><span class="sxs-lookup"><span data-stu-id="ab508-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable</span></span>
</dt> <dd>

<span data-ttu-id="ab508-120">Eine Transaktion muss wiederherstellbar sein und muss daher über Dauerhaftigkeit verfügen.</span><span class="sxs-lookup"><span data-stu-id="ab508-120">A transaction must be recoverable and therefore must have durability.</span></span> <span data-ttu-id="ab508-121">Wenn für eine Transaktion ein Commit ausgeführt wird, gewährleistet das System, dass die Updates dauerhaft bleiben können, auch wenn der Computer unmittelbar nach dem Commit abstürzt.</span><span class="sxs-lookup"><span data-stu-id="ab508-121">If a transaction commits, the system guarantees that its updates can persist even if the computer crashes immediately after the commit.</span></span> <span data-ttu-id="ab508-122">Die spezialisierte Protokollierung ermöglicht es dem Neustart des Systems, nicht abgeschlossene Vorgänge abzuschließen, die für die Transaktion erforderlich sind, sodass die Transaktion dauerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="ab508-122">Specialized logging allows the system's restart procedure to complete unfinished operations required by the transaction, making the transaction durable.</span></span>

</dd> </dl>

 

 



