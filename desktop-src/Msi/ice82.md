---
description: ICE82 überprüft, ob die Aktion registerproduct Action, RegisterUser Action, publishproduct Action und publishfeatures in der Tabelle InstallExecuteSequence vorhanden sind. Das Paket wird überprüft, wenn alle Aktionen vorhanden sind.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758413"
---
# <a name="ice82"></a><span data-ttu-id="d3250-104">ICE82</span><span class="sxs-lookup"><span data-stu-id="d3250-104">ICE82</span></span>

<span data-ttu-id="d3250-105">ICE82 überprüft, ob die [Aktion registerproduct](registerproduct-action.md)Action, [RegisterUser Action](registeruser-action.md), [publishproduct Action](publishproduct-action.md)und [publishfeatures](publishfeatures-action.md) in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d3250-105">ICE82 validates that the [RegisterProduct Action](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [PublishProduct Action](publishproduct-action.md), and [PublishFeatures Action](publishfeatures-action.md) are all present in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="d3250-106">Das Paket wird überprüft, wenn alle Aktionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d3250-106">The package is validated if all the actions are present.</span></span>

<span data-ttu-id="d3250-107">ICE82 gibt eine Warnung aus, wenn zwei Aktionen mit der gleichen Sequenznummer in den Tabellen InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence oder AdvtExecuteSequence aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d3250-107">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables .</span></span>

## <a name="result"></a><span data-ttu-id="d3250-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="d3250-108">Result</span></span>

<span data-ttu-id="d3250-109">ICE82 gibt die folgenden Warnungen aus.</span><span class="sxs-lookup"><span data-stu-id="d3250-109">ICE82 posts the following warnings.</span></span>



| <span data-ttu-id="d3250-110">ICE82-Warnung</span><span class="sxs-lookup"><span data-stu-id="d3250-110">ICE82 warning</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="d3250-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3250-111">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3250-112">Die InstallExecuteSequence-Tabelle enthält nicht die unten erwähnten Aktionen: Aktionen fehlen:</span><span class="sxs-lookup"><span data-stu-id="d3250-112">The InstallExecuteSequence table does not contain the set of actions mentioned below: Actions Missing:</span></span><br/> <span data-ttu-id="d3250-113">Features veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="d3250-113">Publish Features</span></span><br/> <span data-ttu-id="d3250-114">Produkt veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="d3250-114">Publish Product</span></span><br/> <span data-ttu-id="d3250-115">Produkt registrieren</span><span class="sxs-lookup"><span data-stu-id="d3250-115">Register Product</span></span><br/> <span data-ttu-id="d3250-116">Benutzer registrieren</span><span class="sxs-lookup"><span data-stu-id="d3250-116">Register User</span></span><br/> | <span data-ttu-id="d3250-117">ICE82 Custom Action gibt eine Warnung aus, wenn alle vier Aktionen fehlen.</span><span class="sxs-lookup"><span data-stu-id="d3250-117">ICE82 custom action posts a warning if all four actions are absent.</span></span>                                                                                                                                         |
| <span data-ttu-id="d3250-118">Diese Aktion \[ 1 \] weist die doppelte Sequenznummer \[ 2 \] in der Tabelle \[ 3 auf \] .</span><span class="sxs-lookup"><span data-stu-id="d3250-118">This action \[1\] has duplicate sequence number \[2\] in the table \[3\].</span></span>                                                                                                                                                     | <span data-ttu-id="d3250-119">ICE82 gibt eine Warnung aus, wenn zwei Aktionen mit der gleichen Sequenznummer in den Tabellen InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence oder AdvtExecuteSequence aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d3250-119">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables.</span></span> |



 

<span data-ttu-id="d3250-120">ICE82 gibt die folgenden Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="d3250-120">ICE82 posts the following errors.</span></span>



| <span data-ttu-id="d3250-121">ICE82-Fehler</span><span class="sxs-lookup"><span data-stu-id="d3250-121">ICE82 error</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="d3250-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3250-122">Description</span></span>                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d3250-123">InstallExecuteSequence muss entweder alle unten erwähnten Aktionen enthalten, oder es sind keine Aktionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d3250-123">The InstallExecuteSequence should either contain all of the actions mentioned below or none of them Actions Present</span></span><br/> <List of actions present> <br/> <span data-ttu-id="d3250-124">Fehlende Aktionen:</span><span class="sxs-lookup"><span data-stu-id="d3250-124">Actions Missing:</span></span><br/> <List of actions missing> <br/> | <span data-ttu-id="d3250-125">ICE82 gibt einen Fehler aus, wenn einige der vier Aktionen vorhanden sind und andere nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d3250-125">ICE82 posts an error if some of the four actions are present and others are absent.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d3250-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3250-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3250-127">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="d3250-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




