---
description: Aufgaben für COM+-Transaktionen
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Aufgaben für COM+-Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127153"
---
# <a name="com-transactions-tasks"></a><span data-ttu-id="8bddb-103">Aufgaben für COM+-Transaktionen</span><span class="sxs-lookup"><span data-stu-id="8bddb-103">COM+ Transactions Tasks</span></span>

<span data-ttu-id="8bddb-104">Die automatische Transaktionsverarbeitung in com+ ermöglicht es Ihnen, eine produktivere Entwicklungszeit beim Erstellen und Konfigurieren von Objekten auszugeben, die an automatischen Transaktionen teilnehmen sollen. es gibt jedoch einige Programmieraufgaben, die Sie ausführen können, um das Transaktionsverhalten an Ihre Anwendungsanforderungen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="8bddb-104">While automatic transaction processing in COM+ allows you to spend more productive development time in creating and configuring objects that you want to participate in automatic transactions, there are some programming tasks you can perform to tailor transaction behavior to your application requirements.</span></span>

<span data-ttu-id="8bddb-105">In den folgenden Themen werden bestimmte Programmier Optionen im Zusammenhang mit der Transaktionsverarbeitung erörtert.</span><span class="sxs-lookup"><span data-stu-id="8bddb-105">The following topics discuss specific programming options related to transaction processing.</span></span>



| <span data-ttu-id="8bddb-106">Thema</span><span class="sxs-lookup"><span data-stu-id="8bddb-106">Topic</span></span>                                                                                             | <span data-ttu-id="8bddb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bddb-107">Description</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bddb-108">Festlegen des Transaktions Attributs</span><span class="sxs-lookup"><span data-stu-id="8bddb-108">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)<br/>             | <span data-ttu-id="8bddb-109">Beschreibt, wie Transaktions Attributwerte für die Transaktions Objekte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8bddb-109">Describes how to set transaction attribute values for your transaction objects.</span></span><br/>         |
| [<span data-ttu-id="8bddb-110">Festlegen der Transaktionsisolationsstufe</span><span class="sxs-lookup"><span data-stu-id="8bddb-110">Setting the Transaction Isolation Level</span></span>](setting-the-transaction-isolation-level.md)<br/> | <span data-ttu-id="8bddb-111">Beschreibt, wie die Transaktions Isolations Stufen für die Transaktions Objekte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8bddb-111">Describes how to set the transaction isolation levels for your transaction objects.</span></span><br/>     |
| [<span data-ttu-id="8bddb-112">Festlegen des Transaktions Timeouts</span><span class="sxs-lookup"><span data-stu-id="8bddb-112">Setting the Transaction Time-Out</span></span>](setting-the-transaction-time-out.md)<br/>               | <span data-ttu-id="8bddb-113">Beschreibt, wie Timeout Intervalle für Ihre Transaktionen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8bddb-113">Describes how to set time-out intervals for your transactions.</span></span><br/>                          |
| [<span data-ttu-id="8bddb-114">Festlegen der konsistenten und done-Flags</span><span class="sxs-lookup"><span data-stu-id="8bddb-114">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)<br/>     | <span data-ttu-id="8bddb-115">Zeigt, wie die konsistenten und done-Flags verwendet werden, um das Ergebnis einer Transaktion zu steuern.</span><span class="sxs-lookup"><span data-stu-id="8bddb-115">Shows how to use the consistent and done flags to control the outcome of a transaction.</span></span><br/> |
| [<span data-ttu-id="8bddb-116">Erstellen von BYOT-Objekten</span><span class="sxs-lookup"><span data-stu-id="8bddb-116">Creating BYOT Objects</span></span>](creating-byot-objects.md)<br/>                                     | <span data-ttu-id="8bddb-117">Beschreibt, wie Objekte erstellt werden, sodass Sie Ihre eigene Transaktion (BYOT) einbringen können.</span><span class="sxs-lookup"><span data-stu-id="8bddb-117">Describes how to create objects so you can Bring Your Own Transaction (BYOT).</span></span><br/>           |



 

> [!Note]  
> <span data-ttu-id="8bddb-118">Als allgemeine Regel gilt, dass alle Komponenten, die einen persistenten Zustand aktualisieren, Transaktionen unterstützen sollten.</span><span class="sxs-lookup"><span data-stu-id="8bddb-118">As a general rule, any component that updates persistent state should support transactions.</span></span> <span data-ttu-id="8bddb-119">Komponenten, die die Vorgänge von zwei oder mehr Objekten in einer einzigen Aufgabe kombinieren, sollten Transaktionen verwenden, um die Fehlerwiederherstellung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="8bddb-119">Components that combine the operations of two or more objects into a single task should use transactions to simplify error recovery.</span></span> <span data-ttu-id="8bddb-120">Zum Freigeben von Ressourcen, wie z. b. Datenbankverbindungen, sollten Transaktionen in com+ so kurz sein, wie Sie Sie vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="8bddb-120">Also, to release resources, such as database connections, transactions in COM+ should be as short as you can make them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8bddb-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8bddb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bddb-122">Konzepte der com+-Transaktionen</span><span class="sxs-lookup"><span data-stu-id="8bddb-122">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)
</dt> </dl>

 

 




