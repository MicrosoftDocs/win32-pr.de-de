---
description: Die Bedingungs Tabelle kann verwendet werden, um den Auswahl Status eines beliebigen Eintrags in der Featuretabelle basierend auf einem bedingten Ausdruck zu ändern.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Bedingungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958739"
---
# <a name="condition-table"></a><span data-ttu-id="d038b-103">Bedingungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="d038b-103">Condition Table</span></span>

<span data-ttu-id="d038b-104">Die Bedingungs Tabelle kann verwendet werden, um den Auswahl Status eines beliebigen Eintrags in der [Featuretabelle](feature-table.md) basierend auf einem bedingten Ausdruck zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d038b-104">The Condition table can be used to modify the selection state of any entry in the [Feature table](feature-table.md) based on a conditional expression.</span></span>

<span data-ttu-id="d038b-105">Die Bedingungs Tabelle enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="d038b-105">The Condition table has the following columns.</span></span>



| <span data-ttu-id="d038b-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="d038b-106">Column</span></span>    | <span data-ttu-id="d038b-107">Typ</span><span class="sxs-lookup"><span data-stu-id="d038b-107">Type</span></span>                         | <span data-ttu-id="d038b-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d038b-108">Key</span></span> | <span data-ttu-id="d038b-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d038b-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="d038b-110">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="d038b-110">Feature\_</span></span> | [<span data-ttu-id="d038b-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d038b-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d038b-112">J</span><span class="sxs-lookup"><span data-stu-id="d038b-112">Y</span></span>   | <span data-ttu-id="d038b-113">N</span><span class="sxs-lookup"><span data-stu-id="d038b-113">N</span></span>        |
| <span data-ttu-id="d038b-114">Ebene</span><span class="sxs-lookup"><span data-stu-id="d038b-114">Level</span></span>     | [<span data-ttu-id="d038b-115">Integer</span><span class="sxs-lookup"><span data-stu-id="d038b-115">Integer</span></span>](integer.md)       | <span data-ttu-id="d038b-116">J</span><span class="sxs-lookup"><span data-stu-id="d038b-116">Y</span></span>   | <span data-ttu-id="d038b-117">N</span><span class="sxs-lookup"><span data-stu-id="d038b-117">N</span></span>        |
| <span data-ttu-id="d038b-118">Bedingung</span><span class="sxs-lookup"><span data-stu-id="d038b-118">Condition</span></span> | [<span data-ttu-id="d038b-119">Condition</span><span class="sxs-lookup"><span data-stu-id="d038b-119">Condition</span></span>](condition.md)   | <span data-ttu-id="d038b-120">N</span><span class="sxs-lookup"><span data-stu-id="d038b-120">N</span></span>   | <span data-ttu-id="d038b-121">J</span><span class="sxs-lookup"><span data-stu-id="d038b-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d038b-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="d038b-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d038b-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="d038b-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="d038b-124">Externer Schlüssel in Spalte 1 der Featuretabelle.</span><span class="sxs-lookup"><span data-stu-id="d038b-124">External key into column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="d038b-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Geringen</span><span class="sxs-lookup"><span data-stu-id="d038b-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Level</span></span>
</dt> <dd>

<span data-ttu-id="d038b-126">Eine bedingte Installationsstufe für die Funktion in der \_ featurespalte der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d038b-126">A conditional install level for the feature in the Feature\_ column of this table.</span></span> <span data-ttu-id="d038b-127">Der Installer legt die Installations Ebene dieses Features auf die in dieser Spalte angegebene Ebene fest, wenn der Ausdruck in der Spalte Bedingung als true ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="d038b-127">The installer sets the install level of this feature to the level specified in this column if the expression in the Condition column evaluates to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="d038b-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="d038b-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="d038b-129">Wenn dieser bedingte Ausdruck als true ausgewertet wird, wird die Spalte Ebene in der Featuretabelle auf die bedingte Installations Ebene festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d038b-129">If this conditional expression evaluates to TRUE, then the Level column in the Feature table is set to the conditional install level.</span></span>

<span data-ttu-id="d038b-130">Der Ausdruck in der Spalte Bedingung sollte keinen Verweis auf den installierten Zustand eines Features oder einer Komponente enthalten.</span><span class="sxs-lookup"><span data-stu-id="d038b-130">The expression in the Condition column should not contain reference to the installed state of any feature or component.</span></span> <span data-ttu-id="d038b-131">Dies liegt daran, dass die Ausdrücke in der Spalte Bedingung ausgewertet werden, bevor der Installer die installierten Status von Features und Komponenten auswertet.</span><span class="sxs-lookup"><span data-stu-id="d038b-131">This is because the expressions in the Condition column are evaluated before the installer evaluates the installed states of features and components.</span></span> <span data-ttu-id="d038b-132">Jeder Ausdruck in der Bedingungs Tabelle, der versucht, den installierten Zustand eines Features oder einer Komponente zu überprüfen, wird immer auf "false" ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="d038b-132">Any expression in the Condition table that attempts to check the installed state of a feature or component always evaluates to false.</span></span>

<span data-ttu-id="d038b-133">Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="d038b-133">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d038b-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d038b-134">Remarks</span></span>

<span data-ttu-id="d038b-135">Eine Funktion kann durch Festlegen der Ebene-Spalte auf 0 (null) dauerhaft deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d038b-135">A feature can be permanently disabled by setting the Level column to 0.</span></span>

<span data-ttu-id="d038b-136">Die Ebene kann basierend auf einer Bedingungs Anweisung festgelegt werden, z. b. ein Test für Plattform, Betriebssystem oder eine bestimmte Eigenschaften Einstellung.</span><span class="sxs-lookup"><span data-stu-id="d038b-136">The Level may be set based on any conditional statement, such as a test for platform, operating system, or a particular property setting.</span></span>

<span data-ttu-id="d038b-137">Bedingungen sollten sorgfältig ausgewählt werden, damit eine Funktion bei der Deinstallation nicht aktiviert und dann deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="d038b-137">Conditions should be carefully chosen so that a feature is not enabled on install and then disabled on uninstall.</span></span> <span data-ttu-id="d038b-138">Dadurch wird das Feature verwaist, und das Produkt kann nicht deinstalliert werden.</span><span class="sxs-lookup"><span data-stu-id="d038b-138">This will orphan the feature and the product will not be able to be uninstalled.</span></span>

<span data-ttu-id="d038b-139">Diese Tabelle wird beim Ausführen der [Aktion "costfinalize](costfinalize-action.md) " bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d038b-139">This table is referred to when the [CostFinalize action](costfinalize-action.md) is executed.</span></span>

<span data-ttu-id="d038b-140">Wenn die [**vorab ausgewählte**](preselected.md) Eigenschaft auf 1 festgelegt wurde, wertet das Installationsprogramm die Bedingungs Tabelle nicht aus.</span><span class="sxs-lookup"><span data-stu-id="d038b-140">If the [**Preselected**](preselected.md) property has been set to 1, the installer does not evaluate the Condition table.</span></span> <span data-ttu-id="d038b-141">Die Bedingungs Tabelle wirkt sich nur auf die Installation von-Funktionen aus, wenn keine der folgenden Eigenschaften festgelegt wurde:</span><span class="sxs-lookup"><span data-stu-id="d038b-141">The Condition table affects only the installation of features when none of the following properties have been set:</span></span>

<dl>

[<span data-ttu-id="d038b-142">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d038b-142">**ADDLOCAL**</span></span>](addlocal.md)  
[<span data-ttu-id="d038b-143">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="d038b-143">**REMOVE**</span></span>](remove.md)  
[<span data-ttu-id="d038b-144">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="d038b-144">**ADDSOURCE**</span></span>](addsource.md)  
[<span data-ttu-id="d038b-145">**Adddefault**</span><span class="sxs-lookup"><span data-stu-id="d038b-145">**ADDDEFAULT**</span></span>](adddefault.md)  
[<span data-ttu-id="d038b-146">**Installieren Sie**</span><span class="sxs-lookup"><span data-stu-id="d038b-146">**REINSTALL**</span></span>](reinstall.md)  
[<span data-ttu-id="d038b-147">**Benen**</span><span class="sxs-lookup"><span data-stu-id="d038b-147">**ADVERTISE**</span></span>](advertise.md)  
[<span data-ttu-id="d038b-148">**Compaddlocal**</span><span class="sxs-lookup"><span data-stu-id="d038b-148">**COMPADDLOCAL**</span></span>](compaddlocal.md)  
[<span data-ttu-id="d038b-149">**Compaddsource**</span><span class="sxs-lookup"><span data-stu-id="d038b-149">**COMPADDSOURCE**</span></span>](compaddsource.md)  
[<span data-ttu-id="d038b-150">**Compadddefault**</span><span class="sxs-lookup"><span data-stu-id="d038b-150">**COMPADDDEFAULT**</span></span>](compadddefault.md)  
[<span data-ttu-id="d038b-151">**Fileaddlocal**</span><span class="sxs-lookup"><span data-stu-id="d038b-151">**FILEADDLOCAL**</span></span>](fileaddlocal.md)  
[<span data-ttu-id="d038b-152">**Fileaddsource**</span><span class="sxs-lookup"><span data-stu-id="d038b-152">**FILEADDSOURCE**</span></span>](fileaddsource.md)  
[<span data-ttu-id="d038b-153">**Fileadddefault**</span><span class="sxs-lookup"><span data-stu-id="d038b-153">**FILEADDDEFAULT**</span></span>](fileadddefault.md)  
</dl>

## <a name="validation"></a><span data-ttu-id="d038b-154">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="d038b-154">Validation</span></span>

<dl>

[<span data-ttu-id="d038b-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="d038b-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d038b-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="d038b-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d038b-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="d038b-157">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d038b-158">ICE46</span><span class="sxs-lookup"><span data-stu-id="d038b-158">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="d038b-159">ICE79</span><span class="sxs-lookup"><span data-stu-id="d038b-159">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="d038b-160">ICE86</span><span class="sxs-lookup"><span data-stu-id="d038b-160">ICE86</span></span>](ice86.md)  
</dl>

 

 



