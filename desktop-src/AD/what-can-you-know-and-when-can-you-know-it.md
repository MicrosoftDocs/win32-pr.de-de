---
title: Was Sie wissen und wann Sie es wissen können
description: Anwendungen, die sich auf von der Latenz verursachende Zustände unterliegen, müssen Problem Zustände erkennen und entsprechende Maßnahmen ergreifen.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342240"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a><span data-ttu-id="9a72d-103">Was ist Ihnen bekannt, und wann können Sie Sie wissen?</span><span class="sxs-lookup"><span data-stu-id="9a72d-103">What Can You Know, and When Can You Know It?</span></span>

<span data-ttu-id="9a72d-104">Anwendungen, die sich auf von der Latenz verursachende Zustände unterliegen, müssen Problem Zustände erkennen und entsprechende Maßnahmen ergreifen.</span><span class="sxs-lookup"><span data-stu-id="9a72d-104">Applications that are sensitive to latency-induced states must recognize problem states and take appropriate action.</span></span> <span data-ttu-id="9a72d-105">Es gibt zwei Problem Zustände: Versions Schiefe und partielle Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="9a72d-105">There are two problem states: version skew and partial update.</span></span> <span data-ttu-id="9a72d-106">Die Versions Neigung kann nicht erkannt werden, indem der Verzeichnisdienst untersucht wird (Beachten Sie, dass sich das Grundsatz verteilter Computing in der Ursache [Active Directory Domain Services dieses Replikations Modells](why-active-directory-domain-services-uses-this-replication-model.md)befindet).</span><span class="sxs-lookup"><span data-stu-id="9a72d-106">Version skew is not detectable by examining the Directory Service (remember the axiom of distributed computing stated in [Why Active Directory Domain Services Use This Replication Model](why-active-directory-domain-services-uses-this-replication-model.md)).</span></span> <span data-ttu-id="9a72d-107">Teil Updates können durch Hinzufügen von Metadaten zu den Objekten erkannt werden, aus denen sich der verknüpfte Satz zusammensetzt.</span><span class="sxs-lookup"><span data-stu-id="9a72d-107">Partial update can be detected by adding metadata to the objects that compose the related set.</span></span> <span data-ttu-id="9a72d-108">Vorschläge für solche Metadaten werden in den nachfolgenden Abschnitten dieses Dokuments angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9a72d-108">Suggestions for such metadata appear in subsequent sections of this document.</span></span> <span data-ttu-id="9a72d-109">Es gibt Strategien zur Vermeidung von Anwendungen, mit denen die Wahrscheinlichkeit von Versions Schiefe und partiellem Update reduziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9a72d-109">There are avoidance strategies applications can take to reduce the possibility of both version skew and partial update.</span></span> <span data-ttu-id="9a72d-110">Diese Strategien werden auch in den nachfolgenden Abschnitten dieses Dokuments erläutert.</span><span class="sxs-lookup"><span data-stu-id="9a72d-110">These strategies are also discussed in subsequent sections of this document.</span></span>

 

 




