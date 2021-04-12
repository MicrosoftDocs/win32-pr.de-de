---
description: Com+-Transaktionen
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Com+-Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393133"
---
# <a name="com-transactions"></a><span data-ttu-id="2703d-103">Com+-Transaktionen</span><span class="sxs-lookup"><span data-stu-id="2703d-103">COM+ Transactions</span></span>

<span data-ttu-id="2703d-104">Wenn Sie ein Buch von einem Online Buchhandel kaufen, verwenden Sie eine Kreditkarte, um Geld für ein Buch zu kaufen.</span><span class="sxs-lookup"><span data-stu-id="2703d-104">When you purchase a book from an online bookstore, you use a credit card to trade money for a book.</span></span> <span data-ttu-id="2703d-105">Nachdem Sie Ihre Bestellung eingereicht haben, wird durch eine Reihe verwandter Vorgänge (Überprüfung der Kreditkarte, Überprüfung der Bestands Verfügbarkeit usw.) sichergestellt, dass Sie das Buch erhalten und dass der Buchhandel Ihr Geld erhält.</span><span class="sxs-lookup"><span data-stu-id="2703d-105">After you submit your order, a series of related operations (validation of your credit card, verification of inventory availability, and so forth) ensures that you get the book and that the bookstore gets your money.</span></span> <span data-ttu-id="2703d-106">Wenn ein einzelner Vorgang in der Reihe während des Austauschs fehlschlägt, schlägt der gesamte Austausch fehl.</span><span class="sxs-lookup"><span data-stu-id="2703d-106">If a single operation in the series fails during the exchange, the entire exchange fails.</span></span> <span data-ttu-id="2703d-107">Sie erhalten das Buch nicht, und der Buchhandel erhält nicht Ihr Geld.</span><span class="sxs-lookup"><span data-stu-id="2703d-107">You do not get the book, and the bookstore does not get your money.</span></span>

<span data-ttu-id="2703d-108">Die Technologie, die für die ausgeglichene und vorhersagbare Online Verarbeitung zuständig ist, wird als *Transaktionsverarbeitung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2703d-108">The technology responsible for making this online exchange balanced and predictable is called *transaction processing*.</span></span> <span data-ttu-id="2703d-109">Eine *Transaktion* ist Programm gesteuert eine Arbeitseinheit, in der eine Reihe von Vorgängen stattfinden.</span><span class="sxs-lookup"><span data-stu-id="2703d-109">Programmatically, a *transaction* is a unit of work in which a series of operations occur.</span></span> <span data-ttu-id="2703d-110">Com+ verwendet programmgesteuerte Transaktionen, um sicherzustellen, dass Ressourcen nicht dauerhaft aktualisiert werden, es sei denn, alle Vorgänge innerhalb der Transaktion werden erfolgreich abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="2703d-110">COM+ uses programmatic transactions to ensure that resources are not permanently updated unless all operations within the transaction complete successfully.</span></span> <span data-ttu-id="2703d-111">Durch das Binden eines Satzes verwandter Vorgänge in einer com+-Transaktion, die entweder vollständig erfolgreich oder vollständig fehlschlägt, können Sie die Fehlerwiederherstellung erheblich vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="2703d-111">By binding a set of related operations together in a COM+ transaction that either completely succeeds or completely fails, you can vastly simplify error recovery.</span></span>

<span data-ttu-id="2703d-112">In den folgenden Themen wird die allgemeine Transaktions Verarbeitungs Theorie vorgestellt, eine genauere Betrachtung der Transaktionen in com+ und praktische Tipps zum Schreiben von Transaktions Komponenten bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2703d-112">The following topics introduce general transaction processing theory, provide a closer look at transactions in COM+, and present practical tips for writing transactional components.</span></span>



| <span data-ttu-id="2703d-113">Thema</span><span class="sxs-lookup"><span data-stu-id="2703d-113">Topic</span></span>                                                                   | <span data-ttu-id="2703d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2703d-114">Description</span></span>                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="2703d-115">Konzepte der com+-Transaktionen</span><span class="sxs-lookup"><span data-stu-id="2703d-115">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)<br/> | <span data-ttu-id="2703d-116">Stellt grundlegende Begriffe und Konzepte dar.</span><span class="sxs-lookup"><span data-stu-id="2703d-116">Presents basic terms and concepts.</span></span><br/>                                  |
| [<span data-ttu-id="2703d-117">Aufgaben für COM+-Transaktionen</span><span class="sxs-lookup"><span data-stu-id="2703d-117">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)<br/>       | <span data-ttu-id="2703d-118">Bietet praktische Informationen zum Schreiben von transaktionalen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="2703d-118">Provides practical information on writing transactional components.</span></span><br/> |



 

 

 




