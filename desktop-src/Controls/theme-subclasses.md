---
title: Verwenden von Design Unterklassen
description: Designklassen, die Steuerelemente wie ComboBox, Edit, explorbild, Rebar, Tab und Toolbar darstellen, können untergeordnet werden, um Design Variationen für das jeweilige Steuerelement bereitzustellen.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710049"
---
# <a name="using-theme-subclasses"></a><span data-ttu-id="360a0-103">Verwenden von Design Unterklassen</span><span class="sxs-lookup"><span data-stu-id="360a0-103">Using Theme Subclasses</span></span>

<span data-ttu-id="360a0-104">Designklassen, die Steuerelemente wie ComboBox, Edit, explorbild, Rebar, Tab und Toolbar darstellen, können untergeordnet werden, um Design Variationen für das jeweilige Steuerelement bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="360a0-104">Theme classes that represent controls such as ComboBox, Edit, ExplorerBar, Rebar, Tab, and Toolbar can be subclassed in order to provide theme variations for that particular control.</span></span> <span data-ttu-id="360a0-105">Beispielsweise wird die **Schalt** Flächen Klasse als subklassifiziert, um `Start::Button` die Steuerung über das auf die Schaltfläche **Start** angewendete Design bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="360a0-105">For example, the **Button** class is subclassed as `Start::Button` in order to provide control over the theme applied to the **Start** button.</span></span>

> [!Note]  
> <span data-ttu-id="360a0-106">Verwenden Sie beim Erstellen von Unterklassen, die in diesem Thema erläutert werden, Vorsicht.</span><span class="sxs-lookup"><span data-stu-id="360a0-106">Use caution when you create subclasses like those that are discussed in this topic.</span></span> <span data-ttu-id="360a0-107">Da Unterklassen in nachfolgenden Versionen von Windows möglicherweise geändert werden oder nicht verfügbar sind, wird davon abgeraten, Sie zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="360a0-107">Because subclasses might be altered or unavailable in subsequent versions of Windows, you are discouraged from using them.</span></span>

 

## <a name="two-ways-to-use-a-theme-subclass"></a><span data-ttu-id="360a0-108">Zwei Möglichkeiten zur Verwendung einer Design Unterklasse</span><span class="sxs-lookup"><span data-stu-id="360a0-108">Two Ways to Use a Theme Subclass</span></span>

<span data-ttu-id="360a0-109">Eine Anwendung kann ein untergeordnetes Design auf eine der beiden folgenden Arten verwenden:</span><span class="sxs-lookup"><span data-stu-id="360a0-109">An application can use a subclassed theme in one of these two ways:</span></span>

-   <span data-ttu-id="360a0-110">Die [**openfomedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) -Funktion kann mit einer Zeichenfolge in der Form `subclass::class` im *pszclasslist* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="360a0-110">It can use the [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) function with a string of the form `subclass::class` in the *pszClassList* parameter.</span></span>
-   <span data-ttu-id="360a0-111">Sie kann [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) mit dem Design Unterklassen Namen im *pszSubAppName* -Parameter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="360a0-111">It can call [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) with the theme subclass name in the *pszSubAppName* parameter.</span></span>

## <a name="using-theme-messages-that-set-visual-style"></a><span data-ttu-id="360a0-112">Verwenden von Design Meldungen zum Festlegen des visuellen Stils</span><span class="sxs-lookup"><span data-stu-id="360a0-112">Using Theme Messages That Set Visual Style</span></span>

<span data-ttu-id="360a0-113">Bestimmte Steuerelemente, wie z. b. Info Leiste und Symbolleiste, stellen bestimmte Meldungen bereit, die Sie senden können, um das Steuerelement anzuweisen, eine Design Unterklasse zu verwenden</span><span class="sxs-lookup"><span data-stu-id="360a0-113">Certain controls, such as Rebar and Toolbar, provide specific messages that you can send to instruct the control to use a theme subclass.</span></span> <span data-ttu-id="360a0-114">Geben Sie für diese Steuerelemente einen Zeiger auf einen Puffer an, der den Design Unterklassen Namen im *LPARAM* -Parameter der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="360a0-114">For those controls, provide a pointer to a buffer that contains the theme subclass name in the *lParam* parameter of the message.</span></span> <span data-ttu-id="360a0-115">Verwenden Sie die generische [**ccm- \_ SetWindowTheme**](ccm-setwindowtheme.md) -Nachricht, oder verwenden Sie eine bestimmte Variante, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="360a0-115">Use the generic [**CCM\_SETWINDOWTHEME**](ccm-setwindowtheme.md) message, or use a specific variant like those shown in the following table.</span></span>



| <span data-ttu-id="360a0-116">Control</span><span class="sxs-lookup"><span data-stu-id="360a0-116">Control</span></span>    | <span data-ttu-id="360a0-117">`Message`</span><span class="sxs-lookup"><span data-stu-id="360a0-117">Message</span></span>                                             |
|------------|-----------------------------------------------------|
| <span data-ttu-id="360a0-118">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="360a0-118">Tooltip</span></span>    | [<span data-ttu-id="360a0-119">**TTM \_ SetWindowTheme**</span><span class="sxs-lookup"><span data-stu-id="360a0-119">**TTM\_SETWINDOWTHEME**</span></span>](ttm-setwindowtheme.md)   |
| <span data-ttu-id="360a0-120">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="360a0-120">Toolbar</span></span>    | [<span data-ttu-id="360a0-121">**TB \_ SetWindowTheme**</span><span class="sxs-lookup"><span data-stu-id="360a0-121">**TB\_SETWINDOWTHEME**</span></span>](tb-setwindowtheme.md)     |
| <span data-ttu-id="360a0-122">Grund leisten</span><span class="sxs-lookup"><span data-stu-id="360a0-122">Rebar</span></span>      | [<span data-ttu-id="360a0-123">**RB \_ SetWindowTheme**</span><span class="sxs-lookup"><span data-stu-id="360a0-123">**RB\_SETWINDOWTHEME**</span></span>](rb-setwindowtheme.md)     |
| <span data-ttu-id="360a0-124">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="360a0-124">ComboBoxEx</span></span> | [<span data-ttu-id="360a0-125">**CBEM \_ SetWindowTheme**</span><span class="sxs-lookup"><span data-stu-id="360a0-125">**CBEM\_SETWINDOWTHEME**</span></span>](cbem-setwindowtheme.md) |



 

<span data-ttu-id="360a0-126">In der folgenden Tabelle sind einige der Unterklassen aufgelistet, die von Windows Vista definiert werden.</span><span class="sxs-lookup"><span data-stu-id="360a0-126">The following table lists some of the subclasses that Windows Vista defines.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="360a0-127">Klasse</span><span class="sxs-lookup"><span data-stu-id="360a0-127">Class</span></span></th>
<th><span data-ttu-id="360a0-128">Unterklassen von  werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="360a0-128">Subclasses</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="360a0-129">Kombinationsfeld</span><span class="sxs-lookup"><span data-stu-id="360a0-129">ComboBox</span></span></td>
<td><ul>
<li><span data-ttu-id="360a0-130">Adresse</span><span class="sxs-lookup"><span data-stu-id="360a0-130">Address</span></span></li>
<li><span data-ttu-id="360a0-131">Adressierte adressierte</span><span class="sxs-lookup"><span data-stu-id="360a0-131">AddressComposited</span></span></li>
<li><span data-ttu-id="360a0-132">Inactiveaddress</span><span class="sxs-lookup"><span data-stu-id="360a0-132">InactiveAddress</span></span></li>
<li><span data-ttu-id="360a0-133">Inactiveaddresscomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-133">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="360a0-134">Maxaddress</span><span class="sxs-lookup"><span data-stu-id="360a0-134">MaxAddress</span></span></li>
<li><span data-ttu-id="360a0-135">Maxaddresscomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-135">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="360a0-136">Maxinactiveaddress</span><span class="sxs-lookup"><span data-stu-id="360a0-136">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="360a0-137">Maxinactiveaddresscomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-137">MaxInactiveAddressComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="360a0-138">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="360a0-138">Edit</span></span></td>
<td><ul>
<li><span data-ttu-id="360a0-139">Adresse</span><span class="sxs-lookup"><span data-stu-id="360a0-139">Address</span></span></li>
<li><span data-ttu-id="360a0-140">Adressierte adressierte</span><span class="sxs-lookup"><span data-stu-id="360a0-140">AddressComposited</span></span></li>
<li><span data-ttu-id="360a0-141">Inactiveaddress</span><span class="sxs-lookup"><span data-stu-id="360a0-141">InactiveAddress</span></span></li>
<li><span data-ttu-id="360a0-142">Inactiveaddresscomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-142">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="360a0-143">Inactivesearchboxedit</span><span class="sxs-lookup"><span data-stu-id="360a0-143">InactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="360a0-144">Inactivesearchboxeditcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-144">InactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="360a0-145">Maxaddress</span><span class="sxs-lookup"><span data-stu-id="360a0-145">MaxAddress</span></span></li>
<li><span data-ttu-id="360a0-146">Maxaddresscomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-146">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="360a0-147">Maxinactiveaddress</span><span class="sxs-lookup"><span data-stu-id="360a0-147">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="360a0-148">Maxinactiveaddresscomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-148">MaxInactiveAddressComposited</span></span></li>
<li><span data-ttu-id="360a0-149">Maxinactivesearchboxedit</span><span class="sxs-lookup"><span data-stu-id="360a0-149">MaxInactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="360a0-150">Maxinactivesearchboxeditcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-150">MaxInactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="360a0-151">Maxsearchboxedit</span><span class="sxs-lookup"><span data-stu-id="360a0-151">MaxSearchBoxEdit</span></span></li>
<li><span data-ttu-id="360a0-152">Maxsearchboxeditcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-152">MaxSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="360a0-153">Searchboxedit</span><span class="sxs-lookup"><span data-stu-id="360a0-153">SearchBoxEdit</span></span></li>
<li><span data-ttu-id="360a0-154">Searchboxeditcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-154">SearchBoxEditComposited</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="360a0-155">Grund leisten</span><span class="sxs-lookup"><span data-stu-id="360a0-155">Rebar</span></span></td>
<td><ul>
<li><span data-ttu-id="360a0-156">Browsertabbar</span><span class="sxs-lookup"><span data-stu-id="360a0-156">BrowserTabBar</span></span></li>
<li><span data-ttu-id="360a0-157">Inactivenavbar</span><span class="sxs-lookup"><span data-stu-id="360a0-157">InactiveNavbar</span></span></li>
<li><span data-ttu-id="360a0-158">Inactivenavbarcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-158">InactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="360a0-159">Maxinactivenavbar</span><span class="sxs-lookup"><span data-stu-id="360a0-159">MaxInactiveNavbar</span></span></li>
<li><span data-ttu-id="360a0-160">Maxinactivenavbarcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-160">MaxInactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="360a0-161">Maxnavbar</span><span class="sxs-lookup"><span data-stu-id="360a0-161">MaxNavbar</span></span></li>
<li><span data-ttu-id="360a0-162">Maxnavbarcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-162">MaxNavbarComposited</span></span></li>
<li><span data-ttu-id="360a0-163">Navigationsleiste</span><span class="sxs-lookup"><span data-stu-id="360a0-163">Navbar</span></span></li>
<li><span data-ttu-id="360a0-164">Navbarcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-164">NavbarComposited</span></span></li>
<li><span data-ttu-id="360a0-165">Navbarnontopmost</span><span class="sxs-lookup"><span data-stu-id="360a0-165">NavbarNonTopmost</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="360a0-166">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="360a0-166">Tab</span></span></td>
<td><ul>
<li><span data-ttu-id="360a0-167">Browsertab</span><span class="sxs-lookup"><span data-stu-id="360a0-167">BrowserTab</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="360a0-168">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="360a0-168">Toolbar</span></span></td>
<td><ul>
<li><span data-ttu-id="360a0-169">Go</span><span class="sxs-lookup"><span data-stu-id="360a0-169">Go</span></span></li>
<li><span data-ttu-id="360a0-170">Gocomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-170">GoComposited</span></span></li>
<li><span data-ttu-id="360a0-171">Inactivego</span><span class="sxs-lookup"><span data-stu-id="360a0-171">InactiveGo</span></span></li>
<li><span data-ttu-id="360a0-172">Inactivegocomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-172">InactiveGoComposited</span></span></li>
<li><span data-ttu-id="360a0-173">Maxgo</span><span class="sxs-lookup"><span data-stu-id="360a0-173">MaxGo</span></span></li>
<li><span data-ttu-id="360a0-174">Maxgocomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-174">MaxGoComposited</span></span></li>
<li><span data-ttu-id="360a0-175">Maxinactivego</span><span class="sxs-lookup"><span data-stu-id="360a0-175">MaxInactiveGo</span></span></li>
<li><span data-ttu-id="360a0-176">Maxinactivegocomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-176">MaxInactiveGoComposited</span></span></li>
<li><span data-ttu-id="360a0-177">SearchButton</span><span class="sxs-lookup"><span data-stu-id="360a0-177">SearchButton</span></span></li>
<li><span data-ttu-id="360a0-178">Searchbuttoncomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-178">SearchButtonComposited</span></span></li>
<li><span data-ttu-id="360a0-179">Reise</span><span class="sxs-lookup"><span data-stu-id="360a0-179">Travel</span></span></li>
<li><span data-ttu-id="360a0-180">Travelcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-180">TravelComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a><span data-ttu-id="360a0-181">Internet Explorer-Unterklassen</span><span class="sxs-lookup"><span data-stu-id="360a0-181">Internet Explorer Subclasses</span></span>

<span data-ttu-id="360a0-182">In Windows Vista sind die Unterklassen bestimmter Klassen, die sich in Windows Internet Explorer und Windows Explorer befinden, auch dann verfügbar, wenn es sich nicht um die Klassen selbst handelt.</span><span class="sxs-lookup"><span data-stu-id="360a0-182">In Windows Vista, the subclasses of certain classes internal to Windows Internet Explorer and Windows Explorer are available even though the classes themselves are not.</span></span> <span data-ttu-id="360a0-183">In der folgenden Tabelle sind die verfügbaren Unterklassen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="360a0-183">The following table lists the available subclasses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="360a0-184">Addressband</span><span class="sxs-lookup"><span data-stu-id="360a0-184">AddressBand</span></span></td>
<td><ul>
<li><span data-ttu-id="360a0-185">AB</span><span class="sxs-lookup"><span data-stu-id="360a0-185">AB</span></span></li>
<li><span data-ttu-id="360a0-186">Abgrün</span><span class="sxs-lookup"><span data-stu-id="360a0-186">ABGreen</span></span></li>
<li><span data-ttu-id="360a0-187">Abgreencomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-187">ABGreenComposited</span></span></li>
<li><span data-ttu-id="360a0-188">ABrot</span><span class="sxs-lookup"><span data-stu-id="360a0-188">ABRed</span></span></li>
<li><span data-ttu-id="360a0-189">Abredcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-189">ABRedComposited</span></span></li>
<li><span data-ttu-id="360a0-190">Abgelb</span><span class="sxs-lookup"><span data-stu-id="360a0-190">ABYellow</span></span></li>
<li><span data-ttu-id="360a0-191">Abgelb zusammengesetzt</span><span class="sxs-lookup"><span data-stu-id="360a0-191">ABYellowComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="360a0-192">SearchBox</span><span class="sxs-lookup"><span data-stu-id="360a0-192">SearchBox</span></span></td>
<td><ul>
<li><span data-ttu-id="360a0-193">Inactivesearchbox</span><span class="sxs-lookup"><span data-stu-id="360a0-193">InactiveSearchBox</span></span></li>
<li><span data-ttu-id="360a0-194">Inactivesearchboxcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-194">InactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="360a0-195">Maxinactivesearchbox</span><span class="sxs-lookup"><span data-stu-id="360a0-195">MaxInactiveSearchBox</span></span></li>
<li><span data-ttu-id="360a0-196">Maxinactivesearchboxcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-196">MaxInactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="360a0-197">Maxsearchbox</span><span class="sxs-lookup"><span data-stu-id="360a0-197">MaxSearchBox</span></span></li>
<li><span data-ttu-id="360a0-198">Maxsearchboxcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-198">MaxSearchBoxComposited</span></span></li>
<li><span data-ttu-id="360a0-199">Searchboxcomposited</span><span class="sxs-lookup"><span data-stu-id="360a0-199">SearchBoxComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="360a0-200">In der folgenden Tabelle sind die Besonderheiten dieser Klassen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="360a0-200">The following table shows the specifics of these classes.</span></span>



| <span data-ttu-id="360a0-201">Control</span><span class="sxs-lookup"><span data-stu-id="360a0-201">Control</span></span>     | <span data-ttu-id="360a0-202">Teil</span><span class="sxs-lookup"><span data-stu-id="360a0-202">Part</span></span>         | <span data-ttu-id="360a0-203">Zustände</span><span class="sxs-lookup"><span data-stu-id="360a0-203">States</span></span>                                                 |
|-------------|--------------|--------------------------------------------------------|
| <span data-ttu-id="360a0-204">Addressband</span><span class="sxs-lookup"><span data-stu-id="360a0-204">ADDRESSBAND</span></span> | <span data-ttu-id="360a0-205">Abbackground</span><span class="sxs-lookup"><span data-stu-id="360a0-205">ABBACKGROUND</span></span> | <span data-ttu-id="360a0-206">Normal (0x1), Hot (0x2), deaktiviert (0x3), fokussiert (0x4)</span><span class="sxs-lookup"><span data-stu-id="360a0-206">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |
| <span data-ttu-id="360a0-207">SEARCHBOX</span><span class="sxs-lookup"><span data-stu-id="360a0-207">SEARCHBOX</span></span>   | <span data-ttu-id="360a0-208">Sbbackground</span><span class="sxs-lookup"><span data-stu-id="360a0-208">SBBACKGROUND</span></span> | <span data-ttu-id="360a0-209">Normal (0x1), Hot (0x2), deaktiviert (0x3), fokussiert (0x4)</span><span class="sxs-lookup"><span data-stu-id="360a0-209">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |



 

 

 




