---
title: Andere Objektrollen und unterstützte Methoden (REFERENZ ZUM MSAA-UI-Element)
description: Dieses Thema enthält Informationen zu Objektrollen, die in den vorherigen Themen für Benutzeroberflächenelemente nicht enthalten sind.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444001"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="4d1dc-103">Andere Objektrollen und unterstützte Methoden (REFERENZ ZUM MSAA-UI-Element)</span><span class="sxs-lookup"><span data-stu-id="4d1dc-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="4d1dc-104">Dieses Thema enthält Informationen zu Objektrollen, die in den vorherigen Themen für Benutzeroberflächenelemente nicht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="4d1dc-105">Jede Objektrolle enthält eine Liste der [**IAccessible-Methoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Eigenschaften, die für die Objektrolle unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="4d1dc-106">Während in anderen Themen unterstützte **IAccessible-Methoden** und -Eigenschaften für Benutzeroberflächenelemente dokumentiert sind, werden in diesem Thema die Methoden und Eigenschaften aufgeführt, die für eine bestimmte Objektrolle unterstützt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="4d1dc-107">Viele der Benutzeroberflächenelemente, die möglicherweise über eine der hier aufgeführten Rollen verfügen, werden in der Regel in Browsern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="4d1dc-108">Verwenden Sie dieses Thema als Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-108">Use this topic as a guideline.</span></span> <span data-ttu-id="4d1dc-109">Es wird dringend empfohlen, Microsoft Active Accessibility Tools zu verwenden, um das erwartete Verhalten für eine einzelne Objektrolle zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="4d1dc-110">In der folgenden Tabelle sind zusätzliche Objektrollen aufgeführt, die Oleacc.dll unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="4d1dc-111">**ROLE \_ SYSTEM \_ ALERT**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="4d1dc-112">**ROLE \_ SYSTEM \_ DROPLIST**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="4d1dc-113">**\_ \_ ROLLENSYSTEMANWENDUNG**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="4d1dc-114">**\_ \_ ROLLENSYSTEMGLEICHUNG**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="4d1dc-115">**ROLE \_ SYSTEM \_ BORDER**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="4d1dc-116">**\_ \_ ROLLENSYSTEMGRAFIK**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="4d1dc-117">**\_ \_ ROLLENSYSTEMSCHALTFLÄCHEDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="4d1dc-118">**ROLE \_ SYSTEM \_ HELPBALLOON**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="4d1dc-119">**\_ \_ ROLLENSYSTEMSCHALTFLÄCHEDROPDOWNGRID**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="4d1dc-120">**\_ \_ ROLLENSYSTEM-IPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="4d1dc-121">**SCHALTFLÄCHE \_ \_ "ROLLENSYSTEM"MENU**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="4d1dc-122">**ROLE \_ SYSTEM \_ LINK**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="4d1dc-123">**\_ \_ ROLLENSYSTEMZELLE**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="4d1dc-124">**BEREICH \_ \_ "ROLLENSYSTEM"**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="4d1dc-125">**\_ \_ ROLLENSYSTEMZEICHEN**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="4d1dc-126">**ROLE \_ SYSTEM \_ ROW**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="4d1dc-127">**\_ \_ ROLLENSYSTEMDIAGRAMM**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="4d1dc-128">**ROLE \_ SYSTEM \_ ROWHEADER**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="4d1dc-129">**ROLE \_ SYSTEM \_ CLOCK**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="4d1dc-130">**\_ \_ ROLLENSYSTEMTRENNZEICHEN**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="4d1dc-131">**ROLE \_ SYSTEM \_ COLUMN**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="4d1dc-132">**ROLE \_ SYSTEM \_ SOUND**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="4d1dc-133">**\_ \_ ROLLENSYSTEMDIAGRAMM**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="4d1dc-134">**\_ \_ ROLLENSYSTEM-SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="4d1dc-135">**\_ \_ ROLLENSYSTEMWAHL**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="4d1dc-136">**ROLE \_ SYSTEM \_ TABLE**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="4d1dc-137">**ROLE \_ SYSTEM DOCUMENT (ROLLENSYSTEMDOKUMENT) \_**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="4d1dc-138">**\_ \_ ROLLENSYSTEM-LEERRAUM**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="4d1dc-139">ROLE \_ SYSTEM \_ ALERT</span><span class="sxs-lookup"><span data-stu-id="4d1dc-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="4d1dc-140">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ ALERT**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-141">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-142">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-142">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-143">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-143">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-144">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="4d1dc-145">\_ \_ ROLLENSYSTEMANWENDUNG</span><span class="sxs-lookup"><span data-stu-id="4d1dc-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="4d1dc-146">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ APPLICATION**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-147">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-148">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-149">accLocation</span></span>
-   <span data-ttu-id="4d1dc-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-150">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-151">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-151">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-152">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-152">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-153">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-153">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-154">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-154">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-155">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-156">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-157">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-157">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-158">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-158">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-159">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-159">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-160">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="4d1dc-161">ROLE \_ SYSTEM \_ BORDER</span><span class="sxs-lookup"><span data-stu-id="4d1dc-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="4d1dc-162">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ BORDER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-163">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-164">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-165">accLocation</span></span>
-   <span data-ttu-id="4d1dc-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-166">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-167">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-167">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-168">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="4d1dc-169">\_ \_ ROLLENSYSTEMSCHALTFLÄCHEDROPDOWN</span><span class="sxs-lookup"><span data-stu-id="4d1dc-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="4d1dc-170">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ BUTTONDROPDOWN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-171">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-173">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-174">accLocation</span></span>
-   <span data-ttu-id="4d1dc-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-175">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-176">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-176">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-177">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-177">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-178">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-179">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-179">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-180">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-180">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-181">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-182">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-183">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-183">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-184">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-184">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-185">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-185">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-186">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="4d1dc-187">\_ \_ ROLLENSYSTEMSCHALTFLÄCHEDROPDOWNGRID</span><span class="sxs-lookup"><span data-stu-id="4d1dc-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="4d1dc-188">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-189">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-191">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-192">accLocation</span></span>
-   <span data-ttu-id="4d1dc-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-193">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-194">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-194">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-195">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-195">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-196">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-197">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-197">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-198">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-198">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-199">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-200">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-201">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-201">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-202">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-202">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-203">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-203">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-204">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="4d1dc-205">SCHALTFLÄCHE \_ \_ "ROLLENSYSTEM"MENU</span><span class="sxs-lookup"><span data-stu-id="4d1dc-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="4d1dc-206">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ BUTTONMENU**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-207">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-209">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-210">accLocation</span></span>
-   <span data-ttu-id="4d1dc-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-211">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-212">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-213">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-213">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-214">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-214">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-215">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-216">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-217">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-217">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-218">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-218">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-219">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-219">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-220">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="4d1dc-221">\_ \_ ROLLENSYSTEMZELLE</span><span class="sxs-lookup"><span data-stu-id="4d1dc-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="4d1dc-222">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ CELL**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-223">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-224">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-225">accLocation</span></span>
-   <span data-ttu-id="4d1dc-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-226">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="4d1dc-227">accSelect</span></span>
-   <span data-ttu-id="4d1dc-228">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-228">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-229">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-229">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-230">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-230">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-231">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-231">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-232">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-233">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-234">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-234">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-235">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-235">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-236">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-236">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-237">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-237">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-238">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="4d1dc-239">\_ \_ ROLLENSYSTEMZEICHEN</span><span class="sxs-lookup"><span data-stu-id="4d1dc-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="4d1dc-240">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ CHARACTER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-241">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-242">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-243">accLocation</span></span>
-   <span data-ttu-id="4d1dc-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-244">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-245">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="4d1dc-245">get\_accDescription</span></span>
-   <span data-ttu-id="4d1dc-246">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-246">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-247">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-248">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-248">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-249">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-249">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-250">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-250">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-251">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-251">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-252">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="4d1dc-253">\_ \_ ROLLENSYSTEMDIAGRAMM</span><span class="sxs-lookup"><span data-stu-id="4d1dc-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="4d1dc-254">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ CHART**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-255">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-256">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-257">accLocation</span></span>
-   <span data-ttu-id="4d1dc-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-258">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-259">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-259">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-260">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-260">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-261">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-261">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-262">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-262">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-263">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-264">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-265">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-265">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-266">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-266">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-267">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-267">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-268">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="4d1dc-269">ROLE \_ SYSTEM \_ CLOCK</span><span class="sxs-lookup"><span data-stu-id="4d1dc-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="4d1dc-270">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ CLOCK**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-271">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-272">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-273">accLocation</span></span>
-   <span data-ttu-id="4d1dc-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-274">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-275">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-275">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-276">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-276">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-277">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-278">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-279">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-279">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-280">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-280">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-281">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-281">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-282">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-282">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-283">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="4d1dc-284">ROLE \_ SYSTEM \_ COLUMN</span><span class="sxs-lookup"><span data-stu-id="4d1dc-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="4d1dc-285">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ COLUMN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-286">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-287">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-288">accLocation</span></span>
-   <span data-ttu-id="4d1dc-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-289">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="4d1dc-290">accSelect</span></span>
-   <span data-ttu-id="4d1dc-291">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-291">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-292">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-292">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-293">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-293">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-294">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-294">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-295">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-295">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-296">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-296">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-297">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-297">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-298">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="4d1dc-299">\_ \_ ROLLENSYSTEMDIAGRAMM</span><span class="sxs-lookup"><span data-stu-id="4d1dc-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="4d1dc-300">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ DIAGRAM**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-301">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-302">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-303">accLocation</span></span>
-   <span data-ttu-id="4d1dc-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-304">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-305">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-305">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-306">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-306">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-307">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-307">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-308">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-308">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-309">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-310">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-311">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-311">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-312">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-312">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-313">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-313">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-314">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="4d1dc-315">\_ \_ ROLLENSYSTEMWAHL</span><span class="sxs-lookup"><span data-stu-id="4d1dc-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="4d1dc-316">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ DIAL**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-317">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-319">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-320">accLocation</span></span>
-   <span data-ttu-id="4d1dc-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-321">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-322">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-323">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-323">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-324">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-324">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-325">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-326">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-327">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-327">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-328">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-328">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-329">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-329">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-330">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-330">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-331">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="4d1dc-332">ROLE \_ SYSTEM DOCUMENT (ROLLENSYSTEMDOKUMENT) \_</span><span class="sxs-lookup"><span data-stu-id="4d1dc-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="4d1dc-333">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ DOCUMENT**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-334">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-335">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-336">accLocation</span></span>
-   <span data-ttu-id="4d1dc-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-337">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="4d1dc-338">accSelect</span></span>
-   <span data-ttu-id="4d1dc-339">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-339">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-340">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-340">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-341">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-341">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-342">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-342">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-343">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-343">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-344">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-344">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-345">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="4d1dc-346">ROLE \_ SYSTEM \_ DROPLIST</span><span class="sxs-lookup"><span data-stu-id="4d1dc-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="4d1dc-347">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ DROPLIST**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-348">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-350">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-351">accLocation</span></span>
-   <span data-ttu-id="4d1dc-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-352">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-353">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-353">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-354">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-354">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-355">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-356">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-356">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-357">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-357">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-358">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-359">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-360">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-360">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-361">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-361">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-362">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-362">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-363">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="4d1dc-364">\_ \_ ROLLENSYSTEMGLEICHUNG</span><span class="sxs-lookup"><span data-stu-id="4d1dc-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="4d1dc-365">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ EQUATION**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-366">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-367">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-368">accLocation</span></span>
-   <span data-ttu-id="4d1dc-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-369">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-370">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-370">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-371">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-371">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-372">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-372">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-373">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-373">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-374">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-374">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-375">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="4d1dc-376">\_ \_ ROLLENSYSTEMGRAFIK</span><span class="sxs-lookup"><span data-stu-id="4d1dc-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="4d1dc-377">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ GRAPHIC**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-378">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-379">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-380">accLocation</span></span>
-   <span data-ttu-id="4d1dc-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-381">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-382">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-382">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-383">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-383">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-384">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-385">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-386">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-386">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-387">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-387">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-388">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-388">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-389">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="4d1dc-390">ROLE \_ SYSTEM \_ HELPBALLOON</span><span class="sxs-lookup"><span data-stu-id="4d1dc-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="4d1dc-391">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ HELPBALLOON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-392">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-393">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-394">accLocation</span></span>
-   <span data-ttu-id="4d1dc-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-395">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-396">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-396">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-397">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-397">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-398">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-399">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-399">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-400">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-400">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-401">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-401">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-402">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-402">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-403">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="4d1dc-404">ROLE \_ SYSTEM \_ IPADDRESS</span><span class="sxs-lookup"><span data-stu-id="4d1dc-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="4d1dc-405">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ IPADDRESS**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-406">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-407">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-408">accLocation</span></span>
-   <span data-ttu-id="4d1dc-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-409">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-410">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-410">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-411">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-411">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-412">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-412">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-413">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-413">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-414">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-415">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-416">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-416">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-417">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-417">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-418">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-418">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-419">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-419">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-420">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="4d1dc-421">ROLE \_ SYSTEM \_ LINK</span><span class="sxs-lookup"><span data-stu-id="4d1dc-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="4d1dc-422">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ LINK**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-423">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-425">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-426">accLocation</span></span>
-   <span data-ttu-id="4d1dc-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-427">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-428">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-428">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-429">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-429">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-430">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-431">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="4d1dc-431">get\_accDescription</span></span>
-   <span data-ttu-id="4d1dc-432">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-432">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-433">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-434">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-434">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-435">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-435">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-436">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-436">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-437">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-437">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-438">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="4d1dc-439">\_BEREICH \_ "ROLLENSYSTEM"</span><span class="sxs-lookup"><span data-stu-id="4d1dc-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="4d1dc-440">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ PANE**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-441">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-442">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-443">accLocation</span></span>
-   <span data-ttu-id="4d1dc-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-444">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-445">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-445">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-446">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-446">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-447">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-447">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-448">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-448">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-449">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-450">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-451">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-451">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-452">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-452">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-453">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-453">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-454">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="4d1dc-455">ROLE \_ SYSTEM \_ ROW</span><span class="sxs-lookup"><span data-stu-id="4d1dc-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="4d1dc-456">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ ROW**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-457">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-458">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-459">accLocation</span></span>
-   <span data-ttu-id="4d1dc-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-460">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="4d1dc-461">accSelect</span></span>
-   <span data-ttu-id="4d1dc-462">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-462">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-463">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-463">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-464">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="4d1dc-464">get\_accDescription</span></span>
-   <span data-ttu-id="4d1dc-465">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-465">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-466">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-466">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-467">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-467">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-468">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-468">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-469">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-469">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-470">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="4d1dc-471">ROLE \_ SYSTEM \_ ROWHEADER</span><span class="sxs-lookup"><span data-stu-id="4d1dc-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="4d1dc-472">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ ROWHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-473">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-474">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-475">accLocation</span></span>
-   <span data-ttu-id="4d1dc-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-476">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="4d1dc-477">accSelect</span></span>
-   <span data-ttu-id="4d1dc-478">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-478">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-479">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-479">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-480">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-481">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="4d1dc-481">get\_accDescription</span></span>
-   <span data-ttu-id="4d1dc-482">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-482">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-483">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-483">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-484">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-484">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-485">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-485">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-486">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-486">get\_accState</span></span>
-   <span data-ttu-id="4d1dc-487">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="4d1dc-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="4d1dc-488">\_ \_ ROLLENSYSTEMTRENNZEICHEN</span><span class="sxs-lookup"><span data-stu-id="4d1dc-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="4d1dc-489">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ SEPARATOR**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-490">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-491">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-492">accLocation</span></span>
-   <span data-ttu-id="4d1dc-493">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-493">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-494">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-494">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-495">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-495">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-496">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-496">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-497">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="4d1dc-498">ROLE \_ SYSTEM \_ SOUND</span><span class="sxs-lookup"><span data-stu-id="4d1dc-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="4d1dc-499">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ SOUND**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-500">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-501">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="4d1dc-501">get\_accDescription</span></span>
-   <span data-ttu-id="4d1dc-502">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-502">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-503">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-503">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-504">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="4d1dc-505">\_ \_ ROLLENSYSTEM-SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="4d1dc-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="4d1dc-506">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ SPLITBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-507">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-509">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-510">accLocation</span></span>
-   <span data-ttu-id="4d1dc-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-511">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-512">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="4d1dc-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="4d1dc-513">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-513">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-514">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-515">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-516">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-516">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-517">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-517">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-518">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-518">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-519">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="4d1dc-520">ROLE \_ SYSTEM \_ TABLE</span><span class="sxs-lookup"><span data-stu-id="4d1dc-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="4d1dc-521">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ TABLE**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-522">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="4d1dc-523">accHitTest</span></span>
-   <span data-ttu-id="4d1dc-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-524">accLocation</span></span>
-   <span data-ttu-id="4d1dc-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="4d1dc-525">accNavigate</span></span>
-   <span data-ttu-id="4d1dc-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="4d1dc-526">accSelect</span></span>
-   <span data-ttu-id="4d1dc-527">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="4d1dc-527">get\_accChild</span></span>
-   <span data-ttu-id="4d1dc-528">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="4d1dc-528">get\_accChildCount</span></span>
-   <span data-ttu-id="4d1dc-529">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="4d1dc-529">get\_accDescription</span></span>
-   <span data-ttu-id="4d1dc-530">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="4d1dc-530">get\_accFocus</span></span>
-   <span data-ttu-id="4d1dc-531">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="4d1dc-531">get\_accHelp</span></span>
-   <span data-ttu-id="4d1dc-532">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="4d1dc-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="4d1dc-533">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="4d1dc-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="4d1dc-534">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="4d1dc-534">get\_accName</span></span>
-   <span data-ttu-id="4d1dc-535">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-535">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-536">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-536">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-537">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="4d1dc-538">\_ \_ ROLLENSYSTEM-LEERRAUM</span><span class="sxs-lookup"><span data-stu-id="4d1dc-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="4d1dc-539">Weitere Informationen zu dieser Rolle finden Sie unter [**ROLE \_ SYSTEM \_ WHITESPACE**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d1dc-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="4d1dc-540">**Unterstützte Eigenschaften und Methoden**</span><span class="sxs-lookup"><span data-stu-id="4d1dc-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="4d1dc-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="4d1dc-541">accLocation</span></span>
-   <span data-ttu-id="4d1dc-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="4d1dc-542">accSelect</span></span>
-   <span data-ttu-id="4d1dc-543">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="4d1dc-543">get\_accParent</span></span>
-   <span data-ttu-id="4d1dc-544">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="4d1dc-544">get\_accRole</span></span>
-   <span data-ttu-id="4d1dc-545">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="4d1dc-545">get\_accState</span></span>

 

 