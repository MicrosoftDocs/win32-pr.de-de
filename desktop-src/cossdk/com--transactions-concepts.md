---
description: Konzepte der com+-Transaktionen
ms.assetid: e2198514-c403-4b31-8c8c-0b1c83c4f936
title: Konzepte der com+-Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775537128aa0419d02ad3ab614a3ba2ec5eb5b2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127156"
---
# <a name="com-transactions-concepts"></a><span data-ttu-id="39161-103">Konzepte der com+-Transaktionen</span><span class="sxs-lookup"><span data-stu-id="39161-103">COM+ Transactions Concepts</span></span>

<span data-ttu-id="39161-104">Obwohl com+ viele der mühsamen Programmier Details verarbeitet, die mit der Transaktionsverarbeitung in Zusammenhang stehen, ist es hilfreich, wenn Sie Transaktionen in com+ programmieren müssen, um ein konzeptionelles Verständnis der Transaktions Theorie zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="39161-104">Although COM+ handles many of the tedious programming details associated with transaction processing, it is useful to have a conceptual understanding of transaction theory when you need to program transactions in COM+.</span></span>

<span data-ttu-id="39161-105">In den in der folgenden Tabelle beschriebenen Themen werden die Konzepte behandelt, die für die Transaktionsverarbeitung gelten.</span><span class="sxs-lookup"><span data-stu-id="39161-105">The topics described in the following table cover the concepts that apply to transaction processing.</span></span>



| <span data-ttu-id="39161-106">Thema</span><span class="sxs-lookup"><span data-stu-id="39161-106">Topic</span></span>                                                                                                                     | <span data-ttu-id="39161-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39161-107">Description</span></span>                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39161-108">ACID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="39161-108">ACID Properties</span></span>](acid-properties.md)<br/>                                                                         | <span data-ttu-id="39161-109">Beschreibt die atomarischen, konsistenten, isolierten und dauerhaften Eigenschaften von Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="39161-109">Describes the atomic, consistent, isolated, and durable properties of transactions.</span></span><br/>                                                                                              |
| [<span data-ttu-id="39161-110">Konfigurieren von Transaktionen</span><span class="sxs-lookup"><span data-stu-id="39161-110">Configuring Transactions</span></span>](configuring-transactions.md)<br/>                                                       | <span data-ttu-id="39161-111">Beschreibt die Transaktions Attributwerte, die Sie den-Komponenten zuweisen können, um zu bestimmen, welcher Grad an Transaktions Schutz erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="39161-111">Describes the transaction attribute values that you can assign to your components to determine the degree of transaction protection to be enforced.</span></span><br/>                              |
| [<span data-ttu-id="39161-112">Konfigurieren von Transaktions Isolations Stufen</span><span class="sxs-lookup"><span data-stu-id="39161-112">Configuring Transaction Isolation Levels</span></span>](configuring-transaction-isolation-levels.md)<br/>                       | <span data-ttu-id="39161-113">Beschreibt die Isolations Stufen, die Sie Ihren Transaktionen zuweisen können, sodass Sie die Parallelität abhängig von den Leistungs-und Skalierbarkeits Anforderungen erhöhen oder verringern können.</span><span class="sxs-lookup"><span data-stu-id="39161-113">Describes the isolation levels you can assign to your transactions, enabling you to increase or decrease concurrency depending on your performance and scalability requirements.</span></span><br/> |
| [<span data-ttu-id="39161-114">Verwalten von automatischen Transaktionen in com+</span><span class="sxs-lookup"><span data-stu-id="39161-114">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)<br/>                         | <span data-ttu-id="39161-115">Übersicht über den automatisierten Transaktionsprozess, der von com+ unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="39161-115">Overview of the automated transaction process supported by COM+.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="39161-116">Verwenden von nicht transaktionalen Komponenten in einer Transaktion</span><span class="sxs-lookup"><span data-stu-id="39161-116">Using Non-Transactional Components in a Transaction</span></span>](using-non-transactional-components-in-a-transaction.md)<br/> | <span data-ttu-id="39161-117">Beschreibt, wie nicht transaktionale Komponenten in einer Transaktion verwendet werden und wann Sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39161-117">Describes how to use non-transactional components in a transaction and when you would use them.</span></span><br/>                                                                                  |
| [<span data-ttu-id="39161-118">Bring Your Own Transaction (BYOT)</span><span class="sxs-lookup"><span data-stu-id="39161-118">Bring Your Own Transaction (BYOT)</span></span>](bring-your-own-transaction--byot-.md)<br/>                                     | <span data-ttu-id="39161-119">Beschreibt, wie eine Komponente eine externe Transaktion erben kann.</span><span class="sxs-lookup"><span data-stu-id="39161-119">Describes how to allow a component inherit an external transaction.</span></span><br/>                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="39161-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39161-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39161-121">Aufgaben für COM+-Transaktionen</span><span class="sxs-lookup"><span data-stu-id="39161-121">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)
</dt> </dl>

 

 




