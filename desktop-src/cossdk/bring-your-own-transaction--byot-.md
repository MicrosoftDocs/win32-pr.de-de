---
description: Bring Your Own Transaction (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Bring Your Own Transaction (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344618"
---
# <a name="bring-your-own-transaction-byot"></a><span data-ttu-id="945bc-103">Bring Your Own Transaction (BYOT)</span><span class="sxs-lookup"><span data-stu-id="945bc-103">Bring Your Own Transaction (BYOT)</span></span>

<span data-ttu-id="945bc-104">BYOT ermöglicht das Erstellen einer Komponente mit oder, um eine externe Transaktion zu erben.</span><span class="sxs-lookup"><span data-stu-id="945bc-104">BYOT allows a component to be created with or to inherit an external transaction.</span></span> <span data-ttu-id="945bc-105">Dies bedeutet, dass eine Komponente, die noch nicht über eine zugehörige Transaktion verfügt, eine Transaktion abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="945bc-105">That is, a component that does not already have an associated transaction can acquire a transaction.</span></span> <span data-ttu-id="945bc-106">Derzeit sind MTS-Transaktionen automatisch. ob eine Komponenteninstanz in einer Transaktion aktiv ist, wird zur Erstellungszeit bestimmt.</span><span class="sxs-lookup"><span data-stu-id="945bc-106">Currently, MTS transactions are automatic; whether a component instance lives in a transaction is determined at creation time.</span></span> <span data-ttu-id="945bc-107">Die Transaktions Attribute einer Komponente und deren Ersteller bestimmen, welche Transaktion mit einer bestimmten Instanz verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="945bc-107">The transactional attributes of a component and its creator determine what transaction is associated with a given instance.</span></span> <span data-ttu-id="945bc-108">In allen Fällen steuert MTS die Transaktions Lebensdauer.</span><span class="sxs-lookup"><span data-stu-id="945bc-108">In all cases, MTS controls transaction lifetimes.</span></span> <span data-ttu-id="945bc-109">Com+ erweitert dieses, um das Festlegen einer beliebigen bereits vorhandenen DTC-oder Tip-Transaktion als Transaktions Eigenschaft des Kontexts einer neuen Komponente zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="945bc-109">COM+ extends this to allow setting an arbitrary pre-existing DTC or TIP transaction as the transaction property of a new component's context.</span></span> <span data-ttu-id="945bc-110">Dadurch können konfigurierte Komponenten mit Transaktionen verknüpft werden, deren Lebensdauer durch einen TP-Monitor, OTS oder DBMS gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="945bc-110">This allows configured components to be associated with transactions whose lifetimes are controlled by a TP monitor, OTS, or DBMS.</span></span>

> [!Note]  
> <span data-ttu-id="945bc-111">BYOT-Transaktionen müssen mit Bedacht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="945bc-111">BYOT transactions must be used with caution.</span></span> <span data-ttu-id="945bc-112">In bestimmten Situationen können Sie zu einer Transaktion führen, die mehrere Synchronisierungs Domänen umfasst, d. –., Sie ermöglichen eine Parallelität mit einer Transaktion, wodurch eine Deadlockbedingung verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="945bc-112">In certain situations, they can result in a transaction spanning multiple synchronization domains—that is, they allow parallelism with a transaction, causing a deadlock condition.</span></span> <span data-ttu-id="945bc-113">Automatische Transaktionen und keine BYOT-Transaktionen sind das bevorzugte Programmiermodell für Writer von Geschäftskomponenten.</span><span class="sxs-lookup"><span data-stu-id="945bc-113">Automatic transactions, rather than BYOT transactions, are the preferred programming model for writers of business components.</span></span>

 

<span data-ttu-id="945bc-114">Die Schnittstellen für BYOT-Transaktionen umfassen die [**ikreatewithtransaktionex**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) -Schnittstelle und die [**ikreatewithtiptransaktionex**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="945bc-114">The interfaces for BYOT transactions include the [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) interface and the [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) interface.</span></span> <span data-ttu-id="945bc-115">Mit der **ikreatewithtransaktionex** -Schnittstelle wird ein Objekt erstellt, das in einer manuellen Transaktion eingetragen ist.</span><span class="sxs-lookup"><span data-stu-id="945bc-115">The **ICreateWithTransactionEx** interface creates an object that is enlisted within a manual transaction.</span></span> <span data-ttu-id="945bc-116">Mit der **ikreatewithtiptransaktionex** -Schnittstelle wird ein Objekt erstellt, das in einer manuellen Transaktion mit dem Tip (Transaction Internet Protocol) eingetragen ist.</span><span class="sxs-lookup"><span data-stu-id="945bc-116">The **ICreateWithTipTransactionEx** interface creates an object that is enlisted within a manual transaction using the Transaction Internet Protocol (TIP).</span></span>

## <a name="related-topics"></a><span data-ttu-id="945bc-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="945bc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="945bc-118">Erben von manuellen Transaktionen</span><span class="sxs-lookup"><span data-stu-id="945bc-118">Inheriting Manual Transactions</span></span>](inheriting-manual-transactions.md)
</dt> </dl>

 

 



