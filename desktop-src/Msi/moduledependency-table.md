---
description: Die moduledepen-Tabelle speichert eine Liste anderer Mergemodule, die erforderlich sind, damit dieses Mergemodul ordnungsgemäß funktioniert.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Moduledepenptabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368832"
---
# <a name="moduledependency-table"></a><span data-ttu-id="715f0-103">Moduledepenptabelle</span><span class="sxs-lookup"><span data-stu-id="715f0-103">ModuleDependency Table</span></span>

<span data-ttu-id="715f0-104">Die moduledepen-Tabelle speichert eine Liste anderer Mergemodule, die erforderlich sind, damit dieses Mergemodul ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="715f0-104">The ModuleDependency table keeps a list of other merge modules that are required for this merge module to operate properly.</span></span> <span data-ttu-id="715f0-105">Diese Tabelle ermöglicht einem Merge-oder Überprüfungs Tool, sicherzustellen, dass die erforderlichen Mergemodule tatsächlich in der Installer-Datenbank des Benutzers enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="715f0-105">This table enables a merge or verification tool to ensure that the necessary merge modules are in fact included in the user's installer database.</span></span> <span data-ttu-id="715f0-106">Das Tool überprüft, ob Querverweise auf diese Tabelle mit der ModuleSignature-Tabelle in der Installer-Datenbank durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="715f0-106">The tool checks by cross referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="715f0-107">Die moduledepenptabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="715f0-107">The ModuleDependency table has the following columns.</span></span>



| <span data-ttu-id="715f0-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="715f0-108">Column</span></span>           | <span data-ttu-id="715f0-109">Typ</span><span class="sxs-lookup"><span data-stu-id="715f0-109">Type</span></span>                         | <span data-ttu-id="715f0-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="715f0-110">Key</span></span> | <span data-ttu-id="715f0-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="715f0-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="715f0-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="715f0-112">ModuleID</span></span>         | [<span data-ttu-id="715f0-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="715f0-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="715f0-114">J</span><span class="sxs-lookup"><span data-stu-id="715f0-114">Y</span></span>   | <span data-ttu-id="715f0-115">N</span><span class="sxs-lookup"><span data-stu-id="715f0-115">N</span></span>        |
| <span data-ttu-id="715f0-116">Modulelanguage</span><span class="sxs-lookup"><span data-stu-id="715f0-116">ModuleLanguage</span></span>   | [<span data-ttu-id="715f0-117">Integer</span><span class="sxs-lookup"><span data-stu-id="715f0-117">Integer</span></span>](integer.md)       | <span data-ttu-id="715f0-118">J</span><span class="sxs-lookup"><span data-stu-id="715f0-118">Y</span></span>   | <span data-ttu-id="715f0-119">N</span><span class="sxs-lookup"><span data-stu-id="715f0-119">N</span></span>        |
| <span data-ttu-id="715f0-120">Requirements did</span><span class="sxs-lookup"><span data-stu-id="715f0-120">RequiredID</span></span>       | [<span data-ttu-id="715f0-121">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="715f0-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="715f0-122">J</span><span class="sxs-lookup"><span data-stu-id="715f0-122">Y</span></span>   | <span data-ttu-id="715f0-123">N</span><span class="sxs-lookup"><span data-stu-id="715f0-123">N</span></span>        |
| <span data-ttu-id="715f0-124">Requirements-Sprache</span><span class="sxs-lookup"><span data-stu-id="715f0-124">RequiredLanguage</span></span> | [<span data-ttu-id="715f0-125">Integer</span><span class="sxs-lookup"><span data-stu-id="715f0-125">Integer</span></span>](integer.md)       | <span data-ttu-id="715f0-126">J</span><span class="sxs-lookup"><span data-stu-id="715f0-126">Y</span></span>   | <span data-ttu-id="715f0-127">N</span><span class="sxs-lookup"><span data-stu-id="715f0-127">N</span></span>        |
| <span data-ttu-id="715f0-128">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="715f0-128">RequiredVersion</span></span>  | [<span data-ttu-id="715f0-129">Version</span><span class="sxs-lookup"><span data-stu-id="715f0-129">Version</span></span>](version.md)       |     | <span data-ttu-id="715f0-130">J</span><span class="sxs-lookup"><span data-stu-id="715f0-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="715f0-131">Spalten</span><span class="sxs-lookup"><span data-stu-id="715f0-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="715f0-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="715f0-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="715f0-133">Der Bezeichner des Mergemoduls.</span><span class="sxs-lookup"><span data-stu-id="715f0-133">Identifier of the merge module.</span></span> <span data-ttu-id="715f0-134">Dabei handelt es sich um einen Fremdschlüssel in der [Tabelle ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="715f0-134">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="715f0-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>Modulelanguage</span><span class="sxs-lookup"><span data-stu-id="715f0-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="715f0-136">Die dezimale Sprach-ID des Mergemoduls in ModuleID.</span><span class="sxs-lookup"><span data-stu-id="715f0-136">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="715f0-137">Dabei handelt es sich um einen Fremdschlüssel in der [Tabelle ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="715f0-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="715f0-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>Requirements did</span><span class="sxs-lookup"><span data-stu-id="715f0-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span></span>
</dt> <dd>

<span data-ttu-id="715f0-139">Der Bezeichner des Mergemoduls, das vom Mergemodul in ModuleID benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="715f0-139">Identifier of the merge module required by the merge module in ModuleID.</span></span>

</dd> <dt>

<span data-ttu-id="715f0-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>Requirements-Sprache</span><span class="sxs-lookup"><span data-stu-id="715f0-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span></span>
</dt> <dd>

<span data-ttu-id="715f0-141">Numerische Sprach-ID des Mergemoduls in Requirements did.</span><span class="sxs-lookup"><span data-stu-id="715f0-141">Numeric language ID of the merge module in RequiredID.</span></span> <span data-ttu-id="715f0-142">In der Spalte "Requirements-language" können Sie die Sprach-ID für eine einzelne Sprache angeben, z. b. 1033 für US-Englisch, oder Sie können die Sprach-ID für eine Sprachgruppe angeben, z. b. 9 für Englisch.</span><span class="sxs-lookup"><span data-stu-id="715f0-142">The RequiredLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="715f0-143">Wenn das Feld eine Gruppen Sprachen-ID enthält, erfüllt jedes Mergemodul mit einem Sprachcode in dieser Gruppe die Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="715f0-143">If the field contains a group language ID, any merge module with having a language code in that group satisfies the dependency.</span></span> <span data-ttu-id="715f0-144">Wenn für "Requirements" der Wert "0" festgelegt ist, erfüllt jedes Mergemodul, das die anderen Anforderungen erfüllt, die Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="715f0-144">If the RequiredLanguage is set to 0, any merge module filling the other requirements satisfies the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="715f0-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="715f0-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span></span>
</dt> <dd>

<span data-ttu-id="715f0-146">Version des Mergemoduls in Requirements did.</span><span class="sxs-lookup"><span data-stu-id="715f0-146">Version of the merge module in RequiredID.</span></span> <span data-ttu-id="715f0-147">Wenn dieses Feld NULL ist, füllt jede Version die Abhängigkeit aus.</span><span class="sxs-lookup"><span data-stu-id="715f0-147">If this field is Null, any version fills the dependency.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="715f0-148">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="715f0-148">Validation</span></span>

<dl>

[<span data-ttu-id="715f0-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="715f0-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="715f0-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="715f0-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="715f0-151">ICE25</span><span class="sxs-lookup"><span data-stu-id="715f0-151">ICE25</span></span>](ice25.md)  
</dl>

 

 



