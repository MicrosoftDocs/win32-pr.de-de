---
description: Synchronisierungs Werte können automatisch durch die Konfiguration anderer Eigenschaften, z. b. Transaktions Anforderungen und JIT-Aktivierung (Just-in-Time), festgelegt oder eingeschränkt werden.
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Synchronisierungs Abhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860968"
---
# <a name="synchronization-dependencies"></a><span data-ttu-id="8f5b1-103">Synchronisierungs Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="8f5b1-103">Synchronization Dependencies</span></span>

<span data-ttu-id="8f5b1-104">Synchronisierungs Werte können automatisch durch die Konfiguration anderer Eigenschaften, z. b. Transaktions Anforderungen und JIT-Aktivierung (Just-in-Time), festgelegt oder eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="8f5b1-104">Synchronization values can be automatically determined or constrained by the configuration of other properties, such as transactional requirements and just-in-time (JIT) activation.</span></span> <span data-ttu-id="8f5b1-105">Beispielsweise erzwingt com+ die Synchronisierung sowohl für transaktionale als auch für JIT-aktivierte Komponenten.</span><span class="sxs-lookup"><span data-stu-id="8f5b1-105">For example, COM+ enforces synchronization both for transactional and for JIT-activated components.</span></span>

<span data-ttu-id="8f5b1-106">Diese Abhängigkeiten sind vorhanden, da Komponenten, die JIT-aktiviert sind oder an Transaktionen teilnehmen, ordnungsgemäß Isolation und Parallelitäts Verhalten aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="8f5b1-106">These dependencies exist because components that are JIT-activated or participating in transactions must have proper isolation and concurrency behavior.</span></span> <span data-ttu-id="8f5b1-107">Daher erfordert com+, dass der Zugriff auf diese Komponenten durch erzwingen der Synchronisierung serialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="8f5b1-107">Therefore, COM+ requires that access to these components be serialized by enforcing synchronization.</span></span> <span data-ttu-id="8f5b1-108">(Ausführliche Informationen zu diesen Abhängigkeiten finden Sie unter [com+ Just-in-Time-Aktivierung](com--just-in-time-activation.md).)</span><span class="sxs-lookup"><span data-stu-id="8f5b1-108">(For details on these dependencies, see [COM+ Just-in-Time Activation](com--just-in-time-activation.md).)</span></span>

<span data-ttu-id="8f5b1-109">In den folgenden Tabellen werden die Merkmale der com+-Synchronisierungs Attributwerte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f5b1-109">The following tables show the characteristics of the COM+ synchronization attribute values.</span></span>

### <a name="transactional-requirement"></a><span data-ttu-id="8f5b1-110">Transaktionale Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f5b1-110">Transactional requirement</span></span>



| <span data-ttu-id="8f5b1-111">Wenn Transaktionen auf festgelegt sind</span><span class="sxs-lookup"><span data-stu-id="8f5b1-111">When transactions are set to</span></span> | <span data-ttu-id="8f5b1-112">Die Synchronisierung kann auf festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="8f5b1-112">Synchronization can be set to</span></span>                    |
|------------------------------|--------------------------------------------------|
| <span data-ttu-id="8f5b1-113">Disabled</span><span class="sxs-lookup"><span data-stu-id="8f5b1-113">Disabled</span></span><br/>          | <span data-ttu-id="8f5b1-114">Alles, abhängig von der JIT-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="8f5b1-114">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="8f5b1-115">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8f5b1-115">Not Supported</span></span><br/>     | <span data-ttu-id="8f5b1-116">Alles, abhängig von der JIT-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="8f5b1-116">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="8f5b1-117">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="8f5b1-117">Supported</span></span><br/>         | <span data-ttu-id="8f5b1-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8f5b1-118">Required</span></span><br/>                              |
| <span data-ttu-id="8f5b1-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8f5b1-119">Required</span></span><br/>          | <span data-ttu-id="8f5b1-120">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8f5b1-120">Required</span></span><br/>                              |
| <span data-ttu-id="8f5b1-121">Requires New</span><span class="sxs-lookup"><span data-stu-id="8f5b1-121">Requires New</span></span><br/>      | <span data-ttu-id="8f5b1-122">Erforderlich oder erfordert neu</span><span class="sxs-lookup"><span data-stu-id="8f5b1-122">Required or Requires New</span></span><br/>              |



 

### <a name="jit-activation"></a><span data-ttu-id="8f5b1-123">JIT-Aktivierung</span><span class="sxs-lookup"><span data-stu-id="8f5b1-123">JIT Activation</span></span>



| <span data-ttu-id="8f5b1-124">Wenn die JIT-Aktivierung auf festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="8f5b1-124">When JIT Activation is set to</span></span> | <span data-ttu-id="8f5b1-125">Die Synchronisierung kann auf festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="8f5b1-125">Synchronization can be set to</span></span>       |
|-------------------------------|-------------------------------------|
| <span data-ttu-id="8f5b1-126">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="8f5b1-126">Enabled</span></span><br/>            | <span data-ttu-id="8f5b1-127">Erforderlich oder erfordert neu</span><span class="sxs-lookup"><span data-stu-id="8f5b1-127">Required or Requires New</span></span><br/> |
| <span data-ttu-id="8f5b1-128">Disabled</span><span class="sxs-lookup"><span data-stu-id="8f5b1-128">Disabled</span></span><br/>           | <span data-ttu-id="8f5b1-129">Dagegen</span><span class="sxs-lookup"><span data-stu-id="8f5b1-129">Anything</span></span><br/>                 |



 

<span data-ttu-id="8f5b1-130">Weitere Details dazu, wie sich die Transaktions-, JIT-Aktivierungs-und Synchronisierungs Attribute einander Verhalten, finden Sie unter [Konfigurieren von Transaktionen](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="8f5b1-130">For more detail about how transaction, JIT Activation, and Synchronization attributes behave together, see [Configuring Transactions](configuring-transactions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f5b1-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f5b1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f5b1-132">Festlegen des Synchronisierungs Attributs</span><span class="sxs-lookup"><span data-stu-id="8f5b1-132">Setting the Synchronization Attribute</span></span>](setting-the-synchronization-attribute.md)
</dt> <dt>

[<span data-ttu-id="8f5b1-133">Werte der Synchronisierungs Attribute</span><span class="sxs-lookup"><span data-stu-id="8f5b1-133">Synchronization Attribute Values</span></span>](synchronization-attribute-values.md)
</dt> </dl>

 

 




