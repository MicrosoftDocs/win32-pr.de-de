---
description: Mit der Aktion "costinitialize" wird der Installationskosten Prozess initiiert.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Costinitialize-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350294"
---
# <a name="costinitialize-action"></a><span data-ttu-id="a5446-103">Costinitialize-Aktion</span><span class="sxs-lookup"><span data-stu-id="a5446-103">CostInitialize Action</span></span>

<span data-ttu-id="a5446-104">Mit der Aktion "costinitialize" wird der Installations [*Kosten*](c-gly.md) Prozess initiiert.</span><span class="sxs-lookup"><span data-stu-id="a5446-104">The CostInitialize action initiates the installation [*costing*](c-gly.md) process.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a5446-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="a5446-105">Sequence Restrictions</span></span>

<span data-ttu-id="a5446-106">Alle standardmäßigen oder [benutzerdefinierten](custom-actions.md) Aktionen, die sich auf die Kosten auswirken, sollten vor der costinitialize-Aktion sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="a5446-106">Any standard or [custom](custom-actions.md) actions that affect costing should be sequenced before the CostInitialize action.</span></span> <span data-ttu-id="a5446-107">Wenden Sie die Aktion " [filecost](filecost-action.md) " direkt nach der Aktion "costinitialize" an.</span><span class="sxs-lookup"><span data-stu-id="a5446-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action.</span></span> <span data-ttu-id="a5446-108">Anschließend können Sie die Aktion " [costfinalize](costfinalize-action.md) " nach der Aktion "costinitialize Action" aufzurufen, um dem Installer mithilfe der [Komponenten](component-table.md) Tabelle alle abschließenden Kostenberechnungen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="a5446-108">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a5446-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="a5446-109">ActionData Messages</span></span>

<span data-ttu-id="a5446-110">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a5446-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5446-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5446-111">Remarks</span></span>

<span data-ttu-id="a5446-112">Die costinitialize-Aktion lädt die [Komponenten Tabelle und](feature-table.md) die Featuretabelle in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a5446-112">The CostInitialize action loads the Component table and [Feature](feature-table.md) table into memory.</span></span>

<span data-ttu-id="a5446-113">Weitere Informationen zum [*Kosten*](c-gly.md) Prozess im Installationsprogramm finden Sie unter [Datei Kosten](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="a5446-113">For more information on the [*costing*](c-gly.md) process in the installer, see [File Costing](file-costing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5446-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5446-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5446-115">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="a5446-115">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



