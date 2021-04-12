---
description: Im folgenden Verfahren werden die allgemeinen Schritte zum Erstellen von Mergemodulen beschrieben.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Erstellen von Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215711"
---
# <a name="authoring-merge-modules"></a><span data-ttu-id="7f861-103">Erstellen von Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="7f861-103">Authoring Merge Modules</span></span>

<span data-ttu-id="7f861-104">Im folgenden Verfahren werden die allgemeinen Schritte zum Erstellen von Mergemodulen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7f861-104">The following procedure describes the general steps to authoring merge modules.</span></span>

<span data-ttu-id="7f861-105">**So erstellen Sie ein neues Mergemodul**</span><span class="sxs-lookup"><span data-stu-id="7f861-105">**To create a new merge module**</span></span>

1.  <span data-ttu-id="7f861-106">Beziehen Sie ein Software Tool, das Sie zum Bearbeiten der mergemoduldatenbank verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7f861-106">Obtain a software tool you can use to edit the merge module database.</span></span>
2.  <span data-ttu-id="7f861-107">Abrufen einer leeren mergemoduldatenbank.</span><span class="sxs-lookup"><span data-stu-id="7f861-107">Obtain a blank merge module database.</span></span>
3.  <span data-ttu-id="7f861-108">Generieren Sie eine [GUID](guid.md) für das Mergemodul.</span><span class="sxs-lookup"><span data-stu-id="7f861-108">Generate a [GUID](guid.md) for the merge module.</span></span> <span data-ttu-id="7f861-109">Sie müssen diese GUID verwenden, wenn Sie die Primärschlüssel von Datenbanktabellen im Mergemodul erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f861-109">You need to use this GUID when authoring the primary keys of database tables in the merge module.</span></span>
4.  <span data-ttu-id="7f861-110">Fügen Sie der [Komponenten Tabelle](component-table.md) für jede von der Zusammenführung gelieferte Komponente einen Datensatz hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f861-110">Add a record to the [Component table](component-table.md) for each component delivered by the merge.</span></span> <span data-ttu-id="7f861-111">Eine Komponenten Tabelle ist in jedem Mergemodul erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f861-111">A Component table is required in every merge module.</span></span> <span data-ttu-id="7f861-112">Beachten Sie, dass Mergemodule mit-Komponenten arbeiten und nicht mit-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="7f861-112">Note that merge modules operate with components and not with features.</span></span> <span data-ttu-id="7f861-113">In bestimmten Fällen muss ein Datenbanktabellen Eintrag jedoch möglicherweise auf eine Funktion verweisen.</span><span class="sxs-lookup"><span data-stu-id="7f861-113">In certain cases, however, a database table entry may need to reference a feature.</span></span> <span data-ttu-id="7f861-114">Weitere Informationen finden Sie unter [verweisen auf Features in Mergemodulen](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="7f861-114">For details, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>
5.  <span data-ttu-id="7f861-115">Fügen Sie dem Mergemodul eine [Verzeichnis Tabelle](directory-table.md) hinzu, die das Layout der Verzeichnisse angibt, die das Mergemodul der Zieldatenbank hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="7f861-115">Add a [Directory table](directory-table.md) to the merge module that specifies the layout of directories the merge module adds to the target database.</span></span> <span data-ttu-id="7f861-116">Eine Verzeichnis Tabelle ist in jedem Mergemodul erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f861-116">A Directory table is required in every merge module.</span></span>
6.  <span data-ttu-id="7f861-117">Importieren Sie eine leere [FeatureComponents-Tabelle](featurecomponents-table.md) in die mergemoduldatenbank.</span><span class="sxs-lookup"><span data-stu-id="7f861-117">Import a blank [FeatureComponents table](featurecomponents-table.md) into the merge module database.</span></span> <span data-ttu-id="7f861-118">Diese leere Tabelle stellt eine Richtlinie für das Mergetool in Fällen bereit, in denen die MSI-Datei keine eigene FeatureComponents-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="7f861-118">This empty table provides a guideline for the merge tool in cases where the .msi file does not contain its own FeatureComponents table.</span></span>
7.  <span data-ttu-id="7f861-119">Sammeln Sie alle von diesem Mergemodul gelieferten Dateien, und erstellen Sie die [MergeModule.CABinet](mergemodule-cabinet.md) -CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="7f861-119">Collect all the files delivered by this merge module and create the [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file.</span></span> <span data-ttu-id="7f861-120">Fügen Sie die CAB-Datei dem Mergemodul als Stream in der MSM-Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f861-120">Add the cabinet to the merge module as a stream inside the .msm file.</span></span>
8.  <span data-ttu-id="7f861-121">Fügen Sie der Dateitabelle einen Datensatz für jede Datei hinzu, die in MergeModule.CABinet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7f861-121">Add a record to the File table for every file stored in MergeModule.CABinet.</span></span>
9.  <span data-ttu-id="7f861-122">Fügen Sie die erforderlichen Informationen hinzu, um das Mergemodul in der [ModuleSignature-Tabelle](modulesignature-table.md)zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7f861-122">Add the information necessary to identify the merge module in the [ModuleSignature table](modulesignature-table.md).</span></span> <span data-ttu-id="7f861-123">Jedes Mergemodul erfordert eine ModuleSignature-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7f861-123">Every merge module requires a ModuleSignature table.</span></span>
10. <span data-ttu-id="7f861-124">Listet die Komponenten im Mergemodul in der [modulecomponents-Tabelle](modulecomponents-table.md)auf.</span><span class="sxs-lookup"><span data-stu-id="7f861-124">List the components in the merge module in the [ModuleComponents table](modulecomponents-table.md).</span></span> <span data-ttu-id="7f861-125">Jedes Mergemodul erfordert eine modulecomponents-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7f861-125">Every merge module requires a ModuleComponents table.</span></span>
11. <span data-ttu-id="7f861-126">Fügen Sie der MSM-Datei Mergemodul-Sequenz Tabellen nur dann hinzu, wenn das Mergemodul die [*Sequenz Tabellen*](s-gly.md) der Ziel Installations Datenbank ändern muss.</span><span class="sxs-lookup"><span data-stu-id="7f861-126">Add merge module sequence tables to the .msm file only if the merge module needs to modify the [*sequence tables*](s-gly.md) of the target installation database.</span></span>
12. <span data-ttu-id="7f861-127">Fügen Sie \_ dem Mergemodul eine Validierungs Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f861-127">Add a \_Validation table to the merge module.</span></span> <span data-ttu-id="7f861-128">Ein Mergemodul benötigt eine \_ Validierungs Tabelle, um die Überprüfung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="7f861-128">A merge module requires a \_Validation table to pass validation.</span></span>
13. <span data-ttu-id="7f861-129">Mergemodule erfordern nur in seltenen Fällen eine Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="7f861-129">Merge modules require a user interface in only rare cases.</span></span> <span data-ttu-id="7f861-130">Das Einschließen einer Benutzeroberfläche mit einem Mergemodul ist nicht empfehlenswert.</span><span class="sxs-lookup"><span data-stu-id="7f861-130">Including a UI with a merge module is not recommended.</span></span> <span data-ttu-id="7f861-131">In Fällen, in denen eine Benutzeroberfläche erforderlich ist, können die UI-Tabellen wie andere Tabellen in der MSI-Datei zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7f861-131">In cases where a user interface is required, the UI tables can be merged into the .msi file the same as other tables.</span></span>
14. <span data-ttu-id="7f861-132">Fügen Sie Registrierungsinformationen zu den entsprechenden Registrierungs Tabellen in der mergemoduldatenbank hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f861-132">Add registry information to the appropriate registry tables in the merge module database.</span></span> <span data-ttu-id="7f861-133">Fügen Sie Registrierungsinformationen für Typbibliotheken, Klassen, Erweiterungen und Verben in die Tabellen [typelib](typelib-table.md), [Klasse](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)oder [MIME](mime-table.md) ein.</span><span class="sxs-lookup"><span data-stu-id="7f861-133">Add registry information for type libraries, classes, extensions, and verbs into the [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="7f861-134">Alle anderen Registrierungsinformationen können in der [Registrierungs Tabelle](registry-table.md)angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7f861-134">All other registry information can go into the [Registry table](registry-table.md).</span></span> <span data-ttu-id="7f861-135">Die Verwendung der Tabelle "selfreg" wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="7f861-135">The use of the SelfReg table is not recommended.</span></span>
15. <span data-ttu-id="7f861-136">Fügen Sie die Zusammenfassungs Informationen zum [Zusammenfassungs Informationsdaten Strom für Zusammenfassungs Module](merge-module-summary-information-stream-reference.md)hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f861-136">Add the summary information to the [Merge Module Summary Information Stream](merge-module-summary-information-stream-reference.md).</span></span>
16. <span data-ttu-id="7f861-137">Führen Sie die Überprüfung für alle Mergemodule aus, bevor Sie versuchen,</span><span class="sxs-lookup"><span data-stu-id="7f861-137">Run validation on all merge modules before attempting to install.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f861-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f861-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f861-139">Abrufen von leeren mergemoduldatenbanken</span><span class="sxs-lookup"><span data-stu-id="7f861-139">Obtaining Blank Merge Module Databases</span></span>](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="7f861-140">Abrufen von mergemodulauthoring-Tools</span><span class="sxs-lookup"><span data-stu-id="7f861-140">Obtaining Merge Module Authoring Tools</span></span>](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[<span data-ttu-id="7f861-141">Benennen von primär Schlüsseln in mergemoduldatenbanken</span><span class="sxs-lookup"><span data-stu-id="7f861-141">Naming Primary Keys in Merge Module Databases</span></span>](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[<span data-ttu-id="7f861-142">Erstellen von Komponenten Tabellen für Mergemodule</span><span class="sxs-lookup"><span data-stu-id="7f861-142">Authoring Merge Module Component Tables</span></span>](authoring-merge-module-component-tables.md)
</dt> <dt>

[<span data-ttu-id="7f861-143">Erstellen von mergemodulverzeichnistabellen</span><span class="sxs-lookup"><span data-stu-id="7f861-143">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="7f861-144">Erstellen von FeatureComponents-Tabellen für Mergemodule</span><span class="sxs-lookup"><span data-stu-id="7f861-144">Authoring Merge Module FeatureComponents Tables</span></span>](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="7f861-145">Erstellen von MergeModule.CABinet-CAB-Dateien</span><span class="sxs-lookup"><span data-stu-id="7f861-145">Generating MergeModule.CABinet Cabinet Files</span></span>](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[<span data-ttu-id="7f861-146">Erstellen von Mergemodul-Datei Tabellen</span><span class="sxs-lookup"><span data-stu-id="7f861-146">Authoring Merge Module File Tables</span></span>](authoring-merge-module-file-tables.md)
</dt> <dt>

[<span data-ttu-id="7f861-147">Erstellen von ModuleSignature-Tabellen</span><span class="sxs-lookup"><span data-stu-id="7f861-147">Authoring ModuleSignature Tables</span></span>](authoring-modulesignature-tables.md)
</dt> <dt>

[<span data-ttu-id="7f861-148">Erstellen von modulecomponents-Tabellen</span><span class="sxs-lookup"><span data-stu-id="7f861-148">Authoring ModuleComponents Tables</span></span>](authoring-modulecomponents-tables.md)
</dt> <dt>

[<span data-ttu-id="7f861-149">Erstellen von Mergemodul-Sequenz Tabellen</span><span class="sxs-lookup"><span data-stu-id="7f861-149">Authoring Merge Module Sequence Tables</span></span>](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[<span data-ttu-id="7f861-150">Validieren von Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="7f861-150">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="7f861-151">Erstellen von Benutzeroberflächen in Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="7f861-151">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="7f861-152">Erstellen von Mergemodul-Registrierungs Tabellen</span><span class="sxs-lookup"><span data-stu-id="7f861-152">Authoring Merge Module Registry Tables</span></span>](authoring-merge-module-registry-tables.md)
</dt> <dt>

[<span data-ttu-id="7f861-153">Erstellen von Zusammenfassungs Datenströmen für Zusammenfassungs Module</span><span class="sxs-lookup"><span data-stu-id="7f861-153">Authoring Merge Module Summary Information Streams</span></span>](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[<span data-ttu-id="7f861-154">Zusammenfassungs Informationsdaten Strom Referenz für Zusammenfassungs Modul</span><span class="sxs-lookup"><span data-stu-id="7f861-154">Merge Module Summary Information Stream Reference</span></span>](merge-module-summary-information-stream-reference.md)
</dt> <dt>

<span data-ttu-id="7f861-155">Validieren von Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="7f861-155">Validating Merge Modules</span></span>
</dt> <dt>

[<span data-ttu-id="7f861-156">Verwenden von 64-Bit-Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="7f861-156">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



