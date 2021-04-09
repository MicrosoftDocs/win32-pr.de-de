---
description: Sammeln von Partitions Metriken
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Sammeln von Partitions Metriken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126362"
---
# <a name="collecting-partition-metrics"></a><span data-ttu-id="c6693-103">Sammeln von Partitions Metriken</span><span class="sxs-lookup"><span data-stu-id="c6693-103">Collecting Partition Metrics</span></span>

<span data-ttu-id="c6693-104">In einigen Fällen möchte eine Organisation möglicherweise Informationen zur Verwendung der com+-Anwendung für die Überwachung, Kapazitätsplanung und Ressourcen Führung erfassen.</span><span class="sxs-lookup"><span data-stu-id="c6693-104">In some cases, an organization might want to collect information on COM+ application use for the purposes of monitoring, capacity planning, and resource accounting.</span></span>

<span data-ttu-id="c6693-105">Beispielsweise kann ein Anwendungs Dienstanbieter (ASP) einen Kunden für die Ressourcennutzung berechnen.</span><span class="sxs-lookup"><span data-stu-id="c6693-105">For example, an application service provider (ASP) might want to charge a customer for its resource usage.</span></span> <span data-ttu-id="c6693-106">Zu diesem Zweck können Sie mit com+ Ereignis-und metrikinformationen auf Partitions Basis erfassen.</span><span class="sxs-lookup"><span data-stu-id="c6693-106">To do this, COM+ allows you to collect event and metrics information on a per-partition basis.</span></span>

<span data-ttu-id="c6693-107">Die Möglichkeit, diese Informationen für eine bestimmte Partition zu erfassen, besteht darin, für jede com+-Instrumentations Schnittstelle das Partitions-ID-Element in der Standard Ereignis Struktur anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c6693-107">The way to collect this information for a specific partition is by specifying, for each COM+ instrumentation interface, the partition ID member within the standard event structure.</span></span> <span data-ttu-id="c6693-108">Die Ereignis Struktur ist der erste Wert einer com+-Instrumentations Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c6693-108">The event structure is the first value of a COM+ instrumentation interface.</span></span> <span data-ttu-id="c6693-109">Weitere Informationen finden Sie unter [com+-Instrumentierungs Schnittstellen](com--instrumentation-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c6693-109">For more information, see [COM+ Instrumentation Interfaces](com--instrumentation-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6693-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6693-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6693-111">Konfigurieren des Partitions Caches</span><span class="sxs-lookup"><span data-stu-id="c6693-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="c6693-112">Gruppieren von Anwendungen in Partitionen</span><span class="sxs-lookup"><span data-stu-id="c6693-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="c6693-113">Verwalten von lokalen Partitionen</span><span class="sxs-lookup"><span data-stu-id="c6693-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="c6693-114">Verwalten von Partitionen in Active Directory</span><span class="sxs-lookup"><span data-stu-id="c6693-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="c6693-115">Festlegen von Administratorrechten für eine Partition</span><span class="sxs-lookup"><span data-stu-id="c6693-115">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



