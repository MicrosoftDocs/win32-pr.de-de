---
title: Iresultsviewer-Schnittstelle (wdssharedidl. h)
description: Macht Methoden und Eigenschaften für die Ergebnis Ansicht verfügbar.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Iresultviewer-Oberfläche ältere Windows-Umgebungs Features
- Ältere Windows-Umgebungs Features der iresultviewer-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518125"
---
# <a name="iresultsviewer-interface"></a><span data-ttu-id="492d8-105">Iresulensviewer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="492d8-105">IResultsViewer interface</span></span>

> [!NOTE]
> <span data-ttu-id="492d8-106">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="492d8-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="492d8-107">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="492d8-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="492d8-108">Macht Methoden und Eigenschaften für die Ergebnis Ansicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="492d8-108">Exposes methods and properties for the results view.</span></span>

## <a name="members"></a><span data-ttu-id="492d8-109">Member</span><span class="sxs-lookup"><span data-stu-id="492d8-109">Members</span></span>

<span data-ttu-id="492d8-110">Die **iresulensviewer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="492d8-110">The **IResultsViewer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="492d8-111">**Iresulzviewer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="492d8-111">**IResultsViewer** also has these types of members:</span></span>

-   [<span data-ttu-id="492d8-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="492d8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="492d8-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="492d8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="492d8-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="492d8-114">Methods</span></span>

<span data-ttu-id="492d8-115">Die **iresulzviewer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="492d8-115">The **IResultsViewer** interface has these methods.</span></span>



| <span data-ttu-id="492d8-116">Methode</span><span class="sxs-lookup"><span data-stu-id="492d8-116">Method</span></span>                                                   | <span data-ttu-id="492d8-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="492d8-117">Description</span></span>                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="492d8-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="492d8-118">**GoBack**</span></span>](-search-2x-iresultsviewer-goback.md)       | <span data-ttu-id="492d8-119">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="492d8-119">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="492d8-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="492d8-120">**GoForward**</span></span>](-search-2x-iresultsviewer-goforward.md) | <span data-ttu-id="492d8-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="492d8-121">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="492d8-122">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="492d8-122">**Refresh**</span></span>](-search-2x-iresultsviewer-refresh.md)     | <span data-ttu-id="492d8-123">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="492d8-123">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="492d8-124">**Stop**</span><span class="sxs-lookup"><span data-stu-id="492d8-124">**Stop**</span></span>](-search-2x-iresultsviewer-stop.md)           | <span data-ttu-id="492d8-125">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="492d8-125">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="492d8-126">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="492d8-126">**Update**</span></span>](-search-2x-iresultsviewer-update.md)       | <span data-ttu-id="492d8-127">Wendet alle Abfrage Änderungen an und navigiert die Ansicht zum neuen Resultset.</span><span class="sxs-lookup"><span data-stu-id="492d8-127">Applies any query changes and navigates the view to the new set of results.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="492d8-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="492d8-128">Properties</span></span>

<span data-ttu-id="492d8-129">Die **iresulensviewer** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="492d8-129">The **IResultsViewer** interface has these properties.</span></span>



| <span data-ttu-id="492d8-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="492d8-130">Property</span></span>                                                                            | <span data-ttu-id="492d8-131">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="492d8-131">Access type</span></span>           | <span data-ttu-id="492d8-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="492d8-132">Description</span></span>                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="492d8-133">**Inhalte**</span><span class="sxs-lookup"><span data-stu-id="492d8-133">**Contents**</span></span>](-search-2x-iresultsviewer-contents.md)<br/>                   | <span data-ttu-id="492d8-134">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="492d8-134">Write-only</span></span><br/> | <span data-ttu-id="492d8-135">Diese Eigenschaft verfolgt den Typ des Inhalts, der in der Ansicht Ergebnisse angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="492d8-135">This property tracks the type of the content being displayed in the results view.</span></span> <br/>    |
| [<span data-ttu-id="492d8-136">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="492d8-136">**DisplayName**</span></span>](-search-2x-iresultsviewer-displayname.md)<br/>             | <span data-ttu-id="492d8-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="492d8-137">Read-only</span></span><br/>  | <span data-ttu-id="492d8-138">Lokalisierter Anzeige Name des Typs.</span><span class="sxs-lookup"><span data-stu-id="492d8-138">Localized display name of the type.</span></span><br/>                                                   |
| [<span data-ttu-id="492d8-139">**Enumselecteditems**</span><span class="sxs-lookup"><span data-stu-id="492d8-139">**EnumSelectedItems**</span></span>](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | <span data-ttu-id="492d8-140">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="492d8-140">Write-only</span></span><br/> | <span data-ttu-id="492d8-141">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="492d8-141">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="492d8-142">**Filter Type**</span><span class="sxs-lookup"><span data-stu-id="492d8-142">**FilterType**</span></span>](-search-2x-iresultsviewer-filtertype.md)<br/>               | <span data-ttu-id="492d8-143">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="492d8-143">Read/write</span></span><br/> | <span data-ttu-id="492d8-144">Diese Eigenschaft legt den Namen des vorab bereitgestellten Typs fest, nach dem die Ergebnisse gefiltert werden, oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="492d8-144">This property will set or return the name of the preceived type to filter results by.</span></span><br/> |
| [<span data-ttu-id="492d8-145">**HeaderStyle**</span><span class="sxs-lookup"><span data-stu-id="492d8-145">**HeaderStyle**</span></span>](-search-2x-iresultsviewer-headerstyle.md)<br/>             | <span data-ttu-id="492d8-146">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="492d8-146">Read/write</span></span><br/> | <span data-ttu-id="492d8-147">Der Header Stil, der in der Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="492d8-147">The style of header displayed in the view.</span></span><br/>                                            |
| [<span data-ttu-id="492d8-148">**Isupdaten.**</span><span class="sxs-lookup"><span data-stu-id="492d8-148">**IsUpdateNeeded**</span></span>](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | <span data-ttu-id="492d8-149">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="492d8-149">Write-only</span></span><br/> | <span data-ttu-id="492d8-150">Dies gibt true zurück, wenn die Views-Abfrage geändert wurde und aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="492d8-150">This returns TRUE if the views query has been modified and needs updating.</span></span> <br/>           |
| [<span data-ttu-id="492d8-151">**ItemStore**</span><span class="sxs-lookup"><span data-stu-id="492d8-151">**ItemStore**</span></span>](-search-2x-iresultsviewer-itemstore.md)<br/>                 | <span data-ttu-id="492d8-152">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="492d8-152">Read/write</span></span><br/> | <span data-ttu-id="492d8-153">Diese Eigenschaft legt den Namen des Stores fest, nach dem die Ergebnisse gefiltert werden, oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="492d8-153">This property will set or return the name of the store to filter results by.</span></span><br/>          |
| [<span data-ttu-id="492d8-154">**PreviewStyle**</span><span class="sxs-lookup"><span data-stu-id="492d8-154">**PreviewStyle**</span></span>](-search-2x-iresultsviewer-previewstyle.md)<br/>           | <span data-ttu-id="492d8-155">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="492d8-155">Read/write</span></span><br/> | <span data-ttu-id="492d8-156">Steuert den Anzeigemodus des Vorschau Bereichs.</span><span class="sxs-lookup"><span data-stu-id="492d8-156">Controls the preview pane's display mode.</span></span><br/>                                             |
| [<span data-ttu-id="492d8-157">**Propertyfilters**</span><span class="sxs-lookup"><span data-stu-id="492d8-157">**PropertyFilters**</span></span>](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | <span data-ttu-id="492d8-158">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="492d8-158">Write-only</span></span><br/> | <span data-ttu-id="492d8-159">Wenn Sie die Auflistung der Eigenschaften Filter aufrufen, wird Folgendes zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="492d8-159">When calling the property filter collection it will return the following:</span></span><br/>             |
| [<span data-ttu-id="492d8-160">**QueryText**</span><span class="sxs-lookup"><span data-stu-id="492d8-160">**QueryText**</span></span>](-search-2x-iresultsviewer-querytext.md)<br/>                 | <span data-ttu-id="492d8-161">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="492d8-161">Read/write</span></span><br/> | <span data-ttu-id="492d8-162">Ruft den aktuellen Abfragetext ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="492d8-162">Gets or sets the current query text.</span></span><br/>                                                  |
| [<span data-ttu-id="492d8-163">**Resulstistyle**</span><span class="sxs-lookup"><span data-stu-id="492d8-163">**ResultsStyle**</span></span>](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | <span data-ttu-id="492d8-164">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="492d8-164">Write-only</span></span><br/> | <span data-ttu-id="492d8-165">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="492d8-165">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="492d8-166">**Sortorienproperty**</span><span class="sxs-lookup"><span data-stu-id="492d8-166">**SortOrderProperty**</span></span>](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | <span data-ttu-id="492d8-167">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="492d8-167">Read/write</span></span><br/> | <span data-ttu-id="492d8-168">Diese Eigenschaft legt die Reihenfolge der Spalten fest, nach denen die Ergebnisse sortiert werden, oder gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="492d8-168">This property will set or return the order of columns to sort results by.</span></span> <br/>            |
| [<span data-ttu-id="492d8-169">**SortProperty**</span><span class="sxs-lookup"><span data-stu-id="492d8-169">**SortProperty**</span></span>](-search-2x-iresultsviewer-sortproperty.md)<br/>           | <span data-ttu-id="492d8-170">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="492d8-170">Read/write</span></span><br/> | <span data-ttu-id="492d8-171">Diese Eigenschaft legt die indexcolumn der Eigenschaft fest, nach der die Ergebnisse sortiert werden, oder gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="492d8-171">This property will set or return the IndexColumn of the property to sort results by.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="492d8-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="492d8-172">Remarks</span></span>

<span data-ttu-id="492d8-173">Diese Methoden und Eigenschaften werden verwendet, um die angezeigten Informationen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="492d8-173">These methods and properties are used to manipulate the information viewed.</span></span>

## <a name="requirements"></a><span data-ttu-id="492d8-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="492d8-174">Requirements</span></span>



| <span data-ttu-id="492d8-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="492d8-175">Requirement</span></span> | <span data-ttu-id="492d8-176">Wert</span><span class="sxs-lookup"><span data-stu-id="492d8-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="492d8-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="492d8-177">Minimum supported client</span></span><br/> | <span data-ttu-id="492d8-178">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="492d8-178">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="492d8-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="492d8-179">Minimum supported server</span></span><br/> | <span data-ttu-id="492d8-180">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="492d8-180">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="492d8-181">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="492d8-181">Redistributable</span></span><br/>          | <span data-ttu-id="492d8-182">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="492d8-182">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="492d8-183">Header</span><span class="sxs-lookup"><span data-stu-id="492d8-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="492d8-184"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="492d8-184"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

