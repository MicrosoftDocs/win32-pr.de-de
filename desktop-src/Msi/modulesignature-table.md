---
description: Die ModuleSignature-Tabelle ist eine erforderliche Tabelle.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: ModuleSignature-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529243"
---
# <a name="modulesignature-table"></a><span data-ttu-id="27621-103">ModuleSignature-Tabelle</span><span class="sxs-lookup"><span data-stu-id="27621-103">ModuleSignature Table</span></span>

<span data-ttu-id="27621-104">Die ModuleSignature-Tabelle ist eine erforderliche Tabelle.</span><span class="sxs-lookup"><span data-stu-id="27621-104">The ModuleSignature Table is a required table.</span></span> <span data-ttu-id="27621-105">Sie enthält alle Informationen, die zum Identifizieren eines Mergemoduls erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="27621-105">It contains all the information necessary to identify a merge module.</span></span> <span data-ttu-id="27621-106">Das Mergetool fügt diese Tabelle der MSI-Datei hinzu, sofern noch keine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="27621-106">The merge tool adds this table to the .msi file if one does not already exist.</span></span> <span data-ttu-id="27621-107">Die ModuleSignature-Tabelle in einem Mergemodul weist nur eine Zeile auf, die die ModuleID, die Sprache und die Version enthält.</span><span class="sxs-lookup"><span data-stu-id="27621-107">The ModuleSignature table in a merge module has only one row containing the ModuleID, Language, and Version.</span></span> <span data-ttu-id="27621-108">Die ModuleSignature-Tabelle in einer MSI-Datei enthält jedoch eine Zeile, die diese Informationen für jede MSM-Datei enthält, die mit ihr zusammengeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="27621-108">However, the ModuleSignature table in an .msi file has a row containing this information for each .msm file that has been merged into it.</span></span>

<span data-ttu-id="27621-109">Merge-und Überprüfungs Tools überprüfen Sie die ModuleSignature-Tabelle in MSI-Dateien, um festzustellen, ob Sie über alle vom aktuellen Mergemodul benötigten abhängigen Mergemodule verfügt (siehe [moduledependent Table](moduledependency-table.md)) und ob das Installationspaket zuvor mit zusammengesetzten Mergemodulen zusammengeführt wurde (siehe [Tabelle "moduleausschluss](moduleexclusion-table.md)").</span><span class="sxs-lookup"><span data-stu-id="27621-109">Merge and verification tools check the ModuleSignature table in .msi files to determine if it has all of the dependent merge modules required by the current merge module (see [ModuleDependency Table](moduledependency-table.md)) and whether the installation package was previously merged with any conflicting merge modules (see [ModuleExclusion Table](moduleexclusion-table.md)).</span></span>

<span data-ttu-id="27621-110">Die ModuleSignature-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="27621-110">The ModuleSignature table has the following columns.</span></span>



| <span data-ttu-id="27621-111">Spalte</span><span class="sxs-lookup"><span data-stu-id="27621-111">Column</span></span>   | <span data-ttu-id="27621-112">Typ</span><span class="sxs-lookup"><span data-stu-id="27621-112">Type</span></span>                         | <span data-ttu-id="27621-113">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="27621-113">Key</span></span> | <span data-ttu-id="27621-114">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="27621-114">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="27621-115">ModuleID</span><span class="sxs-lookup"><span data-stu-id="27621-115">ModuleID</span></span> | [<span data-ttu-id="27621-116">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="27621-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="27621-117">J</span><span class="sxs-lookup"><span data-stu-id="27621-117">Y</span></span>   | <span data-ttu-id="27621-118">N</span><span class="sxs-lookup"><span data-stu-id="27621-118">N</span></span>        |
| <span data-ttu-id="27621-119">Sprache</span><span class="sxs-lookup"><span data-stu-id="27621-119">Language</span></span> | [<span data-ttu-id="27621-120">Integer</span><span class="sxs-lookup"><span data-stu-id="27621-120">Integer</span></span>](integer.md)       | <span data-ttu-id="27621-121">J</span><span class="sxs-lookup"><span data-stu-id="27621-121">Y</span></span>   | <span data-ttu-id="27621-122">N</span><span class="sxs-lookup"><span data-stu-id="27621-122">N</span></span>        |
| <span data-ttu-id="27621-123">Version</span><span class="sxs-lookup"><span data-stu-id="27621-123">Version</span></span>  | [<span data-ttu-id="27621-124">Version</span><span class="sxs-lookup"><span data-stu-id="27621-124">Version</span></span>](version.md)       |     | <span data-ttu-id="27621-125">N</span><span class="sxs-lookup"><span data-stu-id="27621-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="27621-126">Spalten</span><span class="sxs-lookup"><span data-stu-id="27621-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="27621-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="27621-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="27621-128">Ein Bezeichner, der das Mergemodul eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="27621-128">An identifier that uniquely identifies the merge module.</span></span> <span data-ttu-id="27621-129">Zwei Mergemodule können nicht denselben ModuleID aufweisen, es sei denn, das Mergemodul ist vollständig abwärts kompatibel mit dem Vorgänger.</span><span class="sxs-lookup"><span data-stu-id="27621-129">Two merge modules cannot have the same ModuleID unless the merge module is entirely backward compatible with its predecessor.</span></span> <span data-ttu-id="27621-130">Sie können eine GUID für dieses Feld mit einem Hilfsprogramm wie GUIDGEN erstellen.</span><span class="sxs-lookup"><span data-stu-id="27621-130">You can create a GUID for this field using a utility such as GUIDGEN.</span></span> <span data-ttu-id="27621-131">Die ModuleID-Spalte ist ein Primärschlüssel für die Tabelle und muss daher der Benennungs Konvention unter [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)entsprechen.</span><span class="sxs-lookup"><span data-stu-id="27621-131">The ModuleID column is a primary key for the table and therefore it must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="27621-132">Wenn z. b. der lesbare Name des Mergemoduls MyLibrary lautet und die GUID {880de2s0-cdd8-11d1-a849-006097abde17} lautet, wird der Eintrag in der Spalte ModuleID zu MyLibrary. 880de2s0 \_ CDD8 \_ 11d1 \_ A849 \_ 006097abde17.</span><span class="sxs-lookup"><span data-stu-id="27621-132">For example, if the readable name of the merge module is MyLibrary and the GUID is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

</dd> <dt>

<span data-ttu-id="27621-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Kurse</span><span class="sxs-lookup"><span data-stu-id="27621-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="27621-134">Der sprach Bezeichner gibt die Standardsprache für das Mergemodul an.</span><span class="sxs-lookup"><span data-stu-id="27621-134">The Language identifier specifies the default language for the merge module.</span></span> <span data-ttu-id="27621-135">Der sprach Bezeichner weist das Dezimal Format auf, z. b. US-Englisch ist 1033.</span><span class="sxs-lookup"><span data-stu-id="27621-135">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="27621-136">Die vom Mergemodul verwendete Sprache kann durch Anwenden einer Transformation auf das Mergemodul vor dem Mergen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="27621-136">The language used by the merge module can be changed by applying a transform to the merge module before merging.</span></span>

</dd> <dt>

<span data-ttu-id="27621-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span><span class="sxs-lookup"><span data-stu-id="27621-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="27621-138">Das Versions Feld enthält eine Zeichenfolge, die die Haupt-und neben Versionen des Mergemoduls beschreibt.</span><span class="sxs-lookup"><span data-stu-id="27621-138">The Version field contains a string that describes the major and minor versions of the merge module.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="27621-139">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="27621-139">Validation</span></span>

<dl>

[<span data-ttu-id="27621-140">ICE03</span><span class="sxs-lookup"><span data-stu-id="27621-140">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="27621-141">ICE06</span><span class="sxs-lookup"><span data-stu-id="27621-141">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="27621-142">ICE25</span><span class="sxs-lookup"><span data-stu-id="27621-142">ICE25</span></span>](ice25.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="27621-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27621-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27621-144">Mehrere Language Merge-Module</span><span class="sxs-lookup"><span data-stu-id="27621-144">Multiple Language Merge Modules</span></span>](multiple-language-merge-modules.md)
</dt> </dl>

 

 



