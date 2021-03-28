---
description: Ab Windows XP unterstützt die Systemsteuerung die Kategorisierung von System Steuerungselementen. Elemente werden registriert, damit Sie in einer oder mehreren Kategorien angezeigt werden. Es können keine neuen Kategorien erstellt werden.
title: Zuweisen von System Steuerungs Kategorien
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977408"
---
# <a name="assigning-control-panel-categories"></a><span data-ttu-id="19051-105">Zuweisen von System Steuerungs Kategorien</span><span class="sxs-lookup"><span data-stu-id="19051-105">Assigning Control Panel Categories</span></span>

<span data-ttu-id="19051-106">Ab Windows XP unterstützt die Systemsteuerung die Kategorisierung von System Steuerungselementen.</span><span class="sxs-lookup"><span data-stu-id="19051-106">As of Windows XP, Control Panel supports categorization of Control Panel items.</span></span> <span data-ttu-id="19051-107">Elemente werden registriert, damit Sie in einer oder mehreren Kategorien angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="19051-107">Items are registered to appear in one or more category.</span></span> <span data-ttu-id="19051-108">Es können keine neuen Kategorien erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="19051-108">New categories cannot be created.</span></span>

<span data-ttu-id="19051-109">Wenn Sie ein System Steuerungselement in einer oder mehreren Kategorien registrieren möchten, fügen Sie Werte wie im Abschnitt "System [Steuerungs](registering-control-panel-items.md) Element-Registrierung" oder " [dll-System Steuerungselement Registrierung](registering-control-panel-items.md) " unter "Registrieren von [System Steuerungselementen](registering-control-panel-items.md)" beschrieben hinzu.</span><span class="sxs-lookup"><span data-stu-id="19051-109">To register a Control Panel item in one or more categories, add values as explained in the [Executable Control Panel Item Registration](registering-control-panel-items.md) or [DLL Control Panel Item Registration](registering-control-panel-items.md) section of [Registering Control Panel Items](registering-control-panel-items.md), as appropriate.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19051-110">Kategorie-ID</span><span class="sxs-lookup"><span data-stu-id="19051-110">Category ID</span></span></th>
<th><span data-ttu-id="19051-111">Kategoriename (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="19051-111">Category Name (Windows 7)</span></span></th>
<th><span data-ttu-id="19051-112">Kategoriename (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="19051-112">Category Name (Windows Vista)</span></span></th>
<th><span data-ttu-id="19051-113">Kategoriename (Windows XP)</span><span class="sxs-lookup"><span data-stu-id="19051-113">Category Name (Windows XP)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19051-114">0</span><span class="sxs-lookup"><span data-stu-id="19051-114">0</span></span></td>
<td><span data-ttu-id="19051-115">&quot;Alle System Steuerungselemente&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-115">&quot;All Control Panel Items&quot;</span></span></td>
<td><span data-ttu-id="19051-116">&quot;Zusätzliche Optionen&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-116">&quot;Additional Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19051-117">In dieser Kategorie wird jedes System Steuerungselement, das keine Kategorie-ID angibt, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19051-117">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="19051-118">&quot;Weitere Optionen der Systemsteuerung&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-118">&quot;Other Control Panel Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19051-119">In dieser Kategorie wird jedes System Steuerungselement, das keine Kategorie-ID angibt, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19051-119">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19051-120">1</span><span class="sxs-lookup"><span data-stu-id="19051-120">1</span></span></td>
<td><span data-ttu-id="19051-121">&quot;Darstellung und Personalisierung&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-121">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="19051-122">&quot;Darstellung und Personalisierung&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-122">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="19051-123">&quot;Darstellung und Designs&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-123">&quot;Appearance and Themes&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19051-124">2</span><span class="sxs-lookup"><span data-stu-id="19051-124">2</span></span></td>
<td><span data-ttu-id="19051-125">&quot;Hardware und Sound&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-125">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="19051-126">&quot;Hardware und Sound&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-126">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="19051-127">&quot;Drucker und andere Hardware&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-127">&quot;Printers and Other Hardware&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19051-128">3</span><span class="sxs-lookup"><span data-stu-id="19051-128">3</span></span></td>
<td><span data-ttu-id="19051-129">&quot;Netzwerk und Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-129">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="19051-130">&quot;Netzwerk und Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-130">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="19051-131">&quot;Netzwerk-und Internet Verbindungen&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-131">&quot;Network and Internet Connections&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19051-132">4</span><span class="sxs-lookup"><span data-stu-id="19051-132">4</span></span></td>
<td><span data-ttu-id="19051-133">Nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="19051-133">No longer used.</span></span> <span data-ttu-id="19051-134">Jedes Element, das sich nur in Kategorie 4 einfügt, wird in Kategorie 2 (Hardware und Sound) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19051-134">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="19051-135">Nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="19051-135">No longer used.</span></span> <span data-ttu-id="19051-136">Jedes Element, das sich nur in Kategorie 4 einfügt, wird in Kategorie 2 (Hardware und Sound) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19051-136">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="19051-137">&quot;Sounds, Sprache und Audiogeräte&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-137">&quot;Sounds, Speech, and Audio Devices&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19051-138">5</span><span class="sxs-lookup"><span data-stu-id="19051-138">5</span></span></td>
<td><span data-ttu-id="19051-139">&quot;System und Sicherheit&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-139">&quot;System and Security&quot;</span></span></td>
<td><span data-ttu-id="19051-140">&quot;System und Wartung&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-140">&quot;System and Maintenance&quot;</span></span></td>
<td><span data-ttu-id="19051-141">&quot;Leistung und Wartung&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-141">&quot;Performance and Maintenance&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19051-142">6</span><span class="sxs-lookup"><span data-stu-id="19051-142">6</span></span></td>
<td><span data-ttu-id="19051-143">&quot;Uhr, Sprache und Region&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-143">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="19051-144">&quot;Uhr, Sprache und Region&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-144">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="19051-145">&quot;Datum, Uhrzeit, Sprache und regionale Optionen&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-145">&quot;Date, Time, Language, and Regional Options&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19051-146">7</span><span class="sxs-lookup"><span data-stu-id="19051-146">7</span></span></td>
<td><span data-ttu-id="19051-147">&quot;Erleichterte Bedienung&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-147">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="19051-148">&quot;Erleichterte Bedienung&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-148">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="19051-149">&quot;Barrierefreiheits Optionen&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-149">&quot;Accessibility Options&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19051-150">8</span><span class="sxs-lookup"><span data-stu-id="19051-150">8</span></span></td>
<td><span data-ttu-id="19051-151">&quot;Programs&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-151">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="19051-152">&quot;Programs&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-152">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="19051-153">&quot;Software&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-153">&quot;Add or Remove Programs&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19051-154">9</span><span class="sxs-lookup"><span data-stu-id="19051-154">9</span></span></td>
<td><span data-ttu-id="19051-155">&quot;User Accounts (Benutzerkonten)&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-155">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19051-156">Wenn keine Verbindung mit einer Domäne besteht, wird dies als " &quot; Benutzerkonten" und "Familien Sicherheit" bezeichnet &quot; .</span><span class="sxs-lookup"><span data-stu-id="19051-156">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="19051-157">&quot;User Accounts (Benutzerkonten)&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-157">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19051-158">Wenn keine Verbindung mit einer Domäne besteht, wird dies als " &quot; Benutzerkonten" und "Familien Sicherheit" bezeichnet &quot; .</span><span class="sxs-lookup"><span data-stu-id="19051-158">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="19051-159">&quot;User Accounts (Benutzerkonten)&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-159">&quot;User Accounts&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19051-160">10</span><span class="sxs-lookup"><span data-stu-id="19051-160">10</span></span></td>
<td><span data-ttu-id="19051-161">Nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="19051-161">No longer used.</span></span> <span data-ttu-id="19051-162">Die in dieser Kategorie registrierten Elemente werden in Kategorie 5 (System und Sicherheit) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19051-162">Items registered in this category appear in category 5 (System and Security).</span></span></td>
<td><span data-ttu-id="19051-163">&quot;Security&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-163">&quot;Security&quot;</span></span></td>
<td><span data-ttu-id="19051-164">&quot;Security Center&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-164">&quot;Security Center&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19051-165">Nur in Windows XP Service Pack 2 (SP2) oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19051-165">Available only in Windows XP Service Pack 2 (SP2) or later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19051-166">11</span><span class="sxs-lookup"><span data-stu-id="19051-166">11</span></span></td>
<td><span data-ttu-id="19051-167">Nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="19051-167">No longer used.</span></span> <span data-ttu-id="19051-168">Die in dieser Kategorie registrierten Elemente werden in Kategorie 0 (alle System Steuerungselemente) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19051-168">Items registered in this category appear in category 0 (All Control Panel Items).</span></span></td>
<td><span data-ttu-id="19051-169">&quot;Mobile PCs&quot;</span><span class="sxs-lookup"><span data-stu-id="19051-169">&quot;Mobile PC&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19051-170">Diese Kategorie ist nur auf mobilen PCs sichtbar.</span><span class="sxs-lookup"><span data-stu-id="19051-170">This category is only visible on mobile PCs.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="19051-171">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="19051-171">Not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="19051-172">In Windows XP funktionieren die Kategorien " **Programme** " und " **Benutzerkonten** " unter anderen Kategorien in der Systemsteuerung etwas anders.</span><span class="sxs-lookup"><span data-stu-id="19051-172">In Windows XP, the categories **Add or Remove Programs** and **User Accounts** work somewhat differently from other categories in Control Panel.</span></span> <span data-ttu-id="19051-173">Wenn einer dieser beiden Kategorien ein oder mehrere Elemente hinzugefügt werden, öffnet der zugehörige Link in der Systemsteuerung eine Kategorieseite.</span><span class="sxs-lookup"><span data-stu-id="19051-173">When one or more items are added to one of these two categories, the associated link in Control Panel opens a category page.</span></span> <span data-ttu-id="19051-174">Die registrierten Elemente werden im unteren Teil der Seite unter der Überschrift "oder ein System Steuerungs Symbol auswählen" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19051-174">The registered items appear in the lower portion of the page under the heading "or Pick a Control Panel icon".</span></span> <span data-ttu-id="19051-175">Wenn keine Elemente für eine dieser Kategorien registriert sind, ruft der zugehörige Link in der Systemsteuerung direkt das standardmäßige Windows-Element für diese Kategorie auf.</span><span class="sxs-lookup"><span data-stu-id="19051-175">When no items are registered for one of these categories, the associated link in Control Panel directly invokes the standard Windows item for that category.</span></span> <span data-ttu-id="19051-176">In Windows Vista und höher verfügen die Kategorie " **Programme** " und die Kategorie " **Benutzerkonten** " nicht über diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="19051-176">In Windows Vista and later, the **Programs** category and the **User Accounts** category do not have this property.</span></span>

<span data-ttu-id="19051-177">Die **Security Center** Kategorie, die nur in Windows XP SP2 verfügbar ist, ist auch etwas nicht standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="19051-177">The **Security Center** category, available only in Windows XP SP2, is also somewhat non-standard.</span></span> <span data-ttu-id="19051-178">Wenn Sie auf diese Kategorie klicken, wird die Seite **Security Center** in einem neuen Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="19051-178">Clicking this category opens the **Security Center** page in a new window.</span></span> <span data-ttu-id="19051-179">Die für **Security Center** registrierten Elemente werden im unteren Teil der Seite unter der Überschrift **Manage Security Settings for:** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19051-179">Items registered for **Security Center** appear in the lower portion of that page under the heading **Manage security settings for:**.</span></span> <span data-ttu-id="19051-180">Wenn Sie auf ein Symbol klicken, wird das System Steuerungselement geöffnet.</span><span class="sxs-lookup"><span data-stu-id="19051-180">Clicking an icon opens the Control Panel item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19051-181">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19051-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19051-182">System Steuerungselemente</span><span class="sxs-lookup"><span data-stu-id="19051-182">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="19051-183">Richtlinien zur Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="19051-183">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="19051-184">System Steuerungselemente werden registriert</span><span class="sxs-lookup"><span data-stu-id="19051-184">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="19051-185">Verwenden von CPlApplet</span><span class="sxs-lookup"><span data-stu-id="19051-185">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="19051-186">Nachrichtenverarbeitung in der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="19051-186">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="19051-187">Ausführen von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="19051-187">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="19051-188">Erweitern von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="19051-188">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="19051-189">Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement</span><span class="sxs-lookup"><span data-stu-id="19051-189">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="19051-190">Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19051-190">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




