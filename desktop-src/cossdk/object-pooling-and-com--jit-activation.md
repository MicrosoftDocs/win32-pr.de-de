---
description: Die com+-JIT-Aktivierung stellt im Wesentlichen einen Kompromiss zwischen gierigen Clients und gierigen Servern dar, um eine optimale Leistung zu erzielen. Clients erhalten Objekt Verweise, während Server die Speicherauslastung genauer verwalten können.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Objekt Pooling und com+-JIT-Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393222"
---
# <a name="object-pooling-and-com-jit-activation"></a><span data-ttu-id="8f5e6-104">Objekt Pooling und com+-JIT-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="8f5e6-104">Object Pooling and COM+ JIT Activation</span></span>

<span data-ttu-id="8f5e6-105">Die com+-JIT-Aktivierung stellt im Wesentlichen einen Kompromiss zwischen gierigen Clients und gierigen Servern dar, um eine optimale Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="8f5e6-105">COM+ JIT activation essentially strikes a compromise between greedy clients and greedy servers for the sake of getting optimal performance.</span></span> <span data-ttu-id="8f5e6-106">Clients erhalten Objekt Verweise, während Server die Speicherauslastung genauer verwalten können.</span><span class="sxs-lookup"><span data-stu-id="8f5e6-106">Clients get to keep object references, while servers can more closely manage memory utilization.</span></span>

<span data-ttu-id="8f5e6-107">Sie können dies mithilfe des [com+-Objekt Pooling](com--object-pooling.md)weiter verfeinern.</span><span class="sxs-lookup"><span data-stu-id="8f5e6-107">You can refine this further by using [COM+ Object Pooling](com--object-pooling.md).</span></span> <span data-ttu-id="8f5e6-108">Durch das Pooling von Objekten, die JIT-aktiviert sind, können Sie eine bestimmte Menge an Arbeitsspeicher für eine bestimmte Anzahl von Objekten im Arbeitsspeicher bereitstellen, die sofort wieder verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8f5e6-108">By pooling objects that are JIT activated, you can dedicate a certain amount of memory to hold a certain number of objects active in memory, ready for immediate reuse.</span></span> <span data-ttu-id="8f5e6-109">Dies ist am sinnvollsten, wenn Objekte zu erstellen sind, wie in dem Fall, in dem Sie mehrere Ressourcen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8f5e6-109">This makes the most sense when objects are expensive to create, as in the case where they hold multiple resources.</span></span>

<span data-ttu-id="8f5e6-110">Wenn Sie JIT-aktivierte Objekte auf diese Weise bündeln, können Sie die folgenden Vorteile erzielen:</span><span class="sxs-lookup"><span data-stu-id="8f5e6-110">Pooling JIT-activated objects in this manner, you can achieve the following benefits:</span></span>

-   <span data-ttu-id="8f5e6-111">Sehr beschleunigte Reaktivierungs Zeiten für Objekte.</span><span class="sxs-lookup"><span data-stu-id="8f5e6-111">Greatly accelerated object reactivation times.</span></span>
-   <span data-ttu-id="8f5e6-112">Wiederverwendung kostspieliger Ressourcen, die von den Objekten gehalten werden.</span><span class="sxs-lookup"><span data-stu-id="8f5e6-112">Reuse of any expensive resources the objects are holding.</span></span>
-   <span data-ttu-id="8f5e6-113">Genauere Steuerung der Arbeitsspeicher-und Ressourcenverwendung für die in einem Pool zusammengefassten Objekte.</span><span class="sxs-lookup"><span data-stu-id="8f5e6-113">More precise governing of memory and resource use for the pooled objects.</span></span>
-   <span data-ttu-id="8f5e6-114">Beibehaltung der administrativen Flexibilität, damit Ihre Anwendung skaliert werden kann, um verfügbare Ressourcen zu verwenden und sich an geänderte Leistungsanforderungen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="8f5e6-114">Retention of administrative flexibility so that your application can scale to use available resources and adapt to changing performance requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f5e6-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f5e6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f5e6-116">Konzepte für die Just-in-Time-Aktivierung in com+</span><span class="sxs-lookup"><span data-stu-id="8f5e6-116">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="8f5e6-117">Com+-Objekt Pooling</span><span class="sxs-lookup"><span data-stu-id="8f5e6-117">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="8f5e6-118">Aktivieren der JIT-Aktivierung für eine Komponente</span><span class="sxs-lookup"><span data-stu-id="8f5e6-118">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="8f5e6-119">Transaktionen und com+-JIT-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="8f5e6-119">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



