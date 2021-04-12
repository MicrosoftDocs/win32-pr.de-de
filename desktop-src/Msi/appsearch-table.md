---
description: Die AppSearch-Tabelle enthält die Eigenschaften, die für die Suche nach einer Datei mit einer bestimmten Datei Signatur erforderlich sind. Die AppSearch-Tabelle kann auch verwendet werden, um eine Eigenschaft auf den vorhandenen Wert eines Registrierungs-oder INI-Datei Eintrags festzulegen.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: AppSearch-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215717"
---
# <a name="appsearch-table"></a><span data-ttu-id="35651-104">AppSearch-Tabelle</span><span class="sxs-lookup"><span data-stu-id="35651-104">AppSearch Table</span></span>

<span data-ttu-id="35651-105">Die AppSearch-Tabelle enthält die Eigenschaften, die für die Suche nach einer Datei mit einer bestimmten Datei Signatur erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="35651-105">The AppSearch table contains properties needed to search for a file having a particular file signature.</span></span> <span data-ttu-id="35651-106">Die AppSearch-Tabelle kann auch verwendet werden, um eine Eigenschaft auf den vorhandenen Wert eines Registrierungs-oder INI-Datei Eintrags festzulegen.</span><span class="sxs-lookup"><span data-stu-id="35651-106">The AppSearch table can also be used to set a property to the existing value of a registry or .ini file entry.</span></span>

<span data-ttu-id="35651-107">Die AppSearch-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="35651-107">The AppSearch table has the following columns.</span></span>



| <span data-ttu-id="35651-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="35651-108">Column</span></span>      | <span data-ttu-id="35651-109">Typ</span><span class="sxs-lookup"><span data-stu-id="35651-109">Type</span></span>                         | <span data-ttu-id="35651-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="35651-110">Key</span></span> | <span data-ttu-id="35651-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="35651-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="35651-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="35651-112">Property</span></span>    | [<span data-ttu-id="35651-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="35651-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="35651-114">J</span><span class="sxs-lookup"><span data-stu-id="35651-114">Y</span></span>   | <span data-ttu-id="35651-115">N</span><span class="sxs-lookup"><span data-stu-id="35651-115">N</span></span>        |
| <span data-ttu-id="35651-116">Signatur\_</span><span class="sxs-lookup"><span data-stu-id="35651-116">Signature\_</span></span> | [<span data-ttu-id="35651-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="35651-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="35651-118">J</span><span class="sxs-lookup"><span data-stu-id="35651-118">Y</span></span>   | <span data-ttu-id="35651-119">N</span><span class="sxs-lookup"><span data-stu-id="35651-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="35651-120">Spalten</span><span class="sxs-lookup"><span data-stu-id="35651-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="35651-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span><span class="sxs-lookup"><span data-stu-id="35651-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="35651-122">Durch das Ausführen der [AppSearch](appsearch-action.md) -Aktion wird diese Eigenschaft auf den Speicherort der Datei festgelegt, der in der Signatur Spalte angegeben ist \_ .</span><span class="sxs-lookup"><span data-stu-id="35651-122">Running the [AppSearch](appsearch-action.md) action sets this property to the location of the file indicated by the Signature\_ column.</span></span> <span data-ttu-id="35651-123">Diese Eigenschaft wird festgelegt, wenn die Datei Signatur auf dem Computer des Benutzers vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="35651-123">This property is set if the file signature exists on the user's computer.</span></span> <span data-ttu-id="35651-124">Die in dieser Spalte verwendeten Eigenschaften müssen [öffentliche](public-properties.md) Eigenschaften sein und über einen Bezeichner verfügen, der keine Kleinbuchstaben enthält.</span><span class="sxs-lookup"><span data-stu-id="35651-124">The properties used in this column must be [public](public-properties.md) properties and have an identifier that contains no lowercase letters.</span></span>

<span data-ttu-id="35651-125">Die im Eigenschaften Feld aufgelistete Eigenschaft kann in der [Eigenschaften](property-table.md) Tabelle oder über die Befehlszeile initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="35651-125">The property listed in the Property field may be initialized in the [Property](property-table.md) table or from a command line.</span></span> <span data-ttu-id="35651-126">Wenn die [AppSearch](appsearch-action.md) -Aktion die Signatur sucht, überschreibt der Installer den initialisierten Eigenschafts Wert mit dem gefundenen Wert.</span><span class="sxs-lookup"><span data-stu-id="35651-126">If the [AppSearch](appsearch-action.md) action locates the signature, the installer overrides the initialized property value with the found value.</span></span> <span data-ttu-id="35651-127">Wenn die Signatur nicht gefunden wird, wird der anfängliche Eigenschafts Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="35651-127">If the signature is not found, then the initial property value is used.</span></span> <span data-ttu-id="35651-128">Wenn die Eigenschaft nie initialisiert wurde, wird die Eigenschaft nur festgelegt, wenn die Signatur gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="35651-128">If the property was never initialized, then the property will only be set if the signature is found.</span></span> <span data-ttu-id="35651-129">Andernfalls ist die Eigenschaft nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="35651-129">Otherwise, the property is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="35651-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_</span><span class="sxs-lookup"><span data-stu-id="35651-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="35651-131">Die \_ Spalte Signatur enthält einen eindeutigen Bezeichner, der als Signatur bezeichnet wird, und ist auch ein externer Schlüssel in den Tabellen [reglocator](reglocator-table.md), [inilocator](inilocator-table.md), [complocator](complocator-table.md)und [drlocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="35651-131">The Signature\_ column contains a unique identifier called a signature and is also an external key into the [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span> <span data-ttu-id="35651-132">Wenn Sie nach einer Datei suchen, muss der Wert in dieser Spalte auch ein Fremdschlüssel in der [Signatur](signature-table.md) Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="35651-132">When searching for a file, the value in this column must also be a foreign key into the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="35651-133">Wenn der Wert in dieser Spalte nicht in der Signatur Tabelle aufgeführt ist, ermittelt das Installationsprogramm, dass die Suche nach einem Verzeichnis erfolgt.</span><span class="sxs-lookup"><span data-stu-id="35651-133">If the value in this column is not listed in the Signature table, the installer determines that the search is for a directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35651-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35651-134">Remarks</span></span>

<span data-ttu-id="35651-135">Die [AppSearch](appsearch-action.md) -Aktion in [*Sequenz Tabellen*](s-gly.md) verarbeitet die Informationen in dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="35651-135">The [AppSearch](appsearch-action.md) action in [*sequence tables*](s-gly.md) processes the information in this table.</span></span> <span data-ttu-id="35651-136">Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="35651-136">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="35651-137">Die [AppSearch](appsearch-action.md) -Aktion sucht mithilfe der Tabelle " [complocator](complocator-table.md) " zuerst nach Signaturen, der Tabelle " [reglocator](reglocator-table.md) ", der zweiten Tabelle, der Tabelle " [inilocator](inilocator-table.md) " und schließlich der Tabelle " [drlocator](drlocator-table.md) ".</span><span class="sxs-lookup"><span data-stu-id="35651-137">The [AppSearch](appsearch-action.md) action searches for signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table second, the [IniLocator](inilocator-table.md) table third, and finally the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="35651-138">Datei Signaturen werden in der [Signatur](signature-table.md) Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="35651-138">File signatures are listed in the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="35651-139">Eine Signatur, die nicht in der Signatur Tabelle ist, gibt ein Verzeichnis an, und die-Eigenschaft legt die-Eigenschaft auf den Verzeichnispfad für diese Signatur fest.</span><span class="sxs-lookup"><span data-stu-id="35651-139">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="35651-140">Weitere Informationen finden Sie [untersuchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="35651-140">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="35651-141">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="35651-141">Validation</span></span>

<dl>

[<span data-ttu-id="35651-142">ICE03</span><span class="sxs-lookup"><span data-stu-id="35651-142">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="35651-143">ICE06</span><span class="sxs-lookup"><span data-stu-id="35651-143">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="35651-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="35651-144">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="35651-145">ICE52</span><span class="sxs-lookup"><span data-stu-id="35651-145">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="35651-146">ICE88</span><span class="sxs-lookup"><span data-stu-id="35651-146">ICE88</span></span>](ice88.md)  
</dl>

 

 



