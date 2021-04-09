---
description: Die DbgHelp-Bibliothek verwendet den Symbol Suchpfad, um Debugsymbole (PDB-und dbg-Dateien) zu suchen. Der Suchpfad kann aus einem oder mehreren Pfad Elementen bestehen, die durch Semikolons getrennt sind.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Symbolpfade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 977772e45c345e1e990dc038fccd852d17d279dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958294"
---
# <a name="symbol-paths"></a><span data-ttu-id="99d76-104">Symbolpfade</span><span class="sxs-lookup"><span data-stu-id="99d76-104">Symbol Paths</span></span>

<span data-ttu-id="99d76-105">Die DbgHelp-Bibliothek verwendet den Symbol Suchpfad, um Debugsymbole (PDB-und dbg-Dateien) zu suchen.</span><span class="sxs-lookup"><span data-stu-id="99d76-105">The DbgHelp library uses the symbol search path to locate debug symbols (.pdb and .dbg files).</span></span> <span data-ttu-id="99d76-106">Der Suchpfad kann aus einem oder mehreren Pfad Elementen bestehen, die durch Semikolons getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="99d76-106">The search path can be made up of one or more path elements separated by semicolons.</span></span>

## <a name="specifying-search-paths"></a><span data-ttu-id="99d76-107">Angeben von Suchpfaden</span><span class="sxs-lookup"><span data-stu-id="99d76-107">Specifying Search Paths</span></span>

<span data-ttu-id="99d76-108">Um anzugeben, wo der Symbol Handler Datenträger Verzeichnisse nach Symbol Dateien durchsucht, müssen Sie die [**symsetsearchpath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="99d76-108">To specify where the symbol handler will search disk directories for symbol files, call the [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) function.</span></span> <span data-ttu-id="99d76-109">Alternativ können Sie einen Symbol Suchpfad im *usersearchpath* -Parameter der [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="99d76-109">Alternatively, you can specify a symbol search path in the *UserSearchPath* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

<span data-ttu-id="99d76-110">Der *usersearchpath* -Parameter in " [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) " und der " *SearchPath* "-Parameter in " [**symsetsearchpath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) " verwenden einen Zeiger auf eine auf NULL endenden Zeichenfolge, die einen Pfad oder eine Reihe von Pfaden durch ein Semikolon getrennt angibt.</span><span class="sxs-lookup"><span data-stu-id="99d76-110">The *UserSearchPath* parameter in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) and the *SearchPath* parameter in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) take a pointer to a null-terminated string that specifies a path, or series of paths separated by a semicolon.</span></span> <span data-ttu-id="99d76-111">Der Symbol Handler verwendet diese Pfade, um nach Symbol Dateien zu suchen.</span><span class="sxs-lookup"><span data-stu-id="99d76-111">The symbol handler uses these paths to search for symbol files.</span></span> <span data-ttu-id="99d76-112">Wenn dieser Parameter **null** ist, durchsucht der Symbol Handler das Verzeichnis, das das Modul enthält, für das Symbole durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="99d76-112">If this parameter is **NULL**, the symbol handler searches the directory that contains the module for which symbols are being searched.</span></span> <span data-ttu-id="99d76-113">Andernfalls, wenn dieser Parameter als nicht-**null** -Wert angegeben wird, durchsucht der Symbol Handler zuerst die Pfade, die von der Anwendung festgelegt wurden, bevor das Modul Verzeichnis durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="99d76-113">Otherwise, if this parameter is specified as a non-**NULL** value, the symbol handler first searches the paths set by the application before searching the module directory.</span></span> <span data-ttu-id="99d76-114">Wenn Sie die \_ \_ Umgebungsvariable NT-Symbol \_ Pfad oder \_ NT-alt- \_ \_ Symbol Pfad festlegen \_ , sucht der Symbol Handler in der folgenden Reihenfolge nach Symbol Dateien:</span><span class="sxs-lookup"><span data-stu-id="99d76-114">If you set the \_NT\_SYMBOL\_PATH or \_NT\_ALT\_SYMBOL\_PATH environment variable, the symbol handler searches for symbol files in the following order:</span></span>

1. <span data-ttu-id="99d76-115">Die \_ Umgebungsvariable für den NT- \_ Symbol \_ Pfad.</span><span class="sxs-lookup"><span data-stu-id="99d76-115">The \_NT\_SYMBOL\_PATH environment variable.</span></span>
2. <span data-ttu-id="99d76-116">Die \_ NT- \_ alt- \_ Symbol Pfad- \_ Umgebungsvariable.</span><span class="sxs-lookup"><span data-stu-id="99d76-116">The \_NT\_ALT\_SYMBOL\_PATH environment variable.</span></span>
3. <span data-ttu-id="99d76-117">Das Verzeichnis, das das entsprechende Modul enthält.</span><span class="sxs-lookup"><span data-stu-id="99d76-117">The directory that contains the corresponding module.</span></span>

<span data-ttu-id="99d76-118">Rufen Sie zum Abrufen der Suchpfade die [**symgetsearchpath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="99d76-118">To retrieve the search paths, call the [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) function.</span></span>

<span data-ttu-id="99d76-119">Der Suchpfad für Programm Datenbankdateien (. pdb) unterscheidet sich von dem Pfad für Debugdateien (. dbg).</span><span class="sxs-lookup"><span data-stu-id="99d76-119">The search path for program database (.pdb) files is different than the path for debug (.dbg) files.</span></span> <span data-ttu-id="99d76-120">Der Algorithmus wird durch die Funktionalität der Symbol Bibliothek bestimmt.</span><span class="sxs-lookup"><span data-stu-id="99d76-120">The algorithm is determined by the functionality of the symbol library.</span></span> <span data-ttu-id="99d76-121">Standardmäßig erstellt Microsoft Visual C/C++ Microsoft-Format Symbole, entfernt Sie aus dem Image und platziert Sie in einer separaten PDB-Datei.</span><span class="sxs-lookup"><span data-stu-id="99d76-121">By default, Microsoft Visual C/C++ creates Microsoft format symbols, strips them from the image, and places them in a separate .pdb file.</span></span> <span data-ttu-id="99d76-122">In der Regel befindet sich die PDB-Datei in dem Verzeichnis, das das ausführbare Image enthält.</span><span class="sxs-lookup"><span data-stu-id="99d76-122">Typically, the .pdb file will be located in the directory that contains the executable image.</span></span> <span data-ttu-id="99d76-123">Visual C/C++ bettet den absoluten Pfad zur PDB-Datei im ausführbaren Image ein.</span><span class="sxs-lookup"><span data-stu-id="99d76-123">Visual C/C++ embeds the absolute path to the .pdb file in the executable image.</span></span> <span data-ttu-id="99d76-124">Wenn der Symbol Handler die PDB-Datei an diesem Speicherort nicht finden kann oder wenn die PDB-Datei in ein anderes Verzeichnis verschoben wurde, sucht der Symbol Handler die PDB-Datei mithilfe des Suchpfads, der für dbg-Dateien beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="99d76-124">If the symbol handler cannot find the .pdb file in that location or if the .pdb file was moved to another directory, the symbol handler will locate the .pdb file using the search path described for .dbg files.</span></span>

## <a name="path-element-types"></a><span data-ttu-id="99d76-125">Pfad Element Typen</span><span class="sxs-lookup"><span data-stu-id="99d76-125">Path Element Types</span></span>

<span data-ttu-id="99d76-126">Es gibt drei Typen von Pfad Elementen.</span><span class="sxs-lookup"><span data-stu-id="99d76-126">There are three types of path elements.</span></span>

### <a name="standard-path-element"></a><span data-ttu-id="99d76-127">Standard Pfad Element</span><span class="sxs-lookup"><span data-stu-id="99d76-127">Standard Path Element</span></span>

<span data-ttu-id="99d76-128">Ein Standardpfad Element wird durchsucht, indem im Stammverzeichnis des Verzeichnisses gesucht wird, das vom Path-Element angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="99d76-128">A standard path element is searched by looking in the root of the directory specified by the path element.</span></span> <span data-ttu-id="99d76-129">Der Symbol Handler sucht auch in einem Unterverzeichnis von "Symbols", das mit der Dateierweiterung des Moduls übereinstimmt, nach dem die Symbole gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="99d76-129">The symbol handler also looks in a subdirectory of "symbols" that matches the file extension of the module that symbols are being looked for.</span></span> <span data-ttu-id="99d76-130">Dabei handelt es sich in der Regel um "dll", "exe" oder "sys".</span><span class="sxs-lookup"><span data-stu-id="99d76-130">This is typically "dll", "exe", or "sys".</span></span> <span data-ttu-id="99d76-131">Schließlich wird in einem Unterverzeichnis mit dem Namen "Symbols" ein Verzeichnis mit dem gleichen Namen wie die Erweiterung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="99d76-131">Lastly, it looks in a subdirectory called "symbols" with a directory of the same name as the extension.</span></span> <span data-ttu-id="99d76-132">Wenn das Symbol Pfad Element z. b. "c: \\ mysymbols" lautet und die Datei, nach der Symbole gesucht werden, "boo.dll" ist, werden die folgenden Verzeichnisse durchsucht.</span><span class="sxs-lookup"><span data-stu-id="99d76-132">For example, if the symbol path element is "c:\\mySymbols" and the file that symbols are being searched for is "boo.dll", then the following directories would be searched.</span></span>

- <span data-ttu-id="99d76-133">c: \\ mysymbols</span><span class="sxs-lookup"><span data-stu-id="99d76-133">c:\\mySymbols</span></span>  
- <span data-ttu-id="99d76-134">c: \\ mysymbols- \\ dll</span><span class="sxs-lookup"><span data-stu-id="99d76-134">c:\\mySymbols\\dll</span></span>  
- <span data-ttu-id="99d76-135">c: \\ mysymbols- \\ Symbol- \\ dll</span><span class="sxs-lookup"><span data-stu-id="99d76-135">c:\\mySymbols\\symbols\\dll</span></span>  

<span data-ttu-id="99d76-136">Der Symbol Handler verwendet diese Logik, um alle Path-Elemente zu durchsuchen, die die Kriterien nicht als *Symbol Server* oder *Cache* (unten beschrieben) erfüllen.</span><span class="sxs-lookup"><span data-stu-id="99d76-136">The symbol handler uses this logic to search any path element that does not meet the criteria to be a *symbol server* or *cache* (described below).</span></span>

### <a name="symbol-server-path-element"></a><span data-ttu-id="99d76-137">Symbol Server Pfad-Element</span><span class="sxs-lookup"><span data-stu-id="99d76-137">Symbol Server Path Element</span></span>

<span data-ttu-id="99d76-138">Ein *Symbol Server* -Pfad Element verwendet spezielle Technologie, die ein Symbol finden kann, das eine exakte Entsprechung für das betreffende Modul ist.</span><span class="sxs-lookup"><span data-stu-id="99d76-138">A *symbol server* path element uses special technology that can locate a symbol that is an exact match for the module in question.</span></span> <span data-ttu-id="99d76-139">Weitere Informationen finden [Sie unter Verwenden von SymSrv](using-symsrv.md) .</span><span class="sxs-lookup"><span data-stu-id="99d76-139">See [Using SymSrv](using-symsrv.md) for more details.</span></span>

<span data-ttu-id="99d76-140">Der Symbol Handler behandelt ein Path-Element als Symbol Server, wenn er mit dem Text "SRV \* " beginnt.</span><span class="sxs-lookup"><span data-stu-id="99d76-140">The symbol handler treats a path element as a symbol server if it begins with the text, "srv\*".</span></span>

> [!Note]  
> <span data-ttu-id="99d76-141">Wenn der "SRV \* "-Text nicht angegeben ist, aber das eigentliche Path-Element ein Symbol Server Speicher ist, verhält sich der Symbol Handler so, als ob "SRV \* " angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="99d76-141">If the "srv\*" text is not specified but the actual path element is a symbol server store, then the symbol handler will act as if "srv\*" were specified.</span></span> <span data-ttu-id="99d76-142">Der Symbol Handler trifft diese Bestimmung durchsuchen nach dem vorhanden sein einer Datei namens "pingme.txt" im Stammverzeichnis des angegebenen Pfads.</span><span class="sxs-lookup"><span data-stu-id="99d76-142">The symbol handler makes this determination by searching for the existence of a file called "pingme.txt" in the root directory of the specified path.</span></span>

 

### <a name="cache-path-element"></a><span data-ttu-id="99d76-143">Cache Pfad Element</span><span class="sxs-lookup"><span data-stu-id="99d76-143">Cache Path Element</span></span>

<span data-ttu-id="99d76-144">Ein *Cache* Pfad Element ist eine Variation eines Symbol Server-Pfad Elements.</span><span class="sxs-lookup"><span data-stu-id="99d76-144">A *cache* path element is a variation on a symbol server path element.</span></span>

<span data-ttu-id="99d76-145">Dieses Verzeichnis wird wie ein beliebiger anderer Symbol Server durchsucht.</span><span class="sxs-lookup"><span data-stu-id="99d76-145">This directory is searched like any other symbol server.</span></span> <span data-ttu-id="99d76-146">Wenn das Symbol hier jedoch nicht gefunden wird und es in einem Path-Element weiter unten in der Kette des Symbol Pfads gefunden wird, wird das Symbol kopiert und auf dem Symbol Server gespeichert, der in diesem Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="99d76-146">However, if the symbol is not found here and it is found in a path element farther down the chain of the symbol path, then the symbol will be copied and stored in the symbol server specified in this element.</span></span>

<span data-ttu-id="99d76-147">Der Symbol Handler behandelt ein Path-Element als Cache Element, wenn es mit dem Text "Cache \* " beginnt.</span><span class="sxs-lookup"><span data-stu-id="99d76-147">The symbol handler treats a path element as a cache element if it begins with the text, "cache\*".</span></span> <span data-ttu-id="99d76-148">Um einen Cache in "c: \\ myCache" anzugeben, verwenden Sie ein Symbol Pfad Element von "Cache \* c: \\ myCache".</span><span class="sxs-lookup"><span data-stu-id="99d76-148">To specify a cache in "c:\\myCache", use a symbol path element of "cache\*c:\\myCache".</span></span>

## <a name="example-search-path"></a><span data-ttu-id="99d76-149">Beispiel Suchpfad</span><span class="sxs-lookup"><span data-stu-id="99d76-149">Example Search Path</span></span>

<span data-ttu-id="99d76-150">Um zu sehen, wie dies funktioniert, legen Sie diesen Suchpfad fest.</span><span class="sxs-lookup"><span data-stu-id="99d76-150">To see how this works, set this search path.</span></span>

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

<span data-ttu-id="99d76-151">Im folgenden finden Sie eine Auflistung der ausführlichen Ausgabe des Symbol Handlers bei der Suche nach "Ntdll. pdb" mit dem oben aufgeführten Suchpfad.</span><span class="sxs-lookup"><span data-stu-id="99d76-151">The following is a listing of the symbol handler's verbose output while searching for ntdll.pdb, using the above listed search path.</span></span>

```
DBGHELP: .\ntdll.pdb - file not found
DBGHELP: .\dll\ntdll.pdb - file not found
DBGHELP: .\symbols\dll\ntdll.pdb - file not found
SYMSRV: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb not found
SYMSRV: ntdll.pdb from \\symbols\symbols: 10497024 bytes - copied
DBGHELP: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb already cached
DBGHELP: ntdll - private symbols & lines
c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb
```

<span data-ttu-id="99d76-152">Die ersten drei Zeilen der Ausgabe zeigen den Symbol Handler, der das erste Pfad Element von verarbeitet `.` .</span><span class="sxs-lookup"><span data-stu-id="99d76-152">The first three lines of output show the symbol handler processing the first path element of `.`.</span></span> <span data-ttu-id="99d76-153">Dies ist ein Standardpfad Element.</span><span class="sxs-lookup"><span data-stu-id="99d76-153">This is a standard path element.</span></span>

<span data-ttu-id="99d76-154">Die vierte Zeile zeigt den Symbol Handler, der den Symbol Server verwendet, um nach der Datei im zweiten Path-Element zu suchen, bei `cache*c:\myCache` dem es sich um ein Cache Pfad Element handelt.</span><span class="sxs-lookup"><span data-stu-id="99d76-154">The fourth line shows the symbol handler using the symbol server to look for the file in the second path element of `cache*c:\myCache` which is a cache path element.</span></span>

<span data-ttu-id="99d76-155">Die fünfte Zeile zeigt, dass sich die Datei im dritten Path-Element von befindet `srv*\\symbols\symbols` , bei dem es sich um ein Symbol Server-Pfad Element handelt.</span><span class="sxs-lookup"><span data-stu-id="99d76-155">The fifth line shows the file is found in the third path element of `srv*\\symbols\symbols`, which is a symbol server path element.</span></span>

<span data-ttu-id="99d76-156">Die sechste Zeile zeigt, dass die Datei in den Cache kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="99d76-156">The sixth line shows that the file is copied to the cache.</span></span>

<span data-ttu-id="99d76-157">Die letzten zwei Zeilen, in denen die Datei aus dem Cache geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="99d76-157">The last two lines that the file is opened from the cache.</span></span>
