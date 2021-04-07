---
title: Aufrufen von WDS über die Befehlszeile
description: Sie können die Benutzeroberfläche der Microsoft Windows-Desktop Suche (WDS) mit einem bestimmten Filter, einem bestimmten Speicher oder einer Webseite starten, die das Browserhilfsobjekt (BHO) mithilfe der windowssearch.exe Befehlszeilen Syntax verwendet.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724019"
---
# <a name="calling-wds-from-the-command-line"></a><span data-ttu-id="7bec0-103">Aufrufen von WDS über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="7bec0-103">Calling WDS from the Command Line</span></span>

> [!NOTE]
> <span data-ttu-id="7bec0-104">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="7bec0-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7bec0-105">Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="7bec0-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="7bec0-106">Sie können die Benutzeroberfläche der Microsoft Windows-Desktop Suche (WDS) mit einem bestimmten Filter, einem bestimmten Speicher oder einer Webseite starten, die das Browserhilfsobjekt (BHO) mithilfe der windowssearch.exe Befehlszeilen Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="7bec0-106">You can launch the Microsoft Windows Desktop Search (WDS) user interface with a specific filter, store, and query from another application or a webpage that uses the Browser Helper Object (BHO) by using the windowssearch.exe command line syntax.</span></span> <span data-ttu-id="7bec0-107">Wenn WDS von der Befehlszeile aufgerufen wird, werden keine Informationen über die Aktionen des Benutzers oder die Auswahl im WDS-Fenster an die aufrufenden Anwendung oder Webseite zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7bec0-107">When calling WDS from the command line, no information about the user's actions or selection in the WDS window is returned to the calling application or webpage.</span></span>

<span data-ttu-id="7bec0-108">Der WDS-Installationspfad wird in der Registrierungs Einstellung INSTALLDIR unter HKEY_LOCAL_MACHINE \\ Software \\ Microsoft \\ Windows-Desktop Suche angegeben.</span><span class="sxs-lookup"><span data-stu-id="7bec0-108">The WDS installation path is specified in the InstallDir registry setting under HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows Desktop Search.</span></span> <span data-ttu-id="7bec0-109">Der Standardpfad, auf windowssearch.exe installiert wird, ist Programme \\ Windows-Desktop Suche.</span><span class="sxs-lookup"><span data-stu-id="7bec0-109">The default path that windowssearch.exe is installed to is Program Files\\Windows Desktop Search.</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="7bec0-110">Befehlszeilensyntax</span><span class="sxs-lookup"><span data-stu-id="7bec0-110">Command Line Syntax</span></span>

<span data-ttu-id="7bec0-111">Die folgende Syntax gilt für die Befehlszeilenschnittstelle der Windows-Desktop Suche 2. x.</span><span class="sxs-lookup"><span data-stu-id="7bec0-111">The following syntax applies to the Windows Desktop Search 2.x command-line interface.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7bec0-112">Optionen</span><span class="sxs-lookup"><span data-stu-id="7bec0-112">Options</span></span></th>
<th><span data-ttu-id="7bec0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bec0-113">Parameter</span></span></th>
<th><span data-ttu-id="7bec0-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7bec0-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7bec0-115">/startup</span><span class="sxs-lookup"><span data-stu-id="7bec0-115">/startup</span></span></td>

<td><span data-ttu-id="7bec0-116">Initialisiert die Windows-Desktop Suche.</span><span class="sxs-lookup"><span data-stu-id="7bec0-116">Initializes Windows Desktop Search</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bec0-117">/indexnow</span><span class="sxs-lookup"><span data-stu-id="7bec0-117">/indexnow</span></span></td>

<td><span data-ttu-id="7bec0-118">Deaktiviert die Indizierung und schaltet alle Index Speicherorte um.</span><span class="sxs-lookup"><span data-stu-id="7bec0-118">Turns off indexing back-off and rescans all index locations</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7bec0-119">/showstatus</span><span class="sxs-lookup"><span data-stu-id="7bec0-119">/showstatus</span></span></td>

<td><span data-ttu-id="7bec0-120">Zeigt das Fenster "Index Status" an</span><span class="sxs-lookup"><span data-stu-id="7bec0-120">Shows the indexing status window</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bec0-121">/launchsearchwindow oder/URL</span><span class="sxs-lookup"><span data-stu-id="7bec0-121">/launchsearchwindow or /url</span></span></td>

<td><span data-ttu-id="7bec0-122">Öffnet ein WDS-Fenster mit einer leeren Abfrage.</span><span class="sxs-lookup"><span data-stu-id="7bec0-122">Opens a WDS window with an empty query</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7bec0-123">/url</span><span class="sxs-lookup"><span data-stu-id="7bec0-123">/url</span></span></td>
<td><span data-ttu-id="7bec0-124">Search: [Store | Show | Abfrage] Abfrage Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7bec0-124">search:[store|show|query] query string</span></span></td>
<td><span data-ttu-id="7bec0-125">Öffnet ein WDS-Fenster mit einer Abfrage und einem Filter basierend auf den folgenden Parametern:</span><span class="sxs-lookup"><span data-stu-id="7bec0-125">Opens a WDS window with a query and filter based on the following parameters:</span></span>
<ul>
<li><p><span data-ttu-id="7bec0-126">Store: gibt die Datenquelle für die Abfrage an: Dateien, Outlook, OutlookExpress.</span><span class="sxs-lookup"><span data-stu-id="7bec0-126">store - Specifies the data source to query: files, outlook, outlookexpress.</span></span> <span data-ttu-id="7bec0-127">Wenn nicht angegeben, werden alle Geschäfte durchsucht.</span><span class="sxs-lookup"><span data-stu-id="7bec0-127">If not specified all stores will be searched.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="7bec0-128">Obwohl die Erweiterte Abfrage Syntax das verweisen auf Microsoft Outlook als ' OE ' unterstützt, muss der Store-Parameter in der Befehlszeile ' OutlookExpress ' lauten.</span><span class="sxs-lookup"><span data-stu-id="7bec0-128">While Advanced Query Syntax supports referencing Microsoft Outlook as 'oe', the store parameter on the command line must be 'outlookexpress'.</span></span>
</blockquote>
<p><br/></p></li>
<li><p><span data-ttu-id="7bec0-129">Show: gibt an, welche wahrgenommenen Ergebnisse zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7bec0-129">show - Specifies which perceived type of results to return.</span></span> <span data-ttu-id="7bec0-130">Eine umfassende Liste der Typen finden Sie unter <a href="-search-2x-wds-perceivedtype.md">wahrgenommene Typen</a> .</span><span class="sxs-lookup"><span data-stu-id="7bec0-130">See <a href="-search-2x-wds-perceivedtype.md">Perceived Types</a> for a complete list of types.</span></span> <span data-ttu-id="7bec0-131">Wenn nicht angegeben, werden alle Typen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7bec0-131">If not specified, all types will be returned.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="7bec0-132">Es gibt drei Unterschiede zwischen den wahrgenommenen Typwerten und den Werten für "anzeigen".</span><span class="sxs-lookup"><span data-stu-id="7bec0-132">There are three differences between the perceived type values and the values for show.</span></span> <span data-ttu-id="7bec0-133">Verwenden Sie für <code>show</code> "Dokumente" anstelle von "doc", "Bilder" anstelle von "Fotos" und "textdocuments" anstelle von "Text".</span><span class="sxs-lookup"><span data-stu-id="7bec0-133">For <code>show</code>, use 'documents' instead of 'doc', 'pictures' instead of 'pics', and 'textdocuments' instead of 'text'.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="7bec0-134">Query: gibt die Suchkriterien an.</span><span class="sxs-lookup"><span data-stu-id="7bec0-134">query - Specifies the search criteria.</span></span> <span data-ttu-id="7bec0-135">Dieser Wert unterstützt <a href="-search-2x-wds-aqsreference.md">Erweiterte Abfrage Syntax</a> Parameter, um die Ergebnisse zu verfeinern.</span><span class="sxs-lookup"><span data-stu-id="7bec0-135">This value supports <a href="-search-2x-wds-aqsreference.md">Advanced Query Syntax</a> parameters to refine the results.</span></span> <span data-ttu-id="7bec0-136">Der Abfrage Parameter muss der letzte Parameter in der URL sein.</span><span class="sxs-lookup"><span data-stu-id="7bec0-136">The query parameter must be the last parameter in the URL.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a><span data-ttu-id="7bec0-137">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7bec0-137">Example</span></span>

<span data-ttu-id="7bec0-138">Verwenden Sie beispielsweise den folgenden Befehl, um alle Dateien nach Bildern zu durchsuchen, die mit den Kriterien für das Hintergrund übereinstimmen:</span><span class="sxs-lookup"><span data-stu-id="7bec0-138">For example, to search all files for pictures matching the criteria 'wallpaper' use the following command:</span></span>

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a><span data-ttu-id="7bec0-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7bec0-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7bec0-140">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="7bec0-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7bec0-141">Erweiterte Abfragesyntax</span><span class="sxs-lookup"><span data-stu-id="7bec0-141">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="7bec0-142">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="7bec0-142">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="7bec0-143">Aufrufen von WDS von Webseiten</span><span class="sxs-lookup"><span data-stu-id="7bec0-143">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





