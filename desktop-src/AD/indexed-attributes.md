---
title: Indizierte Attribute (AD DS)
description: Attribute können indiziert werden. Das Indizieren eines Attributs kann die Leistung von Abfragen für dieses Attribut verbessern.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Indizierte Attribute ad
- Attribute ad, indiziert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106341919"
---
# <a name="indexed-attributes-ad-ds"></a><span data-ttu-id="f3305-106">Indizierte Attribute (AD DS)</span><span class="sxs-lookup"><span data-stu-id="f3305-106">Indexed Attributes (AD DS)</span></span>

<span data-ttu-id="f3305-107">Attribute können indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f3305-107">Attributes may be indexed.</span></span> <span data-ttu-id="f3305-108">Das Indizieren eines Attributs kann die Leistung von Abfragen für dieses Attribut verbessern.</span><span class="sxs-lookup"><span data-stu-id="f3305-108">Indexing an attribute can improve the performance of queries for that attribute.</span></span>

<span data-ttu-id="f3305-109">Attribute werden indiziert, wenn für das [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) -Attribut in der Schema Definition des Attributs das am wenigsten bedeutende Bit auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f3305-109">An attributes is indexed when the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute in the attribute's schema definition has the least significant bit set to 1.</span></span> <span data-ttu-id="f3305-110">Wenn Sie das am wenigsten bedeutende Bit der **searchFlags** -Attribut Schema Definition auf 1 festlegen, wird dynamisch ein Index erstellt.</span><span class="sxs-lookup"><span data-stu-id="f3305-110">Setting the least significant bit of the **searchFlags** attribute schema definition to 1 will dynamically build an index.</span></span> <span data-ttu-id="f3305-111">Wenn Sie das am wenigsten bedeutende Bit der **searchFlags** -Attribut Schema Definition auf 0 festlegen, wird der Index für das Attribut entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3305-111">Setting the least significant bit of the **searchFlags** attribute schema definition to 0 will cause the index for the attribute to be removed.</span></span> <span data-ttu-id="f3305-112">Der Index wird automatisch von einem Hintergrund Thread auf dem Domänen Controller erstellt.</span><span class="sxs-lookup"><span data-stu-id="f3305-112">The index will be built automatically by a background thread on the domain controller.</span></span>

<span data-ttu-id="f3305-113">Im Idealfall sollten indizierte Attribute einen Einzelwert mit stark eindeutigen Werten aufweisen, die gleichmäßig auf den Satz von Instanzen verteilt sind.</span><span class="sxs-lookup"><span data-stu-id="f3305-113">Ideally, indexed attributes should be single valued with highly unique values evenly distributed across the set of instances.</span></span> <span data-ttu-id="f3305-114">Weniger eindeutig die Werte eines Attributs sind, desto weniger effektiv ist der Index.</span><span class="sxs-lookup"><span data-stu-id="f3305-114">The less unique the values of an attribute are, the less effective the index will be.</span></span>

<span data-ttu-id="f3305-115">Mehrwertige Attribute können ebenfalls indiziert werden, aber die Kosten für das Erstellen des Indexes für ein mehr wertiges Attribut sind im Hinblick auf Speicher, Update und Suchzeit größer.</span><span class="sxs-lookup"><span data-stu-id="f3305-115">Multi-valued attributes can also be indexed, but the cost to build the index for a multi-valued attribute is larger in terms of storage, update, and search time.</span></span> <span data-ttu-id="f3305-116">Die Eindeutigkeits Anforderung für eine mehrwertige Eigenschaft ist identisch mit der für eine einwertige Eigenschaft – je größer die Werte sind, desto effektiver ist der Index.</span><span class="sxs-lookup"><span data-stu-id="f3305-116">The uniqueness requirement for a multi-valued property is the same as that for a single-valued property—the more unique the values are the more effective the index.</span></span>

<span data-ttu-id="f3305-117">Die mehr indizierten Attribute, die eine Klasse besitzt, desto mehr Zeit ist erforderlich, um neue Instanzen der-Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3305-117">The more indexed attributes a class has, the more time is required to create new instances of the class.</span></span>

<span data-ttu-id="f3305-118">Indizes gelten für Attribute, nicht für Klassen.</span><span class="sxs-lookup"><span data-stu-id="f3305-118">Indexes apply to attributes, not to classes.</span></span> <span data-ttu-id="f3305-119">Das heißt, wenn ein Attribut als indiziert gekennzeichnet ist, werden alle Instanzen des Attributs dem Index hinzugefügt, nicht nur die Instanzen, die Mitglieder einer bestimmten Klasse sind.</span><span class="sxs-lookup"><span data-stu-id="f3305-119">That is, when an attribute is marked as indexed, all instances of the attribute are added to the index, not just the instances that are members of a particular class.</span></span>

<span data-ttu-id="f3305-120">Legen Sie den folgenden Registrierungs Wert auf einem Domänen Controller auf 4 fest, um zu überprüfen, ob ein Server einen Index für die Verarbeitung einer Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3305-120">To verify that a server is using an index to process a query, set the following registry value on a domain controller to 4.</span></span> <span data-ttu-id="f3305-121">Führen Sie dann eine Abfrage auf diesem Domänen Controller aus, und suchen Sie im Verzeichnis Ereignisprotokoll nach Daten zu den Indizes, die zum Verarbeiten der Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3305-121">Then perform a query on that domain controller and look in the directory event log for data about the indexes, if any, used to process the query.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

<span data-ttu-id="f3305-122">Weitere Informationen zu anderen Bits in der [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) -Eigenschaft finden Sie unter [Merkmale von Attributen](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="f3305-122">For more information about other bits in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) property, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

 

 