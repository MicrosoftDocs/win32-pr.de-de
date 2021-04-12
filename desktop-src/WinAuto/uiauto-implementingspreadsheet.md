---
title: Tabellen Steuerungs Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ispreadsheetprovider, einschließlich Informationen zu-Methoden.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Tabellen Steuerungs Musters
- Benutzeroberflächenautomatisierungs-, Tabellen Steuerungs Muster
- UI-Automatisierung, ispreadsheetprovider
- ISpreadsheetProvider
- Implementieren des Steuerelement Musters der Benutzeroberflächen Automatisierung
- Tabellen Steuerungs Muster
- Steuerelement Muster, ispreadsheetprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Tabelle
- Steuerelement Muster, Tabelle
- Schnittstellen, ispreadsheetprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315776"
---
# <a name="spreadsheet-control-pattern"></a><span data-ttu-id="22f81-113">Tabellen Steuerungs Muster</span><span class="sxs-lookup"><span data-stu-id="22f81-113">Spreadsheet Control Pattern</span></span>

<span data-ttu-id="22f81-114">Beschreibt Richtlinien und Konventionen für das Implementieren von [**ispreadsheetprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), einschließlich Informationen zu-Methoden.</span><span class="sxs-lookup"><span data-stu-id="22f81-114">Describes guidelines and conventions for implementing [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), including information about methods.</span></span> <span data-ttu-id="22f81-115">Links zu zusätzlichen Referenzen sind am Ende dieses Themas aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="22f81-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="22f81-116">Das **Tabellen** Steuerungs Muster wird verwendet, um den Inhalt einer Kalkulations Tabelle oder eines anderen Raster basierten Dokuments verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="22f81-116">The **Spreadsheet** control pattern is used to expose the contents of a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="22f81-117">Das **Tabellen** Steuerelement-Muster ist eng mit dem [Raster](uiauto-implementinggrid.md) Steuerelement Muster verknüpft. Steuerelemente, die das **Tabellen** Steuerelement-Muster implementieren, sollten auch das Raster-Steuerelement Muster implementieren.</span><span class="sxs-lookup"><span data-stu-id="22f81-117">The **Spreadsheet** control pattern is closely related to the [Grid](uiauto-implementinggrid.md) control pattern; controls that implement the **Spreadsheet** control pattern should also implement the Grid control pattern.</span></span> <span data-ttu-id="22f81-118">Steuerelemente können ggf. auch das [Table](uiauto-implementingtable.md) -Steuerelement Muster implementieren.</span><span class="sxs-lookup"><span data-stu-id="22f81-118">Controls can also implement the [Table](uiauto-implementingtable.md) control pattern, if appropriate.</span></span> <span data-ttu-id="22f81-119">Beispiele für Steuerelemente, die diese Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="22f81-119">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="22f81-120">Implementierungsrichtlinien und -konventionen</span><span class="sxs-lookup"><span data-stu-id="22f81-120">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="22f81-121">Beachten Sie beim Implementieren des **Tabellen** Steuerelement-Musters die folgenden Richtlinien und Konventionen:</span><span class="sxs-lookup"><span data-stu-id="22f81-121">When implementing the **Spreadsheet** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="22f81-122">Wenn eine Kalkulations Tabelle die Schnittstelle [**ispreadsheetprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) implementiert, muss die Zelle die [**ispreadsheetitemprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="22f81-122">If a spreadsheet implements the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface, its cells must implement the [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>
-   <span data-ttu-id="22f81-123">Die [**ispreadsheetprovider:: GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) -Methode soll die gleiche Art von Navigation bereitstellen, die eine Anwendung möglicherweise mit einer Funktion **zum Springen zur Bezeichnung** bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="22f81-123">The [**ISpreadsheetProvider::GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) method is intended to provide the same kind of navigation that an application might supply with a **Jump to Label** feature.</span></span> <span data-ttu-id="22f81-124">Bei vielen Tabellen Kalkulations Programmen können bestimmte Zellen einen anzeigen Amen oder eine Bezeichnung erhalten.</span><span class="sxs-lookup"><span data-stu-id="22f81-124">Many spreadsheet programs let specific cells be given a friendly name or label.</span></span> <span data-ttu-id="22f81-125">**GetItemByName** ermöglicht es dem Client, eine Zelle auf der Grundlage des anzeigen Amens zu suchen.</span><span class="sxs-lookup"><span data-stu-id="22f81-125">**GetItemByName** enables the client to look up a cell based on its friendly name.</span></span> <span data-ttu-id="22f81-126">Diese Methode sollte keine Zellen abrufen, die den Namenstext enthalten, da die Ergebnisse sehr mehrdeutig sein können.</span><span class="sxs-lookup"><span data-stu-id="22f81-126">This method should not retrieve any cells that contain the name text because the results can be highly ambiguous.</span></span> <span data-ttu-id="22f81-127">Wenn das Tabellen Kalkulations Programm zulässt, dass mehrere Zellen in derselben Tabelle denselben anzeigen Amen oder eine gleiche Bezeichnung aufweisen, ist das Verhalten der Microsoft-Benutzeroberflächen Automatisierung nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="22f81-127">If the spreadsheet program allows multiple cells in the same a spreadsheet to have the same friendly name or label, the Microsoft UI Automation behavior is undefined.</span></span>

## <a name="required-members-for-ispreadsheetprovider"></a><span data-ttu-id="22f81-128">Erforderliche Member für **ispreadsheetprovider**</span><span class="sxs-lookup"><span data-stu-id="22f81-128">Required Members for **ISpreadsheetProvider**</span></span>

<span data-ttu-id="22f81-129">Die folgende Methode ist für die Implementierung der [**ispreadsheetprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) -Schnittstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="22f81-129">The following method is required for implementing the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface.</span></span>



| <span data-ttu-id="22f81-130">Erforderliche Member</span><span class="sxs-lookup"><span data-stu-id="22f81-130">Required members</span></span>                                                       | <span data-ttu-id="22f81-131">Memberart</span><span class="sxs-lookup"><span data-stu-id="22f81-131">Member type</span></span> | <span data-ttu-id="22f81-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22f81-132">Notes</span></span> |
|------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="22f81-133">**GetItemByName**</span><span class="sxs-lookup"><span data-stu-id="22f81-133">**GetItemByName**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | <span data-ttu-id="22f81-134">Methode</span><span class="sxs-lookup"><span data-stu-id="22f81-134">Method</span></span>      | <span data-ttu-id="22f81-135">Keine</span><span class="sxs-lookup"><span data-stu-id="22f81-135">None</span></span>  |



 

<span data-ttu-id="22f81-136">Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="22f81-136">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22f81-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22f81-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22f81-138">Steuerelement Typen und ihre unterstützten Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22f81-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="22f81-139">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="22f81-139">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="22f81-140">Übersicht über die Benutzeroberflächenautomatisierungs-Struktur</span><span class="sxs-lookup"><span data-stu-id="22f81-140">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 