---
description: Die Tabelle "moduleausschluss" speichert eine Liste anderer Mergemodule, die in derselben Installerdatenbank nicht kompatibel sind.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Moduleausschluss-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393741"
---
# <a name="moduleexclusion-table"></a><span data-ttu-id="8718e-103">Moduleausschluss-Tabelle</span><span class="sxs-lookup"><span data-stu-id="8718e-103">ModuleExclusion Table</span></span>

<span data-ttu-id="8718e-104">Die Tabelle "moduleausschluss" speichert eine Liste anderer Mergemodule, die in derselben Installerdatenbank nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="8718e-104">The ModuleExclusion table keeps a list of other merge modules that are incompatible in the same installer database.</span></span> <span data-ttu-id="8718e-105">Diese Tabelle ermöglicht einem Merge-oder Überprüfungs Tool, zu überprüfen, ob in Konflikt stehende Mergemodule nicht in der Installer-Datenbank des Benutzers zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8718e-105">This table enables a merge or verification tool to check that conflicting merge modules are not merged in the user's installer database.</span></span> <span data-ttu-id="8718e-106">Das Tool überprüft, ob diese Tabelle mit der ModuleSignature-Tabelle in der Installer-Datenbank quer referenziert wird.</span><span class="sxs-lookup"><span data-stu-id="8718e-106">The tool checks by cross-referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="8718e-107">Die moduleausschluss-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="8718e-107">The ModuleExclusion table has the following columns.</span></span>



| <span data-ttu-id="8718e-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="8718e-108">Column</span></span>             | <span data-ttu-id="8718e-109">Typ</span><span class="sxs-lookup"><span data-stu-id="8718e-109">Type</span></span>                         | <span data-ttu-id="8718e-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="8718e-110">Key</span></span> | <span data-ttu-id="8718e-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="8718e-111">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="8718e-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="8718e-112">ModuleID</span></span>           | [<span data-ttu-id="8718e-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8718e-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="8718e-114">J</span><span class="sxs-lookup"><span data-stu-id="8718e-114">Y</span></span>   | <span data-ttu-id="8718e-115">N</span><span class="sxs-lookup"><span data-stu-id="8718e-115">N</span></span>        |
| <span data-ttu-id="8718e-116">Modulelanguage</span><span class="sxs-lookup"><span data-stu-id="8718e-116">ModuleLanguage</span></span>     | [<span data-ttu-id="8718e-117">Integer</span><span class="sxs-lookup"><span data-stu-id="8718e-117">Integer</span></span>](integer.md)       | <span data-ttu-id="8718e-118">J</span><span class="sxs-lookup"><span data-stu-id="8718e-118">Y</span></span>   | <span data-ttu-id="8718e-119">N</span><span class="sxs-lookup"><span data-stu-id="8718e-119">N</span></span>        |
| <span data-ttu-id="8718e-120">Excludädid</span><span class="sxs-lookup"><span data-stu-id="8718e-120">ExcludedID</span></span>         | [<span data-ttu-id="8718e-121">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8718e-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="8718e-122">J</span><span class="sxs-lookup"><span data-stu-id="8718e-122">Y</span></span>   | <span data-ttu-id="8718e-123">N</span><span class="sxs-lookup"><span data-stu-id="8718e-123">N</span></span>        |
| <span data-ttu-id="8718e-124">Excludecodlanguage</span><span class="sxs-lookup"><span data-stu-id="8718e-124">ExcludedLanguage</span></span>   | [<span data-ttu-id="8718e-125">Integer</span><span class="sxs-lookup"><span data-stu-id="8718e-125">Integer</span></span>](integer.md)       | <span data-ttu-id="8718e-126">J</span><span class="sxs-lookup"><span data-stu-id="8718e-126">Y</span></span>   | <span data-ttu-id="8718e-127">N</span><span class="sxs-lookup"><span data-stu-id="8718e-127">N</span></span>        |
| <span data-ttu-id="8718e-128">Excludedminversion</span><span class="sxs-lookup"><span data-stu-id="8718e-128">ExcludedMinVersion</span></span> | [<span data-ttu-id="8718e-129">Version</span><span class="sxs-lookup"><span data-stu-id="8718e-129">Version</span></span>](version.md)       |     | <span data-ttu-id="8718e-130">J</span><span class="sxs-lookup"><span data-stu-id="8718e-130">Y</span></span>        |
| <span data-ttu-id="8718e-131">Excludedmaxversion</span><span class="sxs-lookup"><span data-stu-id="8718e-131">ExcludedMaxVersion</span></span> | [<span data-ttu-id="8718e-132">Version</span><span class="sxs-lookup"><span data-stu-id="8718e-132">Version</span></span>](version.md)       |     | <span data-ttu-id="8718e-133">J</span><span class="sxs-lookup"><span data-stu-id="8718e-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8718e-134">Spalten</span><span class="sxs-lookup"><span data-stu-id="8718e-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8718e-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="8718e-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="8718e-136">Der Bezeichner des Mergemoduls.</span><span class="sxs-lookup"><span data-stu-id="8718e-136">Identifier of the merge module.</span></span> <span data-ttu-id="8718e-137">Dabei handelt es sich um einen Fremdschlüssel in der [Tabelle ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8718e-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="8718e-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>Modulelanguage</span><span class="sxs-lookup"><span data-stu-id="8718e-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="8718e-139">Die dezimale Sprach-ID des Mergemoduls in ModuleID.</span><span class="sxs-lookup"><span data-stu-id="8718e-139">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="8718e-140">Dabei handelt es sich um einen Fremdschlüssel in der [Tabelle ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8718e-140">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="8718e-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>Excludädid</span><span class="sxs-lookup"><span data-stu-id="8718e-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span></span>
</dt> <dd>

<span data-ttu-id="8718e-142">Der Bezeichner eines ausgeschlossenen Mergemoduls.</span><span class="sxs-lookup"><span data-stu-id="8718e-142">Identifier of an excluded merge module.</span></span>

</dd> <dt>

<span data-ttu-id="8718e-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>Excludecodlanguage</span><span class="sxs-lookup"><span data-stu-id="8718e-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span></span>
</dt> <dd>

<span data-ttu-id="8718e-144">Numerische Sprach-ID des Mergemoduls in excluabdid.</span><span class="sxs-lookup"><span data-stu-id="8718e-144">Numeric language ID of the merge module in ExcludedID.</span></span> <span data-ttu-id="8718e-145">In der Spalte excludecodlanguage kann die Sprach-ID für eine einzelne Sprache angegeben werden, z. b. 1033 für US-Englisch, oder die Sprach-ID für eine Sprachgruppe, z. b. 9 für Englisch.</span><span class="sxs-lookup"><span data-stu-id="8718e-145">The ExcludedLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="8718e-146">Die excludebug Language-Spalte kann negative Sprach-IDs annehmen.</span><span class="sxs-lookup"><span data-stu-id="8718e-146">The ExcludedLanguage column can accept negative language IDs.</span></span> <span data-ttu-id="8718e-147">Die Bedeutung des Werts in der Spalte excludlanguage lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="8718e-147">The meaning of the value in the ExcludedLanguage column is as follows.</span></span>



| <span data-ttu-id="8718e-148">Excludecodlanguage</span><span class="sxs-lookup"><span data-stu-id="8718e-148">ExcludedLanguage</span></span> | <span data-ttu-id="8718e-149">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8718e-149">Meaning</span></span>                                                              |
|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="8718e-150">> 0</span><span class="sxs-lookup"><span data-stu-id="8718e-150">> 0</span></span>           | <span data-ttu-id="8718e-151">Schließen Sie die Sprach-IDs aus, die von excludlanguage angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8718e-151">Exclude the language IDs specified by ExcludedLanguage.</span></span>              |
| <span data-ttu-id="8718e-152">= 0</span><span class="sxs-lookup"><span data-stu-id="8718e-152">= 0</span></span>              | <span data-ttu-id="8718e-153">Schließen Sie keine Sprach-IDs aus.</span><span class="sxs-lookup"><span data-stu-id="8718e-153">Exclude no language IDs.</span></span>                                             |
| <span data-ttu-id="8718e-154">< 0</span><span class="sxs-lookup"><span data-stu-id="8718e-154">< 0</span></span>           | <span data-ttu-id="8718e-155">Schließen Sie alle Sprach-IDs außer den von excludlanguage angegebenen aus.</span><span class="sxs-lookup"><span data-stu-id="8718e-155">Exclude all language IDs except those specified by ExcludedLanguage.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8718e-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>Excludedminversion</span><span class="sxs-lookup"><span data-stu-id="8718e-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span></span>
</dt> <dd>

<span data-ttu-id="8718e-157">Mindestens von einem Bereich ausgeschlossener Version.</span><span class="sxs-lookup"><span data-stu-id="8718e-157">Minimum version excluded from a range.</span></span> <span data-ttu-id="8718e-158">Wenn das Feld excludedminversion NULL ist, werden alle Versionen vor excludedmaxversion ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8718e-158">If the ExcludedMinVersion field is Null, all versions before ExcludedMaxVersion are excluded.</span></span> <span data-ttu-id="8718e-159">Wenn sowohl excludedminversion als auch excludedmaxversion NULL sind, gibt es keinen Ausschluss, der auf der Version basiert.</span><span class="sxs-lookup"><span data-stu-id="8718e-159">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> <dt>

<span data-ttu-id="8718e-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>Excludedmaxversion</span><span class="sxs-lookup"><span data-stu-id="8718e-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="8718e-161">Die maximale Version, die von einem Bereich ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="8718e-161">Maximum version excluded from a range.</span></span> <span data-ttu-id="8718e-162">Wenn das Feld excludedmaxversion NULL ist, werden alle Versionen nach excludedminversion ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8718e-162">If the ExcludedMaxVersion field is Null, all versions after ExcludedMinVersion are excluded.</span></span> <span data-ttu-id="8718e-163">Wenn sowohl excludedminversion als auch excludedmaxversion NULL sind, gibt es keinen Ausschluss, der auf der Version basiert.</span><span class="sxs-lookup"><span data-stu-id="8718e-163">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="8718e-164">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="8718e-164">Validation</span></span>

<dl>

[<span data-ttu-id="8718e-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="8718e-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8718e-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="8718e-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8718e-167">ICE25</span><span class="sxs-lookup"><span data-stu-id="8718e-167">ICE25</span></span>](ice25.md)  
</dl>

 

 



