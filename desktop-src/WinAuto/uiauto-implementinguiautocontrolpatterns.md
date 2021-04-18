---
title: Implementieren von Steuerungs Mustern für Benutzeroberflächen Automatisierung
description: Dieser Abschnitt enthält ausführliche Informationen zum Implementieren der Microsoft UI Automation Provider-Schnittstellen, die Steuerelement Muster unterstützen.
ms.assetid: d1baa245-62a1-40b1-a671-e227dd3df60a
keywords:
- Benutzeroberflächen Automatisierung, Implementieren von Steuerelement Mustern
- Benutzeroberflächenautomatisierungs, Steuerelement Muster
- Implementieren von Steuerungs Mustern für Benutzeroberflächen Automatisierung
- Steuerelement Muster, Implementieren der Benutzeroberflächen Automatisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfb75b6b275fee9230eb25d9a0b02e1da26ad4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340511"
---
# <a name="implementing-ui-automation-control-patterns"></a><span data-ttu-id="22118-107">Implementieren von Steuerungs Mustern für Benutzeroberflächen Automatisierung</span><span class="sxs-lookup"><span data-stu-id="22118-107">Implementing UI Automation Control Patterns</span></span>

<span data-ttu-id="22118-108">Dieser Abschnitt enthält ausführliche Informationen zum Implementieren der Microsoft UI Automation Provider-Schnittstellen, die Steuerelement Muster unterstützen.</span><span class="sxs-lookup"><span data-stu-id="22118-108">This section provides detailed information about implementing the Microsoft UI Automation provider interfaces that support control patterns.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22118-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="22118-109">In this section</span></span>

-   [<span data-ttu-id="22118-110">Annotation-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-110">Annotation Control Pattern</span></span>](uiauto-implementingannotation.md)
-   [<span data-ttu-id="22118-111">Customnavigation-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-111">CustomNavigation Control Pattern</span></span>](uiauto-implementingcustomnavigation.md)
-   [<span data-ttu-id="22118-112">Dock-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-112">Dock Control Pattern</span></span>](uiauto-implementingdock.md)
-   [<span data-ttu-id="22118-113">Steuerelement Muster ziehen</span><span class="sxs-lookup"><span data-stu-id="22118-113">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
-   [<span data-ttu-id="22118-114">DropTarget-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-114">DropTarget Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
-   [<span data-ttu-id="22118-115">ExpandCollapse-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-115">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
-   [<span data-ttu-id="22118-116">Raster-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-116">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
-   [<span data-ttu-id="22118-117">GridItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-117">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
-   [<span data-ttu-id="22118-118">Steuerelement Muster aufrufen</span><span class="sxs-lookup"><span data-stu-id="22118-118">Invoke Control Pattern</span></span>](uiauto-implementinginvoke.md)
-   [<span data-ttu-id="22118-119">ItemContainer-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-119">ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
-   [<span data-ttu-id="22118-120">Legacyiaccessible-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-120">LegacyIAccessible Control Pattern</span></span>](uiauto-implementinglegacyiaccessible.md)
-   [<span data-ttu-id="22118-121">MultipleView-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-121">MultipleView Control Pattern</span></span>](uiauto-implementingmultipleview.md)
-   [<span data-ttu-id="22118-122">ObjectModel-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-122">ObjectModel Control Pattern</span></span>](uiauto-implementingobjectmodel.md)
-   [<span data-ttu-id="22118-123">RangeValue-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-123">RangeValue Control Pattern</span></span>](uiauto-implementingrangevalue.md)
-   [<span data-ttu-id="22118-124">Scroll-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-124">Scroll Control Pattern</span></span>](uiauto-implementingscroll.md)
-   [<span data-ttu-id="22118-125">ScrollItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-125">ScrollItem Control Pattern</span></span>](uiauto-implementingscrollitem.md)
-   [<span data-ttu-id="22118-126">Auswahl Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-126">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
-   [<span data-ttu-id="22118-127">SelectionItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-127">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
-   [<span data-ttu-id="22118-128">Tabellen Steuerungs Muster</span><span class="sxs-lookup"><span data-stu-id="22118-128">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
-   [<span data-ttu-id="22118-129">Spreadsheetitem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-129">SpreadsheetItem Control Pattern</span></span>](uiauto-implementingspreadsheetitem.md)
-   [<span data-ttu-id="22118-130">Stile-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-130">Styles Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingstyles)
-   [<span data-ttu-id="22118-131">SynchronizedInput-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-131">SynchronizedInput Control Pattern</span></span>](uiauto-implementingsynchronizedinput.md)
-   [<span data-ttu-id="22118-132">Table-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-132">Table Control Pattern</span></span>](uiauto-implementingtable.md)
-   [<span data-ttu-id="22118-133">TableItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-133">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
-   [<span data-ttu-id="22118-134">Text-und TextRange-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-134">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
-   [<span data-ttu-id="22118-135">Textchild-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-135">TextChild Control Pattern</span></span>](textchild-control-pattern.md)
-   [<span data-ttu-id="22118-136">TextEdit-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-136">TextEdit Control Pattern</span></span>](textedit-control-pattern.md)
-   [<span data-ttu-id="22118-137">Toggle-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-137">Toggle Control Pattern</span></span>](uiauto-implementingtoggle.md)
-   [<span data-ttu-id="22118-138">Transform-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-138">Transform Control Pattern</span></span>](uiauto-implementingtransform.md)
-   [<span data-ttu-id="22118-139">Value-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-139">Value Control Pattern</span></span>](uiauto-implementingvalue.md)
-   [<span data-ttu-id="22118-140">VirtualizedItem-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-140">VirtualizedItem Control Pattern</span></span>](uiauto-implementingvirtualizeditem.md)
-   [<span data-ttu-id="22118-141">Window-Steuerelement Muster</span><span class="sxs-lookup"><span data-stu-id="22118-141">Window Control Pattern</span></span>](uiauto-implementingwindow.md)

## <a name="related-topics"></a><span data-ttu-id="22118-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22118-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22118-143">Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="22118-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> <dt>

[<span data-ttu-id="22118-144">Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="22118-144">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="22118-145">Unterstützen der Benutzeroberflächenautomatisierungs</span><span class="sxs-lookup"><span data-stu-id="22118-145">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> </dl>

 

 