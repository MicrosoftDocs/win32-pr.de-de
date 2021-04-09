---
description: Transaktionen und com+-JIT-Aktivierung
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transaktionen und com+-JIT-Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861551"
---
# <a name="transactions-and-com-jit-activation"></a><span data-ttu-id="e9872-103">Transaktionen und com+-JIT-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="e9872-103">Transactions and COM+ JIT Activation</span></span>

<span data-ttu-id="e9872-104">Die com+-JIT-Aktivierung ist eng an automatische Transaktionen gebunden.</span><span class="sxs-lookup"><span data-stu-id="e9872-104">COM+ JIT Activation is closely bound to automatic transactions.</span></span> <span data-ttu-id="e9872-105">Wenn Sie eine Komponente so konfigurieren, dass eine Transaktion erforderlich ist oder eine neue Transaktion erforderlich ist, wird die JIT-Aktivierung ebenfalls automatisch aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e9872-105">When you configure a component so that it requires a transaction or requires a new transaction, JIT Activation is automatically enabled as well.</span></span> <span data-ttu-id="e9872-106">Die beiden Features funktionieren natürlich in Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e9872-106">The two features naturally work in conjunction.</span></span> <span data-ttu-id="e9872-107">Transaktionale, von JIT aktivierte Komponenten haben die folgenden Merkmale:</span><span class="sxs-lookup"><span data-stu-id="e9872-107">Transactional, JIT-activated components share the following characteristics:</span></span>

-   <span data-ttu-id="e9872-108">Zustands losigkeit.</span><span class="sxs-lookup"><span data-stu-id="e9872-108">Statelessness.</span></span> <span data-ttu-id="e9872-109">Der Zustand, der gegen die Transaktions Isolation verstoßen würde, wird nicht aufrechterhalten, und Sie würden den Zustand anhalten, der bei der Objekt-decoaktivierung verloren geht.</span><span class="sxs-lookup"><span data-stu-id="e9872-109">You would not hold state that would violate transaction isolation nor would you hold state that would be lost on object deactivation.</span></span>

-   <span data-ttu-id="e9872-110">Schnelle Verwendung.</span><span class="sxs-lookup"><span data-stu-id="e9872-110">Rapid use.</span></span> <span data-ttu-id="e9872-111">Das kanonische Verwendungs Muster für ein Objekt, das in einer automatischen Transaktion funktioniert, besteht darin, eine kleine Arbeitseinheit auszuführen, abzustimmen und zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e9872-111">The canonical use pattern for an object performing work in an automatic transaction is to do some small unit of work, vote, and exit.</span></span>

    > [!Note]  
    > <span data-ttu-id="e9872-112">Die Methoden, die Sie in com+-Transaktionen und Signal-doneness für die JIT-Aktivierung abstimmen, sind ebenfalls eng miteinander verbunden.</span><span class="sxs-lookup"><span data-stu-id="e9872-112">The ways that you vote in COM+ transactions and signal doneness for JIT Activation are also closely bound together.</span></span> <span data-ttu-id="e9872-113">Weitere Informationen finden Sie unter [Festlegen des done-Bits](setting-the-done-bit.md).</span><span class="sxs-lookup"><span data-stu-id="e9872-113">For more information, see [Setting the Done Bit](setting-the-done-bit.md).</span></span>

     

-   <span data-ttu-id="e9872-114">Wiederholte Verwendung.</span><span class="sxs-lookup"><span data-stu-id="e9872-114">Repeated use.</span></span> <span data-ttu-id="e9872-115">Wenn die Transaktionsarbeit ordnungsgemäß untergliedert ist, verwenden Clients immer wieder dieselben Objekte, um wenig atomarische Arbeiten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e9872-115">When transactional work is properly broken up, clients use the same objects over and over to perform little parcels of atomic work.</span></span>

-   <span data-ttu-id="e9872-116">Bei Commit oder Abbruch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e9872-116">Deactivated on commit or abort.</span></span> <span data-ttu-id="e9872-117">In com+ werden alle Objekte innerhalb der Transaktionsgrenze deaktiviert, wenn die Transaktion ausgeführt wird oder abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="e9872-117">In COM+, all objects within the transaction boundary are deactivated when the transaction commits or aborts.</span></span>

<span data-ttu-id="e9872-118">In Verbindung mit den com+-Transaktions Komponenten ist die JIT-Aktivierung eine große Leistungssteigerung, da der Kanal geöffnet bleibt, da Clients langlebige Verweise auf Transaktions Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9872-118">In conjunction with COM+ transactional components, JIT activation serves as a big performance enhancement by keeping the channel open as clients hold long-lived references to transactional objects.</span></span> <span data-ttu-id="e9872-119">Als weitere Verbesserungen können Sie festlegen, dass die Transaktions Objekte in den Pool eingereihlt werden, um die darin verwendeten Ressourcen wiederzuverwenden, die Reaktivierungs Zeit des Objekts zu beschleunigen und die Arbeitsspeicher Ressourcen für bestimmte Objekte genau zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e9872-119">As further enhancements, you can elect to pool the transactional objects to reuse the resources they hold, speed object reactivation time, and closely manage how you use memory resources for given objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9872-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9872-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9872-121">Konzepte für die Just-in-Time-Aktivierung in com+</span><span class="sxs-lookup"><span data-stu-id="e9872-121">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="e9872-122">Aktivieren der JIT-Aktivierung für eine Komponente</span><span class="sxs-lookup"><span data-stu-id="e9872-122">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="e9872-123">Objekt Pooling und com+-JIT-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="e9872-123">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



