---
description: Die Tabelle "Aktions Text" enthält Text, der in einem Status Dialogfeld angezeigt und in das Protokoll geschrieben wird, um Aktionen auszuführen, deren Ausführung viel Zeit in Anspruch nimmt. Der angezeigte Text besteht aus der Aktions Beschreibung und optional formatierten Daten aus der Aktion.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Tabelle "aktiontext"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351640"
---
# <a name="actiontext-table"></a><span data-ttu-id="3d401-104">Tabelle "aktiontext"</span><span class="sxs-lookup"><span data-stu-id="3d401-104">ActionText Table</span></span>

<span data-ttu-id="3d401-105">Die Tabelle "Aktions Text" enthält Text, der in einem Status Dialogfeld angezeigt und in das Protokoll geschrieben wird, um Aktionen auszuführen, deren Ausführung viel Zeit in Anspruch nimmt.</span><span class="sxs-lookup"><span data-stu-id="3d401-105">The ActionText Table contains text to be displayed in a progress dialog box, and written to the log for actions that take a long time to execute.</span></span> <span data-ttu-id="3d401-106">Der angezeigte Text besteht aus der Aktions Beschreibung und optional formatierten Daten aus der Aktion.</span><span class="sxs-lookup"><span data-stu-id="3d401-106">The displayed text consists of the action description and optionally formatted data from the action.</span></span>

<span data-ttu-id="3d401-107">Die Tabelle "aktiontext" enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="3d401-107">The ActionText Table has the following columns.</span></span>



| <span data-ttu-id="3d401-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="3d401-108">Column</span></span>      | <span data-ttu-id="3d401-109">Typ</span><span class="sxs-lookup"><span data-stu-id="3d401-109">Type</span></span>                         | <span data-ttu-id="3d401-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="3d401-110">Key</span></span> | <span data-ttu-id="3d401-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="3d401-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="3d401-112">Aktion</span><span class="sxs-lookup"><span data-stu-id="3d401-112">Action</span></span>      | [<span data-ttu-id="3d401-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="3d401-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="3d401-114">J</span><span class="sxs-lookup"><span data-stu-id="3d401-114">Y</span></span>   | <span data-ttu-id="3d401-115">N</span><span class="sxs-lookup"><span data-stu-id="3d401-115">N</span></span>        |
| <span data-ttu-id="3d401-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d401-116">Description</span></span> | [<span data-ttu-id="3d401-117">Text</span><span class="sxs-lookup"><span data-stu-id="3d401-117">Text</span></span>](text.md)             | <span data-ttu-id="3d401-118">N</span><span class="sxs-lookup"><span data-stu-id="3d401-118">N</span></span>   | <span data-ttu-id="3d401-119">J</span><span class="sxs-lookup"><span data-stu-id="3d401-119">Y</span></span>        |
| <span data-ttu-id="3d401-120">Vorlage</span><span class="sxs-lookup"><span data-stu-id="3d401-120">Template</span></span>    | [<span data-ttu-id="3d401-121">Vorlage</span><span class="sxs-lookup"><span data-stu-id="3d401-121">Template</span></span>](template.md)     | <span data-ttu-id="3d401-122">N</span><span class="sxs-lookup"><span data-stu-id="3d401-122">N</span></span>   | <span data-ttu-id="3d401-123">J</span><span class="sxs-lookup"><span data-stu-id="3d401-123">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3d401-124">Spalten</span><span class="sxs-lookup"><span data-stu-id="3d401-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3d401-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="3d401-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="3d401-126">Name der Aktion.</span><span class="sxs-lookup"><span data-stu-id="3d401-126">Name of the action.</span></span>

<span data-ttu-id="3d401-127">Primärer Tabellenschlüssel.</span><span class="sxs-lookup"><span data-stu-id="3d401-127">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="3d401-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d401-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="3d401-129">Lokalisierte Beschreibung, die im Dialogfeld "Status" angezeigt wird oder in das Protokoll geschrieben wird, wenn die Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d401-129">Localized description that is displayed in the progress dialog box, or written to the log when the action is executing.</span></span>

</dd> <dt>

<span data-ttu-id="3d401-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Fungiert</span><span class="sxs-lookup"><span data-stu-id="3d401-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Template</span></span>
</dt> <dd>

<span data-ttu-id="3d401-131">Eine lokalisierte Formatvorlage, mit der Aktions Datensätze formatiert werden, die während der Ausführung der Aktion angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3d401-131">A localized format template that is used to format action data records to display during action execution.</span></span> <span data-ttu-id="3d401-132">Wenn keine Vorlage bereitgestellt wird, werden die Aktions Daten nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d401-132">If a template is not supplied, then the action data is not displayed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d401-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d401-133">Remarks</span></span>

<span data-ttu-id="3d401-134">In der Regel beziehen sich die Einträge in der Tabelle "Aktions Text" auf Aktionen in Sequenz Tabellen.</span><span class="sxs-lookup"><span data-stu-id="3d401-134">Typically, the entries in the ActionText table refer to actions in sequence tables.</span></span> <span data-ttu-id="3d401-135">Der Installer führt andere Aktionen aus, die nicht in der Sequenz Tabelle aufgeführt sind, aber trotzdem in der Tabelle angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3d401-135">There are other actions the installer performs that are not listed in the sequence table, but still need to be specified in the table.</span></span> <span data-ttu-id="3d401-136">In der folgenden Tabelle sind die erforderlichen Tabelleneinträge aufgeführt, in denen der Aktionsname und die Vorlage genau wie gezeigt erstellt werden müssen, aber die Beschreibung kann angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="3d401-136">The following table identifies the required table entries where the action name and template must be authored exactly as shown, but the description can be customized.</span></span>



| <span data-ttu-id="3d401-137">Aktion</span><span class="sxs-lookup"><span data-stu-id="3d401-137">Action</span></span>          | <span data-ttu-id="3d401-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d401-138">Description</span></span>                             | <span data-ttu-id="3d401-139">Vorlage</span><span class="sxs-lookup"><span data-stu-id="3d401-139">Template</span></span> |
|-----------------|-----------------------------------------|----------|
| <span data-ttu-id="3d401-140">Rollback</span><span class="sxs-lookup"><span data-stu-id="3d401-140">Rollback</span></span>        | <span data-ttu-id="3d401-141">Macht Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="3d401-141">Undoes actions.</span></span>                         | <span data-ttu-id="3d401-142">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3d401-142">\[1\]</span></span>    |
| <span data-ttu-id="3d401-143">Rollbackcleanup</span><span class="sxs-lookup"><span data-stu-id="3d401-143">RollbackCleanup</span></span> | <span data-ttu-id="3d401-144">Entfernt alte Dateien.</span><span class="sxs-lookup"><span data-stu-id="3d401-144">Removes old files.</span></span>                      | <span data-ttu-id="3d401-145">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3d401-145">\[1\]</span></span>    |
| <span data-ttu-id="3d401-146">Generatescript</span><span class="sxs-lookup"><span data-stu-id="3d401-146">GenerateScript</span></span>  | <span data-ttu-id="3d401-147">Generiert System Vorgänge für-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="3d401-147">Generates system operations for action.</span></span> | <span data-ttu-id="3d401-148">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3d401-148">\[1\]</span></span>    |



 

> [!Note]  
> <span data-ttu-id="3d401-149">Der Aktions Text wird nur für Aktionen angezeigt, die innerhalb des Installations Skripts ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3d401-149">Action text is only displayed for actions that run within the installation script.</span></span> <span data-ttu-id="3d401-150">Daher wird der Aktions Text nur für Aktionen angezeigt, die zwischen den Aktionen [InstallInitialize](installinitialize-action.md) und [InstallFinalize](installfinalize-action.md) sequenziert werden.</span><span class="sxs-lookup"><span data-stu-id="3d401-150">Therefore, action text is only displayed for actions that are sequenced between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

 

<span data-ttu-id="3d401-151">Sie können eine lokalisierte Aktions Text Tabelle mithilfe von Msidb.exe oder [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)in die-Datenbank importieren.</span><span class="sxs-lookup"><span data-stu-id="3d401-151">You can import a localized ActionText table into your database by using Msidb.exe or [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="3d401-152">Das SDK enthält eine lokalisierte Aktions Text Tabelle für jede der Sprachen, die im Abschnitt [lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md) aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="3d401-152">The SDK includes a localized ActionText Table for each of the languages listed in the [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) section.</span></span> <span data-ttu-id="3d401-153">Wenn die Aktions Text Tabelle nicht aufgefüllt ist, lädt das Installationsprogramm lokalisierte Zeichen folgen für die Sprache, die von der [**productlanguage**](productlanguage.md) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3d401-153">If the ActionText table is not populated, the installer loads localized strings for the language specified by the [**ProductLanguage**](productlanguage.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="3d401-154">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="3d401-154">Validation</span></span>

<dl>

[<span data-ttu-id="3d401-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="3d401-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3d401-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="3d401-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3d401-157">ICE46</span><span class="sxs-lookup"><span data-stu-id="3d401-157">ICE46</span></span>](ice46.md)  
</dl>

 

 



