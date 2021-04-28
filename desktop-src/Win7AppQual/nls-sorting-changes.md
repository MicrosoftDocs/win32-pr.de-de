---
description: NLS-Sortierungsänderungen
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: NLS-Sortierungsänderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57cfaf2a9891c2d952637429786729670fc103c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088058"
---
# <a name="nls-sorting-changes"></a><span data-ttu-id="40a12-103">NLS-Sortierungsänderungen</span><span class="sxs-lookup"><span data-stu-id="40a12-103">NLS Sorting Changes</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="40a12-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="40a12-104">Affected Platforms</span></span>

 <span data-ttu-id="40a12-105">**Clients:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="40a12-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="40a12-106">**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="40a12-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="40a12-107">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="40a12-107">Feature Impact</span></span>

 <span data-ttu-id="40a12-108">**Schweregrad:** Hoch</span><span class="sxs-lookup"><span data-stu-id="40a12-108">**Severity** - High</span></span>  
<span data-ttu-id="40a12-109">**Häufigkeit:** Niedrig (nur wenige Apps sind beschädigt, sind jedoch immer beschädigt).</span><span class="sxs-lookup"><span data-stu-id="40a12-109">**Frequency** - Low (few apps impacted, but if impacted, always broken)</span></span>  


## <a name="description"></a><span data-ttu-id="40a12-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40a12-110">Description</span></span>

<span data-ttu-id="40a12-111">Die NlS-Funktionen (National Language Support) unterstützen Anwendungen dabei, die verschiedenen sprach- und ortsspezifischen Anforderungen von Benutzern auf der ganzen Welt zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="40a12-111">The National Language Support (NLS) functions help applications support the different language- and locale-specific needs of users around the world.</span></span> <span data-ttu-id="40a12-112">Neue Windows-Versionen enthalten fast immer NLS-Änderungen.</span><span class="sxs-lookup"><span data-stu-id="40a12-112">New Windows versions almost invariably include NLS changes.</span></span> <span data-ttu-id="40a12-113">Diese Änderung wirkt sich auf die Sortierung und Sortierung aus und somit auf Anwendungen mit persistenten Indizes.</span><span class="sxs-lookup"><span data-stu-id="40a12-113">This change affects collation and sorting, and therefore applications that have persistent indexes.</span></span>

<span data-ttu-id="40a12-114">Eine Sortierungstabelle enthält zwei Zahlen, die ihre Version (Revision) identifizieren: die definierte Version und die NLS-Version.</span><span class="sxs-lookup"><span data-stu-id="40a12-114">A collation table has two numbers that identify its version (revision): the defined version and the NLS version.</span></span> <span data-ttu-id="40a12-115">Beide Versionen sind DWORD-Werte, die aus einer Hauptversion und einer Nebenversion bestehen.</span><span class="sxs-lookup"><span data-stu-id="40a12-115">Both versions are DWORD values, composed of a major version and a minor version.</span></span> <span data-ttu-id="40a12-116">Das erste Byte eines Werts ist reserviert, die nächsten zwei Bytes stellen die Hauptversion dar, und das letzte Byte stellt die Nebenversion dar.</span><span class="sxs-lookup"><span data-stu-id="40a12-116">The first byte of a value is reserved, the next two bytes represent the major version, and the last byte represents the minor version.</span></span> <span data-ttu-id="40a12-117">Hexadezimal ist das Muster 0xRRMMMMmm, wobei R gleich Reserved, M gleich major und m gleich minor ist.</span><span class="sxs-lookup"><span data-stu-id="40a12-117">In hexadecimal terms, the pattern is 0xRRMMMMmm, where R equals Reserved, M equals major, and m equals minor.</span></span> <span data-ttu-id="40a12-118">Beispielsweise wird eine Hauptversion von 3 mit einer Nebenversion von 4 als 0x304.</span><span class="sxs-lookup"><span data-stu-id="40a12-118">For example, a major version of 3 with a minor version of 4 is represented as 0x304.</span></span>

<span data-ttu-id="40a12-119">Bei einer Hauptversion ändern sich ein oder mehrere Codepunkte, sodass die Anwendung alle Daten neu indizieren muss, damit Vergleiche gültig sind.</span><span class="sxs-lookup"><span data-stu-id="40a12-119">For a major version, one or more code points change so that the application must re-index all data for comparisons to be valid.</span></span> <span data-ttu-id="40a12-120">Bei einer Nebenversion wird nichts bewegt, aber Codepunkte werden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="40a12-120">For a minor version, nothing moves, but code points are added.</span></span> <span data-ttu-id="40a12-121">Bei dieser Version muss die Anwendung nur Zeichenfolgen mit zuvor nicht amortisierbaren Werten neu indizieren.</span><span class="sxs-lookup"><span data-stu-id="40a12-121">For this type of version, the application only has to re-index strings with previously unsortable values.</span></span> <span data-ttu-id="40a12-122">Zusammengefasst bedeutet dies, was die Versionsnummern in Bezug auf die Datenänderungen in den lokalen Ausnahmetabellen und Standardtabellen bedeuten:</span><span class="sxs-lookup"><span data-stu-id="40a12-122">In summary, here is what the version numbers mean in relation to the data changes in the locale-specific exception tables and default tables:</span></span>

<span data-ttu-id="40a12-123">**NLSVersion-Hauptversion:** Geänderte Codepunkte in den "Ausnahme"- oder lokalspezifischen Tabellen</span><span class="sxs-lookup"><span data-stu-id="40a12-123">**NLSVersion Major** – Changed code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="40a12-124">**NLSVersion-Nebenversion:** Neue Codepunkte in den tabellen "exception" oder "locale-specific" hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="40a12-124">**NLSVersion Minor** – Added new code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="40a12-125">**DefinedVersion Major:** Geänderte Codepunkte in der Standardtabelle</span><span class="sxs-lookup"><span data-stu-id="40a12-125">**DefinedVersion Major** – Changed code points in the default table</span></span>  
<span data-ttu-id="40a12-126">**DefinedVersion Minor:** Neue Codepunkte in der Standardtabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="40a12-126">**DefinedVersion Minor** – Added new code points in the default table</span></span>  


<span data-ttu-id="40a12-127">**Sortieren von Versionsnummern für veröffentlichte Versionen:**</span><span class="sxs-lookup"><span data-stu-id="40a12-127">**Sorting version numbers for released versions:**</span></span>



| <span data-ttu-id="40a12-128">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="40a12-128">Operating System</span></span>    | <span data-ttu-id="40a12-129">Release</span><span class="sxs-lookup"><span data-stu-id="40a12-129">Release</span></span>           | <span data-ttu-id="40a12-130">Version (0xRRMMMMmm)</span><span class="sxs-lookup"><span data-stu-id="40a12-130">Version (0xRRMMMMmm)</span></span>         |
|---------------------|-------------------|------------------------------|
| <span data-ttu-id="40a12-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="40a12-131">Windows XP</span></span>          | <span data-ttu-id="40a12-132">RTM/SP1/SP2/SP3/...</span><span class="sxs-lookup"><span data-stu-id="40a12-132">RTM/SP1/SP2/SP3/…</span></span> | <span data-ttu-id="40a12-133">Nicht verfügbar – keine GetNLSVersion()-API</span><span class="sxs-lookup"><span data-stu-id="40a12-133">N/A - no GetNLSVersion() API</span></span> |
| <span data-ttu-id="40a12-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="40a12-134">Windows Server 2003</span></span> | <span data-ttu-id="40a12-135">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="40a12-135">RTM/SP1</span></span>           | <span data-ttu-id="40a12-136">0x00 0000 01</span><span class="sxs-lookup"><span data-stu-id="40a12-136">0x00 0000 01</span></span>                 |
| <span data-ttu-id="40a12-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40a12-137">Windows Vista</span></span>       | <span data-ttu-id="40a12-138">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="40a12-138">RTM/SP1</span></span>           | <span data-ttu-id="40a12-139">0x00 0405 00</span><span class="sxs-lookup"><span data-stu-id="40a12-139">0x00 0405 00</span></span>                 |
| <span data-ttu-id="40a12-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40a12-140">Windows Server 2008</span></span> | <span data-ttu-id="40a12-141">RTM</span><span class="sxs-lookup"><span data-stu-id="40a12-141">RTM</span></span>               | <span data-ttu-id="40a12-142">0x00 0501 00/0x00 5001 00</span><span class="sxs-lookup"><span data-stu-id="40a12-142">0x00 0501 00 / 0x00 5001 00</span></span>  |
| <span data-ttu-id="40a12-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40a12-143">Windows 7</span></span>           | <span data-ttu-id="40a12-144">RTM</span><span class="sxs-lookup"><span data-stu-id="40a12-144">RTM</span></span>               | <span data-ttu-id="40a12-145">0x00060100</span><span class="sxs-lookup"><span data-stu-id="40a12-145">0x00060100</span></span>                   |



 

## <a name="manifestation"></a><span data-ttu-id="40a12-146">Manifestation</span><span class="sxs-lookup"><span data-stu-id="40a12-146">Manifestation</span></span>

<span data-ttu-id="40a12-147">Anwendungen (z. B. Datenbanken) mit persistenten Indizes, die die NLS-Version nicht überprüfen und bei Versionsänderung erneut indizieren, können nicht ordnungsgemäß sortiert werden oder liefern möglicherweise keine angeforderten Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="40a12-147">Applications (such as databases) with persistent indexes that do not check the NLS version and re-index upon version change will fail to sort correctly or may fail to provide requested results.</span></span>

<span data-ttu-id="40a12-148">Bei Benutzeroberflächen können Listen (z. B. alphabetisch, numerisch, alphanumerisch, Symbole und so weiter) falsch sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="40a12-148">In the case of user interfaces, lists (for example, alphabetical, numeric, alphanumeric, symbols, and so on) may sort incorrectly.</span></span>

## <a name="solution"></a><span data-ttu-id="40a12-149">Lösung</span><span class="sxs-lookup"><span data-stu-id="40a12-149">Solution</span></span>

<span data-ttu-id="40a12-150">Ihre Anwendung kann **entweder GetNLSVersionEx** (Windows Vista oder höher) oder **GetNLSVersion** (vor Windows Vista) aufrufen, um sowohl die definierte Version als auch die NLS-Version für eine Sortierungstabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="40a12-150">Your application can call either **GetNLSVersionEx** (Windows Vista or later) or **GetNLSVersion** (prior to Windows Vista) to retrieve both the defined version and the NLS version for a collation table.</span></span>

-   <span data-ttu-id="40a12-151">GetNLSVersionEx:</span><span class="sxs-lookup"><span data-stu-id="40a12-151">GetNLSVersionEx:</span></span>

<span data-ttu-id="40a12-152">*Ruft Informationen zur aktuellen Version einer angegebenen NLS-Funktion für ein durch den Namen angegebenes Gebietsschema ab.*</span><span class="sxs-lookup"><span data-stu-id="40a12-152">*Retrieves information about the current version of a specified NLS capability for a locale specified by name*</span></span>  
<span data-ttu-id="40a12-153">Mit dieser Funktion kann eine Anwendung wie Active Directory bestimmen, ob sich eine NLS-Änderung auf das gebietsschema auswirkt, das für eine bestimmte Indextabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40a12-153">This function allows an application such as Active Directory to determine whether an NLS change affects the locale used for a particular index table.</span></span> <span data-ttu-id="40a12-154">Wenn dies nicht dere ist, ist es nicht erforderlich, die Tabelle neu zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="40a12-154">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="40a12-155">Weitere Informationen finden Sie unter Behandeln von Gebietsschema- und Sprachinformationen.</span><span class="sxs-lookup"><span data-stu-id="40a12-155">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="40a12-156">Diese Funktion unterstützt benutzerdefinierte Gebietsschemas.</span><span class="sxs-lookup"><span data-stu-id="40a12-156">This function supports custom locales.</span></span> <span data-ttu-id="40a12-157">Wenn *lpLocaleName* ein zusätzliches Gebietsschema angibt, sind die abgerufenen Daten die richtigen Daten für die Sortierungsreihenfolge, die diesem ergänzenden Gebietsschema zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="40a12-157">If *lpLocaleName* specifies a supplemental locale, the data retrieved is the correct data for the collation order associated with that supplemental locale.</span></span>  

<span data-ttu-id="40a12-158">**Hinweis:** Versionen von Windows vor Windows Vista unterstützen **GetNLSVersionEx** nicht.</span><span class="sxs-lookup"><span data-stu-id="40a12-158">**Note:** Versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  


-   <span data-ttu-id="40a12-159">GetNLSVersion (wird für Anwendungen verwendet, die unter Windows-Versionen vor Windows Vista ausgeführt werden):</span><span class="sxs-lookup"><span data-stu-id="40a12-159">GetNLSVersion (use for applications running on versions of Windows prior to Windows Vista):</span></span>

<span data-ttu-id="40a12-160">*Ruft Informationen zur aktuellen Version einer angegebenen NLS-Funktion für ein gebietsschema ab, das durch bezeichner angegeben wird.*</span><span class="sxs-lookup"><span data-stu-id="40a12-160">*Retrieves information about the current version of a specified NLS capability for a locale specified by identifier*</span></span>  
<span data-ttu-id="40a12-161">Mit dieser Funktion kann eine Anwendung wie Active Directory bestimmen, ob sich eine NLS-Änderung auf den Gebietsschemabezeichner auswirkt, der für eine bestimmte Indextabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40a12-161">This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table.</span></span> <span data-ttu-id="40a12-162">Wenn dies nicht dere ist, ist es nicht erforderlich, die Tabelle neu zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="40a12-162">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="40a12-163">Weitere Informationen finden Sie unter Behandeln von Gebietsschema- und Sprachinformationen.</span><span class="sxs-lookup"><span data-stu-id="40a12-163">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="40a12-164">**Hinweis:** Diese Funktion ruft nur Informationen zu einem gebietsschema ab, das vom Bezeichner angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="40a12-164">**Note:** This function retrieves information only about a locale specified by identifier.</span></span> <span data-ttu-id="40a12-165">Die **GetNLSVersionEx-Funktion** unterstützt zusätzliche Gebietsschemas, Features und RFC 4646-Namen.</span><span class="sxs-lookup"><span data-stu-id="40a12-165">The **GetNLSVersionEx** function supports additional locales, features, and RFC 4646 names.</span></span> <span data-ttu-id="40a12-166">Versionen von Windows vor Windows Vista unterstützen **getNLSVersionEx** jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="40a12-166">However, versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  
<span data-ttu-id="40a12-167">Anwendungen, die nur unter Windows Vista und höher ausgeführt werden sollen, sollten **GetNLSVersionEx** vor dieser Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="40a12-167">Applications meant to run only on Windows Vista and later should use **GetNLSVersionEx** in preference to this function.</span></span> <span data-ttu-id="40a12-168">**GetNLSVersionEx** bietet gute Unterstützung für zusätzliche Gebietsschemas.</span><span class="sxs-lookup"><span data-stu-id="40a12-168">**GetNLSVersionEx** provides good support for supplemental locales.</span></span>  


## <a name="compatibility-test"></a><span data-ttu-id="40a12-169">Kompatibilitätstest</span><span class="sxs-lookup"><span data-stu-id="40a12-169">Compatibility Test</span></span>

<span data-ttu-id="40a12-170">**Schritte, mit denen Sie feststellen können, ob sich eine Sortierungsversion geändert hat (d. b. sie müssen neu indiziert werden):**</span><span class="sxs-lookup"><span data-stu-id="40a12-170">**Steps to tell if a collation version changed (that is, you need to re-index):**</span></span>

-   <span data-ttu-id="40a12-171">**Verwenden Sie GetNLSVersionEx(),** um eine **NLSVERSIONINFOEX-Struktur** abzurufen, wenn Sie die ursprüngliche Indizierung Ihrer Daten durchführen.</span><span class="sxs-lookup"><span data-stu-id="40a12-171">**Use GetNLSVersionEx()** to retrieve an **NLSVERSIONINFOEX** structure when doing the original indexing of your data.</span></span>
-   <span data-ttu-id="40a12-172">Speichern Sie die folgenden Eigenschaften mit Ihrem Index, um die Version zu identifizieren:  **NLSVERSIONINFOEX.dwNLSVersion** und **NLSVERSIONINFOEX.dwDefinedVersion–** Diese beiden Eigenschaften geben zusammen die Version der von Ihnen verwendeten Sortiertabelle an.</span><span class="sxs-lookup"><span data-stu-id="40a12-172">Store the following properties with your index to identify the version:  **NLSVERSIONINFOEX.dwNLSVersion** and **NLSVERSIONINFOEX.dwDefinedVersion** – These two properties together specify the version of the sorting table you are using.</span></span>  
    <span data-ttu-id="40a12-173">**NLSVERSIONINFOEX.dwEffectiveId: Gibt** das effektive Locale Ihrer Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="40a12-173">**NLSVERSIONINFOEX.dwEffectiveId** - This specifies the effective locale of your sort.</span></span> <span data-ttu-id="40a12-174">Ein benutzerdefiniertes Locale wird auf die Sortierreihenfolge eines In-Box-Locales verweisen.</span><span class="sxs-lookup"><span data-stu-id="40a12-174">A custom locale will point to an in-box locale's sort.</span></span>  
    
-   <span data-ttu-id="40a12-175">Wenn Sie den Index verwenden, **verwenden Sie GetNlsVersionEx(),** um die Version Ihrer Daten zu finden.</span><span class="sxs-lookup"><span data-stu-id="40a12-175">When using the index use **GetNlsVersionEx()** to discover the version of your data.</span></span>
-   <span data-ttu-id="40a12-176">Wenn sich eine der drei Eigenschaften geändert hat, können die von Ihnen verwendeten Sortierdaten unterschiedliche Ergebnisse zurückgeben, und jede Indizierung, die Sie erstellt haben, kann zu einem Fehler bei der Suche nach Datensätzen führen.</span><span class="sxs-lookup"><span data-stu-id="40a12-176">If any of the three properties has changed, the sorting data you are using could return different results and any indexing you have may fail to find records.</span></span>
-   <span data-ttu-id="40a12-177">Wenn Sie wissen, dass Ihre Daten keine ungültigen Unicode-Codepunkte enthalten (d. h. alle Zeichenfolgen, die **true** von einem Aufruf von **IsNLSDefinedString() zurückgegeben** haben), können Sie sie als identisch betrachten, wenn SICH NUR das niedrige Byte von **dwNLSVersion** und **dwDefinedVersion** geändert hat (die oben beschriebenen Nebenversionen).</span><span class="sxs-lookup"><span data-stu-id="40a12-177">If you KNOW that your data does not contain invalid Unicode code points (that is, all of your strings returned **TRUE** from a call to **IsNLSDefinedString()**), then you may consider them the same if ONLY the low byte of **dwNLSVersion** and **dwDefinedVersion** changed (the minor versions described above).</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="40a12-178">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="40a12-178">Links to Other Resources</span></span>

-   [<span data-ttu-id="40a12-179">Internationalisierung für Windows-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="40a12-179">Internationalization for Windows Applications</span></span>](../intl/international-support.md)
-   [<span data-ttu-id="40a12-180">GetNLSVersionEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="40a12-180">GetNLSVersionEx Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [<span data-ttu-id="40a12-181">GetNLSVersion-Funktion</span><span class="sxs-lookup"><span data-stu-id="40a12-181">GetNLSVersion Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [<span data-ttu-id="40a12-182">Erkennen, ob sich die Sortierungsversion geändert hat</span><span class="sxs-lookup"><span data-stu-id="40a12-182">How to tell if the collation version changed</span></span>](/archive/blogs/shawnste/)

 

 
