---
description: Erfahren Sie mehr über die Unterstützung von PrintTicket-Deltas. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Unterstützen von PrintTicket Deltas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548779"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="97217-105">Unterstützen von PrintTicket Deltas</span><span class="sxs-lookup"><span data-stu-id="97217-105">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="97217-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="97217-106">This topic is not current.</span></span> <span data-ttu-id="97217-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="97217-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="97217-108">Die PrintTicket-Anbieterschnittstelle verfügt über Methoden, mit denen inkrementelle Änderungen an einem vorhandenen PrintTicket vorgenommen werden können.</span><span class="sxs-lookup"><span data-stu-id="97217-108">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="97217-109">Die inkrementellen PrintTicket-Änderungen können in einem partiellen PrintTicket angegeben werden, das als PrintTicket-Delta bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="97217-109">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="97217-110">Ein überarbeitetes PrintTicket wird erstellt, indem ein PrintTicket-Delta mit einem vorhandenen PrintTicket zusammengeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97217-110">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="97217-111">Weitere Informationen zu Methoden im Zusammenhang mit PrintTicket-Deltas finden Sie im bevorstehenden Dokument PrintTicket Provider Interface ( PrintTicket-Anbieterschnittstelle).</span><span class="sxs-lookup"><span data-stu-id="97217-111">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="97217-112">Wenn ein PrintTicket-Delta verarbeitet wird, müssen die folgenden Schritte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="97217-112">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="97217-113">Identifizieren Sie Feature- oder ParameterInit-Instanzen, die sowohl dem vorhandenen PrintTicket (dem PrintTicket-Ziel) als auch dem PrintTicket-Delta gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="97217-113">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="97217-114">Ersetzen Sie für jedes Feature, das sowohl dem PrintTicket-Ziel als auch dem PrintTicket-Delta gemeinsam ist, das Feature im PrintTicket-Ziel durch das entsprechende Feature im PrintTicket-Delta.</span><span class="sxs-lookup"><span data-stu-id="97217-114">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="97217-115">Ersetzen Sie für jeden ParameterInit, der sowohl für das PrintTicket-Ziel als auch für das PrintTicket-Delta gilt, die ParameterInit im PrintTicket-Ziel durch die entsprechende ParameterInit im PrintTicket-Delta.</span><span class="sxs-lookup"><span data-stu-id="97217-115">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="97217-116">Kopieren Sie alle verbleibenden Feature- und ParameterInit-Instanzen im PrintTicket-Delta auf das PrintTicket-Ziel.</span><span class="sxs-lookup"><span data-stu-id="97217-116">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="97217-117">Wenn Ihr Konfliktlösungsalgorithmus die Angabe von Prioritäten im PrintTicket selbst zulässt, können Sie die Prioritäten der Im PrintTicket-Delta benannten Feature- und ParameterInit-Instanzen erhöhen.</span><span class="sxs-lookup"><span data-stu-id="97217-117">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="97217-118">Führen Sie die PrintTicket-Überprüfung wie unter Prüfliste für [die PrintTicket-Überprüfung](printticket-validation-checklist.md)beschrieben durch.</span><span class="sxs-lookup"><span data-stu-id="97217-118">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="97217-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97217-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97217-120">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="97217-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



