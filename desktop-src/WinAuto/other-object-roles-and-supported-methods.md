---
title: Andere Objekt Rollen und unterstützte Methoden (MSAA UI-Element Referenz)
description: Dieses Thema enthält Informationen zu Objekt Rollen, die nicht in den vorherigen Themen zu Benutzeroberflächen Elementen enthalten sind.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729025"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="b6535-103">Andere Objekt Rollen und unterstützte Methoden (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="b6535-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="b6535-104">Dieses Thema enthält Informationen zu Objekt Rollen, die nicht in den vorherigen Themen zu Benutzeroberflächen Elementen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b6535-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="b6535-105">Jede Objekt Rolle enthält eine Liste der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden und-Eigenschaften, die für die Objekt Rolle unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b6535-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="b6535-106">In anderen Themen werden unterstützte **IAccessible** -Methoden und-Eigenschaften für Benutzeroberflächen Elemente dokumentiert. in diesem Thema werden die Methoden und Eigenschaften aufgelistet, die für eine bestimmte Objekt Rolle erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="b6535-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="b6535-107">Viele Benutzeroberflächen Elemente, die möglicherweise eine der hier aufgeführten Rollen aufweisen, werden in der Regel in Browsern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b6535-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="b6535-108">Verwenden Sie dieses Thema als Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b6535-108">Use this topic as a guideline.</span></span> <span data-ttu-id="b6535-109">Wir empfehlen dringend, Microsoft Active Accessibility Tools zu verwenden, um das erwartete Verhalten für eine einzelne Objekt Rolle zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b6535-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="b6535-110">In der folgenden Tabelle werden zusätzliche Objekt Rollen aufgelistet, die Oleacc.dll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6535-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="b6535-111">**Rollen \_ System \_ Warnung**</span><span class="sxs-lookup"><span data-stu-id="b6535-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="b6535-112">**Rollen \_ System- \_ Dropdown Liste**</span><span class="sxs-lookup"><span data-stu-id="b6535-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="b6535-113">**Rollen \_ System \_ Anwendung**</span><span class="sxs-lookup"><span data-stu-id="b6535-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="b6535-114">**Rollen \_ System \_ Gleichung**</span><span class="sxs-lookup"><span data-stu-id="b6535-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="b6535-115">**Rollen \_ System \_ Rahmen**</span><span class="sxs-lookup"><span data-stu-id="b6535-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="b6535-116">**Grafik zum Rollen \_ System \_**</span><span class="sxs-lookup"><span data-stu-id="b6535-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="b6535-117">**\_ \_ ButtonDropDown für Rollen System**</span><span class="sxs-lookup"><span data-stu-id="b6535-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="b6535-118">**Hilfe Sprechblase für Rollen \_ System \_**</span><span class="sxs-lookup"><span data-stu-id="b6535-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="b6535-119">**\_ \_ buttondropdowngrid für Rollen System**</span><span class="sxs-lookup"><span data-stu-id="b6535-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="b6535-120">**Rollen \_ System- \_ IPAddress**</span><span class="sxs-lookup"><span data-stu-id="b6535-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="b6535-121">**\_ \_ ButtonMenu für Rollen System**</span><span class="sxs-lookup"><span data-stu-id="b6535-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="b6535-122">**Rollen \_ System \_ Link**</span><span class="sxs-lookup"><span data-stu-id="b6535-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="b6535-123">**Rollen \_ System \_ Zelle**</span><span class="sxs-lookup"><span data-stu-id="b6535-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="b6535-124">**Bereich "Rollen \_ System" \_**</span><span class="sxs-lookup"><span data-stu-id="b6535-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="b6535-125">**Rollen \_ System \_ Zeichen**</span><span class="sxs-lookup"><span data-stu-id="b6535-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="b6535-126">**Rollen \_ System \_ Zeile**</span><span class="sxs-lookup"><span data-stu-id="b6535-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="b6535-127">**Rollen \_ System \_ Diagramm**</span><span class="sxs-lookup"><span data-stu-id="b6535-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="b6535-128">**Rollen \_ System ( \_ RowHeader)**</span><span class="sxs-lookup"><span data-stu-id="b6535-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="b6535-129">**Rollen \_ \_ Systemuhr**</span><span class="sxs-lookup"><span data-stu-id="b6535-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="b6535-130">**Rollen \_ System \_ Trennzeichen**</span><span class="sxs-lookup"><span data-stu-id="b6535-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="b6535-131">**Rollen \_ System \_ Spalte**</span><span class="sxs-lookup"><span data-stu-id="b6535-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="b6535-132">**Sound des Rollen \_ Systems \_**</span><span class="sxs-lookup"><span data-stu-id="b6535-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="b6535-133">**Rollen \_ System \_ Diagramm**</span><span class="sxs-lookup"><span data-stu-id="b6535-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="b6535-134">**Rollen \_ System ( \_ SplitButton)**</span><span class="sxs-lookup"><span data-stu-id="b6535-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="b6535-135">**Rollen \_ System- \_ Wahl**</span><span class="sxs-lookup"><span data-stu-id="b6535-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="b6535-136">**Rollen \_ System \_ Tabelle**</span><span class="sxs-lookup"><span data-stu-id="b6535-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="b6535-137">**Rollen \_ System \_ Dokument**</span><span class="sxs-lookup"><span data-stu-id="b6535-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="b6535-138">**\_Leerraum für Rollen System \_**</span><span class="sxs-lookup"><span data-stu-id="b6535-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="b6535-139">Rollen \_ System \_ Warnung</span><span class="sxs-lookup"><span data-stu-id="b6535-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="b6535-140">Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ Warnung zu Rollen Systemen**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="b6535-141">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-142">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-142">get\_accName</span></span>
-   <span data-ttu-id="b6535-143">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-143">get\_accRole</span></span>
-   <span data-ttu-id="b6535-144">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="b6535-145">Rollen \_ System \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="b6535-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="b6535-146">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Application**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="b6535-147">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-148">accHitTest</span></span>
-   <span data-ttu-id="b6535-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-149">accLocation</span></span>
-   <span data-ttu-id="b6535-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-150">accNavigate</span></span>
-   <span data-ttu-id="b6535-151">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-151">get\_accChild</span></span>
-   <span data-ttu-id="b6535-152">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-152">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-153">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-153">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-154">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-154">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-155">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-156">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-157">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-157">get\_accName</span></span>
-   <span data-ttu-id="b6535-158">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-158">get\_accParent</span></span>
-   <span data-ttu-id="b6535-159">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-159">get\_accRole</span></span>
-   <span data-ttu-id="b6535-160">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="b6535-161">Rollen \_ System \_ Rahmen</span><span class="sxs-lookup"><span data-stu-id="b6535-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="b6535-162">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Border**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="b6535-163">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-164">accHitTest</span></span>
-   <span data-ttu-id="b6535-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-165">accLocation</span></span>
-   <span data-ttu-id="b6535-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-166">accNavigate</span></span>
-   <span data-ttu-id="b6535-167">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-167">get\_accRole</span></span>
-   <span data-ttu-id="b6535-168">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="b6535-169">\_ \_ ButtonDropDown für Rollen System</span><span class="sxs-lookup"><span data-stu-id="b6535-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="b6535-170">Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ ButtonDropDown für Rollen System**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="b6535-171">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="b6535-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="b6535-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-173">accHitTest</span></span>
-   <span data-ttu-id="b6535-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-174">accLocation</span></span>
-   <span data-ttu-id="b6535-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-175">accNavigate</span></span>
-   <span data-ttu-id="b6535-176">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-176">get\_accChild</span></span>
-   <span data-ttu-id="b6535-177">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-177">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-178">get \_ accdefaultaction</span><span class="sxs-lookup"><span data-stu-id="b6535-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="b6535-179">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-179">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-180">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-180">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-181">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-182">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-183">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-183">get\_accName</span></span>
-   <span data-ttu-id="b6535-184">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-184">get\_accParent</span></span>
-   <span data-ttu-id="b6535-185">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-185">get\_accRole</span></span>
-   <span data-ttu-id="b6535-186">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="b6535-187">\_ \_ buttondropdowngrid für Rollen System</span><span class="sxs-lookup"><span data-stu-id="b6535-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="b6535-188">Weitere Informationen zu dieser Rolle finden Sie im Thema zum [**Rollen \_ System \_ buttondropdowngrid**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="b6535-189">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="b6535-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="b6535-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-191">accHitTest</span></span>
-   <span data-ttu-id="b6535-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-192">accLocation</span></span>
-   <span data-ttu-id="b6535-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-193">accNavigate</span></span>
-   <span data-ttu-id="b6535-194">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-194">get\_accChild</span></span>
-   <span data-ttu-id="b6535-195">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-195">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-196">get \_ accdefaultaction</span><span class="sxs-lookup"><span data-stu-id="b6535-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="b6535-197">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-197">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-198">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-198">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-199">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-200">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-201">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-201">get\_accName</span></span>
-   <span data-ttu-id="b6535-202">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-202">get\_accParent</span></span>
-   <span data-ttu-id="b6535-203">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-203">get\_accRole</span></span>
-   <span data-ttu-id="b6535-204">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="b6535-205">\_ \_ ButtonMenu für Rollen System</span><span class="sxs-lookup"><span data-stu-id="b6535-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="b6535-206">Weitere Informationen zu dieser Rolle finden Sie unter [**\_ Button- \_ Menü "Rollen System**](object-roles.md)".</span><span class="sxs-lookup"><span data-stu-id="b6535-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="b6535-207">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="b6535-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="b6535-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-209">accHitTest</span></span>
-   <span data-ttu-id="b6535-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-210">accLocation</span></span>
-   <span data-ttu-id="b6535-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-211">accNavigate</span></span>
-   <span data-ttu-id="b6535-212">get \_ accdefaultaction</span><span class="sxs-lookup"><span data-stu-id="b6535-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="b6535-213">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-213">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-214">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-214">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-215">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-216">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-217">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-217">get\_accName</span></span>
-   <span data-ttu-id="b6535-218">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-218">get\_accParent</span></span>
-   <span data-ttu-id="b6535-219">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-219">get\_accRole</span></span>
-   <span data-ttu-id="b6535-220">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="b6535-221">Rollen \_ System \_ Zelle</span><span class="sxs-lookup"><span data-stu-id="b6535-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="b6535-222">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Cell**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="b6535-223">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-224">accHitTest</span></span>
-   <span data-ttu-id="b6535-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-225">accLocation</span></span>
-   <span data-ttu-id="b6535-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-226">accNavigate</span></span>
-   <span data-ttu-id="b6535-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="b6535-227">accSelect</span></span>
-   <span data-ttu-id="b6535-228">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-228">get\_accChild</span></span>
-   <span data-ttu-id="b6535-229">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-229">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-230">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-230">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-231">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-231">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-232">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-233">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-234">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-234">get\_accName</span></span>
-   <span data-ttu-id="b6535-235">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-235">get\_accParent</span></span>
-   <span data-ttu-id="b6535-236">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-236">get\_accRole</span></span>
-   <span data-ttu-id="b6535-237">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-237">get\_accState</span></span>
-   <span data-ttu-id="b6535-238">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="b6535-239">Rollen \_ System \_ Zeichen</span><span class="sxs-lookup"><span data-stu-id="b6535-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="b6535-240">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Character**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="b6535-241">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-242">accHitTest</span></span>
-   <span data-ttu-id="b6535-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-243">accLocation</span></span>
-   <span data-ttu-id="b6535-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-244">accNavigate</span></span>
-   <span data-ttu-id="b6535-245">get- \_ accdescription</span><span class="sxs-lookup"><span data-stu-id="b6535-245">get\_accDescription</span></span>
-   <span data-ttu-id="b6535-246">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-246">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-247">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-248">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-248">get\_accName</span></span>
-   <span data-ttu-id="b6535-249">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-249">get\_accParent</span></span>
-   <span data-ttu-id="b6535-250">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-250">get\_accRole</span></span>
-   <span data-ttu-id="b6535-251">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-251">get\_accState</span></span>
-   <span data-ttu-id="b6535-252">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="b6535-253">Rollen \_ System \_ Diagramm</span><span class="sxs-lookup"><span data-stu-id="b6535-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="b6535-254">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Chart**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="b6535-255">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-256">accHitTest</span></span>
-   <span data-ttu-id="b6535-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-257">accLocation</span></span>
-   <span data-ttu-id="b6535-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-258">accNavigate</span></span>
-   <span data-ttu-id="b6535-259">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-259">get\_accChild</span></span>
-   <span data-ttu-id="b6535-260">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-260">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-261">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-261">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-262">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-262">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-263">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-264">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-265">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-265">get\_accName</span></span>
-   <span data-ttu-id="b6535-266">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-266">get\_accParent</span></span>
-   <span data-ttu-id="b6535-267">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-267">get\_accRole</span></span>
-   <span data-ttu-id="b6535-268">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="b6535-269">Rollen \_ \_ Systemuhr</span><span class="sxs-lookup"><span data-stu-id="b6535-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="b6535-270">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Clock**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="b6535-271">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-272">accHitTest</span></span>
-   <span data-ttu-id="b6535-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-273">accLocation</span></span>
-   <span data-ttu-id="b6535-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-274">accNavigate</span></span>
-   <span data-ttu-id="b6535-275">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-275">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-276">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-276">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-277">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-278">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-279">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-279">get\_accName</span></span>
-   <span data-ttu-id="b6535-280">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-280">get\_accParent</span></span>
-   <span data-ttu-id="b6535-281">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-281">get\_accRole</span></span>
-   <span data-ttu-id="b6535-282">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-282">get\_accState</span></span>
-   <span data-ttu-id="b6535-283">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="b6535-284">Rollen \_ System \_ Spalte</span><span class="sxs-lookup"><span data-stu-id="b6535-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="b6535-285">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Column**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="b6535-286">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-287">accHitTest</span></span>
-   <span data-ttu-id="b6535-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-288">accLocation</span></span>
-   <span data-ttu-id="b6535-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-289">accNavigate</span></span>
-   <span data-ttu-id="b6535-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="b6535-290">accSelect</span></span>
-   <span data-ttu-id="b6535-291">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-291">get\_accChild</span></span>
-   <span data-ttu-id="b6535-292">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-292">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-293">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-293">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-294">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-294">get\_accName</span></span>
-   <span data-ttu-id="b6535-295">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-295">get\_accParent</span></span>
-   <span data-ttu-id="b6535-296">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-296">get\_accRole</span></span>
-   <span data-ttu-id="b6535-297">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-297">get\_accState</span></span>
-   <span data-ttu-id="b6535-298">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="b6535-299">Rollen \_ System \_ Diagramm</span><span class="sxs-lookup"><span data-stu-id="b6535-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="b6535-300">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Diagram**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="b6535-301">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-302">accHitTest</span></span>
-   <span data-ttu-id="b6535-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-303">accLocation</span></span>
-   <span data-ttu-id="b6535-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-304">accNavigate</span></span>
-   <span data-ttu-id="b6535-305">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-305">get\_accChild</span></span>
-   <span data-ttu-id="b6535-306">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-306">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-307">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-307">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-308">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-308">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-309">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-310">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-311">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-311">get\_accName</span></span>
-   <span data-ttu-id="b6535-312">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-312">get\_accParent</span></span>
-   <span data-ttu-id="b6535-313">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-313">get\_accRole</span></span>
-   <span data-ttu-id="b6535-314">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="b6535-315">Rollen \_ System- \_ Wahl</span><span class="sxs-lookup"><span data-stu-id="b6535-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="b6535-316">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Dial**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="b6535-317">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="b6535-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="b6535-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-319">accHitTest</span></span>
-   <span data-ttu-id="b6535-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-320">accLocation</span></span>
-   <span data-ttu-id="b6535-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-321">accNavigate</span></span>
-   <span data-ttu-id="b6535-322">get \_ accdefaultaction</span><span class="sxs-lookup"><span data-stu-id="b6535-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="b6535-323">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-323">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-324">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-324">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-325">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-326">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-327">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-327">get\_accName</span></span>
-   <span data-ttu-id="b6535-328">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-328">get\_accParent</span></span>
-   <span data-ttu-id="b6535-329">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-329">get\_accRole</span></span>
-   <span data-ttu-id="b6535-330">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-330">get\_accState</span></span>
-   <span data-ttu-id="b6535-331">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="b6535-332">Rollen \_ System \_ Dokument</span><span class="sxs-lookup"><span data-stu-id="b6535-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="b6535-333">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Document**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="b6535-334">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-335">accHitTest</span></span>
-   <span data-ttu-id="b6535-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-336">accLocation</span></span>
-   <span data-ttu-id="b6535-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-337">accNavigate</span></span>
-   <span data-ttu-id="b6535-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="b6535-338">accSelect</span></span>
-   <span data-ttu-id="b6535-339">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-339">get\_accChild</span></span>
-   <span data-ttu-id="b6535-340">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-340">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-341">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-341">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-342">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-342">get\_accName</span></span>
-   <span data-ttu-id="b6535-343">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-343">get\_accParent</span></span>
-   <span data-ttu-id="b6535-344">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-344">get\_accRole</span></span>
-   <span data-ttu-id="b6535-345">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="b6535-346">Rollen \_ System- \_ Dropdown Liste</span><span class="sxs-lookup"><span data-stu-id="b6535-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="b6535-347">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ droplist**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="b6535-348">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="b6535-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="b6535-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-350">accHitTest</span></span>
-   <span data-ttu-id="b6535-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-351">accLocation</span></span>
-   <span data-ttu-id="b6535-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-352">accNavigate</span></span>
-   <span data-ttu-id="b6535-353">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-353">get\_accChild</span></span>
-   <span data-ttu-id="b6535-354">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-354">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-355">get \_ accdefaultaction</span><span class="sxs-lookup"><span data-stu-id="b6535-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="b6535-356">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-356">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-357">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-357">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-358">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-359">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-360">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-360">get\_accName</span></span>
-   <span data-ttu-id="b6535-361">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-361">get\_accParent</span></span>
-   <span data-ttu-id="b6535-362">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-362">get\_accRole</span></span>
-   <span data-ttu-id="b6535-363">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="b6535-364">Rollen \_ System \_ Gleichung</span><span class="sxs-lookup"><span data-stu-id="b6535-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="b6535-365">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Gleichung**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="b6535-366">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-367">accHitTest</span></span>
-   <span data-ttu-id="b6535-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-368">accLocation</span></span>
-   <span data-ttu-id="b6535-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-369">accNavigate</span></span>
-   <span data-ttu-id="b6535-370">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-370">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-371">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-371">get\_accName</span></span>
-   <span data-ttu-id="b6535-372">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-372">get\_accParent</span></span>
-   <span data-ttu-id="b6535-373">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-373">get\_accRole</span></span>
-   <span data-ttu-id="b6535-374">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-374">get\_accState</span></span>
-   <span data-ttu-id="b6535-375">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="b6535-376">Grafik zum Rollen \_ System \_</span><span class="sxs-lookup"><span data-stu-id="b6535-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="b6535-377">Weitere Informationen zu dieser Rolle finden Sie in [**der \_ \_ Grafik zum Rollen System**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="b6535-378">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-379">accHitTest</span></span>
-   <span data-ttu-id="b6535-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-380">accLocation</span></span>
-   <span data-ttu-id="b6535-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-381">accNavigate</span></span>
-   <span data-ttu-id="b6535-382">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-382">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-383">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-383">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-384">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-385">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-386">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-386">get\_accName</span></span>
-   <span data-ttu-id="b6535-387">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-387">get\_accParent</span></span>
-   <span data-ttu-id="b6535-388">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-388">get\_accRole</span></span>
-   <span data-ttu-id="b6535-389">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="b6535-390">Hilfe Sprechblase für Rollen \_ System \_</span><span class="sxs-lookup"><span data-stu-id="b6535-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="b6535-391">Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ helpballoon für Rollen Systeme**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="b6535-392">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-393">accHitTest</span></span>
-   <span data-ttu-id="b6535-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-394">accLocation</span></span>
-   <span data-ttu-id="b6535-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-395">accNavigate</span></span>
-   <span data-ttu-id="b6535-396">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-396">get\_accChild</span></span>
-   <span data-ttu-id="b6535-397">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-397">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-398">get \_ accdefaultaction</span><span class="sxs-lookup"><span data-stu-id="b6535-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="b6535-399">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-399">get\_accName</span></span>
-   <span data-ttu-id="b6535-400">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-400">get\_accParent</span></span>
-   <span data-ttu-id="b6535-401">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-401">get\_accRole</span></span>
-   <span data-ttu-id="b6535-402">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-402">get\_accState</span></span>
-   <span data-ttu-id="b6535-403">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="b6535-404">Rollen \_ System- \_ IPAddress</span><span class="sxs-lookup"><span data-stu-id="b6535-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="b6535-405">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ IPAddress**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="b6535-406">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-407">accHitTest</span></span>
-   <span data-ttu-id="b6535-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-408">accLocation</span></span>
-   <span data-ttu-id="b6535-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-409">accNavigate</span></span>
-   <span data-ttu-id="b6535-410">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-410">get\_accChild</span></span>
-   <span data-ttu-id="b6535-411">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-411">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-412">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-412">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-413">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-413">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-414">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-415">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-416">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-416">get\_accName</span></span>
-   <span data-ttu-id="b6535-417">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-417">get\_accParent</span></span>
-   <span data-ttu-id="b6535-418">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-418">get\_accRole</span></span>
-   <span data-ttu-id="b6535-419">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-419">get\_accState</span></span>
-   <span data-ttu-id="b6535-420">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="b6535-421">Rollen \_ System \_ Link</span><span class="sxs-lookup"><span data-stu-id="b6535-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="b6535-422">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Link**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="b6535-423">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="b6535-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="b6535-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-425">accHitTest</span></span>
-   <span data-ttu-id="b6535-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-426">accLocation</span></span>
-   <span data-ttu-id="b6535-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-427">accNavigate</span></span>
-   <span data-ttu-id="b6535-428">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-428">get\_accChild</span></span>
-   <span data-ttu-id="b6535-429">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-429">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-430">get \_ accdefaultaction</span><span class="sxs-lookup"><span data-stu-id="b6535-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="b6535-431">get- \_ accdescription</span><span class="sxs-lookup"><span data-stu-id="b6535-431">get\_accDescription</span></span>
-   <span data-ttu-id="b6535-432">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-432">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-433">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-434">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-434">get\_accName</span></span>
-   <span data-ttu-id="b6535-435">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-435">get\_accParent</span></span>
-   <span data-ttu-id="b6535-436">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-436">get\_accRole</span></span>
-   <span data-ttu-id="b6535-437">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-437">get\_accState</span></span>
-   <span data-ttu-id="b6535-438">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="b6535-439">Bereich "Rollen \_ System" \_</span><span class="sxs-lookup"><span data-stu-id="b6535-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="b6535-440">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Pane**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="b6535-441">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-442">accHitTest</span></span>
-   <span data-ttu-id="b6535-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-443">accLocation</span></span>
-   <span data-ttu-id="b6535-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-444">accNavigate</span></span>
-   <span data-ttu-id="b6535-445">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-445">get\_accChild</span></span>
-   <span data-ttu-id="b6535-446">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-446">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-447">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-447">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-448">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-448">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-449">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-450">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-451">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-451">get\_accName</span></span>
-   <span data-ttu-id="b6535-452">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-452">get\_accParent</span></span>
-   <span data-ttu-id="b6535-453">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-453">get\_accRole</span></span>
-   <span data-ttu-id="b6535-454">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="b6535-455">Rollen \_ System \_ Zeile</span><span class="sxs-lookup"><span data-stu-id="b6535-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="b6535-456">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Row**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="b6535-457">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-458">accHitTest</span></span>
-   <span data-ttu-id="b6535-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-459">accLocation</span></span>
-   <span data-ttu-id="b6535-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-460">accNavigate</span></span>
-   <span data-ttu-id="b6535-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="b6535-461">accSelect</span></span>
-   <span data-ttu-id="b6535-462">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-462">get\_accChild</span></span>
-   <span data-ttu-id="b6535-463">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-463">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-464">get- \_ accdescription</span><span class="sxs-lookup"><span data-stu-id="b6535-464">get\_accDescription</span></span>
-   <span data-ttu-id="b6535-465">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-465">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-466">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-466">get\_accName</span></span>
-   <span data-ttu-id="b6535-467">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-467">get\_accParent</span></span>
-   <span data-ttu-id="b6535-468">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-468">get\_accRole</span></span>
-   <span data-ttu-id="b6535-469">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-469">get\_accState</span></span>
-   <span data-ttu-id="b6535-470">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="b6535-471">Rollen \_ System ( \_ RowHeader)</span><span class="sxs-lookup"><span data-stu-id="b6535-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="b6535-472">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ RowHeader**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="b6535-473">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-474">accHitTest</span></span>
-   <span data-ttu-id="b6535-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-475">accLocation</span></span>
-   <span data-ttu-id="b6535-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-476">accNavigate</span></span>
-   <span data-ttu-id="b6535-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="b6535-477">accSelect</span></span>
-   <span data-ttu-id="b6535-478">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-478">get\_accChild</span></span>
-   <span data-ttu-id="b6535-479">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-479">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-480">get \_ accdefaultaction</span><span class="sxs-lookup"><span data-stu-id="b6535-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="b6535-481">get- \_ accdescription</span><span class="sxs-lookup"><span data-stu-id="b6535-481">get\_accDescription</span></span>
-   <span data-ttu-id="b6535-482">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-482">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-483">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-483">get\_accName</span></span>
-   <span data-ttu-id="b6535-484">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-484">get\_accParent</span></span>
-   <span data-ttu-id="b6535-485">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-485">get\_accRole</span></span>
-   <span data-ttu-id="b6535-486">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-486">get\_accState</span></span>
-   <span data-ttu-id="b6535-487">\_accValue erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="b6535-488">Rollen \_ System \_ Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b6535-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="b6535-489">Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ Trennzeichen für Rollen Systeme**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="b6535-490">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-491">accHitTest</span></span>
-   <span data-ttu-id="b6535-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-492">accLocation</span></span>
-   <span data-ttu-id="b6535-493">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-493">get\_accChild</span></span>
-   <span data-ttu-id="b6535-494">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-494">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-495">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-495">get\_accParent</span></span>
-   <span data-ttu-id="b6535-496">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-496">get\_accRole</span></span>
-   <span data-ttu-id="b6535-497">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="b6535-498">Sound des Rollen \_ Systems \_</span><span class="sxs-lookup"><span data-stu-id="b6535-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="b6535-499">Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ Sound des Rollen Systems**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="b6535-500">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-501">get- \_ accdescription</span><span class="sxs-lookup"><span data-stu-id="b6535-501">get\_accDescription</span></span>
-   <span data-ttu-id="b6535-502">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-502">get\_accName</span></span>
-   <span data-ttu-id="b6535-503">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-503">get\_accRole</span></span>
-   <span data-ttu-id="b6535-504">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="b6535-505">Rollen \_ System ( \_ SplitButton)</span><span class="sxs-lookup"><span data-stu-id="b6535-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="b6535-506">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ SplitButton**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="b6535-507">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="b6535-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="b6535-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-509">accHitTest</span></span>
-   <span data-ttu-id="b6535-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-510">accLocation</span></span>
-   <span data-ttu-id="b6535-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-511">accNavigate</span></span>
-   <span data-ttu-id="b6535-512">get \_ accdefaultaction</span><span class="sxs-lookup"><span data-stu-id="b6535-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="b6535-513">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-513">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-514">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-515">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-516">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-516">get\_accName</span></span>
-   <span data-ttu-id="b6535-517">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-517">get\_accParent</span></span>
-   <span data-ttu-id="b6535-518">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-518">get\_accRole</span></span>
-   <span data-ttu-id="b6535-519">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="b6535-520">Rollen \_ System \_ Tabelle</span><span class="sxs-lookup"><span data-stu-id="b6535-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="b6535-521">Weitere Informationen zu dieser Rolle finden Sie unter [**role \_ System \_ Table**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="b6535-522">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="b6535-523">accHitTest</span></span>
-   <span data-ttu-id="b6535-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-524">accLocation</span></span>
-   <span data-ttu-id="b6535-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="b6535-525">accNavigate</span></span>
-   <span data-ttu-id="b6535-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="b6535-526">accSelect</span></span>
-   <span data-ttu-id="b6535-527">\_accChild erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-527">get\_accChild</span></span>
-   <span data-ttu-id="b6535-528">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="b6535-528">get\_accChildCount</span></span>
-   <span data-ttu-id="b6535-529">get- \_ accdescription</span><span class="sxs-lookup"><span data-stu-id="b6535-529">get\_accDescription</span></span>
-   <span data-ttu-id="b6535-530">\_Zugriffs Fokus erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-530">get\_accFocus</span></span>
-   <span data-ttu-id="b6535-531">\_accHelp erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-531">get\_accHelp</span></span>
-   <span data-ttu-id="b6535-532">\_accHelpTopic erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="b6535-533">\_accKeyboardShortcut erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="b6535-534">\_accName erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-534">get\_accName</span></span>
-   <span data-ttu-id="b6535-535">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-535">get\_accParent</span></span>
-   <span data-ttu-id="b6535-536">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-536">get\_accRole</span></span>
-   <span data-ttu-id="b6535-537">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="b6535-538">\_Leerraum für Rollen System \_</span><span class="sxs-lookup"><span data-stu-id="b6535-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="b6535-539">Weitere Informationen zu dieser Rolle finden Sie unter [**\_ \_ Leerraum für Rollen Systeme**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="b6535-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="b6535-540">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="b6535-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="b6535-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="b6535-541">accLocation</span></span>
-   <span data-ttu-id="b6535-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="b6535-542">accSelect</span></span>
-   <span data-ttu-id="b6535-543">\_accParent erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-543">get\_accParent</span></span>
-   <span data-ttu-id="b6535-544">get- \_ Zugriffs Rolle</span><span class="sxs-lookup"><span data-stu-id="b6535-544">get\_accRole</span></span>
-   <span data-ttu-id="b6535-545">\_accState erhalten</span><span class="sxs-lookup"><span data-stu-id="b6535-545">get\_accState</span></span>

 

 