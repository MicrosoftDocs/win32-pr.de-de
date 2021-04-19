---
description: Die Erweiterungs Tabelle enthält Informationen zu Dateinamen Erweiterungs Servern, die als Teil der Produktankündigung generiert werden müssen. Jede Zeile generiert einen Satz von Registrierungs Schlüsseln und-Werten.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Erweiterungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350545"
---
# <a name="extension-table"></a><span data-ttu-id="e9531-104">Erweiterungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="e9531-104">Extension Table</span></span>

<span data-ttu-id="e9531-105">Die Erweiterungs Tabelle enthält Informationen zu Dateinamen Erweiterungs Servern, die als Teil der Produktankündigung generiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e9531-105">The Extension table contains information about file name extension servers that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="e9531-106">Jede Zeile generiert einen Satz von Registrierungs Schlüsseln und-Werten.</span><span class="sxs-lookup"><span data-stu-id="e9531-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="e9531-107">Die Erweiterungs Tabelle enthält die Spalten, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e9531-107">The Extension table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="e9531-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="e9531-108">Column</span></span>      | <span data-ttu-id="e9531-109">Typ</span><span class="sxs-lookup"><span data-stu-id="e9531-109">Type</span></span>                         | <span data-ttu-id="e9531-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e9531-110">Key</span></span> | <span data-ttu-id="e9531-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="e9531-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="e9531-112">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="e9531-112">Extension</span></span>   | [<span data-ttu-id="e9531-113">Text</span><span class="sxs-lookup"><span data-stu-id="e9531-113">Text</span></span>](text.md)             | <span data-ttu-id="e9531-114">J</span><span class="sxs-lookup"><span data-stu-id="e9531-114">Y</span></span>   | <span data-ttu-id="e9531-115">N</span><span class="sxs-lookup"><span data-stu-id="e9531-115">N</span></span>        |
| <span data-ttu-id="e9531-116">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="e9531-116">Component\_</span></span> | [<span data-ttu-id="e9531-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e9531-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="e9531-118">J</span><span class="sxs-lookup"><span data-stu-id="e9531-118">Y</span></span>   | <span data-ttu-id="e9531-119">N</span><span class="sxs-lookup"><span data-stu-id="e9531-119">N</span></span>        |
| <span data-ttu-id="e9531-120">ProgID\_</span><span class="sxs-lookup"><span data-stu-id="e9531-120">ProgId\_</span></span>    | [<span data-ttu-id="e9531-121">Text</span><span class="sxs-lookup"><span data-stu-id="e9531-121">Text</span></span>](text.md)             | <span data-ttu-id="e9531-122">N</span><span class="sxs-lookup"><span data-stu-id="e9531-122">N</span></span>   | <span data-ttu-id="e9531-123">J</span><span class="sxs-lookup"><span data-stu-id="e9531-123">Y</span></span>        |
| <span data-ttu-id="e9531-124">Medi\_</span><span class="sxs-lookup"><span data-stu-id="e9531-124">MIME\_</span></span>      | [<span data-ttu-id="e9531-125">Text</span><span class="sxs-lookup"><span data-stu-id="e9531-125">Text</span></span>](text.md)             | <span data-ttu-id="e9531-126">N</span><span class="sxs-lookup"><span data-stu-id="e9531-126">N</span></span>   | <span data-ttu-id="e9531-127">J</span><span class="sxs-lookup"><span data-stu-id="e9531-127">Y</span></span>        |
| <span data-ttu-id="e9531-128">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="e9531-128">Feature\_</span></span>   | [<span data-ttu-id="e9531-129">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e9531-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="e9531-130">N</span><span class="sxs-lookup"><span data-stu-id="e9531-130">N</span></span>   | <span data-ttu-id="e9531-131">N</span><span class="sxs-lookup"><span data-stu-id="e9531-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e9531-132">Spalten</span><span class="sxs-lookup"><span data-stu-id="e9531-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e9531-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Weiterung</span><span class="sxs-lookup"><span data-stu-id="e9531-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extension</span></span>
</dt> <dd>

<span data-ttu-id="e9531-134">Die der Tabellenzeile zugeordnete Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="e9531-134">The extension associated with the table row.</span></span> <span data-ttu-id="e9531-135">Die Erweiterung kann bis zu 255 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="e9531-135">The extension can be up to 255 characters long.</span></span> <span data-ttu-id="e9531-136">Geben Sie die Erweiterung in diesem Feld ohne den vorangehenden Zeitraum ein.</span><span class="sxs-lookup"><span data-stu-id="e9531-136">Enter the extension in this field without the preceding period.</span></span>

</dd> <dt>

<span data-ttu-id="e9531-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="e9531-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="e9531-138">Ein externer Schlüssel für die erste Spalte der [Komponenten](component-table.md) Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e9531-138">An external key to the first column of the [Component](component-table.md) table.</span></span> <span data-ttu-id="e9531-139">Diese Spalte verweist auf die Komponente, mit der die Installation der Erweiterung gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="e9531-139">This column references the component that controls the installation of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="e9531-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgID\_</span><span class="sxs-lookup"><span data-stu-id="e9531-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span></span>
</dt> <dd>

<span data-ttu-id="e9531-141">Die Programm-ID, die dieser Erweiterung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e9531-141">The Program ID associated with this extension.</span></span> <span data-ttu-id="e9531-142">Dabei handelt es sich um einen Fremdschlüssel in der [ProgID](progid-table.md) -Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e9531-142">This is a foreign key into the [ProgId](progid-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="e9531-143"><span id="MIME_"></span><span id="mime_"></span>Medi\_</span><span class="sxs-lookup"><span data-stu-id="e9531-143"><span id="MIME_"></span><span id="mime_"></span>MIME\_</span></span>
</dt> <dd>

<span data-ttu-id="e9531-144">Der Inhaltstyp, der für die Erweiterungs Spalte geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9531-144">The Content Type that is to be written for the Extension column.</span></span>

<span data-ttu-id="e9531-145">Ein externer Schlüssel für die erste Spalte der [MIME](mime-table.md) -Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e9531-145">An external key to the first column of the [MIME](mime-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="e9531-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="e9531-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="e9531-147">Ein externer Schlüssel in der ersten [Spalte der Featuretabelle,](feature-table.md) der das Feature angibt, das den Erweiterungs Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e9531-147">An external key into the first column of the [Feature](feature-table.md) table specifying the feature that provides the extension server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9531-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9531-148">Remarks</span></span>

<span data-ttu-id="e9531-149">Auf die Erweiterungs Tabelle wird verwiesen, wenn die [RegisterExtensionInfo](registerextensioninfo-action.md) -Aktion oder die [unregisterextensioninfo](unregisterextensioninfo-action.md) -Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9531-149">The Extension table is referred to when the [RegisterExtensionInfo](registerextensioninfo-action.md) action or the [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) action is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="e9531-150">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="e9531-150">Validation</span></span>

<dl>

[<span data-ttu-id="e9531-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="e9531-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e9531-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="e9531-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e9531-153">ICE15</span><span class="sxs-lookup"><span data-stu-id="e9531-153">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="e9531-154">ICE19</span><span class="sxs-lookup"><span data-stu-id="e9531-154">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="e9531-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="e9531-155">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e9531-156">ICE41</span><span class="sxs-lookup"><span data-stu-id="e9531-156">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="e9531-157">ICE69</span><span class="sxs-lookup"><span data-stu-id="e9531-157">ICE69</span></span>](ice69.md)  
</dl>

 

 



