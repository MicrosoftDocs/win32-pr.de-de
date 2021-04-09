---
description: Die filecostaction initiiert dynamische costingof-Standard Installations Aktionen.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Filecost-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050635"
---
# <a name="filecost-action"></a><span data-ttu-id="e31e0-103">Filecost-Aktion</span><span class="sxs-lookup"><span data-stu-id="e31e0-103">FileCost Action</span></span>

<span data-ttu-id="e31e0-104">Mit filecostaction werden die dynamischen [*Kosten*](c-gly.md)der Standard Installations Aktionen initiiert.</span><span class="sxs-lookup"><span data-stu-id="e31e0-104">The FileCostaction initiates dynamic [*costing*](c-gly.md)of standard installation actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e31e0-105">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="e31e0-105">ActionData Messages</span></span>

<span data-ttu-id="e31e0-106">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e31e0-106">There are no ActionData messages.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e31e0-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="e31e0-107">Sequence Restrictions</span></span>

<span data-ttu-id="e31e0-108">Alle standardmäßigen oder [benutzerdefinierten Aktionen](custom-actions.md) , die die Kosten beeinflussen, sollten vor der [costinitialize](costinitialize-action.md) -Aktion sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="e31e0-108">Any standard or [custom actions](custom-actions.md) that affect costing should sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="e31e0-109">Wenden Sie die Aktion "filecost" direkt nach der Aktion "costinitialize" an.</span><span class="sxs-lookup"><span data-stu-id="e31e0-109">Call the FileCost action immediately following the CostInitialize action.</span></span> <span data-ttu-id="e31e0-110">Anschließend können Sie die Aktion " [costfinalize](costfinalize-action.md) " nach der Aktion "costinitialize" aufzurufen, um dem Installer alle abschließenden Kostenberechnungen über die [Komponenten](component-table.md) Tabelle zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="e31e0-110">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="e31e0-111">Die [costinitialize](costinitialize-action.md) -Aktion muss vor der filecost-Aktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e31e0-111">The [CostInitialize](costinitialize-action.md) action must be executed before the FileCost action.</span></span> <span data-ttu-id="e31e0-112">Das Installationsprogramm ermittelt dann die Speicherplatz Kosten jeder Datei in der [Datei](file-table.md) Tabelle pro Komponente (siehe [Komponenten Tabelle](component-table.md)) und übernimmt sowohl das volumeclustering als [](v-gly.md) auch das vorhanden sein vorhandener Dateien, die möglicherweise in das Konto überschrieben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e31e0-112">The installer then determines the disk-space cost of every file in the [File](file-table.md) table, on a per-component basis (See [Component Table](component-table.md)), taking both [*volume*](v-gly.md) clustering and the presence of existing files that may need to be overwritten into account.</span></span> <span data-ttu-id="e31e0-113">Alle Aktionen, die Speicherplatz belegen oder freigeben, werden ebenfalls berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e31e0-113">All actions that consume or release disk space are also considered.</span></span> <span data-ttu-id="e31e0-114">Wenn eine vorhandene Datei gefunden wird, wird eine Überprüfung der Dateiversion durchgeführt, um zu bestimmen, ob die neue Datei tatsächlich installiert werden muss oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e31e0-114">If an existing file is found, a file version check is performed to determine whether the new file actually needs to be installed or not.</span></span> <span data-ttu-id="e31e0-115">Wenn die vorhandene Datei dieselbe oder eine höhere Versionsnummer hat, wird die vorhandene Datei nicht überschrieben, und es fallen keine Kosten für den Speicherplatz an.</span><span class="sxs-lookup"><span data-stu-id="e31e0-115">If the existing file is of an equal or greater version number, the existing file is not overwritten and no disk-space cost is incurred.</span></span> <span data-ttu-id="e31e0-116">In allen Fällen verwendet das Installationsprogramm die Ergebnisse der Versionsnummern Überprüfung, um den Installationsstatus der einzelnen Dateien festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e31e0-116">In all cases, the installer uses the results of version number checking to set the installation state of each file.</span></span>

<span data-ttu-id="e31e0-117">Die filecost-Aktion initialisiert die Kostenberechnung mit TheInstaller.</span><span class="sxs-lookup"><span data-stu-id="e31e0-117">The FileCost action initializes cost calculation with theinstaller.</span></span> <span data-ttu-id="e31e0-118">Die tatsächliche dynamische [*Kosten*](c-gly.md) tritt erst auf, wenn die [costfinalize](costfinalize-action.md) -Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e31e0-118">Actual dynamic [*costing*](c-gly.md) does not occur until the [CostFinalize](costfinalize-action.md) action is executed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e31e0-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e31e0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e31e0-120">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="e31e0-120">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



