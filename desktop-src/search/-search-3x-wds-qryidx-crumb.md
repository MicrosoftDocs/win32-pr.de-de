---
description: Das Breadcrumb)-Argument unterstützt vollständige Anweisungen der erweiterten Abfrage Syntax (AQS) und ist besonders nützlich, um den Suchbereich zu steuern.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Crumb-Argument (Windows-Suche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f36764174e0eecaedee4a9c360bb9d7dabca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128596"
---
# <a name="crumb-argument-windows-search"></a><span data-ttu-id="094ac-103">Crumb-Argument (Windows-Suche)</span><span class="sxs-lookup"><span data-stu-id="094ac-103">CRUMB Argument (Windows Search)</span></span>

<span data-ttu-id="094ac-104">Das `crumb` -Argument unterstützt vollständige Anweisungen der erweiterten Abfrage Syntax (AQS) und ist besonders nützlich, um den Suchbereich zu steuern.</span><span class="sxs-lookup"><span data-stu-id="094ac-104">The `crumb` argument supports full Advanced Query Syntax (AQS) statements and is especially useful as a means of controlling the scope of a search.</span></span> <span data-ttu-id="094ac-105">Zusätzlich zu den AQS-Elementen kann das- `crumb` Argument einen speziellen `location` Parameter für Windows Vista und `kind` und `store` Parameter in XP verwenden, wie weiter unten in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="094ac-105">In addition to AQS ements, the `crumb` argument can take a special `location` parameter on Windows Vista and `kind` and `store` parameters on XP, as described later in this topic.</span></span>

<span data-ttu-id="094ac-106">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="094ac-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="094ac-107">Crumb-Syntax</span><span class="sxs-lookup"><span data-stu-id="094ac-107">Crumb Syntax</span></span>](#crumb-syntax)
    -   [<span data-ttu-id="094ac-108">Allgemeine Beispiele</span><span class="sxs-lookup"><span data-stu-id="094ac-108">General Examples</span></span>](#general-examples)
-   [<span data-ttu-id="094ac-109">Verwenden von Breadcrumb) mit Vista (Speicherort)</span><span class="sxs-lookup"><span data-stu-id="094ac-109">Using crumb with Vista (location)</span></span>](#using-crumb-with-vista-location)
    -   [<span data-ttu-id="094ac-110">Vista-Beispiele</span><span class="sxs-lookup"><span data-stu-id="094ac-110">Vista Examples</span></span>](#vista-examples)
    -   [<span data-ttu-id="094ac-111">Konstanten für allgemeine Ordner</span><span class="sxs-lookup"><span data-stu-id="094ac-111">Constants for Common Folders</span></span>](#constants-for-common-folders)
-   [<span data-ttu-id="094ac-112">Verwenden von Breadcrumb) mit Windows XP (Kind und Store)</span><span class="sxs-lookup"><span data-stu-id="094ac-112">Using crumb with Windows XP (kind and store)</span></span>](#using-crumb-with-windows-xp-kind-and-store)
    -   [<span data-ttu-id="094ac-113">XP-Beispiele</span><span class="sxs-lookup"><span data-stu-id="094ac-113">XP Examples</span></span>](#xp-examples)
-   [<span data-ttu-id="094ac-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="094ac-114">Related topics</span></span>](#related-topics)

 

## <a name="crumb-syntax"></a><span data-ttu-id="094ac-115">Crumb-Syntax</span><span class="sxs-lookup"><span data-stu-id="094ac-115">Crumb Syntax</span></span>

<span data-ttu-id="094ac-116">Die Breadcrumb)-Syntax lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="094ac-116">The crumb syntax is as follows:</span></span>


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



<span data-ttu-id="094ac-117">Der <column> Teil ist eine beliebige Eigenschaft im Eigenschaften System, und der</span><span class="sxs-lookup"><span data-stu-id="094ac-117">The <column> portion is any property in the property system, and the</span></span> <value> <span data-ttu-id="094ac-118">"Teil" ist ein gültiger Wert für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="094ac-118">portion is a valid value for that property.</span></span> <span data-ttu-id="094ac-119">Der- <label> Teil ist ein optionaler Alias für die Eigenschaft, die als Benutzeroberflächen Hinweis angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="094ac-119">The <label> portion is an optional alias for the property that displays as a user interface hint.</span></span>

### <a name="general-examples"></a><span data-ttu-id="094ac-120">Allgemeine Beispiele</span><span class="sxs-lookup"><span data-stu-id="094ac-120">General Examples</span></span>


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a><span data-ttu-id="094ac-121">Verwenden von Breadcrumb) mit Vista (Speicherort)</span><span class="sxs-lookup"><span data-stu-id="094ac-121">Using crumb with Vista (location)</span></span>

<span data-ttu-id="094ac-122">Im Breadcrumb)-Parameter unterstützt Windows Vista vollständige AQS und auch die- `location` Eigenschaft, die über eine spezielle Implementierung verfügt, die nur unter Windows Vista verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="094ac-122">In the crumb parameter, Windows Vista supports full AQS and also the `location` property, which has a special implementation available only on Windows Vista.</span></span> <span data-ttu-id="094ac-123">Sie können entweder eine AQS-Zeichenfolge oder die- `location` Eigenschaft innerhalb eines einzelnen Breadcrumb)-Parameters verwenden, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="094ac-123">You can use either an AQS string or the `location` property within a single crumb parameter, but not both.</span></span> <span data-ttu-id="094ac-124">Wenn der Breadcrumb)-Parameter AQS enthält, wird alles andere in diesem Breadcrumb)-Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="094ac-124">If the crumb parameter includes AQS, everything else in that crumb parameter is ignored.</span></span>

<span data-ttu-id="094ac-125">Mit der- `location` Eigenschaft können Sie einen zu suchenden Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="094ac-125">The `location` property enables you to specify a path to search.</span></span> <span data-ttu-id="094ac-126">Windows Vista kann den Indexer umgehen und das Verzeichnis direkt durchlaufen, wenn der Speicherort außerhalb des Durchforstungs Bereichs des Indexers liegt.</span><span class="sxs-lookup"><span data-stu-id="094ac-126">Windows Vista can bypass the Indexer and traverse the directory directly if the location is outside the Indexer's crawl scope.</span></span> <span data-ttu-id="094ac-127">Folglich sind diese Suchvorgänge möglicherweise langsamer als Suchvorgänge, die den Indexer verwenden.</span><span class="sxs-lookup"><span data-stu-id="094ac-127">Consequently, these searches may be slower than searches that use the Indexer.</span></span>

<span data-ttu-id="094ac-128">Wenn Sie eine `location` Eigenschaft angeben, werden zwei zusätzliche Parameter unterstützt und optional:</span><span class="sxs-lookup"><span data-stu-id="094ac-128">When you specify a `location` property, two additional parameters are supported and optional:</span></span>



| <span data-ttu-id="094ac-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="094ac-129">Parameter</span></span> | <span data-ttu-id="094ac-130">Werte</span><span class="sxs-lookup"><span data-stu-id="094ac-130">Values</span></span>                  | <span data-ttu-id="094ac-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="094ac-131">Description</span></span>                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="094ac-132">Aufnahme</span><span class="sxs-lookup"><span data-stu-id="094ac-132">inclusion</span></span> | <span data-ttu-id="094ac-133">einschließen, ausschließen</span><span class="sxs-lookup"><span data-stu-id="094ac-133">include, exclude</span></span>        | <span data-ttu-id="094ac-134">Gibt an, ob die Abfrage Elemente von diesem Pfad einschließen oder ausschließen soll.</span><span class="sxs-lookup"><span data-stu-id="094ac-134">Specifies whether the query should include or exclude items from that path.</span></span> <span data-ttu-id="094ac-135">"Include" ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="094ac-135">"Include" is the default.</span></span> <span data-ttu-id="094ac-136">Windows Vista unterstützt keine Ausschlüsse ohne Inklusions.</span><span class="sxs-lookup"><span data-stu-id="094ac-136">Windows Vista does not support exclusions without inclusions.</span></span> <span data-ttu-id="094ac-137">(Siehe Beispiel)</span><span class="sxs-lookup"><span data-stu-id="094ac-137">(See example)</span></span> |
| <span data-ttu-id="094ac-138">Rekursion</span><span class="sxs-lookup"><span data-stu-id="094ac-138">recursion</span></span> | <span data-ttu-id="094ac-139">rekursiv, nicht rekursiv</span><span class="sxs-lookup"><span data-stu-id="094ac-139">recursive, nonrecursive</span></span> | <span data-ttu-id="094ac-140">Gibt an, ob bei der Suche alle Unterordner beginnend mit dem am Speicherort definierten Wert rekursiert werden sollen:</span><span class="sxs-lookup"><span data-stu-id="094ac-140">Specifies whether the search should recurse all subfolders starting from the value defined in the location:</span></span><value><span data-ttu-id="094ac-141">.</span><span class="sxs-lookup"><span data-stu-id="094ac-141">.</span></span> <span data-ttu-id="094ac-142">Der Standardwert ist rekursiv.</span><span class="sxs-lookup"><span data-stu-id="094ac-142">"Recursive" is the default.</span></span>                             |



 

<span data-ttu-id="094ac-143">Wenn Sie den Bereich für eine Suche mithilfe des Such-MS:-Protokolls festlegen möchten, haben Sie je nach Ziel des Bereichs unterschiedliche Optionen.</span><span class="sxs-lookup"><span data-stu-id="094ac-143">To scope a search using the search-ms: protocol, you have different options depending on the target of the scope.</span></span>

<span data-ttu-id="094ac-144">Ordner auf einem lokalen Computer:</span><span class="sxs-lookup"><span data-stu-id="094ac-144">Folder on a local machine:</span></span>

-   <span data-ttu-id="094ac-145">Verwenden Sie AQS (Crumb = Ordner: <URL-codierter Pfad>).</span><span class="sxs-lookup"><span data-stu-id="094ac-145">Use AQS (crumb=folder:<URL-encoded path>)</span></span>
-   <span data-ttu-id="094ac-146">Use Location-Argument (Crumb = Speicherort: <URL-codierter Pfad>)</span><span class="sxs-lookup"><span data-stu-id="094ac-146">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="094ac-147">Ordner auf einem Remote Computer/Netzwerk:</span><span class="sxs-lookup"><span data-stu-id="094ac-147">Folder on a remote machine/network:</span></span>

-   <span data-ttu-id="094ac-148">Use Location-Argument (Crumb = Speicherort: <URL-codierter Pfad>)</span><span class="sxs-lookup"><span data-stu-id="094ac-148">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="094ac-149">Ordner, auf den über einen bekannten UNC-Protokollhandler zugegriffen wird:</span><span class="sxs-lookup"><span data-stu-id="094ac-149">Folder accessed via a known UNC protocol handler:</span></span>

-   <span data-ttu-id="094ac-150">Verwenden Sie AQS (Crumb = Store: <UNC protocol handler name> ).</span><span class="sxs-lookup"><span data-stu-id="094ac-150">Use AQS (crumb=store:<UNC protocol handler name>)</span></span>
-   <span data-ttu-id="094ac-151">Use Location-Argument (Crumb = Speicherort: <URL-codierter Pfad>)</span><span class="sxs-lookup"><span data-stu-id="094ac-151">Use location argument (crumb=location:<URL-encoded path>)</span></span>

### <a name="vista-examples"></a><span data-ttu-id="094ac-152">Vista-Beispiele</span><span class="sxs-lookup"><span data-stu-id="094ac-152">Vista Examples</span></span>


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



<span data-ttu-id="094ac-153">Im ersten Beispiel wird eine Suche nach "Vacation" begonnen, beginnend an der Shell://Personal (eine besondere Verknüpfung zum Ordner "eigene Dateien" des Benutzers), einschließlich dieses Ordners und aller Unterordner.</span><span class="sxs-lookup"><span data-stu-id="094ac-153">The first example executes a search for "vacation" starting at the shell://Personal location (a special shortcut to the user's My Documents folder), including that folder and all subfolders.</span></span> <span data-ttu-id="094ac-154">Siehe dazu die folgende Tabelle.</span><span class="sxs-lookup"><span data-stu-id="094ac-154">See table below.</span></span>

<span data-ttu-id="094ac-155">Im zweiten Beispiel wird eine Suche in c:- \\ Bildern ausgeführt, aber nicht in c: \\ Bilder \\ Duplikaten.</span><span class="sxs-lookup"><span data-stu-id="094ac-155">The second example executes a search within C:\\Pictures, but not in C:\\Pictures\\Duplicates.</span></span>

<span data-ttu-id="094ac-156">Im dritten Beispiel wird eine Suche innerhalb von C: \\ Documents ausgeführt, die auf Dateien beschränkt ist, deren Kind-Eigenschaft auf Bilder festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="094ac-156">The third example executes a search within C:\\Documents, limited to files with the kind property set to pics.</span></span>

### <a name="constants-for-common-folders"></a><span data-ttu-id="094ac-157">Konstanten für allgemeine Ordner</span><span class="sxs-lookup"><span data-stu-id="094ac-157">Constants for Common Folders</span></span>

<span data-ttu-id="094ac-158">Windows Vista ermöglicht die Verwendung von [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) -Werten, die eine eindeutige, systemunabhängige Möglichkeit zur Identifizierung spezieller Ordner bieten, die häufig von Anwendungen verwendet werden, aber nicht denselben Namen oder Speicherort auf einem beliebigen System haben.</span><span class="sxs-lookup"><span data-stu-id="094ac-158">Windows Vista enables the use of [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) values that provide a unique system-independent way to identify special folders used frequently by applications, but which may not have the same name or location on any given system.</span></span> <span data-ttu-id="094ac-159">Der Systemordner kann z. b. "c: \\ Windows" auf einem System und "c: \\ Winnt" auf einem anderen System sein.</span><span class="sxs-lookup"><span data-stu-id="094ac-159">For example, the system folder may be "C:\\Windows" on one system and "C:\\Winnt" on another.</span></span> <span data-ttu-id="094ac-160">Vor Windows Vista wurden [CSIDLs](/windows/desktop/shell/csidl) verwendet.</span><span class="sxs-lookup"><span data-stu-id="094ac-160">Prior to Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) were used.</span></span>

<span data-ttu-id="094ac-161">Verwenden Sie diese Speicherorte mit der folgenden Syntax:</span><span class="sxs-lookup"><span data-stu-id="094ac-161">Use these locations with this syntax:</span></span>


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a><span data-ttu-id="094ac-162">Verwenden von Breadcrumb) mit Windows XP (Kind und Store)</span><span class="sxs-lookup"><span data-stu-id="094ac-162">Using crumb with Windows XP (kind and store)</span></span>

<span data-ttu-id="094ac-163">Für Windows Search unter Windows XP (WDS 3. x) verfügen die AQS-Begriffe "Kind" und "Store" über eine besondere Implementierung.</span><span class="sxs-lookup"><span data-stu-id="094ac-163">For Windows Search on Windows XP (WDS 3.x), the AQS terms "kind" and "store" have a special implementation.</span></span> <span data-ttu-id="094ac-164">Die "Kind"-Werte entsprechen den [Werten, die in WDS 2. x verwendet](../lwef/-search-2x-wds-perceivedtype.md)werden.</span><span class="sxs-lookup"><span data-stu-id="094ac-164">The "kind" values are the same [values used in WDS 2.x](../lwef/-search-2x-wds-perceivedtype.md).</span></span> <span data-ttu-id="094ac-165">Die "Store"-Werte umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="094ac-165">The "store" values include the following:</span></span>

-   <span data-ttu-id="094ac-166">MAPI</span><span class="sxs-lookup"><span data-stu-id="094ac-166">mapi</span></span>
-   <span data-ttu-id="094ac-167">file</span><span class="sxs-lookup"><span data-stu-id="094ac-167">file</span></span>
-   <span data-ttu-id="094ac-168">OutlookExpress</span><span class="sxs-lookup"><span data-stu-id="094ac-168">outlookexpress</span></span>
-   <span data-ttu-id="094ac-169">any</span><span class="sxs-lookup"><span data-stu-id="094ac-169">any</span></span>

### <a name="xp-examples"></a><span data-ttu-id="094ac-170">XP-Beispiele</span><span class="sxs-lookup"><span data-stu-id="094ac-170">XP Examples</span></span>


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



<span data-ttu-id="094ac-171">Im ersten Beispiel werden Microsoft Outlook Express-e-Mails von John mit der benutzerdefinierten Bezeichnung "OE Mail" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="094ac-171">The first example returns Microsoft Outlook Express emails from John with the custom label, "OE Mail".</span></span> <span data-ttu-id="094ac-172">Im zweiten Beispiel wird eine Suche nach einer beliebigen Kommunikation von John ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="094ac-172">The second example executes a search for any communication from John.</span></span>

## <a name="related-topics"></a><span data-ttu-id="094ac-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="094ac-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="094ac-174">Die ersten Schritte mit Parameter-Value Argumenten</span><span class="sxs-lookup"><span data-stu-id="094ac-174">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="094ac-175">Locale-bezeichnerargumente</span><span class="sxs-lookup"><span data-stu-id="094ac-175">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="094ac-176">Syntax Argument</span><span class="sxs-lookup"><span data-stu-id="094ac-176">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="094ac-177">Stackedby-Argument</span><span class="sxs-lookup"><span data-stu-id="094ac-177">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="094ac-178">Unterabfrage Argument</span><span class="sxs-lookup"><span data-stu-id="094ac-178">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
