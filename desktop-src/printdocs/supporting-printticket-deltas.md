---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Unterstützen von PrintTicket-Delta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730c8d32d881dd30a6ab57b88d8fc1dfa87eee7a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106351861"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="bbc4d-104">Unterstützen von PrintTicket-Delta</span><span class="sxs-lookup"><span data-stu-id="bbc4d-104">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="bbc4d-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-105">This topic is not current.</span></span> <span data-ttu-id="bbc4d-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bbc4d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bbc4d-107">Die PrintTicket-Anbieter Schnittstelle verfügt über Methoden, die verwendet werden können, um inkrementelle Änderungen an einem vorhandenen PrintTicket vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-107">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="bbc4d-108">Die inkrementellen PrintTicket-Änderungen können in einem PrintTicket-Teil angegeben werden, das als PrintTicket-Delta bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-108">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="bbc4d-109">Ein überarbeitetes PrintTicket wird durch Zusammenführen eines PrintTicket-Deltas mit einem vorhandenen PrintTicket erstellt.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-109">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="bbc4d-110">Weitere Informationen zu Methoden, die PrintTicket-Delta betreffen, finden Sie im bevorstehenden Dokument der PrintTicket-Anbieter Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-110">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="bbc4d-111">Wenn ein PrintTicket-Delta verarbeitet wird, müssen die folgenden Schritte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-111">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="bbc4d-112">Identifizieren Sie Feature-oder parameterinit-Instanzen, die sowohl für das vorhandene PrintTicket (das PrintTicket-Ziel) als auch für das PrintTicket-Delta gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-112">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="bbc4d-113">Ersetzen Sie für jedes Feature, das sowohl für das PrintTicket-Ziel als auch für das PrintTicket-Delta üblich ist, die Funktion im PrintTicket-Ziel durch die entsprechende Funktion im PrintTicket-Delta.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-113">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="bbc4d-114">Ersetzen Sie für jede parameterinit, die sowohl für das PrintTicket-Ziel als auch für das PrintTicket-Delta üblich ist, den Parameter "parameterinit" im PrintTicket-Ziel durch die entsprechende parameterinit im PrintTicket-Delta.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-114">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="bbc4d-115">Kopieren Sie alle verbleibenden Feature-und parameterinit-Instanzen im PrintTicket-Delta in das PrintTicket-Ziel.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-115">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="bbc4d-116">Wenn der Konflikt Auflösungs Algorithmus das Festlegen von Prioritäten im PrintTicket selbst ermöglicht, können Sie die Prioritäten der Funktionen und parameterinit-Instanzen im PrintTicket-Delta erhöhen.</span><span class="sxs-lookup"><span data-stu-id="bbc4d-116">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="bbc4d-117">Führen Sie die PrintTicket-Überprüfung wie in der [PrintTicket-Überprüfungs Checkliste](printticket-validation-checklist.md)beschrieben</span><span class="sxs-lookup"><span data-stu-id="bbc4d-117">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbc4d-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbc4d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbc4d-119">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="bbc4d-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



