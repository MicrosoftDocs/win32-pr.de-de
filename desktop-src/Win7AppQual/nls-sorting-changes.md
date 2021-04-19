---
description: .
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: NLS-Sortier Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4935a6874e28270e73904eb352cd6332e650b7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314953"
---
# <a name="nls-sorting-changes"></a><span data-ttu-id="719a5-103">NLS-Sortier Änderungen</span><span class="sxs-lookup"><span data-stu-id="719a5-103">NLS Sorting Changes</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="719a5-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="719a5-104">Affected Platforms</span></span>

 <span data-ttu-id="719a5-105">**Clients** -Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="719a5-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="719a5-106">**Server** -Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="719a5-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="719a5-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="719a5-107">Feature Impact</span></span>

 <span data-ttu-id="719a5-108">**Schweregrad** -hoch</span><span class="sxs-lookup"><span data-stu-id="719a5-108">**Severity** - High</span></span>  
<span data-ttu-id="719a5-109">**Häufigkeit** -niedrig (wenige apps betroffen, aber wenn betroffen, immer beschädigt)</span><span class="sxs-lookup"><span data-stu-id="719a5-109">**Frequency** - Low (few apps impacted, but if impacted, always broken)</span></span>  


## <a name="description"></a><span data-ttu-id="719a5-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="719a5-110">Description</span></span>

<span data-ttu-id="719a5-111">Mithilfe der NLS-Funktionen (National Language Support) unterstützen Anwendungen die verschiedenen Sprach-und Gebiets Schema spezifischen Anforderungen von Benutzern auf der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="719a5-111">The National Language Support (NLS) functions help applications support the different language- and locale-specific needs of users around the world.</span></span> <span data-ttu-id="719a5-112">Neue Windows-Versionen enthalten fast ausnahmslos nls-Änderungen.</span><span class="sxs-lookup"><span data-stu-id="719a5-112">New Windows versions almost invariably include NLS changes.</span></span> <span data-ttu-id="719a5-113">Diese Änderung wirkt sich auf Sortierung und Sortierung aus, und damit auf Anwendungen mit permanenten Indizes.</span><span class="sxs-lookup"><span data-stu-id="719a5-113">This change affects collation and sorting, and therefore applications that have persistent indexes.</span></span>

<span data-ttu-id="719a5-114">Eine Sortierungs Tabelle verfügt über zwei Zahlen, die Ihre Version (Revision) identifizieren: die definierte Version und die NLS-Version.</span><span class="sxs-lookup"><span data-stu-id="719a5-114">A collation table has two numbers that identify its version (revision): the defined version and the NLS version.</span></span> <span data-ttu-id="719a5-115">Beide Versionen sind DWORD-Werte, die aus einer Hauptversion und einer neben Version bestehen.</span><span class="sxs-lookup"><span data-stu-id="719a5-115">Both versions are DWORD values, composed of a major version and a minor version.</span></span> <span data-ttu-id="719a5-116">Das erste Byte eines Werts ist reserviert, die nächsten zwei Bytes stellen die Hauptversion dar, und das letzte Byte stellt die neben Version dar.</span><span class="sxs-lookup"><span data-stu-id="719a5-116">The first byte of a value is reserved, the next two bytes represent the major version, and the last byte represents the minor version.</span></span> <span data-ttu-id="719a5-117">In hexadezimalen begriffen ist das Muster "0xrrmmmmmm", wobei "R" reserviert ist, "m" den Wert "Major" und "m" kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="719a5-117">In hexadecimal terms, the pattern is 0xRRMMMMmm, where R equals Reserved, M equals major, and m equals minor.</span></span> <span data-ttu-id="719a5-118">Beispielsweise wird eine Hauptversion von 3 mit einer neben Version von 4 als 0x304 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="719a5-118">For example, a major version of 3 with a minor version of 4 is represented as 0x304.</span></span>

<span data-ttu-id="719a5-119">Bei einer Hauptversion wird ein oder mehrere Code Punkte geändert, sodass die Anwendung alle Daten neu indizieren muss, damit Vergleiche gültig sind.</span><span class="sxs-lookup"><span data-stu-id="719a5-119">For a major version, one or more code points change so that the application must re-index all data for comparisons to be valid.</span></span> <span data-ttu-id="719a5-120">Bei einer neben Version wird nichts verschoben, aber es werden Code Punkte hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="719a5-120">For a minor version, nothing moves, but code points are added.</span></span> <span data-ttu-id="719a5-121">Bei dieser Art von Version muss die Anwendung nur Zeichen folgen mit zuvor nicht sortierbar-Werten neu indizieren.</span><span class="sxs-lookup"><span data-stu-id="719a5-121">For this type of version, the application only has to re-index strings with previously unsortable values.</span></span> <span data-ttu-id="719a5-122">Im folgenden finden Sie eine Zusammenfassung der Versionsnummern in Bezug auf die Datenänderungen in den Gebiets Schema spezifischen Ausnahme Tabellen und Standard Tabellen:</span><span class="sxs-lookup"><span data-stu-id="719a5-122">In summary, here is what the version numbers mean in relation to the data changes in the locale-specific exception tables and default tables:</span></span>

<span data-ttu-id="719a5-123">**Nlsversion Major** – geänderte Code Punkte in den "Exception"-oder "Locale-Specific"-Tabellen</span><span class="sxs-lookup"><span data-stu-id="719a5-123">**NLSVersion Major** – Changed code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="719a5-124">**Nlsversion Minor** – neue Code Punkte in den "Exception"-oder "Locale-Specific"-Tabellen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="719a5-124">**NLSVersion Minor** – Added new code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="719a5-125">**Definedversion Major** – geänderte Code Punkte in der Standardtabelle</span><span class="sxs-lookup"><span data-stu-id="719a5-125">**DefinedVersion Major** – Changed code points in the default table</span></span>  
<span data-ttu-id="719a5-126">**Definedversion Minor** – neue Code Punkte in der Standardtabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="719a5-126">**DefinedVersion Minor** – Added new code points in the default table</span></span>  


<span data-ttu-id="719a5-127">**Sortieren von Versionsnummern für veröffentlichte Versionen:**</span><span class="sxs-lookup"><span data-stu-id="719a5-127">**Sorting version numbers for released versions:**</span></span>



| <span data-ttu-id="719a5-128">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="719a5-128">Operating System</span></span>    | <span data-ttu-id="719a5-129">Release</span><span class="sxs-lookup"><span data-stu-id="719a5-129">Release</span></span>           | <span data-ttu-id="719a5-130">Version (0xrrmmmmmm)</span><span class="sxs-lookup"><span data-stu-id="719a5-130">Version (0xRRMMMMmm)</span></span>         |
|---------------------|-------------------|------------------------------|
| <span data-ttu-id="719a5-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="719a5-131">Windows XP</span></span>          | <span data-ttu-id="719a5-132">RTM/SP1/SP2/SP3/...</span><span class="sxs-lookup"><span data-stu-id="719a5-132">RTM/SP1/SP2/SP3/…</span></span> | <span data-ttu-id="719a5-133">N/v-keine getnlsversion ()-API</span><span class="sxs-lookup"><span data-stu-id="719a5-133">N/A - no GetNLSVersion() API</span></span> |
| <span data-ttu-id="719a5-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="719a5-134">Windows Server 2003</span></span> | <span data-ttu-id="719a5-135">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="719a5-135">RTM/SP1</span></span>           | <span data-ttu-id="719a5-136">0x00 0000 01</span><span class="sxs-lookup"><span data-stu-id="719a5-136">0x00 0000 01</span></span>                 |
| <span data-ttu-id="719a5-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="719a5-137">Windows Vista</span></span>       | <span data-ttu-id="719a5-138">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="719a5-138">RTM/SP1</span></span>           | <span data-ttu-id="719a5-139">0x00 0405 00</span><span class="sxs-lookup"><span data-stu-id="719a5-139">0x00 0405 00</span></span>                 |
| <span data-ttu-id="719a5-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="719a5-140">Windows Server 2008</span></span> | <span data-ttu-id="719a5-141">RTM</span><span class="sxs-lookup"><span data-stu-id="719a5-141">RTM</span></span>               | <span data-ttu-id="719a5-142">0x00 0501 00/0x00 5001 00</span><span class="sxs-lookup"><span data-stu-id="719a5-142">0x00 0501 00 / 0x00 5001 00</span></span>  |
| <span data-ttu-id="719a5-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="719a5-143">Windows 7</span></span>           | <span data-ttu-id="719a5-144">RTM</span><span class="sxs-lookup"><span data-stu-id="719a5-144">RTM</span></span>               | <span data-ttu-id="719a5-145">0x00060100</span><span class="sxs-lookup"><span data-stu-id="719a5-145">0x00060100</span></span>                   |



 

## <a name="manifestation"></a><span data-ttu-id="719a5-146">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="719a5-146">Manifestation</span></span>

<span data-ttu-id="719a5-147">Anwendungen (z. b. Datenbanken) mit permanenten Indizes, die die NLS-Version nicht überprüfen und bei der Versionsänderung neu indizieren, können nicht ordnungsgemäß sortiert werden oder die angeforderten Ergebnisse nicht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="719a5-147">Applications (such as databases) with persistent indexes that do not check the NLS version and re-index upon version change will fail to sort correctly or may fail to provide requested results.</span></span>

<span data-ttu-id="719a5-148">Im Fall von Benutzeroberflächen können Listen (z. b. alphabetisch, numerisch, alphanumerisch, Symbole usw.) falsch sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="719a5-148">In the case of user interfaces, lists (for example, alphabetical, numeric, alphanumeric, symbols, and so on) may sort incorrectly.</span></span>

## <a name="solution"></a><span data-ttu-id="719a5-149">Lösung</span><span class="sxs-lookup"><span data-stu-id="719a5-149">Solution</span></span>

<span data-ttu-id="719a5-150">Die Anwendung kann entweder **GetNLSVersionEx** (Windows Vista oder höher) oder **getnlsversion** (vor Windows Vista) aufrufen, um sowohl die definierte Version als auch die NLS-Version für eine Sortierungs Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="719a5-150">Your application can call either **GetNLSVersionEx** (Windows Vista or later) or **GetNLSVersion** (prior to Windows Vista) to retrieve both the defined version and the NLS version for a collation table.</span></span>

-   <span data-ttu-id="719a5-151">GetNLSVersionEx:</span><span class="sxs-lookup"><span data-stu-id="719a5-151">GetNLSVersionEx:</span></span>

<span data-ttu-id="719a5-152">*Ruft Informationen über die aktuelle Version einer angegebenen nls-Funktion für ein durch den Namen angegebenes Gebiets Schema ab.*</span><span class="sxs-lookup"><span data-stu-id="719a5-152">*Retrieves information about the current version of a specified NLS capability for a locale specified by name*</span></span>  
<span data-ttu-id="719a5-153">Mit dieser Funktion kann eine Anwendung wie Active Directory bestimmen, ob sich eine NLS-Änderung auf das für eine bestimmte Indextabelle verwendete Gebiets Schema auswirkt.</span><span class="sxs-lookup"><span data-stu-id="719a5-153">This function allows an application such as Active Directory to determine whether an NLS change affects the locale used for a particular index table.</span></span> <span data-ttu-id="719a5-154">Wenn dies nicht der Fall ist, muss die Tabelle nicht neu indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="719a5-154">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="719a5-155">Weitere Informationen finden Sie unter Behandeln von Gebiets Schema-und Sprachinformationen.</span><span class="sxs-lookup"><span data-stu-id="719a5-155">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="719a5-156">Diese Funktion unterstützt benutzerdefinierte Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="719a5-156">This function supports custom locales.</span></span> <span data-ttu-id="719a5-157">Wenn *lplocalename* ein zusätzliches Gebiets Schema angibt, sind die abgerufenen Daten die richtigen Daten für die Sortierreihenfolge, die dem ergänzenden Gebiets Schema zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="719a5-157">If *lpLocaleName* specifies a supplemental locale, the data retrieved is the correct data for the collation order associated with that supplemental locale.</span></span>  

<span data-ttu-id="719a5-158">**Hinweis:** Von Windows-Versionen vor Windows Vista wird **GetNLSVersionEx** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="719a5-158">**Note:** Versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  


-   <span data-ttu-id="719a5-159">Getnlsversion (Verwendung für Anwendungen, die auf Windows-Versionen vor Windows Vista ausgeführt werden):</span><span class="sxs-lookup"><span data-stu-id="719a5-159">GetNLSVersion (use for applications running on versions of Windows prior to Windows Vista):</span></span>

<span data-ttu-id="719a5-160">*Ruft Informationen über die aktuelle Version einer angegebenen nls-Funktion für ein durch den Bezeichner festgelegtes Gebiets Schema ab.*</span><span class="sxs-lookup"><span data-stu-id="719a5-160">*Retrieves information about the current version of a specified NLS capability for a locale specified by identifier*</span></span>  
<span data-ttu-id="719a5-161">Diese Funktion ermöglicht es einer Anwendung, wie z. b. Active Directory, festzustellen, ob eine NLS-Änderung den für eine bestimmte Indextabelle verwendeten Gebiets Schema Bezeichner beeinflusst</span><span class="sxs-lookup"><span data-stu-id="719a5-161">This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table.</span></span> <span data-ttu-id="719a5-162">Wenn dies nicht der Fall ist, muss die Tabelle nicht neu indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="719a5-162">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="719a5-163">Weitere Informationen finden Sie unter Behandeln von Gebiets Schema-und Sprachinformationen.</span><span class="sxs-lookup"><span data-stu-id="719a5-163">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="719a5-164">**Hinweis:** Diese Funktion ruft nur Informationen über ein durch den Bezeichner festgelegtes Gebiets Schema ab.</span><span class="sxs-lookup"><span data-stu-id="719a5-164">**Note:** This function retrieves information only about a locale specified by identifier.</span></span> <span data-ttu-id="719a5-165">Die **GetNLSVersionEx** -Funktion unterstützt zusätzliche Gebiets Schemata, Features und RFC 4646-Namen.</span><span class="sxs-lookup"><span data-stu-id="719a5-165">The **GetNLSVersionEx** function supports additional locales, features, and RFC 4646 names.</span></span> <span data-ttu-id="719a5-166">Allerdings wird von Windows-Versionen vor Windows Vista **GetNLSVersionEx** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="719a5-166">However, versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  
<span data-ttu-id="719a5-167">Anwendungen, die nur unter Windows Vista und höher ausgeführt werden sollen, sollten **GetNLSVersionEx** für diese Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="719a5-167">Applications meant to run only on Windows Vista and later should use **GetNLSVersionEx** in preference to this function.</span></span> <span data-ttu-id="719a5-168">**GetNLSVersionEx** bietet eine gute Unterstützung für zusätzliche Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="719a5-168">**GetNLSVersionEx** provides good support for supplemental locales.</span></span>  


## <a name="compatibility-test"></a><span data-ttu-id="719a5-169">Kompatibilitäts Test</span><span class="sxs-lookup"><span data-stu-id="719a5-169">Compatibility Test</span></span>

<span data-ttu-id="719a5-170">**Schritte, um zu ermitteln, ob eine Sortierungs Version geändert wurde (d. h., Sie müssen den Index neu indizieren):**</span><span class="sxs-lookup"><span data-stu-id="719a5-170">**Steps to tell if a collation version changed (that is, you need to re-index):**</span></span>

-   <span data-ttu-id="719a5-171">**Verwenden Sie GetNLSVersionEx ()** , um eine **nlsversioninfoex** -Struktur abzurufen, wenn Sie die ursprüngliche Indizierung Ihrer Daten durchführen.</span><span class="sxs-lookup"><span data-stu-id="719a5-171">**Use GetNLSVersionEx()** to retrieve an **NLSVERSIONINFOEX** structure when doing the original indexing of your data.</span></span>
-   <span data-ttu-id="719a5-172">Speichern Sie die folgenden Eigenschaften mit Ihrem Index, um die Version zu identifizieren:  **nlsversioninfoex. dwnlsversion** und **nlsversioninfoex. dwdefinedversion** – diese beiden Eigenschaften geben die Version der Sortier Tabelle an, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="719a5-172">Store the following properties with your index to identify the version:  **NLSVERSIONINFOEX.dwNLSVersion** and **NLSVERSIONINFOEX.dwDefinedVersion** – These two properties together specify the version of the sorting table you are using.</span></span>  
    <span data-ttu-id="719a5-173">**Nlsversioninfoex. dweffectiveid** : gibt das effektive Gebiets Schema Ihrer Sortierreihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="719a5-173">**NLSVERSIONINFOEX.dwEffectiveId** - This specifies the effective locale of your sort.</span></span> <span data-ttu-id="719a5-174">Ein benutzerdefiniertes Gebiets Schema verweist auf die Sortierung eines in Box-Box-Schemas.</span><span class="sxs-lookup"><span data-stu-id="719a5-174">A custom locale will point to an in-box locale's sort.</span></span>  
    
-   <span data-ttu-id="719a5-175">Wenn Sie den Index verwenden, verwenden Sie **GetNLSVersionEx ()** , um die Version der Daten zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="719a5-175">When using the index use **GetNlsVersionEx()** to discover the version of your data.</span></span>
-   <span data-ttu-id="719a5-176">Wenn eine der drei Eigenschaften geändert wurde, können die von Ihnen verwendeten Sortier Daten andere Ergebnisse zurückgeben, und jede Indizierung kann möglicherweise keine Datensätze finden.</span><span class="sxs-lookup"><span data-stu-id="719a5-176">If any of the three properties has changed, the sorting data you are using could return different results and any indexing you have may fail to find records.</span></span>
-   <span data-ttu-id="719a5-177">Wenn Sie wissen, dass Ihre Daten keine ungültigen Unicode-Code Punkte enthalten (d. h., alle Zeichen folgen werden von einem **IsNLSDefinedString ()-IsNLSDefinedString**-Befehl als " **true** " zurückgegeben), dann können Sie diese identisch sein, wenn nur das niedrige Byte von **dwnlsversion** und **dwdefinedversion** geändert wurde</span><span class="sxs-lookup"><span data-stu-id="719a5-177">If you KNOW that your data does not contain invalid Unicode code points (that is, all of your strings returned **TRUE** from a call to **IsNLSDefinedString()**), then you may consider them the same if ONLY the low byte of **dwNLSVersion** and **dwDefinedVersion** changed (the minor versions described above).</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="719a5-178">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="719a5-178">Links to Other Resources</span></span>

-   [<span data-ttu-id="719a5-179">Internationalisierung für Windows-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="719a5-179">Internationalization for Windows Applications</span></span>](../intl/international-support.md)
-   [<span data-ttu-id="719a5-180">GetNLSVersionEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="719a5-180">GetNLSVersionEx Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [<span data-ttu-id="719a5-181">Getnlsversion-Funktion</span><span class="sxs-lookup"><span data-stu-id="719a5-181">GetNLSVersion Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [<span data-ttu-id="719a5-182">Erkennen, ob die Sortierungs Version geändert wurde</span><span class="sxs-lookup"><span data-stu-id="719a5-182">How to tell if the collation version changed</span></span>](/archive/blogs/shawnste/)

 

 
