---
description: Erfahren Sie, wie Sie das CRUMB-Argument in Windows Search, um den Bereich einer Suche zu steuern.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: CRUMB-Argument (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f56287c7182c0cf370250d53075a1c951ddf28b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403733"
---
# <a name="crumb-argument-windows-search"></a><span data-ttu-id="e245e-103">CRUMB-Argument (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="e245e-103">CRUMB Argument (Windows Search)</span></span>

<span data-ttu-id="e245e-104">Das `crumb` -Argument unterstützt vollständige AQS-Anweisungen (Advanced Query Syntax) und ist besonders nützlich, um den Bereich einer Suche zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e245e-104">The `crumb` argument supports full Advanced Query Syntax (AQS) statements and is especially useful as a means of controlling the scope of a search.</span></span> <span data-ttu-id="e245e-105">Zusätzlich zu AQS-E-Mails kann das -Argument einen speziellen Parameter unter Windows Vista und Parameter unter XP verwenden, wie weiter unten `crumb` `location` in diesem Thema `kind` `store` beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e245e-105">In addition to AQS ements, the `crumb` argument can take a special `location` parameter on Windows Vista and `kind` and `store` parameters on XP, as described later in this topic.</span></span>

<span data-ttu-id="e245e-106">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="e245e-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e245e-107">Crumb-Syntax</span><span class="sxs-lookup"><span data-stu-id="e245e-107">Crumb Syntax</span></span>](#crumb-syntax)
    -   [<span data-ttu-id="e245e-108">Allgemeine Beispiele</span><span class="sxs-lookup"><span data-stu-id="e245e-108">General Examples</span></span>](#general-examples)
-   [<span data-ttu-id="e245e-109">Verwenden von Crumb mit Vista (Standort)</span><span class="sxs-lookup"><span data-stu-id="e245e-109">Using crumb with Vista (location)</span></span>](#using-crumb-with-vista-location)
    -   [<span data-ttu-id="e245e-110">Vista-Beispiele</span><span class="sxs-lookup"><span data-stu-id="e245e-110">Vista Examples</span></span>](#vista-examples)
    -   [<span data-ttu-id="e245e-111">Konstanten für allgemeine Ordner</span><span class="sxs-lookup"><span data-stu-id="e245e-111">Constants for Common Folders</span></span>](#constants-for-common-folders)
-   [<span data-ttu-id="e245e-112">Verwenden von Crumb mit Windows XP (Art und Speicher)</span><span class="sxs-lookup"><span data-stu-id="e245e-112">Using crumb with Windows XP (kind and store)</span></span>](#using-crumb-with-windows-xp-kind-and-store)
    -   [<span data-ttu-id="e245e-113">XP-Beispiele</span><span class="sxs-lookup"><span data-stu-id="e245e-113">XP Examples</span></span>](#xp-examples)
-   [<span data-ttu-id="e245e-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="e245e-114">Related topics</span></span>](#related-topics)

 

## <a name="crumb-syntax"></a><span data-ttu-id="e245e-115">Crumb-Syntax</span><span class="sxs-lookup"><span data-stu-id="e245e-115">Crumb Syntax</span></span>

<span data-ttu-id="e245e-116">Die Crumb-Syntax lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e245e-116">The crumb syntax is as follows:</span></span>


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



<span data-ttu-id="e245e-117">Der <column> -Teil ist eine beliebige Eigenschaft im Eigenschaftensystem, und</span><span class="sxs-lookup"><span data-stu-id="e245e-117">The <column> portion is any property in the property system, and the</span></span> <value> <span data-ttu-id="e245e-118">-Teil ist ein gültiger Wert für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e245e-118">portion is a valid value for that property.</span></span> <span data-ttu-id="e245e-119">Der <label> -Teil ist ein optionaler Alias für die Eigenschaft, die als Benutzeroberflächenhinweis angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e245e-119">The <label> portion is an optional alias for the property that displays as a user interface hint.</span></span>

### <a name="general-examples"></a><span data-ttu-id="e245e-120">Allgemeine Beispiele</span><span class="sxs-lookup"><span data-stu-id="e245e-120">General Examples</span></span>


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a><span data-ttu-id="e245e-121">Verwenden von Crumb mit Vista (Standort)</span><span class="sxs-lookup"><span data-stu-id="e245e-121">Using crumb with Vista (location)</span></span>

<span data-ttu-id="e245e-122">Im crumb-Parameter unterstützt Windows Vista die vollständige AQS-Version sowie die -Eigenschaft, die nur unter Windows Vista über eine spezielle Implementierung `location` verfügt.</span><span class="sxs-lookup"><span data-stu-id="e245e-122">In the crumb parameter, Windows Vista supports full AQS and also the `location` property, which has a special implementation available only on Windows Vista.</span></span> <span data-ttu-id="e245e-123">Sie können entweder eine AQS-Zeichenfolge oder die -Eigenschaft innerhalb eines `location` einzelnen crumb-Parameters verwenden, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="e245e-123">You can use either an AQS string or the `location` property within a single crumb parameter, but not both.</span></span> <span data-ttu-id="e245e-124">Wenn der crumb-Parameter AQS enthält, wird alles andere in diesem crumb-Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e245e-124">If the crumb parameter includes AQS, everything else in that crumb parameter is ignored.</span></span>

<span data-ttu-id="e245e-125">Mit `location` der -Eigenschaft können Sie einen Zu suchpfad angeben.</span><span class="sxs-lookup"><span data-stu-id="e245e-125">The `location` property enables you to specify a path to search.</span></span> <span data-ttu-id="e245e-126">Windows Vista kann den Indexer umgehen und das Verzeichnis direkt durchlaufen, wenn sich der Speicherort außerhalb des Indexer-Durchforstungsbereichs befindet.</span><span class="sxs-lookup"><span data-stu-id="e245e-126">Windows Vista can bypass the Indexer and traverse the directory directly if the location is outside the Indexer's crawl scope.</span></span> <span data-ttu-id="e245e-127">Folglich sind diese Suchvorgänge möglicherweise langsamer als Suchvorgänge, die den Indexer verwenden.</span><span class="sxs-lookup"><span data-stu-id="e245e-127">Consequently, these searches may be slower than searches that use the Indexer.</span></span>

<span data-ttu-id="e245e-128">Wenn Sie eine Eigenschaft `location` angeben, werden zwei zusätzliche Parameter unterstützt und optional:</span><span class="sxs-lookup"><span data-stu-id="e245e-128">When you specify a `location` property, two additional parameters are supported and optional:</span></span>



| <span data-ttu-id="e245e-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="e245e-129">Parameter</span></span> | <span data-ttu-id="e245e-130">Werte</span><span class="sxs-lookup"><span data-stu-id="e245e-130">Values</span></span>                  | <span data-ttu-id="e245e-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e245e-131">Description</span></span>                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e245e-132">Aufnahme</span><span class="sxs-lookup"><span data-stu-id="e245e-132">inclusion</span></span> | <span data-ttu-id="e245e-133">include, exclude</span><span class="sxs-lookup"><span data-stu-id="e245e-133">include, exclude</span></span>        | <span data-ttu-id="e245e-134">Gibt an, ob die Abfrage Elemente in diesen Pfad ein- oder ausschließen soll.</span><span class="sxs-lookup"><span data-stu-id="e245e-134">Specifies whether the query should include or exclude items from that path.</span></span> <span data-ttu-id="e245e-135">"Include" ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="e245e-135">"Include" is the default.</span></span> <span data-ttu-id="e245e-136">Windows Vista unterstützt keine Ausschlüsse ohne Einschlüsse.</span><span class="sxs-lookup"><span data-stu-id="e245e-136">Windows Vista does not support exclusions without inclusions.</span></span> <span data-ttu-id="e245e-137">(Siehe Beispiel)</span><span class="sxs-lookup"><span data-stu-id="e245e-137">(See example)</span></span> |
| <span data-ttu-id="e245e-138">Rekursion</span><span class="sxs-lookup"><span data-stu-id="e245e-138">recursion</span></span> | <span data-ttu-id="e245e-139">rekursiv, nicht rekursiv</span><span class="sxs-lookup"><span data-stu-id="e245e-139">recursive, nonrecursive</span></span> | <span data-ttu-id="e245e-140">Gibt an, ob bei der Suche alle Unterordner beginnend mit dem am Speicherort definierten Wert erneut wiederholt werden sollen:</span><span class="sxs-lookup"><span data-stu-id="e245e-140">Specifies whether the search should recurse all subfolders starting from the value defined in the location:</span></span><value><span data-ttu-id="e245e-141">.</span><span class="sxs-lookup"><span data-stu-id="e245e-141">.</span></span> <span data-ttu-id="e245e-142">"Rekursiv" ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="e245e-142">"Recursive" is the default.</span></span>                             |



 

<span data-ttu-id="e245e-143">Für den Bereich einer Suche mithilfe des Protokolls search-ms: stehen Ihnen je nach Ziel des Bereichs unterschiedliche Optionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e245e-143">To scope a search using the search-ms: protocol, you have different options depending on the target of the scope.</span></span>

<span data-ttu-id="e245e-144">Ordner auf einem lokalen Computer:</span><span class="sxs-lookup"><span data-stu-id="e245e-144">Folder on a local machine:</span></span>

-   <span data-ttu-id="e245e-145">Verwenden Sie AQS (crumb=folder:<URL-codierten Pfad>)</span><span class="sxs-lookup"><span data-stu-id="e245e-145">Use AQS (crumb=folder:<URL-encoded path>)</span></span>
-   <span data-ttu-id="e245e-146">Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)</span><span class="sxs-lookup"><span data-stu-id="e245e-146">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="e245e-147">Ordner auf einem Remotecomputer/-netzwerk:</span><span class="sxs-lookup"><span data-stu-id="e245e-147">Folder on a remote machine/network:</span></span>

-   <span data-ttu-id="e245e-148">Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)</span><span class="sxs-lookup"><span data-stu-id="e245e-148">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="e245e-149">Ordner, auf den über einen bekannten UNC-Protokollhandler zugegriffen wird:</span><span class="sxs-lookup"><span data-stu-id="e245e-149">Folder accessed via a known UNC protocol handler:</span></span>

-   <span data-ttu-id="e245e-150">Verwenden Sie AQS (crumb=store: <UNC protocol handler name> ).</span><span class="sxs-lookup"><span data-stu-id="e245e-150">Use AQS (crumb=store:<UNC protocol handler name>)</span></span>
-   <span data-ttu-id="e245e-151">Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)</span><span class="sxs-lookup"><span data-stu-id="e245e-151">Use location argument (crumb=location:<URL-encoded path>)</span></span>

### <a name="vista-examples"></a><span data-ttu-id="e245e-152">Vista-Beispiele</span><span class="sxs-lookup"><span data-stu-id="e245e-152">Vista Examples</span></span>


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



<span data-ttu-id="e245e-153">Im ersten Beispiel wird eine Suche nach "Vacation" ausgeführt, die am Shell://Personal-Speicherort beginnt (eine spezielle Verknüpfung zum Eigene Dokumente-Ordner des Benutzers), einschließlich dieses Ordners und aller Unterordner.</span><span class="sxs-lookup"><span data-stu-id="e245e-153">The first example executes a search for "vacation" starting at the shell://Personal location (a special shortcut to the user's My Documents folder), including that folder and all subfolders.</span></span> <span data-ttu-id="e245e-154">Siehe dazu die folgende Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e245e-154">See table below.</span></span>

<span data-ttu-id="e245e-155">Im zweiten Beispiel wird eine Suche in C: \\ Bilder ausgeführt, jedoch nicht in C: \\ \\ Bildduplizieren.</span><span class="sxs-lookup"><span data-stu-id="e245e-155">The second example executes a search within C:\\Pictures, but not in C:\\Pictures\\Duplicates.</span></span>

<span data-ttu-id="e245e-156">Im dritten Beispiel wird eine Suche in C: Dokumente ausgeführt, die auf Dateien beschränkt ist, deren \\ kind-Eigenschaft auf Pics festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e245e-156">The third example executes a search within C:\\Documents, limited to files with the kind property set to pics.</span></span>

### <a name="constants-for-common-folders"></a><span data-ttu-id="e245e-157">Konstanten für allgemeine Ordner</span><span class="sxs-lookup"><span data-stu-id="e245e-157">Constants for Common Folders</span></span>

<span data-ttu-id="e245e-158">Windows Vista ermöglicht die Verwendung von [KNOWNFOLDERID-Werten,](/previous-versions//bb762584(v=vs.85)) die eine eindeutige systemunabhängige Möglichkeit bieten, spezielle Ordner zu identifizieren, die häufig von Anwendungen verwendet werden, aber möglicherweise nicht denselben Namen oder Speicherort auf einem bestimmten System haben.</span><span class="sxs-lookup"><span data-stu-id="e245e-158">Windows Vista enables the use of [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) values that provide a unique system-independent way to identify special folders used frequently by applications, but which may not have the same name or location on any given system.</span></span> <span data-ttu-id="e245e-159">Der Systemordner kann beispielsweise "C: Windows" auf einem System und \\ "C: \\ Winnt" auf einem anderen System sein.</span><span class="sxs-lookup"><span data-stu-id="e245e-159">For example, the system folder may be "C:\\Windows" on one system and "C:\\Winnt" on another.</span></span> <span data-ttu-id="e245e-160">Vor Windows Vista wurden [CSIDLs](/windows/desktop/shell/csidl) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e245e-160">Prior to Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) were used.</span></span>

<span data-ttu-id="e245e-161">Verwenden Sie diese Speicherorte mit dieser Syntax:</span><span class="sxs-lookup"><span data-stu-id="e245e-161">Use these locations with this syntax:</span></span>


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a><span data-ttu-id="e245e-162">Verwenden von Crumb mit Windows XP (Art und Speicher)</span><span class="sxs-lookup"><span data-stu-id="e245e-162">Using crumb with Windows XP (kind and store)</span></span>

<span data-ttu-id="e245e-163">Für Windows Search Windows XP (WDS 3.x) verfügen die AQS-Begriffe "kind" und "store" über eine spezielle Implementierung.</span><span class="sxs-lookup"><span data-stu-id="e245e-163">For Windows Search on Windows XP (WDS 3.x), the AQS terms "kind" and "store" have a special implementation.</span></span> <span data-ttu-id="e245e-164">Die "kind"-Werte sind dieselben [Werte, die in WDS 2.x verwendet werden.](../lwef/-search-2x-wds-perceivedtype.md)</span><span class="sxs-lookup"><span data-stu-id="e245e-164">The "kind" values are the same [values used in WDS 2.x](../lwef/-search-2x-wds-perceivedtype.md).</span></span> <span data-ttu-id="e245e-165">Die Werte für "store" umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e245e-165">The "store" values include the following:</span></span>

-   <span data-ttu-id="e245e-166">Mapi</span><span class="sxs-lookup"><span data-stu-id="e245e-166">mapi</span></span>
-   <span data-ttu-id="e245e-167">file</span><span class="sxs-lookup"><span data-stu-id="e245e-167">file</span></span>
-   <span data-ttu-id="e245e-168">outlookexpress</span><span class="sxs-lookup"><span data-stu-id="e245e-168">outlookexpress</span></span>
-   <span data-ttu-id="e245e-169">any</span><span class="sxs-lookup"><span data-stu-id="e245e-169">any</span></span>

### <a name="xp-examples"></a><span data-ttu-id="e245e-170">XP-Beispiele</span><span class="sxs-lookup"><span data-stu-id="e245e-170">XP Examples</span></span>


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



<span data-ttu-id="e245e-171">Im ersten Beispiel werden Microsoft Outlook Express-E-Mails von John mit der benutzerdefinierten Bezeichnung "OE Mail" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e245e-171">The first example returns Microsoft Outlook Express emails from John with the custom label, "OE Mail".</span></span> <span data-ttu-id="e245e-172">Im zweiten Beispiel wird eine Suche nach einer beliebigen Kommunikation von John ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e245e-172">The second example executes a search for any communication from John.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e245e-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e245e-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e245e-174">Erste Schritte mit Parameter-Value Argumenten</span><span class="sxs-lookup"><span data-stu-id="e245e-174">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="e245e-175">Locale Identifier Arguments</span><span class="sxs-lookup"><span data-stu-id="e245e-175">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="e245e-176">SYNTAX-Argument</span><span class="sxs-lookup"><span data-stu-id="e245e-176">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="e245e-177">STACKEDBY-Argument</span><span class="sxs-lookup"><span data-stu-id="e245e-177">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="e245e-178">SUBQUERY-Argument</span><span class="sxs-lookup"><span data-stu-id="e245e-178">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
