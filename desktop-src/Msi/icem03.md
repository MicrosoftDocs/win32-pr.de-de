---
description: ICEM03 überprüft, ob alle Aktionen im Modul entweder Basis Aktionen sind oder von einer gültigen Basis Aktion abgeleitet werden.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368807"
---
# <a name="icem03"></a><span data-ttu-id="f0b8b-103">ICEM03</span><span class="sxs-lookup"><span data-stu-id="f0b8b-103">ICEM03</span></span>

<span data-ttu-id="f0b8b-104">ICEM03 überprüft, ob alle Aktionen im Modul entweder Basis Aktionen sind oder von einer gültigen Basis Aktion abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f0b8b-104">ICEM03 verifies that all actions in the module are either base actions or derive from a valid base action.</span></span>

<span data-ttu-id="f0b8b-105">Das Mergemodul "ICES" wird in der Datei "Merge Module. Cub" mit dem Namen "Mergemod. Cub" und nicht in der CUB-Datei gespeichert, die die für die Paketüberprüfung verwendeten Verb</span><span class="sxs-lookup"><span data-stu-id="f0b8b-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="f0b8b-106">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f0b8b-106">Result</span></span>

<span data-ttu-id="f0b8b-107">ICEM03 veröffentlicht die Fehlermeldungen für ein Modul, das Aktionen in einer Sequenz Tabelle enthält, bei der es sich nicht um eine Basis Aktion handelt oder die von einer gültigen Basis Aktion abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="f0b8b-107">ICEM03 posts the error messages for a module containing actions in a sequence table that is not a base action or derived from a valid base action.</span></span>

## <a name="example"></a><span data-ttu-id="f0b8b-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f0b8b-108">Example</span></span>

<span data-ttu-id="f0b8b-109">ICEM03 gibt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen aus.</span><span class="sxs-lookup"><span data-stu-id="f0b8b-109">ICEM03 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[<span data-ttu-id="f0b8b-110">Moduleinstallexecutesequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="f0b8b-110">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="f0b8b-111">Aktion</span><span class="sxs-lookup"><span data-stu-id="f0b8b-111">Action</span></span>  | <span data-ttu-id="f0b8b-112">Sequenz</span><span class="sxs-lookup"><span data-stu-id="f0b8b-112">Sequence</span></span> | <span data-ttu-id="f0b8b-113">Baseaction</span><span class="sxs-lookup"><span data-stu-id="f0b8b-113">BaseAction</span></span> | <span data-ttu-id="f0b8b-114">Nach</span><span class="sxs-lookup"><span data-stu-id="f0b8b-114">After</span></span> | <span data-ttu-id="f0b8b-115">Bedingung</span><span class="sxs-lookup"><span data-stu-id="f0b8b-115">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="f0b8b-116">Action1</span><span class="sxs-lookup"><span data-stu-id="f0b8b-116">Action1</span></span> |          | <span data-ttu-id="f0b8b-117">Action2</span><span class="sxs-lookup"><span data-stu-id="f0b8b-117">Action2</span></span>    | <span data-ttu-id="f0b8b-118">0</span><span class="sxs-lookup"><span data-stu-id="f0b8b-118">0</span></span>     |           |
| <span data-ttu-id="f0b8b-119">Action2</span><span class="sxs-lookup"><span data-stu-id="f0b8b-119">Action2</span></span> |          | <span data-ttu-id="f0b8b-120">Action1</span><span class="sxs-lookup"><span data-stu-id="f0b8b-120">Action1</span></span>    | <span data-ttu-id="f0b8b-121">0</span><span class="sxs-lookup"><span data-stu-id="f0b8b-121">0</span></span>     |           |



 

<span data-ttu-id="f0b8b-122">ICEM03 gibt Fehler für diese beiden Aktionen aus, da Sie als Basis Aktionen in der Tabelle moduleinstallexecutesequence aufeinander verweisen.</span><span class="sxs-lookup"><span data-stu-id="f0b8b-122">ICEM03 posts errors for these two actions because they refer to each other as base actions in the ModuleInstallExecuteSequence table.</span></span> <span data-ttu-id="f0b8b-123">Alle Aktionen in den Tabellen " [moduleadminuisequence](moduleadminuisequence-table.md)", " [moduleadminexecutesequence](moduleadminexecutesequence-table.md)", " [moduleadvtuisequence](moduleadvtuisequence-table.md)", " [moduleadvtexecutesequence](moduleadvtexecutesequence-table.md)", " [moduleinstalluisequence](moduleinstalluisequence-table.md)" und " [moduleinstallexecutesequence](moduleinstallexecutesequence-table.md) " müssen entweder Basis Aktionen sein oder ihre Position aus der Kombination einer anderen</span><span class="sxs-lookup"><span data-stu-id="f0b8b-123">All actions in the [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md), and [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) tables must either be base actions or derive their position from the combination of another action and a before and after flag.</span></span>

<span data-ttu-id="f0b8b-124">Um diesen Fehler zu beheben, bestimmen Sie die Basis Aktionen für die beiden Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f0b8b-124">To fix this error, determine the base actions for the two actions.</span></span> <span data-ttu-id="f0b8b-125">Fügen Sie einen Datensatz für die Basis Aktionen mit einer Standard Sequenznummer hinzu.</span><span class="sxs-lookup"><span data-stu-id="f0b8b-125">Add a record for the base actions with a default sequence number.</span></span> <span data-ttu-id="f0b8b-126">Geben Sie für Action1 und Action2 die Basis Aktions Namen in der Spalte baseaction und in der Spalte after den Wert 0 oder 1 ein.</span><span class="sxs-lookup"><span data-stu-id="f0b8b-126">For Action1 and Action2 enter the base action names in the BaseAction column and 0 or 1 in the After column.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0b8b-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0b8b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0b8b-128">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="f0b8b-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



