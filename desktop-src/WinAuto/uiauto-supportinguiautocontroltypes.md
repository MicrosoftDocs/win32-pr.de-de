---
title: Unterstützen der Benutzeroberflächenautomatisierungs
description: Dieser Abschnitt enthält ausführliche Informationen über die Struktur, Eigenschaften, Steuerelement Muster und Ereignisse, die von den einzelnen Steuerelement Typen der Microsoft-Benutzeroberflächen Automatisierung unterstützt werden müssen.
ms.assetid: 35232907-6c54-47cd-b82a-0daee279ef17
keywords:
- UI-Automatisierung, Informationen zu Steuerelement Typen
- UI-Automatisierung, Übersicht über den Steuer ungstyp
- Unterstützung für Steuerelement Typen
- Steuerelement Typen, Support
- Steuerelement Typen, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac6f857da87691428c747cfe5dbff5102218f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390824"
---
# <a name="supporting-ui-automation-control-types"></a><span data-ttu-id="adec0-108">Unterstützen der Benutzeroberflächenautomatisierungs</span><span class="sxs-lookup"><span data-stu-id="adec0-108">Supporting UI Automation Control Types</span></span>

<span data-ttu-id="adec0-109">Dieser Abschnitt enthält ausführliche Informationen über die Struktur, Eigenschaften, Steuerelement Muster und Ereignisse, die von den einzelnen Steuerelement Typen der Microsoft-Benutzeroberflächen Automatisierung unterstützt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="adec0-109">This section contains detailed information about the tree structure, properties, control patterns, and events that each Microsoft UI Automation control type is required to support.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="adec0-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="adec0-110">In this section</span></span>

-   [<span data-ttu-id="adec0-111">Appbar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-111">AppBar Control Type</span></span>](uiauto-supportappbarcontroltype.md)
-   [<span data-ttu-id="adec0-112">Button-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-112">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="adec0-113">Typ des Kalender Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="adec0-113">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="adec0-114">CheckBox-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-114">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="adec0-115">ComboBox-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-115">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="adec0-116">DataGrid-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-116">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="adec0-117">DataItem-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-117">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="adec0-118">Dokument Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="adec0-118">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="adec0-119">Steuerelement-Typ bearbeiten</span><span class="sxs-lookup"><span data-stu-id="adec0-119">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="adec0-120">Gruppen Steuerungstyp</span><span class="sxs-lookup"><span data-stu-id="adec0-120">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="adec0-121">Header Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="adec0-121">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="adec0-122">Header Item-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="adec0-122">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="adec0-123">Hyperlink-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-123">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="adec0-124">Bild Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="adec0-124">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="adec0-125">List-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-125">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="adec0-126">ListItem-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="adec0-126">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="adec0-127">Menu-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-127">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="adec0-128">MenuBar-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="adec0-128">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="adec0-129">MenuItem-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="adec0-129">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="adec0-130">Pane-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-130">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="adec0-131">ProgressBar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-131">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="adec0-132">RadioButton-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="adec0-132">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="adec0-133">ScrollBar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-133">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="adec0-134">Typ des semanticzoom-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="adec0-134">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="adec0-135">Separator-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-135">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="adec0-136">Slider-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-136">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="adec0-137">Spinner-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-137">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="adec0-138">SplitButton-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="adec0-138">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="adec0-139">StatusBar-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="adec0-139">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="adec0-140">Register Steuerungstyp</span><span class="sxs-lookup"><span data-stu-id="adec0-140">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="adec0-141">TabItem-Steuer Elementtyp</span><span class="sxs-lookup"><span data-stu-id="adec0-141">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="adec0-142">Table-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-142">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="adec0-143">Text Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="adec0-143">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="adec0-144">Thumb-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="adec0-144">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="adec0-145">TitleBar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-145">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="adec0-146">ToolBar-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-146">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="adec0-147">ToolTip-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-147">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="adec0-148">Struktur Steuerungstyp</span><span class="sxs-lookup"><span data-stu-id="adec0-148">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="adec0-149">TreeItem-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="adec0-149">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="adec0-150">Fenster Steuerelement-Typ</span><span class="sxs-lookup"><span data-stu-id="adec0-150">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="adec0-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="adec0-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adec0-152">Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="adec0-152">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 