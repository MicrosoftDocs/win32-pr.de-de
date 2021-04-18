---
description: Die TypeLib-Tabelle enthält die Informationen, die in der Registrierungs Registrierung von Typbibliotheken abgelegt werden müssen.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: TypeLib-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0aa8949df75162ffb7107b633ab766d276c4b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341169"
---
# <a name="typelib-table"></a><span data-ttu-id="98ea7-103">TypeLib-Tabelle</span><span class="sxs-lookup"><span data-stu-id="98ea7-103">TypeLib Table</span></span>

<span data-ttu-id="98ea7-104">Die TypeLib-Tabelle enthält die Informationen, die in der Registrierungs Registrierung von Typbibliotheken abgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="98ea7-104">The TypeLib table contains the information that needs to be placed in the registry registration of type libraries.</span></span>

<span data-ttu-id="98ea7-105">Die TypeLib-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="98ea7-105">The TypeLib table has the following columns.</span></span>



| <span data-ttu-id="98ea7-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="98ea7-106">Column</span></span>      | <span data-ttu-id="98ea7-107">Typ</span><span class="sxs-lookup"><span data-stu-id="98ea7-107">Type</span></span>                               | <span data-ttu-id="98ea7-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="98ea7-108">Key</span></span> | <span data-ttu-id="98ea7-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="98ea7-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="98ea7-110">LIBID</span><span class="sxs-lookup"><span data-stu-id="98ea7-110">LibID</span></span>       | [<span data-ttu-id="98ea7-111">GUID</span><span class="sxs-lookup"><span data-stu-id="98ea7-111">GUID</span></span>](guid.md)                   | <span data-ttu-id="98ea7-112">J</span><span class="sxs-lookup"><span data-stu-id="98ea7-112">Y</span></span>   | <span data-ttu-id="98ea7-113">N</span><span class="sxs-lookup"><span data-stu-id="98ea7-113">N</span></span>        |
| <span data-ttu-id="98ea7-114">Sprache</span><span class="sxs-lookup"><span data-stu-id="98ea7-114">Language</span></span>    | [<span data-ttu-id="98ea7-115">Integer</span><span class="sxs-lookup"><span data-stu-id="98ea7-115">Integer</span></span>](integer.md)             | <span data-ttu-id="98ea7-116">J</span><span class="sxs-lookup"><span data-stu-id="98ea7-116">Y</span></span>   | <span data-ttu-id="98ea7-117">N</span><span class="sxs-lookup"><span data-stu-id="98ea7-117">N</span></span>        |
| <span data-ttu-id="98ea7-118">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="98ea7-118">Component\_</span></span> | [<span data-ttu-id="98ea7-119">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="98ea7-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="98ea7-120">J</span><span class="sxs-lookup"><span data-stu-id="98ea7-120">Y</span></span>   | <span data-ttu-id="98ea7-121">N</span><span class="sxs-lookup"><span data-stu-id="98ea7-121">N</span></span>        |
| <span data-ttu-id="98ea7-122">Version</span><span class="sxs-lookup"><span data-stu-id="98ea7-122">Version</span></span>     | [<span data-ttu-id="98ea7-123">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="98ea7-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="98ea7-124">N</span><span class="sxs-lookup"><span data-stu-id="98ea7-124">N</span></span>   | <span data-ttu-id="98ea7-125">J</span><span class="sxs-lookup"><span data-stu-id="98ea7-125">Y</span></span>        |
| <span data-ttu-id="98ea7-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98ea7-126">Description</span></span> | [<span data-ttu-id="98ea7-127">Text</span><span class="sxs-lookup"><span data-stu-id="98ea7-127">Text</span></span>](text.md)                   | <span data-ttu-id="98ea7-128">N</span><span class="sxs-lookup"><span data-stu-id="98ea7-128">N</span></span>   | <span data-ttu-id="98ea7-129">J</span><span class="sxs-lookup"><span data-stu-id="98ea7-129">Y</span></span>        |
| <span data-ttu-id="98ea7-130">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="98ea7-130">Directory\_</span></span> | [<span data-ttu-id="98ea7-131">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="98ea7-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="98ea7-132">N</span><span class="sxs-lookup"><span data-stu-id="98ea7-132">N</span></span>   | <span data-ttu-id="98ea7-133">J</span><span class="sxs-lookup"><span data-stu-id="98ea7-133">Y</span></span>        |
| <span data-ttu-id="98ea7-134">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="98ea7-134">Feature\_</span></span>   | [<span data-ttu-id="98ea7-135">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="98ea7-135">Identifier</span></span>](identifier.md)       | <span data-ttu-id="98ea7-136">N</span><span class="sxs-lookup"><span data-stu-id="98ea7-136">N</span></span>   | <span data-ttu-id="98ea7-137">N</span><span class="sxs-lookup"><span data-stu-id="98ea7-137">N</span></span>        |
| <span data-ttu-id="98ea7-138">„Cost“ (Kosten)</span><span class="sxs-lookup"><span data-stu-id="98ea7-138">Cost</span></span>        | [<span data-ttu-id="98ea7-139">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="98ea7-139">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="98ea7-140">N</span><span class="sxs-lookup"><span data-stu-id="98ea7-140">N</span></span>   | <span data-ttu-id="98ea7-141">J</span><span class="sxs-lookup"><span data-stu-id="98ea7-141">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="98ea7-142">Spalten</span><span class="sxs-lookup"><span data-stu-id="98ea7-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="98ea7-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LIBID</span><span class="sxs-lookup"><span data-stu-id="98ea7-143"><span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID</span></span>
</dt> <dd>

<span data-ttu-id="98ea7-144">Der GUID, der die Bibliothek identifiziert.</span><span class="sxs-lookup"><span data-stu-id="98ea7-144">The GUID that identifies the library.</span></span>

</dd> <dt>

<span data-ttu-id="98ea7-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Kurse</span><span class="sxs-lookup"><span data-stu-id="98ea7-145"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="98ea7-146">Die Sprache der Typbibliothek.</span><span class="sxs-lookup"><span data-stu-id="98ea7-146">The language of the type library.</span></span> <span data-ttu-id="98ea7-147">Dabei muss es sich um eine nicht negative Zahl handeln.</span><span class="sxs-lookup"><span data-stu-id="98ea7-147">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="98ea7-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="98ea7-148"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="98ea7-149">Externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="98ea7-149">External key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="98ea7-150">Diese Spalte identifiziert die Komponente, die zu der Funktion gehört, \_ deren Schlüsseldatei die Typbibliothek ist, die registriert wird.</span><span class="sxs-lookup"><span data-stu-id="98ea7-150">This column identifies the component belonging to Feature\_ whose key file is the type library being registered.</span></span>

</dd> <dt>

<span data-ttu-id="98ea7-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span><span class="sxs-lookup"><span data-stu-id="98ea7-151"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="98ea7-152">Dies ist die Version der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="98ea7-152">This is the version of the library.</span></span> <span data-ttu-id="98ea7-153">Die Haupt-und neben Versionen werden im ganzzahligen Wert von vier Bytes codiert.</span><span class="sxs-lookup"><span data-stu-id="98ea7-153">The major and minor versions are encoded in the four byte integer value.</span></span> <span data-ttu-id="98ea7-154">Die neben Version ist in den unteren acht Bits.</span><span class="sxs-lookup"><span data-stu-id="98ea7-154">The minor version is in the lower eight bits.</span></span> <span data-ttu-id="98ea7-155">Die Hauptversion liegt in den Mitte sechzehn Bits.</span><span class="sxs-lookup"><span data-stu-id="98ea7-155">The major version is in the middle sixteen bits.</span></span>

</dd> <dt>

<span data-ttu-id="98ea7-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98ea7-156"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="98ea7-157">Eine lokalisierbare Beschreibung der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="98ea7-157">A localizable description of the library.</span></span>

</dd> <dt>

<span data-ttu-id="98ea7-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="98ea7-158"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="98ea7-159">Externer Schlüssel in der ersten Spalte der [Verzeichnis Tabelle](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="98ea7-159">External key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="98ea7-160">Diese Spalte identifiziert den Hilfepfad für die Typbibliothek.</span><span class="sxs-lookup"><span data-stu-id="98ea7-160">This column identifies the Help path for the type library.</span></span> <span data-ttu-id="98ea7-161">Diese Spalte wird bei der Werbung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="98ea7-161">This column is ignored during advertising.</span></span>

</dd> <dt>

<span data-ttu-id="98ea7-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="98ea7-162"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="98ea7-163">Externer Schlüssel in der ersten Spalte der [Funktions Tabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="98ea7-163">External key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="98ea7-164">Diese Spalte gibt die Funktion an, die installiert werden muss, damit die Typbibliothek funktionstüchtig ist.</span><span class="sxs-lookup"><span data-stu-id="98ea7-164">This column specifies the feature that must be installed for the type library to be operational.</span></span>

</dd> <dt>

<span data-ttu-id="98ea7-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Preis</span><span class="sxs-lookup"><span data-stu-id="98ea7-165"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="98ea7-166">Die Kosten, die mit der Registrierung der Typbibliothek in Bytes verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="98ea7-166">The cost associated with the registration of the type library in bytes.</span></span> <span data-ttu-id="98ea7-167">Dies muss eine nicht negative Zahl oder NULL sein.</span><span class="sxs-lookup"><span data-stu-id="98ea7-167">This must be a non-negative number or null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98ea7-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98ea7-168">Remarks</span></span>

<span data-ttu-id="98ea7-169">Auf diese Tabelle wird verwiesen, wenn die Aktion [registertypelibraries](registertypelibraries-action.md) oder die [unregistertypelibraries-Aktion](unregistertypelibraries-action.md) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98ea7-169">This table is referred to when the [RegisterTypeLibraries action](registertypelibraries-action.md) or the [UnregisterTypeLibraries action](unregistertypelibraries-action.md) is executed.</span></span>

<span data-ttu-id="98ea7-170">Das Installationsprogramm schreibt alle Typbibliotheks-Registrierungsinformationen in den \_ \_ Registrierungs Speicherort HKLM (HKEY Local Machine).</span><span class="sxs-lookup"><span data-stu-id="98ea7-170">The installer writes all type library registration information into the HKEY\_LOCAL\_MACHINE (HKLM) registry location.</span></span> <span data-ttu-id="98ea7-171">Dies gilt auch für Installationen pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="98ea7-171">This is the case even for per-user installations.</span></span> <span data-ttu-id="98ea7-172">Typbibliotheken können nicht an Benutzer Standorten (HKCU) registriert werden.</span><span class="sxs-lookup"><span data-stu-id="98ea7-172">Type libraries cannot be registered in per-user locations (HKCU).</span></span>

<span data-ttu-id="98ea7-173">Autoren von Installationspaketen wird dringend empfohlen, die TypeLib-Tabelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="98ea7-173">Installation package authors are strongly advised against using the TypeLib table.</span></span> <span data-ttu-id="98ea7-174">Stattdessen sollten Sie Typbibliotheken mithilfe der [Registrierungs](registry-table.md) Tabelle registrieren.</span><span class="sxs-lookup"><span data-stu-id="98ea7-174">Instead, they should register type libraries by using the [Registry](registry-table.md) table.</span></span> <span data-ttu-id="98ea7-175">Gründe für die Vermeidung der Selbstregistrierung:</span><span class="sxs-lookup"><span data-stu-id="98ea7-175">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="98ea7-176">Wenn eine Installation mit der TypeLib-Tabelle fehlschlägt und ein Rollback ausgeführt werden muss, wird der Computer vom Rollback möglicherweise nicht in demselben Zustand wieder hergestellt, der vor dem Rollback vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="98ea7-176">If an installation using the TypeLib table fails and must be rolled back, the rollback may not restore the computer to the same state that existed prior to the rollback.</span></span> <span data-ttu-id="98ea7-177">Typbibliotheken, die vor dem Rollback registriert wurden, werden nach dem Rollback möglicherweise nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="98ea7-177">Type libraries registered prior to rollback may not be registered after rollback.</span></span>

## <a name="validation"></a><span data-ttu-id="98ea7-178">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="98ea7-178">Validation</span></span>

<dl>

[<span data-ttu-id="98ea7-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="98ea7-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="98ea7-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="98ea7-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="98ea7-181">ICE19</span><span class="sxs-lookup"><span data-stu-id="98ea7-181">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="98ea7-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="98ea7-182">ICE32</span></span>](ice32.md)  
</dl>

 

 



