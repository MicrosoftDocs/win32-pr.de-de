---
title: Benutzeroberflächenautomatisierungs-Unterstützung für Standardsteuerelemente
description: In diesem Thema werden die standardmäßigen Windows-Steuerelemente beschrieben, die von der Microsoft UI Automation unterstützt werden Vollständige Unterstützung wird nur für Steuerelemente ab Version 6 von ComCtrl32.dll bereitgestellt (verfügbar in Windows XP und höher).
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- Clients, Unterstützung der Benutzeroberflächen Automatisierung für Standard Steuerelemente
- Clients, Standard Steuerungs Unterstützung
- Clients, Win32-Steuerelemente
- Benutzeroberflächen Automatisierung, Unterstützung für Standard Steuerelemente
- Benutzeroberflächen Automatisierung, Unterstützung von Standard Steuerelementen
- UI-Automatisierung, Win32-Steuerelemente
- Unterstützung für Standardsteuerelemente
- Standard Steuerelement Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515536"
---
# <a name="ui-automation-support-for-standard-controls"></a><span data-ttu-id="ccb6f-112">Benutzeroberflächenautomatisierungs-Unterstützung für Standardsteuerelemente</span><span class="sxs-lookup"><span data-stu-id="ccb6f-112">UI Automation Support for Standard Controls</span></span>

<span data-ttu-id="ccb6f-113">In diesem Thema werden die standardmäßigen Windows-Steuerelemente beschrieben, die von der Microsoft UI Automation unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="ccb6f-113">This topic identifies the standard Windows controls that are supported by Microsoft UI Automation.</span></span> <span data-ttu-id="ccb6f-114">Vollständige Unterstützung wird nur für Steuerelemente ab Version 6 von ComCtrl32.dll bereitgestellt (verfügbar in Windows XP und höher).</span><span class="sxs-lookup"><span data-stu-id="ccb6f-114">Full support is provided only for controls from version 6 of ComCtrl32.dll (available with Windows XP and later).</span></span>

> [!Note]  
> <span data-ttu-id="ccb6f-115">Das RichEdit-Steuerelement wird nur für Versionen unterstützt, die mit Windows Vista ausgeliefert wurden (in RichEd20.dll Version 3,1 und höher sowie MsftEdit.dll Version 4,1 und höher).</span><span class="sxs-lookup"><span data-stu-id="ccb6f-115">The RichEdit control is supported only for versions shipped with Windows Vista (in RichEd20.dll version 3.1 and later, and MsftEdit.dll version 4.1 and later).</span></span>

 

<span data-ttu-id="ccb6f-116">In der folgenden Tabelle werden die Klassennamen der unterstützten Standard Steuerelemente zusammen mit den entsprechenden Steuerelement Typen der Benutzeroberflächen Automatisierung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-116">The following table lists the class names of the supported standard controls, along with the corresponding UI Automation control types.</span></span>



| <span data-ttu-id="ccb6f-117">Klassenname</span><span class="sxs-lookup"><span data-stu-id="ccb6f-117">Class Name</span></span>          | <span data-ttu-id="ccb6f-118">Steuerelementtyp</span><span class="sxs-lookup"><span data-stu-id="ccb6f-118">Control Type</span></span>        |
|---------------------|---------------------|
| <span data-ttu-id="ccb6f-119">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ccb6f-119">Button</span></span>              | <span data-ttu-id="ccb6f-120">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ccb6f-120">Button</span></span>              |
| <span data-ttu-id="ccb6f-121">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ccb6f-121">Button</span></span>              | <span data-ttu-id="ccb6f-122">RadioButton</span><span class="sxs-lookup"><span data-stu-id="ccb6f-122">RadioButton</span></span>         |
| <span data-ttu-id="ccb6f-123">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ccb6f-123">Button</span></span>              | <span data-ttu-id="ccb6f-124">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="ccb6f-124">Group</span></span>               |
| <span data-ttu-id="ccb6f-125">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ccb6f-125">Button</span></span>              | <span data-ttu-id="ccb6f-126">CheckBox</span><span class="sxs-lookup"><span data-stu-id="ccb6f-126">CheckBox</span></span>            |
| <span data-ttu-id="ccb6f-127">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ccb6f-127">Button</span></span>              | <span data-ttu-id="ccb6f-128">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="ccb6f-128">Hyperlink</span></span>           |
| <span data-ttu-id="ccb6f-129">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ccb6f-129">Button</span></span>              | <span data-ttu-id="ccb6f-130">SplitButton</span><span class="sxs-lookup"><span data-stu-id="ccb6f-130">SplitButton</span></span>         |
| <span data-ttu-id="ccb6f-131">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ccb6f-131">Button</span></span>              | <span data-ttu-id="ccb6f-132">CheckBox</span><span class="sxs-lookup"><span data-stu-id="ccb6f-132">CheckBox</span></span>            |
| <span data-ttu-id="ccb6f-133">ComboBoxEx32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-133">ComboBoxEx32</span></span>        | <span data-ttu-id="ccb6f-134">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="ccb6f-134">ComboBox</span></span>            |
| <span data-ttu-id="ccb6f-135">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="ccb6f-135">ComboBox</span></span>            | <span data-ttu-id="ccb6f-136">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="ccb6f-136">ComboBox</span></span>            |
| <span data-ttu-id="ccb6f-137">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="ccb6f-137">Edit</span></span>                | <span data-ttu-id="ccb6f-138">Dokument</span><span class="sxs-lookup"><span data-stu-id="ccb6f-138">Document</span></span>            |
| <span data-ttu-id="ccb6f-139">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="ccb6f-139">Edit</span></span>                | <span data-ttu-id="ccb6f-140">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="ccb6f-140">Edit</span></span>                |
| <span data-ttu-id="ccb6f-141">SysLink</span><span class="sxs-lookup"><span data-stu-id="ccb6f-141">SysLink</span></span>             | <span data-ttu-id="ccb6f-142">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="ccb6f-142">Hyperlink</span></span>           |
| <span data-ttu-id="ccb6f-143">statischen</span><span class="sxs-lookup"><span data-stu-id="ccb6f-143">Static</span></span>              | <span data-ttu-id="ccb6f-144">Text</span><span class="sxs-lookup"><span data-stu-id="ccb6f-144">Text</span></span>                |
| <span data-ttu-id="ccb6f-145">statischen</span><span class="sxs-lookup"><span data-stu-id="ccb6f-145">Static</span></span>              | <span data-ttu-id="ccb6f-146">Image</span><span class="sxs-lookup"><span data-stu-id="ccb6f-146">Image</span></span>               |
| <span data-ttu-id="ccb6f-147">SysIPAddress32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-147">SysIPAddress32</span></span>      | <span data-ttu-id="ccb6f-148">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="ccb6f-148">Custom</span></span>              |
| <span data-ttu-id="ccb6f-149">SysHeader32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-149">SysHeader32</span></span>         | <span data-ttu-id="ccb6f-150">Header/HeaderItem</span><span class="sxs-lookup"><span data-stu-id="ccb6f-150">Header/HeaderItem</span></span>   |
| <span data-ttu-id="ccb6f-151">SysListView32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-151">SysListView32</span></span>       | <span data-ttu-id="ccb6f-152">DataGrid</span><span class="sxs-lookup"><span data-stu-id="ccb6f-152">DataGrid</span></span>            |
| <span data-ttu-id="ccb6f-153">SysListView32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-153">SysListView32</span></span>       | <span data-ttu-id="ccb6f-154">List</span><span class="sxs-lookup"><span data-stu-id="ccb6f-154">List</span></span>                |
| <span data-ttu-id="ccb6f-155">ListBox</span><span class="sxs-lookup"><span data-stu-id="ccb6f-155">ListBox</span></span>             | <span data-ttu-id="ccb6f-156">List</span><span class="sxs-lookup"><span data-stu-id="ccb6f-156">List</span></span>                |
| <span data-ttu-id="ccb6f-157">ListBox</span><span class="sxs-lookup"><span data-stu-id="ccb6f-157">ListBox</span></span>             | <span data-ttu-id="ccb6f-158">ListItem</span><span class="sxs-lookup"><span data-stu-id="ccb6f-158">ListItem</span></span>            |
| <span data-ttu-id="ccb6f-159">\#32768</span><span class="sxs-lookup"><span data-stu-id="ccb6f-159">\#32768</span></span>             | <span data-ttu-id="ccb6f-160">Menü</span><span class="sxs-lookup"><span data-stu-id="ccb6f-160">Menu</span></span>                |
| <span data-ttu-id="ccb6f-161">\#32768</span><span class="sxs-lookup"><span data-stu-id="ccb6f-161">\#32768</span></span>             | <span data-ttu-id="ccb6f-162">MenuItem</span><span class="sxs-lookup"><span data-stu-id="ccb6f-162">MenuItem</span></span>            |
| <span data-ttu-id="ccb6f-163">msctls \_ progress32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-163">msctls\_progress32</span></span>  | <span data-ttu-id="ccb6f-164">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="ccb6f-164">ProgressBar</span></span>         |
| <span data-ttu-id="ccb6f-165">RichEdit</span><span class="sxs-lookup"><span data-stu-id="ccb6f-165">RichEdit</span></span>            | <span data-ttu-id="ccb6f-166">Dokument.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-166">Document.</span></span> <span data-ttu-id="ccb6f-167">Siehe Hinweis.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-167">See note.</span></span> |
| <span data-ttu-id="ccb6f-168">RichEdit20A</span><span class="sxs-lookup"><span data-stu-id="ccb6f-168">RichEdit20A</span></span>         | <span data-ttu-id="ccb6f-169">Dokument</span><span class="sxs-lookup"><span data-stu-id="ccb6f-169">Document</span></span>            |
| <span data-ttu-id="ccb6f-170">RichEdit20W</span><span class="sxs-lookup"><span data-stu-id="ccb6f-170">RichEdit20W</span></span>         | <span data-ttu-id="ccb6f-171">Dokument</span><span class="sxs-lookup"><span data-stu-id="ccb6f-171">Document</span></span>            |
| <span data-ttu-id="ccb6f-172">RichEdit50W</span><span class="sxs-lookup"><span data-stu-id="ccb6f-172">RichEdit50W</span></span>         | <span data-ttu-id="ccb6f-173">Dokument</span><span class="sxs-lookup"><span data-stu-id="ccb6f-173">Document</span></span>            |
| <span data-ttu-id="ccb6f-174">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="ccb6f-174">ScrollBar</span></span>           | <span data-ttu-id="ccb6f-175">Schieberegler</span><span class="sxs-lookup"><span data-stu-id="ccb6f-175">Slider</span></span>              |
| <span data-ttu-id="ccb6f-176">msctls \_ trackbar32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-176">msctls\_trackbar32</span></span>  | <span data-ttu-id="ccb6f-177">Schieberegler</span><span class="sxs-lookup"><span data-stu-id="ccb6f-177">Slider</span></span>              |
| <span data-ttu-id="ccb6f-178">msctls \_ updown32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-178">msctls\_updown32</span></span>    | <span data-ttu-id="ccb6f-179">Spinner</span><span class="sxs-lookup"><span data-stu-id="ccb6f-179">Spinner</span></span>             |
| <span data-ttu-id="ccb6f-180">msctls \_ statusbar32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-180">msctls\_statusbar32</span></span> | <span data-ttu-id="ccb6f-181">StatusBar</span><span class="sxs-lookup"><span data-stu-id="ccb6f-181">StatusBar</span></span>           |
| <span data-ttu-id="ccb6f-182">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-182">SysTabControl32</span></span>     | <span data-ttu-id="ccb6f-183">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="ccb6f-183">Tab</span></span>                 |
| <span data-ttu-id="ccb6f-184">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-184">SysTabControl32</span></span>     | <span data-ttu-id="ccb6f-185">TabItem</span><span class="sxs-lookup"><span data-stu-id="ccb6f-185">TabItem</span></span>             |
| <span data-ttu-id="ccb6f-186">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-186">ToolbarWindow32</span></span>     | <span data-ttu-id="ccb6f-187">ToolBar</span><span class="sxs-lookup"><span data-stu-id="ccb6f-187">ToolBar</span></span>             |
| <span data-ttu-id="ccb6f-188">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-188">ToolbarWindow32</span></span>     | <span data-ttu-id="ccb6f-189">MenuItem</span><span class="sxs-lookup"><span data-stu-id="ccb6f-189">MenuItem</span></span>            |
| <span data-ttu-id="ccb6f-190">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-190">ToolbarWindow32</span></span>     | <span data-ttu-id="ccb6f-191">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="ccb6f-191">Button</span></span>              |
| <span data-ttu-id="ccb6f-192">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-192">ToolbarWindow32</span></span>     | <span data-ttu-id="ccb6f-193">CheckBox</span><span class="sxs-lookup"><span data-stu-id="ccb6f-193">CheckBox</span></span>            |
| <span data-ttu-id="ccb6f-194">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-194">ToolbarWindow32</span></span>     | <span data-ttu-id="ccb6f-195">RadioButton</span><span class="sxs-lookup"><span data-stu-id="ccb6f-195">RadioButton</span></span>         |
| <span data-ttu-id="ccb6f-196">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-196">ToolbarWindow32</span></span>     | <span data-ttu-id="ccb6f-197">Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="ccb6f-197">Separator</span></span>           |
| <span data-ttu-id="ccb6f-198">Quick Infos \_ class32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-198">tooltips\_class32</span></span>   | <span data-ttu-id="ccb6f-199">ToolTip</span><span class="sxs-lookup"><span data-stu-id="ccb6f-199">ToolTip</span></span>             |
| <span data-ttu-id="ccb6f-200">\#32774</span><span class="sxs-lookup"><span data-stu-id="ccb6f-200">\#32774</span></span>             | <span data-ttu-id="ccb6f-201">ToolTip</span><span class="sxs-lookup"><span data-stu-id="ccb6f-201">ToolTip</span></span>             |
| <span data-ttu-id="ccb6f-202">ReBarWindow32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-202">ReBarWindow32</span></span>       | <span data-ttu-id="ccb6f-203">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="ccb6f-203">Toolbar</span></span>             |
| <span data-ttu-id="ccb6f-204">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-204">SysTreeView32</span></span>       | <span data-ttu-id="ccb6f-205">Struktur</span><span class="sxs-lookup"><span data-stu-id="ccb6f-205">Tree</span></span>                |
| <span data-ttu-id="ccb6f-206">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-206">SysTreeView32</span></span>       | <span data-ttu-id="ccb6f-207">TreeItem</span><span class="sxs-lookup"><span data-stu-id="ccb6f-207">TreeItem</span></span>            |



 

<span data-ttu-id="ccb6f-208">Die in der folgenden Tabelle aufgeführten Steuerelemente werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-208">The controls listed in the following table are not supported.</span></span>



| <span data-ttu-id="ccb6f-209">Klassenname</span><span class="sxs-lookup"><span data-stu-id="ccb6f-209">Class Name</span></span>                                    | <span data-ttu-id="ccb6f-210">Steuerelementtyp</span><span class="sxs-lookup"><span data-stu-id="ccb6f-210">Control Type</span></span> |
|-----------------------------------------------|--------------|
| <span data-ttu-id="ccb6f-211">SysAnimate32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-211">SysAnimate32</span></span>                                  | <span data-ttu-id="ccb6f-212">Image</span><span class="sxs-lookup"><span data-stu-id="ccb6f-212">Image</span></span>        |
| <span data-ttu-id="ccb6f-213">SysPager</span><span class="sxs-lookup"><span data-stu-id="ccb6f-213">SysPager</span></span>                                      | <span data-ttu-id="ccb6f-214">Spinner</span><span class="sxs-lookup"><span data-stu-id="ccb6f-214">Spinner</span></span>      |
| <span data-ttu-id="ccb6f-215">SysDateTimePick32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-215">SysDateTimePick32</span></span>                             | <span data-ttu-id="ccb6f-216">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="ccb6f-216">Custom</span></span>       |
| <span data-ttu-id="ccb6f-217">SysMonthCal32</span><span class="sxs-lookup"><span data-stu-id="ccb6f-217">SysMonthCal32</span></span>                                 | <span data-ttu-id="ccb6f-218">Kalender</span><span class="sxs-lookup"><span data-stu-id="ccb6f-218">Calendar</span></span>     |
| <span data-ttu-id="ccb6f-219">MS \_ winnote</span><span class="sxs-lookup"><span data-stu-id="ccb6f-219">MS\_WINNOTE</span></span>                                   | <span data-ttu-id="ccb6f-220">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ccb6f-220">Tooltip</span></span>      |
| <span data-ttu-id="ccb6f-221">VBBubble</span><span class="sxs-lookup"><span data-stu-id="ccb6f-221">VBBubble</span></span>                                      | <span data-ttu-id="ccb6f-222">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ccb6f-222">Tooltip</span></span>      |
| <span data-ttu-id="ccb6f-223">ScrollBar (wenn als eigenständiges Steuerelement verwendet)</span><span class="sxs-lookup"><span data-stu-id="ccb6f-223">ScrollBar (when used as a standalone control)</span></span> | <span data-ttu-id="ccb6f-224">Schieberegler</span><span class="sxs-lookup"><span data-stu-id="ccb6f-224">Slider</span></span>       |
| <span data-ttu-id="ccb6f-225">SuperGrid</span><span class="sxs-lookup"><span data-stu-id="ccb6f-225">SuperGrid</span></span>                                     | <span data-ttu-id="ccb6f-226">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="ccb6f-226">Custom</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="ccb6f-227">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ccb6f-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccb6f-228">Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="ccb6f-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




