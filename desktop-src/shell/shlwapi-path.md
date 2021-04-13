---
description: In diesem Abschnitt werden die Windows Shell-Pfad Behandlungs Funktionen beschrieben. Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.
title: Shellpfad-Verarbeitungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8ed0a5e0f2e91a2e647af461ee6679a5542d28b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995071"
---
# <a name="shell-path-handling-functions"></a><span data-ttu-id="ab360-104">Shellpfad-Verarbeitungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ab360-104">Shell Path Handling Functions</span></span>

<span data-ttu-id="ab360-105">In diesem Abschnitt werden die Windows Shell-Pfad Behandlungs Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ab360-105">This section describes the Windows Shell path handling functions.</span></span> <span data-ttu-id="ab360-106">Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.</span><span class="sxs-lookup"><span data-stu-id="ab360-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ab360-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ab360-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab360-108">Thema</span><span class="sxs-lookup"><span data-stu-id="ab360-108">Topic</span></span></th>
<th><span data-ttu-id="ab360-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab360-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab360-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>Pathaddbackschräg Strich</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-111">Fügt einen umgekehrten Schrägstrich am Ende einer Zeichenfolge hinzu, um die korrekte Syntax für einen Pfad zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab360-111">Adds a backslash to the end of a string to create the correct syntax for a path.</span></span> <span data-ttu-id="ab360-112">Wenn der Quellpfad bereits einen nachfolgenden umgekehrten Schrägstrich enthält, wird kein umgekehrter Schrägstrich hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ab360-112">If the source path already has a trailing backslash, no backslash will be added.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab360-113">Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen.</span><span class="sxs-lookup"><span data-stu-id="ab360-113">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="ab360-114">Es wird empfohlen, die Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>pathcchaddbackschräg Strich</strong></a> " oder " <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>pathcchaddbackslashex</strong></a> " zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab360-114">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>Pathaddextension</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-116">Fügt einer Pfad Zeichenfolge eine Dateinamenerweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="ab360-116">Adds a file name extension to a path string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab360-117">Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen.</span><span class="sxs-lookup"><span data-stu-id="ab360-117">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="ab360-118">Es wird empfohlen, die Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>pathcchaddextension</strong></a> " zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab360-118">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-120">Fügt einen Pfad am Ende eines anderen ein.</span><span class="sxs-lookup"><span data-stu-id="ab360-120">Appends one path to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab360-121">Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen.</span><span class="sxs-lookup"><span data-stu-id="ab360-121">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="ab360-122">Wir empfehlen die Verwendung der Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>pathcchappend</strong></a> " oder " <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>pathcchappdex</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="ab360-122">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>Pathbuildroot</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-124">Erstellt einen Stammpfad aus einer angegebenen Laufwerksnummer.</span><span class="sxs-lookup"><span data-stu-id="ab360-124">Creates a root path from a given drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>Pathcanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-126">Vereinfacht einen Pfad, indem Navigationselemente wie &quot; . &quot; und. entfernt werden &quot; &quot; , um einen direkten, wohlgeformten Pfad zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab360-126">Simplifies a path by removing navigation elements such as &quot;.&quot; and &quot;..&quot; to produce a direct, well-formed path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>Pathcombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-128">Verkettet zwei Zeichen folgen, die ordnungsgemäß geformte Pfade zu einem Pfad darstellen. verkettet außerdem alle relativen Pfad Elemente.</span><span class="sxs-lookup"><span data-stu-id="ab360-128">Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab360-129">Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen.</span><span class="sxs-lookup"><span data-stu-id="ab360-129">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="ab360-130">Es wird empfohlen, die Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>pathcchcombine</strong></a> " oder " <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>pathcchcombineex</strong></a> " zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab360-130">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>Pathcommonprefix</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-132">Vergleicht zwei Pfade, um zu bestimmen, ob Sie ein gemeinsames Präfix haben.</span><span class="sxs-lookup"><span data-stu-id="ab360-132">Compares two paths to determine if they share a common prefix.</span></span> <span data-ttu-id="ab360-133">Ein Präfix ist einer der folgenden Typen: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .</span><span class="sxs-lookup"><span data-stu-id="ab360-133">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>Pathcompactpath</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-135">Verkürzt einen Dateipfad, der in eine bestimmte Pixel Breite passt, indem Pfad Komponenten durch Ellipsen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ab360-135">Truncates a file path to fit within a given pixel width by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>Pathcompactpathex</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-137">Verkürzt einen Pfad, der in eine bestimmte Anzahl von Zeichen passt, indem Pfad Komponenten durch Ellipsen ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ab360-137">Truncates a path to fit within a certain number of characters by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>Pathkreatefromurl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-139">Konvertiert eine Datei-URL in einen Microsoft MS-DOS-Pfad.</span><span class="sxs-lookup"><span data-stu-id="ab360-139">Converts a file URL to a Microsoft MS-DOS path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>Pathkreatefromurlzuweisung</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-141">Erstellt einen Pfad aus einer Datei-URL.</span><span class="sxs-lookup"><span data-stu-id="ab360-141">Creates a path from a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>Pathfilevorhanden</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-143">Bestimmt, ob ein Pfad zu einem Dateisystem Objekt (z. b. eine Datei oder ein Ordner) gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-143">Determines whether a path to a file system object such as a file or folder is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>Pathfindextension</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-145">Durchsucht einen Pfad nach einer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="ab360-145">Searches a path for an extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>Pathfindfilename</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-147">Durchsucht einen Pfad nach einem Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="ab360-147">Searches a path for a file name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>Pathfindnextcomponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-149">Analysiert einen Pfad und gibt den Teil dieses Pfads zurück, der dem ersten umgekehrten Schrägstrich folgt.</span><span class="sxs-lookup"><span data-stu-id="ab360-149">Parses a path and returns the portion of that path that follows the first backslash.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>Pathfindonpath</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-151">Sucht nach einer Datei.</span><span class="sxs-lookup"><span data-stu-id="ab360-151">Searches for a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>Pathfindsuffixarray</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-153">Bestimmt, ob ein bestimmter Dateiname eine Liste von Suffixen hat.</span><span class="sxs-lookup"><span data-stu-id="ab360-153">Determines whether a given file name has one of a list of suffixes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>Pathgetargs</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-155">Sucht die Befehlszeilenargumente innerhalb eines angegebenen Pfads.</span><span class="sxs-lookup"><span data-stu-id="ab360-155">Finds the command line arguments within a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>Pathgetchartype</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-157">Bestimmt den Typ des Zeichens im Verhältnis zu einem Pfad.</span><span class="sxs-lookup"><span data-stu-id="ab360-157">Determines the type of character in relation to a path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>Pathgetdrivenumschlag</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-159">Durchsucht einen Pfad nach einem Laufwerksbuchstaben innerhalb des Bereichs von "a" bis "Z" und gibt die entsprechende Laufwerksnummer zurück.</span><span class="sxs-lookup"><span data-stu-id="ab360-159">Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>Pathiscontenttype</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-161">Bestimmt, ob der registrierte Inhaltstyp einer Datei mit dem angegebenen Inhaltstyp übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ab360-161">Determines if a file's registered content type matches the specified content type.</span></span> <span data-ttu-id="ab360-162">Diese Funktion Ruft den Inhaltstyp für den angegebenen Dateityp ab und vergleicht diese Zeichenfolge mit dem <em>pszcontenttype</em>.</span><span class="sxs-lookup"><span data-stu-id="ab360-162">This function obtains the content type for the specified file type and compares that string with the <em>pszContentType</em>.</span></span> <span data-ttu-id="ab360-163">Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ab360-163">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>Pathisdirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-165">Überprüft, ob ein Pfad ein gültiges Verzeichnis ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-165">Verifies that a path is a valid directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>Pathisdirectoriyempty</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-167">Bestimmt, ob ein angegebener Pfad ein leeres Verzeichnis ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-167">Determines whether a specified path is an empty directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>Pathisfilespec</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-169">Durchsucht einen Pfad nach beliebigen Pfad Begrenzungs Zeichen (z. b. ': ' oder ' \' ) '.</span><span class="sxs-lookup"><span data-stu-id="ab360-169">Searches a path for any path-delimiting characters (for example, ':' or '\' ).</span></span> <span data-ttu-id="ab360-170">Wenn keine Pfad Trennzeichen vorhanden sind, wird der Pfad als dateispezifikations Pfad betrachtet.</span><span class="sxs-lookup"><span data-stu-id="ab360-170">If there are no path-delimiting characters present, the path is considered to be a File Spec path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>"Pthishtmlfile"</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-172">Bestimmt, ob eine Datei eine HTML-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-172">Determines if a file is an HTML file.</span></span> <span data-ttu-id="ab360-173">Die Bestimmung erfolgt basierend auf dem Inhaltstyp, der für die Dateierweiterung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-173">The determination is made based on the content type that is registered for the file's extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>Pathislfnfilespec</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-175">Bestimmt, ob ein Dateiname im langen Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ab360-175">Determines whether a file name is in long format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>Pathisnetworkpath</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-177">Bestimmt, ob eine Pfad Zeichenfolge eine Netzwerkressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab360-177">Determines whether a path string represents a network resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>"Pthistreufix"</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-179">Durchsucht einen Pfad, um zu bestimmen, ob er ein gültiges Präfix des von <em>pszprefix</em>weiter gegebenen Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="ab360-179">Searches a path to determine if it contains a valid prefix of the type passed by <em>pszPrefix</em>.</span></span> <span data-ttu-id="ab360-180">Ein Präfix ist einer der folgenden Typen: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .</span><span class="sxs-lookup"><span data-stu-id="ab360-180">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>Pathisrelative</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-182">Durchsucht einen Pfad und bestimmt, ob er relativ ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-182">Searches a path and determines if it is relative.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>Pathisroot</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-184">Bestimmt, ob eine Pfad Zeichenfolge auf den Stamm eines Volumes verweist.</span><span class="sxs-lookup"><span data-stu-id="ab360-184">Determines whether a path string refers to the root of a volume.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>"Pthissameroot"</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-186">Vergleicht zwei Pfade, um zu bestimmen, ob Sie eine gemeinsame Stamm Komponente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ab360-186">Compares two paths to determine if they have a common root component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>Ordner "Ordner"</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-188">Bestimmt, ob ein vorhandener Ordner die Attribute enthält, die ihn zu einem Systemordner machen.</span><span class="sxs-lookup"><span data-stu-id="ab360-188">Determines if an existing folder contains the attributes that make it a system folder.</span></span> <span data-ttu-id="ab360-189">Alternativ gibt diese Funktion an, ob bestimmte Attribute einen Ordner als Systemordner qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="ab360-189">Alternately, this function indicates if certain attributes qualify a folder to be a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-191">Bestimmt, ob eine Pfad Zeichenfolge ein gültiger Universal Naming Convention (UNC)-Pfad ist, im Gegensatz zu einem Pfad, der auf einem Laufwerk Buchstaben basiert.</span><span class="sxs-lookup"><span data-stu-id="ab360-191">Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>Pathisuncserver</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-193">Bestimmt, ob eine Zeichenfolge eine gültige UNC-Datei für einen Serverpfad ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-193">Determines if a string is a valid UNC for a server path only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>Pathisuncservershare</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-195">Bestimmt, ob eine Zeichenfolge ein gültiger UNC-Freigabe Pfad ( \\ <em>Server</em> \ <em>Freigabe</em>) ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-195">Determines if a string is a valid UNC share path, \\<em>server</em>\<em>share</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>Pathisurl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-197">Testet eine angegebene Zeichenfolge, um zu bestimmen, ob Sie einem gültigen URL-Format entspricht.</span><span class="sxs-lookup"><span data-stu-id="ab360-197">Tests a given string to determine if it conforms to a valid URL format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>Pathmakepretty</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-199">Konvertiert einen Großbuchstaben Pfad in alle Kleinbuchstaben, um dem Pfad eine konsistente Darstellung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="ab360-199">Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>Pathmakesystemordner</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-201">Gibt einem vorhandenen Ordner die richtigen Attribute, die zu einem Systemordner werden.</span><span class="sxs-lookup"><span data-stu-id="ab360-201">Gives an existing folder the proper attributes to become a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-203">Durchsucht eine Zeichenfolge mit einem Platzhalter-Übereinstimmungs Typ.</span><span class="sxs-lookup"><span data-stu-id="ab360-203">Searches a string using a MS-DOS wildcard match type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>Pathmatchspecex</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-205">Entspricht einem Dateinamen aus einem Pfad mit einem oder mehreren Dateinamen Mustern.</span><span class="sxs-lookup"><span data-stu-id="ab360-205">Matches a file name from a path against one or more file name patterns.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>Pathparametenconlocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-207">Analysiert eine Datei Speicherort Zeichenfolge, die einen Datei Speicherort und einen Symbol Index enthält, und gibt separate Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ab360-207">Parses a file location string that contains a file location and icon index, and returns separate values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>Pathquotespaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-209">Durchsucht einen Pfad nach Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="ab360-209">Searches a path for spaces.</span></span> <span data-ttu-id="ab360-210">Wenn Leerzeichen gefunden werden, wird der gesamte Pfad in Anführungszeichen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ab360-210">If spaces are found, the entire path is enclosed in quotation marks.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>Pathrelativepathto</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-212">Erstellt einen relativen Pfad von einer Datei oder einem Ordner zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="ab360-212">Creates a relative path from one file or folder to another.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>"Pthremuveargs"</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-214">Entfernt alle Argumente aus einem angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="ab360-214">Removes any arguments from a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>Umgekehrter Schrägstrich</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-216">Entfernt den nachfolgenden umgekehrten Schrägstrich aus einem angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="ab360-216">Removes the trailing backslash from a given path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab360-217">Diese Funktion ist als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="ab360-217">This function is deprecated.</span></span> <span data-ttu-id="ab360-218">Es wird empfohlen, die Funktion <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>pathcchremovebackschräg Strich</strong></a> oder <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>pathcchremovebackslashex</strong></a> zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab360-218">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>"Pthremuveblank"</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-220">Entfernt alle führenden und nachfolgenden Leerzeichen aus einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ab360-220">Removes all leading and trailing spaces from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>"Pthremuveextension"</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-222">Entfernt die Dateinamenerweiterung aus einem Pfad, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ab360-222">Removes the file name extension from a path, if one is present.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab360-223">Diese Funktion ist als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="ab360-223">This function is deprecated.</span></span> <span data-ttu-id="ab360-224">Wir empfehlen die Verwendung von <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>pathcchremoveextension</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ab360-224">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>"Pthremuvefilespec"</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-226">Entfernt den nachfolgenden Dateinamen und den umgekehrten Schrägstrich aus einem Pfad, sofern diese vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ab360-226">Removes the trailing file name and backslash from a path, if they are present.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab360-227">Diese Funktion ist als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="ab360-227">This function is deprecated.</span></span> <span data-ttu-id="ab360-228">Wir empfehlen die Verwendung der <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>pathcchremovefilespec</strong></a> -Funktion an dieser Stelle.</span><span class="sxs-lookup"><span data-stu-id="ab360-228">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>Pathrenameextension</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-230">Ersetzt die Erweiterung eines Datei namens durch eine neue Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="ab360-230">Replaces the extension of a file name with a new extension.</span></span> <span data-ttu-id="ab360-231">Wenn der Dateiname keine Erweiterung enthält, wird die Erweiterung an das Ende der Zeichenfolge angefügt.</span><span class="sxs-lookup"><span data-stu-id="ab360-231">If the file name does not contain an extension, the extension will be attached to the end of the string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab360-232">Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen.</span><span class="sxs-lookup"><span data-stu-id="ab360-232">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="ab360-233">Es wird empfohlen, die Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>pathcchrenrenameextension</strong></a> " zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab360-233">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>Pathsearchandqualify</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-235">Bestimmt, ob ein angegebener Pfad ordnungsgemäß formatiert und voll qualifiziert ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-235">Determines if a given path is correctly formatted and fully qualified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>Pathsetdlgitempath</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-237">Legt den Text eines untergeordneten Steuer Elements in einem Fenster oder Dialogfeld fest. dabei wird <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>pathcompactpath</strong></a> verwendet, um sicherzustellen, dass der Pfad in das Steuerelement passt.</span><span class="sxs-lookup"><span data-stu-id="ab360-237">Sets the text of a child control in a window or dialog box, using <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> to ensure the path fits in the control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>Pathskiproot</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-239">Ruft einen Zeiger auf das erste Zeichen in einem Pfad ab, der auf die Elemente Laufwerk Buchstabe oder UNC-Server/Freigabe Pfad folgt.</span><span class="sxs-lookup"><span data-stu-id="ab360-239">Retrieves a pointer to the first character in a path following the drive letter or UNC server/share path elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>Pathstrippath</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-241">Entfernt den Pfadteil eines voll qualifizierten Pfads und einer Datei.</span><span class="sxs-lookup"><span data-stu-id="ab360-241">Removes the path portion of a fully qualified path and file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>Pathstriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-243">Entfernt alle Datei-und Verzeichnis Elemente in einem Pfad außer den Stamm Informationen.</span><span class="sxs-lookup"><span data-stu-id="ab360-243">Removes all file and directory elements in a path except for the root information.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ab360-244">Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen.</span><span class="sxs-lookup"><span data-stu-id="ab360-244">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="ab360-245">Es wird empfohlen, die Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>pathcchstriptoroot</strong></a> " zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab360-245">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>Pathundekorieren</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-247">Entfernt die Dekoration aus einer Pfad Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ab360-247">Removes the decoration from a path string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>Pathunexpandenvstrings</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-249">Ersetzt bestimmte Ordnernamen in einem voll qualifizierten Pfad durch die zugehörige Umgebungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ab360-249">Replaces certain folder names in a fully qualified path with their associated environment string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>Ordner "pathunmakesystem"</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-251">Entfernt die Attribute aus einem Ordner, in dem Sie einen Systemordner bilden.</span><span class="sxs-lookup"><span data-stu-id="ab360-251">Removes the attributes from a folder that make it a system folder.</span></span> <span data-ttu-id="ab360-252">Dieser Ordner muss tatsächlich im Dateisystem vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ab360-252">This folder must actually exist in the file system.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>Pathunquotespaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-254">Entfernt Anführungszeichen am Anfang und Ende eines Pfads.</span><span class="sxs-lookup"><span data-stu-id="ab360-254">Removes quotes from the beginning and end of a path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>Shskipconnection</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-256">Überprüft einen Bindungs Kontext, um festzustellen, ob es sicher ist, eine Bindung an ein bestimmtes Komponenten Objekt herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ab360-256">Checks a bind context to see if it is safe to bind to a particular component object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>Urlapplyscheme</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-258">Bestimmt ein Schema für eine angegebene URL-Zeichenfolge und gibt eine Zeichenfolge mit einem entsprechenden Präfix zurück.</span><span class="sxs-lookup"><span data-stu-id="ab360-258">Determines a scheme for a specified URL string, and returns a string with an appropriate prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-260">Konvertiert eine URL-Zeichenfolge in ein kanonisches Format.</span><span class="sxs-lookup"><span data-stu-id="ab360-260">Converts a URL string into canonical form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>Urlcombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-262">Wenn eine relative URL und deren Basis bereitgestellt wird, wird eine URL in kanonischer Form zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab360-262">When provided with a relative URL and its base, returns a URL in canonical form.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>Urlcompare</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-264">Berücksichtigt den Vergleich von zwei URL-Zeichen folgen in Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="ab360-264">Makes a case-sensitive comparison of two URL strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>Urlkreatefrompath</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-266">Konvertiert einen MS-DOS-Pfad in eine kanonisierte URL.</span><span class="sxs-lookup"><span data-stu-id="ab360-266">Converts a MS-DOS path to a canonicalized URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>Urlescape</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-268">Konvertiert Zeichen oder Ersatz Zeichenpaare in eine URL, die möglicherweise während des Transports über das Internet ( &quot; Unsichere Zeichen) in die entsprechenden Escapesequenzen geändert wird &quot; .</span><span class="sxs-lookup"><span data-stu-id="ab360-268">Converts characters or surrogate pairs in a URL that might be altered during transport across the Internet (&quot;unsafe&quot; characters) into their corresponding escape sequences.</span></span> <span data-ttu-id="ab360-269">Ersatz Zeichenpaare sind Zeichen zwischen u + 10000 und U + 10FFFF (in UTF-32) oder zwischen DC00 und und DFFF (in UTF-16).</span><span class="sxs-lookup"><span data-stu-id="ab360-269">Surrogate pairs are characters between U+10000 to U+10FFFF (in UTF-32) or between DC00 to DFFF (in UTF-16).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>Urlescapespaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-271">Ein Makro, das Leerzeichen in die entsprechende Escapesequenz konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ab360-271">A macro that converts space characters into their corresponding escape sequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>Urlgetlocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-273">Ruft den Speicherort von einer URL ab.</span><span class="sxs-lookup"><span data-stu-id="ab360-273">Retrieves the location from a URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>Urlgetpart</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-275">Akzeptiert eine URL-Zeichenfolge und gibt einen angegebenen Teil dieser URL zurück.</span><span class="sxs-lookup"><span data-stu-id="ab360-275">Accepts a URL string and returns a specified part of that URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>Urlhash</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-277">Hashes einer URL-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ab360-277">Hashes a URL string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-279">Testet, ob eine URL ein angegebener Typ ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-279">Tests whether a URL is a specified type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>Urlisfileurl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-281">Testet eine URL, um zu bestimmen, ob es sich um eine Datei-URL handelt.</span><span class="sxs-lookup"><span data-stu-id="ab360-281">Tests a URL to determine if it is a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>Urlisnohistory</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-283">Gibt zurück, ob eine URL eine URL ist, die Browser in der Regel nicht in den Navigationsverlauf einschließen.</span><span class="sxs-lookup"><span data-stu-id="ab360-283">Returns whether a URL is a URL that browsers typically do not include in navigation history.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>Urlisopaque</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-285">Gibt zurück, ob eine URL nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="ab360-285">Returns whether a URL is opaque.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab360-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>Urlunescape</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-287">Konvertiert Escapesequenzen zurück in normale Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ab360-287">Converts escape sequences back into ordinary characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab360-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>Urlunescapanplace</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab360-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span></span><br/></td>
<td><span data-ttu-id="ab360-289">Konvertiert Escapesequenzen zurück in normale Zeichen und überschreibt die Original Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ab360-289">Converts escape sequences back into ordinary characters and overwrites the original string.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




