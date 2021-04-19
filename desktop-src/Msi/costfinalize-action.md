---
description: Die Aktion "costfinalize" beendet den Prozess der internen Installationskosten, der von der Aktion "costinitialize" gestartet wurde.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Costfinalize-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369018"
---
# <a name="costfinalize-action"></a><span data-ttu-id="29441-103">Costfinalize-Aktion</span><span class="sxs-lookup"><span data-stu-id="29441-103">CostFinalize Action</span></span>

<span data-ttu-id="29441-104">Die Aktion "costfinalize" beendet den Prozess der internen Installations [*Kosten*](c-gly.md) , der von der Aktion " [costinitialize](costinitialize-action.md) " gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="29441-104">The CostFinalize action ends the internal installation [*costing*](c-gly.md) process begun by the [CostInitialize](costinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="29441-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="29441-105">Sequence Restrictions</span></span>

<span data-ttu-id="29441-106">Alle standardmäßigen oder [benutzerdefinierten Aktionen](custom-actions.md) , die sich auf die Kosten auswirken, sollten vor der [costinitialize](costinitialize-action.md) -Aktion sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="29441-106">Any standard or [custom actions](custom-actions.md) that affect costing should be sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="29441-107">Nennen Sie die Aktion " [filecost](filecost-action.md) " unmittelbar nach der Aktion "costinitialize", und wenden Sie dann die Aktion "costfinalize" an, um dem Installer alle abschließenden Kostenberechnungen über die [Komponenten](component-table.md) Tabelle zur Verfügung zu stellen</span><span class="sxs-lookup"><span data-stu-id="29441-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action and then call the CostFinalize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="29441-108">Die costfinalize-Aktion muss ausgeführt werden, bevor eine Benutzeroberflächen Sequenz gestartet wird, die es dem Benutzer [](feature-table.md) ermöglicht, featuretabellenauswahl oder-Verzeichnisse anzuzeigen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="29441-108">The CostFinalize action must be executed before starting any user interface sequence which allows the user to view or modify [Feature](feature-table.md) table selections or directories.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="29441-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="29441-109">ActionData Messages</span></span>

<span data-ttu-id="29441-110">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="29441-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="29441-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29441-111">Remarks</span></span>

<span data-ttu-id="29441-112">Mit der costfinalize-Aktion wird die [Bedingungs Tabelle](condition-table.md) abgefragt, um zu bestimmen, welche Features installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="29441-112">The CostFinalize action queries the [Condition](condition-table.md) table to determine which features are scheduled to be installed.</span></span> <span data-ttu-id="29441-113">Die Kosten werden für jede Komponente in der [Komponenten](component-table.md) Tabelle durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="29441-113">Costing is done for each component in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="29441-114">Mit der Aktion "costfinalize" wird außerdem überprüft, ob alle Zielverzeichnisse beschreibbar sind, bevor die Installation fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="29441-114">The CostFinalize action also verifies that all the target directories are writable before allowing the installation to continue.</span></span>

> [!Note]  
> <span data-ttu-id="29441-115">Bei einer [administrativen Installation](administrative-installation.md)werden von "costfinalize" alle Features für die Installation festgelegt, außer bei den Funktionen, die in der Spalte Ebene der [Featuretabelle](feature-table.md)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="29441-115">During an [administrative installation](administrative-installation.md), CostFinalize sets all features for installation except features having 0 authored in the Level column of the [Feature table](feature-table.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="29441-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="29441-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29441-117">Datei Kosten</span><span class="sxs-lookup"><span data-stu-id="29441-117">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



