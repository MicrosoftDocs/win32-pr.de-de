---
title: Überprüfungs Routinen
description: In diesem Abschnitt werden die Überprüfungs Routinen beschrieben, die die UI-Zugriffs Prüfung ausführen kann, um die Barrierefreiheits Implementierung einer Anwendung zu testen.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310148"
---
# <a name="verification-routines"></a><span data-ttu-id="7e7a0-103">Überprüfungs Routinen</span><span class="sxs-lookup"><span data-stu-id="7e7a0-103">Verification Routines</span></span>

<span data-ttu-id="7e7a0-104">In diesem Abschnitt werden die Überprüfungs Routinen beschrieben, die die UI-Zugriffs Prüfung ausführen kann, um die Barrierefreiheits Implementierung einer Anwendung zu testen.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-104">This section describes the verification routines that UI Accessibility Checker can run to test an application's accessibility implementation.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7e7a0-105">Category</span><span class="sxs-lookup"><span data-stu-id="7e7a0-105">Category</span></span></th>
<th><span data-ttu-id="7e7a0-106">-Routine zurückgegebener Wert</span><span class="sxs-lookup"><span data-stu-id="7e7a0-106">Routine</span></span></th>
<th><span data-ttu-id="7e7a0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e7a0-107">Description</span></span></th>
</tr><span data-ttu-id="7e7a0-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Konsistenz</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7e7a0-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Consistency</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7e7a0-109"><strong>Screenreader</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-109"><strong>ScreenReader</strong></span></span></td>
<td><span data-ttu-id="7e7a0-110">Kompiliert alle sichtbaren Elemente im Überprüfungs Ziel und zeigt Sie in einem ListView-Steuerelement in der Reihenfolge an, in der Sie einem Benutzer von einem Standard Bildschirm Reader angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-110">Compiles all visible elements in the verification target and displays them in a ListView control in the order that a standard screen reader announces them to a user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-111"><strong>Uiaskrerereader</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-111"><strong>UiaScreenReader</strong></span></span></td>
<td><span data-ttu-id="7e7a0-112">Identisch mit <strong>Screenreader</strong>, aber für UIA-Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-112">Same as <strong>ScreenReader</strong>, but for UIA implementations.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="7e7a0-113"><strong>Navigation</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7e7a0-113"><strong>Navigation</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7e7a0-114"><strong>Checktreetiefe</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-114"><strong>CheckTreeDepth</strong></span></span></td>
<td><span data-ttu-id="7e7a0-115">Sendet Tabstopps (oder Umschalt + Tab-Zeichen) als Eingabe an das Überprüfungs Ziel, um zu bestätigen, dass die Benutzeroberfläche des Ziels nicht übermäßig Komplex ist oder nicht auf die standardmäßige Tastaturnavigation zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-115">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that the target's UI isn't overly complex or inaccessible using standard keyboard navigation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-116"><strong>Checktabbinguia</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-116"><strong>CheckTabbingUia</strong></span></span></td>
<td><span data-ttu-id="7e7a0-117">Sendet Tabstopps (oder Umschalt + Tab-Zeichen) als Eingabe an das Überprüfungs Ziel, um zu bestätigen, dass alle fokussierbaren Elemente in der Benutzeroberfläche mithilfe der Standardtastatur Navigation ordnungsgemäß und logisch erreichbar sind.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-117">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that all focusable elements in the UI are reachable in an orderly, logical fashion using standard keyboard navigation.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="7e7a0-118"><strong>Eigenschaften</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7e7a0-118"><strong>Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7e7a0-119"><strong>Checkrole</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-119"><strong>CheckRole</strong></span></span></td>
<td><span data-ttu-id="7e7a0-120">Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche eine gültige, logische MSAA-Rolle meldet und dass das Steuerelement über einen Wert verfügt, der für diese Rolle erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-120">Confirms that each focusable element in the UI reports a valid, logical MSAA role, and that the control has a value as required by that role.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-121"><strong>CheckState</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-121"><strong>CheckState</strong></span></span></td>
<td><span data-ttu-id="7e7a0-122">Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche einen gültigen, logischen MSAA-Zustand meldet.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-122">Confirms that each focusable element in the UI reports a valid, logical MSAA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-123"><strong>CheckName</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-123"><strong>CheckName</strong></span></span></td>
<td><span data-ttu-id="7e7a0-124">Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche einen gültigen, logischen MSAA-Namen meldet.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-124">Confirms that each focusable element in the UI reports a valid, logical MSAA name.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-125"><strong>Checkaccesskeys</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-125"><strong>CheckAccessKeys</strong></span></span></td>
<td><span data-ttu-id="7e7a0-126">Bestätigt, dass Zugriffsschlüssel, die Elementen im Überprüfungs Ziel zugewiesen sind, innerhalb des Überprüfungs Ziels eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-126">Confirms that access keys that are assigned to elements in the verification target are unique within the verification target.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-127"><strong>Checkboundingrect</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-127"><strong>CheckBoundingRect</strong></span></span></td>
<td><span data-ttu-id="7e7a0-128">Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche über ein Begrenzungs Rechteck verfügt, das als Ziel für Treffer Tests verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-128">Confirms that each focusable element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="7e7a0-129"><strong>Tree</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7e7a0-129"><strong>Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7e7a0-130"><strong>Checkparser</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-130"><strong>CheckParentChild</strong></span></span></td>
<td><span data-ttu-id="7e7a0-131">Übergeordnete und untergeordnete Beziehungen in der-Elementstruktur sind konsistent und vorhersagbar.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-131">Parent and child relationships in the element tree are consistent and predictable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-132"><strong>Checkwaisen Children</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-132"><strong>CheckOrphanChildren</strong></span></span></td>
<td><span data-ttu-id="7e7a0-133">Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche ein gültiges MSAA-übergeordnetes Element meldet.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-133">Confirms that each focusable element in the UI reports a valid MSAA parent.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="7e7a0-134"><strong>UIA-Eigenschaften</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7e7a0-134"><strong>UIA Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7e7a0-135"><strong>Checknameuia</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-135"><strong>CheckNameUIA</strong></span></span></td>
<td><span data-ttu-id="7e7a0-136">Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche einen gültigen, logischen UIA-Namen meldet.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-136">Confirms that each focusable element in the UI reports a valid, logical UIA name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-137"><strong>Checktreedepthuia</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-137"><strong>CheckTreeDepthUIA</strong></span></span></td>
<td><span data-ttu-id="7e7a0-138">Sendet Tabstopps (oder Umschalt + Tab-Zeichen) als Eingabe an das Überprüfungs Ziel, um zu bestätigen, dass die UIA-Elemente in der Benutzeroberfläche des Ziels nicht übermäßig komplex sind oder nicht auf die standardmäßige Tastaturnavigation zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-138">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that to UIA elements in the target's UI aren't overly complex or inaccessible using standard keyboard navigation.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-139"><strong>CheckStatus</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-139"><strong>CheckStateUIA</strong></span></span></td>
<td><span data-ttu-id="7e7a0-140">Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche einen gültigen, logischen UIA-Zustand meldet.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-140">Confirms that each focusable element in the UI reports a valid, logical UIA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-141"><strong>Checkaccesskeysuia</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-141"><strong>CheckAccessKeysUIA</strong></span></span></td>
<td><span data-ttu-id="7e7a0-142">Bestätigt, dass neben geordnete Elemente nicht denselben Zugriffs-und/oder Zugriffstasten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-142">Confirms that sibling elements do not have the same access and/or accelerator key.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-143"><strong>Checkboundingrectuia</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-143"><strong>CheckBoundingRectUIA</strong></span></span></td>
<td><span data-ttu-id="7e7a0-144">Bestätigt, dass jedes Fokussier Bare UIA-Element in der Benutzeroberfläche über ein Begrenzungs Rechteck verfügt, das als Ziel für Treffer Tests verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-144">Confirms that each focusable UIA element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-145"><strong>Checkcontroltypeuia</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-145"><strong>CheckControlTypeUIA</strong></span></span></td>
<td><span data-ttu-id="7e7a0-146">Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche einen gültigen, logischen UIA-Steuer Elementtyp meldet.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-146">Confirms that each focusable element in the UI reports a valid, logical UIA control type.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="7e7a0-147"><strong>UIA</strong>-Struktur $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7e7a0-147"><strong>UIA Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7e7a0-148"><strong>Checknavigateuia</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-148"><strong>CheckNavigateUia</strong></span></span></td>
<td><span data-ttu-id="7e7a0-149">Bestätigt, dass der UIA TreeWalker durch die untergeordneten Elemente eines Elements navigieren kann.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-149">Confirms that the UIA TreeWalker can navigate through an element's children.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-150"><strong>Checkwaisen-Kinder</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-150"><strong>CheckOrphanChildrenUia</strong></span></span></td>
<td><span data-ttu-id="7e7a0-151">Bestätigt, dass jedes Fokussier Bare Element in der Benutzeroberfläche ein gültiges UIA-übergeordnetes Element meldet.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-151">Confirms that each focusable element in the UI reports a valid UIA parent.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-152"><strong>Checksiblingsuia</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-152"><strong>CheckSiblingsUia</strong></span></span></td>
<td><span data-ttu-id="7e7a0-153">Bestätigt, dass neben geordnete Elemente nicht denselben Namen haben: ControlType-Paare und keine der gleichen automationids.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-153">Confirms that sibling elements do not have the same Name:ControlType pairs, nor the same AutomationId's.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-154">$ {ROWSPAN9} $<strong>Aria Web verifications</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7e7a0-154">${ROWSPAN9}$<strong>ARIA Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7e7a0-155"><strong>Checkariarole</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-155"><strong>CheckARIARole</strong></span></span></td>
<td><span data-ttu-id="7e7a0-156">Bestätigt, dass alle Elemente über eine gültige Aria-Rolle verfügen.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-156">Confirms that all elements have a valid ARIA role.</span></span> <span data-ttu-id="7e7a0-157">Das zugehörige HTML-Tag und die Aria-Rolle sind Informationselemente, bei denen ungültige Rollen als Fehler gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-157">The associated HTML tag and ARIA role are information elements with invalid roles flagged as errors.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-158"><strong>Checklabel</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-158"><strong>CheckLabel</strong></span></span></td>
<td><span data-ttu-id="7e7a0-159">Bestätigt, dass jedes Element mit Eingabe, Schaltfläche, Bild Schaltfläche oder der Rolle "Landmark" über eine Bezeichnung verfügt.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-159">Confirms each element with input, button, image-button, or landmark role has a label.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-160"><strong>Checkrangecontrols</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-160"><strong>CheckRangeControls</strong></span></span></td>
<td><span data-ttu-id="7e7a0-161">Bestätigt Bereichs Steuerelemente mit dem Schieberegler oder der Statusanzeige Rolle sind die richtigen Aria-Attribute definiert.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-161">Confirms range controls with slider or progress bar role have proper ARIA attributes defined.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-162"><strong>Checkcontainerrole</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-162"><strong>CheckContainerRole</strong></span></span></td>
<td><span data-ttu-id="7e7a0-163">Bestätigt, dass ein Element, oder mindestens eines seiner untergeordneten Elemente, OnKeyDown/OnKeyPress definiert hat.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-163">Confirms an element, or at least one of its children, has onkeydown/onkeypress defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-164"><strong>Checklayoutfähig</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-164"><strong>CheckLayoutTable</strong></span></span></td>
<td><span data-ttu-id="7e7a0-165">Bestätigt, dass ein Tabellenlayout eine Zusammenfassung/Th/Aria-DescribedBy enthält.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-165">Confirms a table layout has a summary/th/aria-describedby included.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-166"><strong>Checkgridstructure</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-166"><strong>CheckGridStructure</strong></span></span></td>
<td><span data-ttu-id="7e7a0-167">Bestätigt, dass ein nicht Tabellen Element mit der Raster Rolle über eine Struktur von Raster>Zeile>gridcell mit zugeordneten Attributen verfügt.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-167">Confirms a non-table element with grid role has a structure of grid>row>gridcell with associated attributes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-168"><strong>Checkdatdatababel</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-168"><strong>CheckDataTable</strong></span></span></td>
<td><span data-ttu-id="7e7a0-169">Bestätigt die Eigenschaften von Datentabellen.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-169">Confirms the properties of data tables.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-170"><strong>Checkactivedescendants</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-170"><strong>CheckActiveDescendants</strong></span></span></td>
<td><span data-ttu-id="7e7a0-171">Bestätigt die Eigenschaften von Elementen mit einem aktiven Nachfolger, der definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-171">Confirms the properties of elements with an active descendant defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-172"><strong>Checkelementswithclickhandler</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-172"><strong>CheckElementsWithClickHandler</strong></span></span></td>
<td><span data-ttu-id="7e7a0-173">Bestätigt den Registerkarten Index von Elementen mit Klick Handlern.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-173">Confirms the tab index of elements with click handlers.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="7e7a0-174"><strong>Webüberprüfungen</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7e7a0-174"><strong>Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7e7a0-175"><strong>Checkhtml (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-175"><strong>CheckHtml (Web)</strong></span></span></td>
<td><span data-ttu-id="7e7a0-176">Bestätigt verschiedene HTML-Merkmale, wie z. b. Header, Name, Rahmen und Titel.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-176">Confirms various HTML characteristics such as headers, name, frames, and titles.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e7a0-177"><strong>Checkname (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-177"><strong>CheckName (Web)</strong></span></span></td>
<td><span data-ttu-id="7e7a0-178">Bestätigt namens Merkmale, wie z. b. Länge, ungültige Zeichen und Rollen Einbindung.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-178">Confirms name characteristics such as length, invalid characters, and role inclusion.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7e7a0-179"><strong>Checkrole (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="7e7a0-179"><strong>CheckRole (Web)</strong></span></span></td>
<td><span data-ttu-id="7e7a0-180">Bestätigt ungültige Rollen, Rollen, die Werte aufweisen sollten und/oder Rollen nicht implementiert sind.</span><span class="sxs-lookup"><span data-stu-id="7e7a0-180">Confirms invalid roles, roles that should have values, and/or roles not implemented.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7e7a0-181">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7e7a0-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e7a0-182">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="7e7a0-182">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




