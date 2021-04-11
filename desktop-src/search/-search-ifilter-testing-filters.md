---
description: Die IFilter-Test Sammlung überprüft die Filter Handler.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Testen von Filter Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2a2b0b6a6728051ab22590a481ad23a7197692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128564"
---
# <a name="testing-filter-handlers"></a><span data-ttu-id="22602-103">Testen von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="22602-103">Testing Filter Handlers</span></span>

<span data-ttu-id="22602-104">Die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Test Sammlung überprüft die Filter Handler.</span><span class="sxs-lookup"><span data-stu-id="22602-104">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite validates your filter handlers.</span></span> <span data-ttu-id="22602-105">Die Test Sammlung bewirkt dies: Aufrufen von [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Methoden und Überprüfen der zurückgegebenen Werte auf Konformität mit der **IFilter** -Schnittstellen Spezifikation; und die Überprüfung, ob Block Bezeichner eindeutig sind und zunehmen, dass sich die **IFilter** -Schnittstelle nach der erneuten Initialisierung konsistent verhält, und dass alle **IFilter** -Methodenaufrufe mit ungültigen Parametern erwartete Fehlercodes zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="22602-105">The test suite does so by: calling [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) methods and checking the returned values for compliance with the **IFilter** interface specification; and checking that chunk identifiers are unique and increasing, that the **IFilter** interface behaves consistently after re-initialization, and that any **IFilter** method calls with invalid parameters return expected error codes.</span></span> <span data-ttu-id="22602-106">Die Test Sammlungs Programme sichern auch die Ausgabe einer Datei, die von einem Filter Handler gefiltert wurde, und überprüfen die **IFilter** -Registrierungsinformationen in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="22602-106">The test suite programs also dump the output of a file filtered by a filter handler, and check the **IFilter** registration information in the registry.</span></span>

<span data-ttu-id="22602-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="22602-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="22602-108">Befehlszeilen Aufruf</span><span class="sxs-lookup"><span data-stu-id="22602-108">Command-Line Invocation</span></span>](#command-line-invocation)
  - [<span data-ttu-id="22602-109">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="22602-109">ifilttst.exe</span></span>](#ifilttstexe)
  - [<span data-ttu-id="22602-110">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="22602-110">filtdump.exe</span></span>](#filtdumpexe)
  - [<span data-ttu-id="22602-111">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="22602-111">filtreg.exe</span></span>](#filtregexe)
  - [<span data-ttu-id="22602-112">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="22602-112">ifilttst.ini</span></span>](#ifilttstini)
- [<span data-ttu-id="22602-113">IFilter-Test Prozedur</span><span class="sxs-lookup"><span data-stu-id="22602-113">IFilter Test Procedure</span></span>](#ifilter-test-procedure)
  - [<span data-ttu-id="22602-114">Validierungs Test</span><span class="sxs-lookup"><span data-stu-id="22602-114">Validation Test</span></span>](#validation-test)
  - [<span data-ttu-id="22602-115">Konsistenz Test</span><span class="sxs-lookup"><span data-stu-id="22602-115">Consistency Test</span></span>](#consistency-test)
  - [<span data-ttu-id="22602-116">Ungültiger Eingabe Test</span><span class="sxs-lookup"><span data-stu-id="22602-116">Invalid Input Test</span></span>](#invalid-input-test)
  - [<span data-ttu-id="22602-117">Testen verschiedener IFilter-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="22602-117">Testing Different IFilter Configurations</span></span>](#testing-different-ifilter-configurations)
- [<span data-ttu-id="22602-118">Sicherstellen, dass registrierte Elemente indiziert werden</span><span class="sxs-lookup"><span data-stu-id="22602-118">Ensuring Registered Items Get Indexed</span></span>](#ensuring-registered-items-get-indexed)
  - [<span data-ttu-id="22602-119">Beispiel Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="22602-119">Sample Log File</span></span>](#sample-log-file)
  - [<span data-ttu-id="22602-120">Beispiel Dumpdatei</span><span class="sxs-lookup"><span data-stu-id="22602-120">Sample Dump File</span></span>](#sample-dump-file)
- [<span data-ttu-id="22602-121">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="22602-121">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="22602-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22602-122">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="22602-123">Wenn ein neuer Filter Handler für einen Dateityp als Ersatz für eine vorhandene Filter Registrierung installiert wird, sollte der Installer die aktuelle Registrierung speichern und wiederherstellen, wenn der neue Filter Handler deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="22602-123">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="22602-124">Es gibt keinen Mechanismus zum Verketten von Filtern.</span><span class="sxs-lookup"><span data-stu-id="22602-124">There is no mechanism to chain filters.</span></span> <span data-ttu-id="22602-125">Daher ist der neue Filter Handler für die Replikation aller notwendigen Funktionen des alten Filters verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="22602-125">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="command-line-invocation"></a><span data-ttu-id="22602-126">Command-Line Aufruf</span><span class="sxs-lookup"><span data-stu-id="22602-126">Command-Line Invocation</span></span>

<span data-ttu-id="22602-127">Die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Test Sammlung besteht aus drei Befehlszeilen Anwendungen: [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)und [ #d2](#filtregexe) und einer Initialisierungsdatei, [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="22602-127">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite consists of three command-line applications - [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe), and [filtreg.exe](#filtregexe) and an initialization file, [ifilttst.ini](#ifilttstini).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22602-128">In Windows 7 und höher werden in verwaltetem Code geschriebene Filter explizit blockiert.</span><span class="sxs-lookup"><span data-stu-id="22602-128">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="22602-129">Filter müssen in nativem Code geschrieben werden, da bei dem Prozess, in dem mehrere Add-Ins ausgeführt werden, mögliche Common Language Runtime (CLR)-Versions Probleme aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="22602-129">Filters MUST be written in native code due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="ifilttstexe"></a><span data-ttu-id="22602-130">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="22602-130">ifilttst.exe</span></span>

<span data-ttu-id="22602-131">Das ifilttst.exe Programm führt mehrere Tests aus, um einen Filter Handler zu validieren.</span><span class="sxs-lookup"><span data-stu-id="22602-131">The ifilttst.exe program runs several tests to validate a filter handler.</span></span> <span data-ttu-id="22602-132">Im folgenden Beispiel wird veranschaulicht, wie Sie das ifilttst.exe Programm über die Befehlszeile aufrufen:</span><span class="sxs-lookup"><span data-stu-id="22602-132">The following example illustrates how to invoke the ifilttst.exe program from the command line:</span></span>


```
ifilttst /i test.htm /l /d /v 1
```

<span data-ttu-id="22602-133">Das Beispiel führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="22602-133">The example performs the following tasks:</span></span>

- <span data-ttu-id="22602-134">Weist das Programm an, die Datei zu filtern test.htm</span><span class="sxs-lookup"><span data-stu-id="22602-134">Directs the program to filter the file test.htm</span></span>
- <span data-ttu-id="22602-135">Leitet die Protokollmeldungen an test.htm. log um.</span><span class="sxs-lookup"><span data-stu-id="22602-135">Redirects the log messages to test.htm.log</span></span>
- <span data-ttu-id="22602-136">Leitet die dumpnachrichten an test.htm. dmp um.</span><span class="sxs-lookup"><span data-stu-id="22602-136">Redirects the dump messages to test.htm.dmp</span></span>
- <span data-ttu-id="22602-137">Legt die Ausführlichkeit auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="22602-137">Sets the verbosity to 1</span></span>

<span data-ttu-id="22602-138">Damit der vorherige Befehl funktioniert, müssen sich drei Dateien im aktuellen Arbeitsverzeichnis befinden: `test.htm` , [ifilttst.exe](#ifilttstexe)und [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="22602-138">For the preceding command to work, three files must be located in the current working directory: `test.htm`, [ifilttst.exe](#ifilttstexe), and [ifilttst.ini](#ifilttstini).</span></span> <span data-ttu-id="22602-139">Befehls Zeilenschalter sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="22602-139">Command-line switches are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22602-140">Switch und mögliche Variablen</span><span class="sxs-lookup"><span data-stu-id="22602-140">Switch and possible variables</span></span></th>
<th><span data-ttu-id="22602-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22602-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22602-142"><strong>/i-Dateiname</strong></span><span class="sxs-lookup"><span data-stu-id="22602-142"><strong>/i file name</strong></span></span></td>
<td><span data-ttu-id="22602-143">Die zu filternde Eingabedatei oder das Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="22602-143">The input file or directory to be filtered.</span></span> <span data-ttu-id="22602-144">Der Dateiname kann die Platzhalter Zeichen <code>\*</code> und enthalten <code>?</code> .</span><span class="sxs-lookup"><span data-stu-id="22602-144">The file name can contain the wildcard characters <code>\*</code> and <code>?</code>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22602-145"><strong>/l</strong></span><span class="sxs-lookup"><span data-stu-id="22602-145"><strong>/l</strong></span></span></td>
<td><span data-ttu-id="22602-146">Protokollmeldungen werden an eine Datei statt an den Bildschirm geleitet.</span><span class="sxs-lookup"><span data-stu-id="22602-146">Log messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="22602-147">Protokollmeldungen beschreiben die einzelnen Tests, die ausgeführt werden, sowie die Erfolgs-/Fehler-Ergebnisse der Tests.</span><span class="sxs-lookup"><span data-stu-id="22602-147">Log messages describe the individual tests performed and the pass/fail results of the tests.</span></span> <span data-ttu-id="22602-148">Der Name der Protokolldatei ist mit dem Namen der Eingabedatei, jedoch mit der Dateierweiterung ". log" identisch.</span><span class="sxs-lookup"><span data-stu-id="22602-148">The log file name is the same as the input file name but with a .log extension.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22602-149"><strong>/d</strong></span><span class="sxs-lookup"><span data-stu-id="22602-149"><strong>/d</strong></span></span></td>
<td><span data-ttu-id="22602-150">Das Absichern von Nachrichten wird an eine Datei statt an den Bildschirm geleitet.</span><span class="sxs-lookup"><span data-stu-id="22602-150">Dump messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="22602-151">Dumpmeldungen beschreiben den Inhalt der Blöcke.</span><span class="sxs-lookup"><span data-stu-id="22602-151">Dump messages describe the contents of the chunks.</span></span> <span data-ttu-id="22602-152">Die Blockstruktur wird gekippt, wenn der ausführlichkeits Grad 3 ist.</span><span class="sxs-lookup"><span data-stu-id="22602-152">The chunk structure is dumped when the verbosity level is 3.</span></span> <span data-ttu-id="22602-153">Der Name der Dumpdatei ist mit dem Eingabe Dateinamen identisch, aber mit der Erweiterung DMP.</span><span class="sxs-lookup"><span data-stu-id="22602-153">The dump file name is the same as the input file name but with a .dmp extension.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22602-154"><strong>/-l</strong></span><span class="sxs-lookup"><span data-stu-id="22602-154"><strong>/-l</strong></span></span></td>
<td><span data-ttu-id="22602-155">Deaktiviert die Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="22602-155">Disable logging.</span></span> <span data-ttu-id="22602-156">Dieses Flag überschreibt den <code>/l</code> Switch.</span><span class="sxs-lookup"><span data-stu-id="22602-156">This flag overrides the <code>/l</code> switch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22602-157"><strong>/-d</strong></span><span class="sxs-lookup"><span data-stu-id="22602-157"><strong>/-d</strong></span></span></td>
<td><span data-ttu-id="22602-158">Deaktivieren Sie die Sicherung.</span><span class="sxs-lookup"><span data-stu-id="22602-158">Disable dumping.</span></span> <span data-ttu-id="22602-159">Dieses Flag überschreibt den <code>/d</code> Switch.</span><span class="sxs-lookup"><span data-stu-id="22602-159">This flag overrides the <code>/d</code> switch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22602-160"><strong>/v-Ganzzahl</strong></span><span class="sxs-lookup"><span data-stu-id="22602-160"><strong>/v integer</strong></span></span></td>
<td><span data-ttu-id="22602-161">Der Ausführlichkeitsgrad.</span><span class="sxs-lookup"><span data-stu-id="22602-161">The verbosity level.</span></span> <span data-ttu-id="22602-162">Der Standardwert ist 3.</span><span class="sxs-lookup"><span data-stu-id="22602-162">The default is 3.</span></span>
<ul>
<li><span data-ttu-id="22602-163">0-der Test protokolliert nur Meldungen zu bestimmten Fehlern der <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="22602-163">0 - The test logs only messages concerning specific <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> interface failures.</span></span> <span data-ttu-id="22602-164">Der Test sichert den Block Inhalt.</span><span class="sxs-lookup"><span data-stu-id="22602-164">The test dumps the chunk contents.</span></span></li>
<li><span data-ttu-id="22602-165">1-der Test protokolliert Warnmeldungen und die für Ebene 0.</span><span class="sxs-lookup"><span data-stu-id="22602-165">1 - The test logs warning messages as well as those for level 0.</span></span></li>
<li><span data-ttu-id="22602-166">2: der Test protokolliert Nachrichten zu bestandenen Tests sowie zu den für Ebene 1 übergebenen Tests.</span><span class="sxs-lookup"><span data-stu-id="22602-166">2 - The test logs messages concerning tests that passed as well as those for level 1.</span></span></li>
<li><span data-ttu-id="22602-167">3-der Test protokolliert Informationsmeldungen und die für Ebene 2.</span><span class="sxs-lookup"><span data-stu-id="22602-167">3 - The test logs informational messages as well as those for level 2.</span></span> <span data-ttu-id="22602-168">Außerdem sichert der Test die Struktur des Blocks.</span><span class="sxs-lookup"><span data-stu-id="22602-168">In addition, the test dumps the structure of the chunk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22602-169"><strong>/t-Ganzzahl</strong></span><span class="sxs-lookup"><span data-stu-id="22602-169"><strong>/t integer</strong></span></span></td>
<td><span data-ttu-id="22602-170">Die Anzahl der zu startenden Threads.</span><span class="sxs-lookup"><span data-stu-id="22602-170">The number of threads to launch.</span></span> <span data-ttu-id="22602-171">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="22602-171">The default is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22602-172"><strong>/r-Ganzzahl</strong>]</span><span class="sxs-lookup"><span data-stu-id="22602-172"><strong>/r integer</strong>]</span></span></td>
<td><span data-ttu-id="22602-173">Filtert Unterverzeichnisse rekursiv.</span><span class="sxs-lookup"><span data-stu-id="22602-173">Recursively filters subdirectories.</span></span> <span data-ttu-id="22602-174">Der optionale INTEGER-Parameter gibt die Tiefe an, in der Rekursion durchlaufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="22602-174">The optional integer parameter specifies the depth to which to exercise recursion.</span></span> <span data-ttu-id="22602-175">Wenn keine Ganzzahl angegeben wird, oder wenn die Ganzzahl 0 ist, wird die vollständige Rekursion angenommen.</span><span class="sxs-lookup"><span data-stu-id="22602-175">If no integer is specified, or if the integer is 0, full recursion is assumed.</span></span> <span data-ttu-id="22602-176">Standardmäßig ist die Rekursions Tiefe 1.</span><span class="sxs-lookup"><span data-stu-id="22602-176">By default, the recursion depth is 1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22602-177"><strong>/c-Ganzzahl</strong></span><span class="sxs-lookup"><span data-stu-id="22602-177"><strong>/c integer</strong></span></span></td>
<td><span data-ttu-id="22602-178">Gibt an, wie oft die Schleife durchlaufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="22602-178">The number of times to loop.</span></span> <span data-ttu-id="22602-179">Wenn die Ganzzahl 0 ist, wird der Test unendlich durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="22602-179">If the integer is 0, the test loops infinitely.</span></span> <span data-ttu-id="22602-180">Standardmäßig wird der Test nur einmal durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="22602-180">By default, the test loops only once.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]  
> <span data-ttu-id="22602-181">Sie müssen ein Leerzeichen zwischen dem Befehls Zeilenschalter und dem Wert einschließen.</span><span class="sxs-lookup"><span data-stu-id="22602-181">You must include a space between the command line switch and the value.</span></span>

### <a name="filtdumpexe"></a><span data-ttu-id="22602-182">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="22602-182">filtdump.exe</span></span>

<span data-ttu-id="22602-183">Das filtdump.exe Programm lädt einen Filter Handler für ein angegebenes Dokument und druckt die Ausgabe, die von der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -dll erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="22602-183">The filtdump.exe program loads a filter handler for a specified document and prints the output produced by the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL.</span></span> <span data-ttu-id="22602-184">Im folgenden Beispiel wird veranschaulicht, wie Sie das filtdump.exe Programm aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22602-184">The following example illustrates how to invoke the filtdump.exe program.</span></span>

```
filtdump filename.ext
```
<span data-ttu-id="22602-185">Filtdump.exe verwendet die [iloadfilter:: loadifilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) -Methode, um die für die angegebene Dateinamenerweiterung geeignete [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -dll zu laden und die Ergebnisse zu drucken.</span><span class="sxs-lookup"><span data-stu-id="22602-185">Filtdump.exe uses the [ILoadFilter::LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) method to load the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL appropriate for the specified file name extension and prints the results.</span></span> <span data-ttu-id="22602-186">Beispielsweise weist der folgende Befehl filtdump.exe an, den smpfilt.dll Filter Handler für die Erweiterung ". SMP" zu laden, den gesamten Text und die Eigenschaften aus der Datei "MyFile. SMP" zu extrahieren und die Ergebnisse zu drucken.</span><span class="sxs-lookup"><span data-stu-id="22602-186">For example, the following command instructs filtdump.exe to load the smpfilt.dll filter handler for the extension .smp, extract all text and properties from the file myfile.smp, and print the results.</span></span>

```
filtdump myfile.smp
```

### <a name="filtregexe"></a><span data-ttu-id="22602-187">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="22602-187">filtreg.exe</span></span>

<span data-ttu-id="22602-188">Das filtreg.exe Programm überprüft die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Installationsinformationen in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="22602-188">The filtreg.exe program inspects [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) installation information in the registry.</span></span> <span data-ttu-id="22602-189">Sie rufen das filtreg.exe Programm von der Befehlszeile aus, indem Sie seinen Namen eingeben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="22602-189">You invoke the filtreg.exe program from the command line by typing its name, as in the following example.</span></span>

```
filtreg
```

<span data-ttu-id="22602-190">Filtreg.exe listet alle Dateinamen Erweiterungen auf, denen Filter Handler zugeordnet sind, indem die Dateinamenerweiterung und der Name der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -dll für die Erweiterung gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="22602-190">Filtreg.exe enumerates all file name extensions that have filter handlers associated with them by printing the file name extension and the name of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL for the extension.</span></span> <span data-ttu-id="22602-191">Dies ist eine einfache Möglichkeit, die korrekte Installation eines **IFilters** zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="22602-191">This is a simple way to verify the correct installation of an **IFilter**.</span></span>

### <a name="ifilttstini"></a><span data-ttu-id="22602-192">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="22602-192">ifilttst.ini</span></span>

<span data-ttu-id="22602-193">Eine [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle wird initialisiert, indem die [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="22602-193">An [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface is initialized by calling the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="22602-194">Die **IFilter:: init** -Methode übernimmt die folgenden vier Parameter:</span><span class="sxs-lookup"><span data-stu-id="22602-194">The **IFilter::Init** method takes the following four parameters:</span></span>

1. <span data-ttu-id="22602-195">*grfFlags*</span><span class="sxs-lookup"><span data-stu-id="22602-195">*grfFlags*</span></span>
2. <span data-ttu-id="22602-196">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="22602-196">*cAttributes*</span></span>
3. <span data-ttu-id="22602-197">*aattribute*</span><span class="sxs-lookup"><span data-stu-id="22602-197">*aAttributes*</span></span>
4. <span data-ttu-id="22602-198">*pdwflags*</span><span class="sxs-lookup"><span data-stu-id="22602-198">*pdwFlags*</span></span>

<span data-ttu-id="22602-199">Der Benutzer des ifilttst.exe Programms der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Test Sammlung kann die Werte für diese Parameter in einer Datei namens ifilttst.ini angeben.</span><span class="sxs-lookup"><span data-stu-id="22602-199">The user of the ifilttst.exe program of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite can specify the values for these parameters in a file called ifilttst.ini.</span></span> <span data-ttu-id="22602-200">In der folgenden Tabelle werden die Einträge in der ifilttst.ini-Datei beschrieben, in denen die ersten drei Parameter (die Eingabeparameter) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="22602-200">The following table describes the entries in the ifilttst.ini file that specify the first three parameters(the input parameters).</span></span> <span data-ttu-id="22602-201">Eine Beispieldatei finden Sie unter [Sample ifilttst.ini File](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="22602-201">For a sample file, see [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span>

> [!NOTE]  
> <span data-ttu-id="22602-202">Es ist kein Tabelleneintrag für den *pdwflags* -Parameter vorhanden, da es sich um einen Output-Parameter handelt. vor dem Aufrufe der [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Methode muss kein spezieller Wert vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="22602-202">There is no table entry for the *pdwFlags* parameter because it is an output parameter; it does not need to have any special value prior to the call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

 | <span data-ttu-id="22602-203">Eingabe</span><span class="sxs-lookup"><span data-stu-id="22602-203">Entry</span></span>         | <span data-ttu-id="22602-204">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22602-204">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22602-205">Flags</span><span class="sxs-lookup"><span data-stu-id="22602-205">Flags</span></span>         | <span data-ttu-id="22602-206">Die Namen der [**IFilter- \_ Init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) -Flags, die durch den or-Operator verknüpft werden sollen, um den *grfFlags* -Parameter der [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Methode zu bilden.</span><span class="sxs-lookup"><span data-stu-id="22602-206">The names of the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) flags that are to be joined by the OR operator to form the *grfFlags* parameter of the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="22602-207">Die flagnamen müssen in Großbuchstaben und in derselben Zeile angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="22602-207">The flag names must all be uppercase, and on the same line.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="22602-208">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="22602-208">*cAttributes*</span></span> | <span data-ttu-id="22602-209">Eine ganze Dezimalzahl, die den Wert *des Parameters* "-Parameter" darstellt.</span><span class="sxs-lookup"><span data-stu-id="22602-209">A decimal integer representing the value of the *cAttributes* parameter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="22602-210">*aattribute*</span><span class="sxs-lookup"><span data-stu-id="22602-210">*aAttributes*</span></span> | <span data-ttu-id="22602-211">Dieser Eintrag muss mit " *aattributs* " beginnen und muss sich von den anderen " *aattribute* "-Einträgen innerhalb des Abschnitts unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="22602-211">This entry must start with *aAttributes* and must be different from the other *aAttributes* entries within the section.</span></span> <span data-ttu-id="22602-212">Zulässige Namen für den *aattribute* -Eintrag lauten: *aattribute*, *aAttributes1*, *aAttributes2* usw.</span><span class="sxs-lookup"><span data-stu-id="22602-212">Legal names for the *aAttributes* entry are: *aAttributes*, *aAttributes1*, *aAttributes2*, and so forth.</span></span> <span data-ttu-id="22602-213">Das erste Token muss eine GUID sein.</span><span class="sxs-lookup"><span data-stu-id="22602-213">The first token must be a GUID.</span></span> <span data-ttu-id="22602-214">Die GUID muss genau so formatiert sein, wie im `[Test3]` Abschnitt der [Beispiel ifilttst.ini Datei](#sample-ifilttstini-file)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="22602-214">The GUID must be formatted exactly as illustrated in the `[Test3]` section of the [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span> <span data-ttu-id="22602-215">Das zweite Token kann entweder ein Eigenschaften Bezeichner (PID) sein, der aus einer Zahl in hexadezimal Notation besteht, oder ein Zeiger auf eine breit Zeichen Zeichenfolge (LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="22602-215">The second token can be either a property identifier (PID) consisting of a number in hexadecimal notation, or a pointer to a wide character string (lpwstr).</span></span> <span data-ttu-id="22602-216">Ein LPWSTR kann angegeben werden, indem die Zeichenfolge in doppelte Anführungszeichen eingeschlossen wird, wie im `[Test6]` Abschnitt der Beispiel ifilttst.ini Datei veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="22602-216">A lpwstr can be specified by enclosing the string in double quotes, as illustrated in the `[Test6]` section of the Sample ifilttst.ini File.</span></span> |

<span data-ttu-id="22602-217">Wenn die *Flags und die* "}"-Einträge nicht angegeben sind, werden Sie standardmäßig auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22602-217">If the Flags and *cAttributes* entries are not specified, they default to 0.</span></span> <span data-ttu-id="22602-218">Wenn Sie "" auf "2 *" festlegen,* sollten Sie zwei *aattribute* -Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="22602-218">If you set *cAttributes* equal to 2, you should specify two *aAttributes* names.</span></span> <span data-ttu-id="22602-219">Im- `[Test5]` Abschnitt des Beispiels ist "  " für "" "" "1", aber es wurden keine *aattribute* angegeben.</span><span class="sxs-lookup"><span data-stu-id="22602-219">In the `[Test5]` section of the sample, *cAttributes* is 1, but no *aAttributes* have been specified.</span></span> <span data-ttu-id="22602-220">Der Test ruft dann die [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Methode *mit "* " für "1" und " *aattribute* " auf, die gleich **null** sind.</span><span class="sxs-lookup"><span data-stu-id="22602-220">The test then calls the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method with *cAttributes* equal to 1 and *aAttributes* equal to **NULL**.</span></span> <span data-ttu-id="22602-221">Dies ist ein nützlicher Testfall, da er wahrscheinlich eine Zugriffsverletzung in der **IFilter:: init** -Methode verursacht.</span><span class="sxs-lookup"><span data-stu-id="22602-221">This is a useful test case because it is likely to cause an access violation in the **IFilter::Init** method.</span></span>

<span data-ttu-id="22602-222">Wenn ifilttst.exe im Arbeitsverzeichnis eine Datei mit dem Namen ifilttst.ini nicht finden kann, wird eine Standardkonfiguration verwendet, um das [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="22602-222">If ifilttst.exe cannot find a file named ifilttst.ini in the working directory, a default configuration is used to initialize the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) object.</span></span> <span data-ttu-id="22602-223">Das folgende Beispiel veranschaulicht die Standardkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="22602-223">The following example illustrates the default configuration.</span></span>

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a><span data-ttu-id="22602-224">Beispiel ifilttst.ini Datei</span><span class="sxs-lookup"><span data-stu-id="22602-224">Sample ifilttst.ini File</span></span>

<span data-ttu-id="22602-225">Die ifilttst.ini-Datei ist in Abschnitten organisiert, wobei der Abschnitts Name in eckige Klammern eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="22602-225">The ifilttst.ini file is organized in sections, with the section name enclosed in square brackets.</span></span> <span data-ttu-id="22602-226">Im Beispiel werden die Abschnitte, `[Test1]` `[Test2]` usw. benannt.</span><span class="sxs-lookup"><span data-stu-id="22602-226">In the example, the sections are named `[Test1]`, `[Test2]`, and so forth.</span></span> <span data-ttu-id="22602-227">Alle Abschnittsnamen müssen eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="22602-227">All section names must be unique.</span></span> <span data-ttu-id="22602-228">Der Test liest die Werte aus dem ersten Abschnitt und initialisiert den [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) mit diesen Werten.</span><span class="sxs-lookup"><span data-stu-id="22602-228">The test reads the values from the first section and initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) with those values.</span></span> <span data-ttu-id="22602-229">Anschließend werden alle Tests mit dieser **IFilter** -Konfiguration ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22602-229">Then all the tests are run using this **IFilter** configuration.</span></span> <span data-ttu-id="22602-230">Anschließend wird der **IFilter** freigegeben und mit den oben aufgeführten Parametern erneut initialisiert.</span><span class="sxs-lookup"><span data-stu-id="22602-230">Then the **IFilter** is released and reinitialized, using parameters that are listed above.</span></span> <span data-ttu-id="22602-231">Der Prozess wird wiederholt, bis alle Konfigurationen getestet wurden.</span><span class="sxs-lookup"><span data-stu-id="22602-231">The process is repeated until all configurations are tested.</span></span>

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a><span data-ttu-id="22602-232">IFilter-Test Prozedur</span><span class="sxs-lookup"><span data-stu-id="22602-232">IFilter Test Procedure</span></span>

<span data-ttu-id="22602-233">Nachdem der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) initialisiert wurde, führt das ifilttst.exe Programm eine Reihe von Tests für den **IFilter** aus.</span><span class="sxs-lookup"><span data-stu-id="22602-233">After the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) has been initialized, the ifilttst.exe program conducts a series of tests on the **IFilter**.</span></span> <span data-ttu-id="22602-234">Zusätzlich zu den **IFilter** -Test Prozeduren müssen Sie sicherstellen, dass Ihre **IFilter** -Implementierung sichere Code Praktiken einsetzt.</span><span class="sxs-lookup"><span data-stu-id="22602-234">In addition to following the **IFilter** test procedures, ensure that your **IFilter** implementation employs secure code practices.</span></span> <span data-ttu-id="22602-235">Weitere Informationen finden Sie unter "sichere Code Praktiken für Windows Search" in [Implementieren von Filter Handlern in Windows Search](-search-ifilter-constructing-filters.md).</span><span class="sxs-lookup"><span data-stu-id="22602-235">See "Secure Code Practices for Windows Search" in [Implementing Filter Handlers in Windows Search](-search-ifilter-constructing-filters.md).</span></span>

### <a name="validation-test"></a><span data-ttu-id="22602-236">Validierungs Test</span><span class="sxs-lookup"><span data-stu-id="22602-236">Validation Test</span></span>

<span data-ttu-id="22602-237">Bei der Überprüfung werden die einzelnen einzelnen Blöcke und alle Rückgabecodes schrittweise durch das Objekt überprüfen.</span><span class="sxs-lookup"><span data-stu-id="22602-237">The validation test steps through the object one chunk at a time, verifying each individual chunk and all return codes.</span></span> <span data-ttu-id="22602-238">Beim Validierungstest werden alle zurück [**gegebenen \_ stat**](/windows/win32/api/filter/ns-filter-stat_chunk) -Block Strukturen in einer Liste gespeichert.</span><span class="sxs-lookup"><span data-stu-id="22602-238">The validation test saves all returned [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structures in a list.</span></span>

<span data-ttu-id="22602-239">Der Validierungstest überprüft die folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="22602-239">The validation test verifies the following conditions:</span></span>

- <span data-ttu-id="22602-240">Der [**stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk)-Block.*idchunk* -Block-IDs müssen eindeutig sein und zunehmen.</span><span class="sxs-lookup"><span data-stu-id="22602-240">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunk* chunk IDs must be unique and increasing.</span></span>
- <span data-ttu-id="22602-241">Der [**stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk)-Block.*der Flags* -Parameter ist ein erkannter Block Zustand, wie z. b. " [**chunkstate**](/windows/win32/api/filter/ne-filter-chunkstate)", " \_ Block Text" oder "cenabledhunk"- \_ Wert Konstanten.</span><span class="sxs-lookup"><span data-stu-id="22602-241">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*flags* parameter is a recognized chunk state, such as [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), CHUNK\_TEXT, or CenabledHUNK\_VALUE constants.</span></span>
- <span data-ttu-id="22602-242">Der [**stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk)-Block.*der breaktype* -Parameter ist ein erkannter breaktyp (0, 1, 2, 3, 4).</span><span class="sxs-lookup"><span data-stu-id="22602-242">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*breakType* parameter is a recognized break type (0, 1, 2, 3, 4).</span></span>
- <span data-ttu-id="22602-243">Wenn die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Initialisierungs Attribute angeben, dass der **IFilter** nur Segmente mit internen Werttyp Eigenschaften zurückgeben soll, muss *idchunksource* gleich 0 sein.</span><span class="sxs-lookup"><span data-stu-id="22602-243">If the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) initialization attributes specify that the **IFilter** should return only chunks containing internal value-type properties, then *idChunkSource* must equal 0.</span></span>
- <span data-ttu-id="22602-244">Wenn der Block nicht abgeleitet ist, d. h., wenn es sich nicht um eine Eigenschaft des internen Werttyps handelt, dann ist [**stat \_**](/windows/win32/api/filter/ns-filter-stat_chunk)Block.*idchunksource* muss dem **stat \_**-Block entsprechen.*idblock*.</span><span class="sxs-lookup"><span data-stu-id="22602-244">If the chunk is not derived that is, if it is not an internal value-type property, then [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* must equal **STAT\_CHUNK**.*idChunk*.</span></span>
- <span data-ttu-id="22602-245">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) gibt S \_ OK oder einen anderen akzeptablen Rückgabewert zurück, wie \_ z \_ . b. Filter e Ende \_ von \_ Blöcken, Filter \_ \_ -e-Link nicht verfügbar usw \_ .</span><span class="sxs-lookup"><span data-stu-id="22602-245">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>
- <span data-ttu-id="22602-246">Wenn der Block Text enthält, gibt [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) s \_ OK zurück, filtert den \_ \_ letzten \_ Text oder filtert \_ E \_ nicht \_ mehr \_ Text.</span><span class="sxs-lookup"><span data-stu-id="22602-246">If the chunk contains text, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns S\_OK, FILTER\_S\_LAST\_TEXT, or FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="22602-247">Wenn [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) Filter \_ S \_ Last Text zurückgibt \_ , gibt der nächste **IFilter:: gettext** -Aufrufe Filter \_ E \_ nicht \_ mehr Text zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="22602-247">If [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_S\_LAST\_TEXT, the next call to **IFilter::GetText** returns FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="22602-248">Wenn der Block einen Wert enthält, gibt [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) S \_ OK zurück oder filtert \_ E \_ nicht \_ mehr \_ .</span><span class="sxs-lookup"><span data-stu-id="22602-248">If the chunk contains a value, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns S\_OK or FILTER\_E\_NO\_MORE\_VALUES.</span></span>

### <a name="consistency-test"></a><span data-ttu-id="22602-249">Konsistenz Test</span><span class="sxs-lookup"><span data-stu-id="22602-249">Consistency Test</span></span>

<span data-ttu-id="22602-250">Das ifilttxt.exe Programm initialisiert die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erneut mit denselben Parametern wie im Validierungstest und führt einen Konsistenz Test aus.</span><span class="sxs-lookup"><span data-stu-id="22602-250">The ifilttxt.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters as in the validation test and performs a consistency test.</span></span> <span data-ttu-id="22602-251">Wenn die **IFilter** -Implementierung mit dem Flag [**IFilter \_**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) init IFilter \_ Init \_ Indizierung nur initialisiert wurde \_ , gibt der Test die **IFilter** -Schnittstelle frei und bindet Sie erneut, bevor Sie einen weiteren Rückruf an die [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) -Methode durchführen.</span><span class="sxs-lookup"><span data-stu-id="22602-251">If the **IFilter** implementation has been initialized with the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFILTER\_INIT\_INDEXING\_ONLY flag, the test releases the **IFilter** interface and re-binds it before making another call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

<span data-ttu-id="22602-252">Der Konsistenz Test überprüft die folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="22602-252">The consistency test verifies the following conditions:</span></span>

- <span data-ttu-id="22602-253">Jede von der [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) -Methode zurückgegebene stat-Blockstruktur ist mit dem entsprechenden im Validierungstest zurückgegebenen **stat \_** -Block identisch. [**\_**](/windows/win32/api/filter/ns-filter-stat_chunk)</span><span class="sxs-lookup"><span data-stu-id="22602-253">Each [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structure returned by the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method is identical to the corresponding **STAT\_CHUNK** returned in the validation test.</span></span>
- <span data-ttu-id="22602-254">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) gibt S \_ OK oder einen anderen akzeptablen Rückgabewert zurück, wie \_ z \_ . b. Filter e Ende \_ von \_ Blöcken, Filter \_ \_ -e-Link nicht verfügbar usw \_ .</span><span class="sxs-lookup"><span data-stu-id="22602-254">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>

### <a name="invalid-input-test"></a><span data-ttu-id="22602-255">Ungültiger Eingabe Test</span><span class="sxs-lookup"><span data-stu-id="22602-255">Invalid Input Test</span></span>

<span data-ttu-id="22602-256">Das ifilttst.exe Programm initialisiert die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle mit denselben Parametern erneut und führt einen ungültigen Eingabe Test aus.</span><span class="sxs-lookup"><span data-stu-id="22602-256">The ifilttst.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters,and performs an invalid input test.</span></span> <span data-ttu-id="22602-257">Dieser Test durchläuft das Dokument einen Block zu einem Zeitpunkt, an dem Funktionsaufrufe nicht ordnungsgemäß ausgeführt werden, wie z. b. das Aufrufen der [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) -Methode, wenn der aktuelle Chuck Text enthält.</span><span class="sxs-lookup"><span data-stu-id="22602-257">This test steps through the document one chunk at a time making function calls incorrectly, such as calling the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method when the current chuck contains text.</span></span> <span data-ttu-id="22602-258">Der Test überprüft alle Rückgabecodes auf Konformität mit der **IFilter** -Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="22602-258">The test checks all return codes for compliance with the **IFilter** specification.</span></span>

<span data-ttu-id="22602-259">Der ungültige Eingabe Test überprüft die folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="22602-259">The invalid input test verifies the following conditions:</span></span>

- <span data-ttu-id="22602-260">Wenn der aktuelle Block Text enthält, gibt [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) Filter \_ E \_ No \_ -Werte zurück, und ein [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) -Rückruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="22602-260">If the current chunk contains text, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns FILTER\_E\_NO\_VALUES, and a call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) succeeds.</span></span>
- <span data-ttu-id="22602-261">Wenn der aktuelle Block einen Wert enthält, gibt [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) Filter \_ E \_ No Text zurück \_ , und ein [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) -Rückruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="22602-261">If the current chunk contains a value, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_E\_NO\_TEXT, and a call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) succeeds.</span></span>
- <span data-ttu-id="22602-262">Wenn beim vorherigen Aufruf von [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) der Filter \_ e \_ nicht \_ mehr \_ Text zurückgegeben wurde, wird bei aufeinander folgenden Aufrufen von **IFilter:: gettext** der Filter \_ e \_ nicht \_ mehr Text zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="22602-262">If the previous call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returned FILTER\_E\_NO\_MORE\_TEXT, successive calls to **IFilter::GetText** return FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="22602-263">Wenn der vorherige Aufruf von [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) den Filter \_ e \_ nicht \_ mehr zurückgegeben \_ hat, werden bei aufeinander folgenden Aufrufen von **IFilter:: GetValue** Filter \_ e \_ nicht \_ mehr Werte zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="22602-263">If the previous call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returned FILTER\_E\_NO\_MORE\_VALUES, successive calls to **IFilter::GetValue** return FILTER\_E\_NO\_MORE\_VALUES.</span></span>
- <span data-ttu-id="22602-264">Wenn der vorherige Aufruf von [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) das Ende von Segmenten filtert \_ \_ \_ \_ , werden nachfolgende Aufrufe von **IFilter:: GetChunk** das \_ \_ Ende von Blöcken am Ende Filtern \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="22602-264">If the previous call to [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returned FILTER\_E\_END\_OF\_CHUNKS, successive calls to **IFilter::GetChunk** return FILTER\_E\_END\_OF\_CHUNKS.</span></span>

> [!NOTE]  
> <span data-ttu-id="22602-265">Der ungültige Eingabe Test vergleicht die aktuellen Block Strukturen mit den im Validierungstest zurückgegebenen, um sicherzustellen, dass Sie identisch sind.</span><span class="sxs-lookup"><span data-stu-id="22602-265">The invalid input test compares the current chunk structures to those returned in the validation test to make sure they are identical.</span></span>

### <a name="testing-different-ifilter-configurations"></a><span data-ttu-id="22602-266">Testen verschiedener IFilter-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="22602-266">Testing Different IFilter Configurations</span></span>

<span data-ttu-id="22602-267">Mit dem ifilttst.exe Programm wird die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle freigegeben und die Bindung wieder hergestellt. dieses Mal wird Sie mit dem nächsten Parametersatz initialisiert.</span><span class="sxs-lookup"><span data-stu-id="22602-267">The ifilttst.exe program releases the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface and rebinds, this time initializing it with the next set of parameters.</span></span> <span data-ttu-id="22602-268">Der Test wiederholt den Zeitraum: Validierungstest, Konsistenz Test und Ungültiger Eingabe Test, bis alle gewünschten **IFilter** -Konfigurationen, die in [ifilttst.ini](#ifilttstini) Datei angegeben wurden, getestet wurden.</span><span class="sxs-lookup"><span data-stu-id="22602-268">The test repeats the cycle: validation test, consistency test, and invalid input test, until all the desired **IFilter** configurations specified in [ifilttst.ini](#ifilttstini) file have been tested.</span></span>

## <a name="ensuring-registered-items-get-indexed"></a><span data-ttu-id="22602-269">Sicherstellen, dass registrierte Elemente indiziert werden</span><span class="sxs-lookup"><span data-stu-id="22602-269">Ensuring Registered Items Get Indexed</span></span>

<span data-ttu-id="22602-270">Der abschließende Test Ihres [**IFilters**](/windows/win32/api/filter/nn-filter-ifilter) stellt sicher, dass Ihr **IFilter** ordnungsgemäß registriert ist und aufgerufen wird, um die Elemente zu indizieren, die Sie für die Verwendung registriert haben.</span><span class="sxs-lookup"><span data-stu-id="22602-270">The final test of your [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ensures that your **IFilter** is properly registered and that it is invoked to index the items that you registered to use it.</span></span> <span data-ttu-id="22602-271">Sie können den Katalog-Manager verwenden, um die erneute Indizierung zu initiieren, oder Sie verwenden den Crawl Scope Manager (CSM) zum Einrichten von Standardregeln, die die URLs angeben, die der Indexer durchforsten soll.</span><span class="sxs-lookup"><span data-stu-id="22602-271">You can use the Catalog Manager to initiate re-indexing, or use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl.</span></span> <span data-ttu-id="22602-272">Nachdem die Indizierung durchgeführt wurde, verwenden Sie die Windows-Such Benutzeroberfläche, um eine Zeichenfolge im Inhalt oder in den Eigenschaften von Elementen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="22602-272">After indexing is complete, use the Windows Search UI to search for a string in the content or properties of items.</span></span> <span data-ttu-id="22602-273">Wenn die Elemente indiziert wurden, werden Sie in den Suchergebnissen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22602-273">If the items were indexed, they will appear in the search results.</span></span>

<span data-ttu-id="22602-274">Weitere Informationen zur erneuten Indizierung finden Sie unter [using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) und [using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="22602-274">For more information about re-indexing, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span> <span data-ttu-id="22602-275">Das Codebeispiel für das XML-matchingurls veranschaulicht, wie Sie angeben können, welche Dateien neu indiziert werden sollen und wie.</span><span class="sxs-lookup"><span data-stu-id="22602-275">The ReindexMatchingUrls code sample demonstrates ways to specify which files to re-index and how.</span></span> <span data-ttu-id="22602-276">Das Codebeispiel crawlscopecommandline veranschaulicht, wie Befehlszeilenoptionen für CSM-Indizierungs Vorgänge (Crawl Scope Manager) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="22602-276">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span> <span data-ttu-id="22602-277">Beide Codebeispiele sind auf [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22602-277">Both code samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

### <a name="sample-log-file"></a><span data-ttu-id="22602-278">Beispiel Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="22602-278">Sample Log File</span></span>

<span data-ttu-id="22602-279">Bei der Anforderung kann das Ifilttst.exe Programm ein Protokoll mit einer Beschreibung der Schritte, die während der Ausführung ausgeführt werden, liefern.</span><span class="sxs-lookup"><span data-stu-id="22602-279">Upon request, the Ifilttst.exe program can produce a log containing a description of the steps it takes during execution.</span></span> <span data-ttu-id="22602-280">Die folgenden Beispiele sind Ausschnitte aus einer Protokolldatei, wobei der ausführlichkeits Grad auf den höchstmöglichen Wert 3 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="22602-280">The following examples are excerpts from a log file, with the verbosity set to the highest possible value 3.</span></span>

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

<span data-ttu-id="22602-281">Die erste Zeile ist eine Informations Meldung, die angibt, dass eine neue Konfiguration aus der ifilttst.ini Datei geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="22602-281">The first line is an informational message, indicating that a new configuration has been loaded from the ifilttst.ini file.</span></span> <span data-ttu-id="22602-282">Line (3) gibt den Abschnittsnamen in der ifilttst.ini Datei an, aus der die aktuelle Konfiguration gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="22602-282">Line (3) indicates the section name in the ifilttst.ini file from which the current configuration has been read.</span></span> <span data-ttu-id="22602-283">In Zeilen (4) bis (7) werden die Parameter für [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init)aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="22602-283">Lines (4) through (7) list the parameters to [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span></span> <span data-ttu-id="22602-284">Die Zeilen, die mit beginnen, `INFO` sind Informationsmeldungen zur Bindung von [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) und zum Beginn des Validierungstests.</span><span class="sxs-lookup"><span data-stu-id="22602-284">The lines starting with `INFO` are informational messages about the binding of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and the start of the validation test.</span></span> <span data-ttu-id="22602-285">Zeilen `PASS` , die mit beginnen, sind Meldungen in Bezug auf bestimmte Tests, die bestanden wurden.</span><span class="sxs-lookup"><span data-stu-id="22602-285">Lines starting with `PASS` are messages regarding specific tests that have passed.</span></span>

<span data-ttu-id="22602-286">Die Zeile im folgenden Protokoll Beispiel ist eine Warnung.</span><span class="sxs-lookup"><span data-stu-id="22602-286">The line in the following log example is a warning.</span></span> <span data-ttu-id="22602-287">Warnungen werden auf das [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Verhalten aufmerksam gemacht, das problematisch ist, auch wenn dies rechtmäßig</span><span class="sxs-lookup"><span data-stu-id="22602-287">Warnings call attention to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) behavior that is problematic, although legal.</span></span> <span data-ttu-id="22602-288">Diese Warnung gibt an, dass die [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) -Methode einen Textabschnitt zurückgegeben hat, der keinen Text enthält.</span><span class="sxs-lookup"><span data-stu-id="22602-288">This warning indicates that the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method has returned a text chunk that contains no text.</span></span>

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

<span data-ttu-id="22602-289">Die folgende Beispiel Fehlermeldung gibt an, dass der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) einen nicht angeforderten Block ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="22602-289">The following example error message indicates that the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk that was not requested.</span></span>

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

<span data-ttu-id="22602-290">Im Fall dieser Beispiel Fehlermeldung hat der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) einen Block mit einer PID von ausgegeben `0x5` .</span><span class="sxs-lookup"><span data-stu-id="22602-290">In the case of this example error message, the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk with a PID of `0x5`.</span></span> <span data-ttu-id="22602-291">Die Überprüfung des Abschnitts `[Test1]` in ifilttst.ini würde zeigen, dass der **IFilter** so konfiguriert wurde, dass keine Blöcke mit dieser PID ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="22602-291">Inspection of section `[Test1]` in ifilttst.ini would show that the **IFilter** was configured to not emit chunks with this PID.</span></span> <span data-ttu-id="22602-292">Wenn z. b. weder die IFilter- \_ Init \_ \_ Index \_ Attribute noch die IFilter-init anwenden, werden \_ \_ \_ \_ im Flags-Eintrag andere Attribute festgelegt, und bei der Erstellung von " *jtributes* " würde " **IFilter** " nur Blöcke mit einer PID von ausgeben, `0x13` die dem PID- \_ STG- \_ Inhalt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="22602-292">For example, if neither IFILTER\_INIT\_APPLY\_INDEX\_ATTRIBUTES nor IFILTER\_INIT\_APPLY\_OTHER\_ATTRIBUTES were specified in the Flags entry and if *cAttributes* were 0, then **IFilter** would emit only chunks with a PID of `0x13` and corresponding to PID\_STG\_CONTENTS.</span></span>

### <a name="sample-dump-file"></a><span data-ttu-id="22602-293">Beispiel Dumpdatei</span><span class="sxs-lookup"><span data-stu-id="22602-293">Sample Dump File</span></span>

<span data-ttu-id="22602-294">Bei der Anforderung kann das Ifilttst.exe Programm einen Dump mit den gefundenen Segmenten und deren Inhalt liefern.</span><span class="sxs-lookup"><span data-stu-id="22602-294">Upon request, the Ifilttst.exe program can produce a dump containing the chunks it finds and their content.</span></span> <span data-ttu-id="22602-295">Das folgende Beispiel ist ein Auszug aus einer solchen Dumpdatei.</span><span class="sxs-lookup"><span data-stu-id="22602-295">The following example is an excerpt from such a dump file.</span></span>

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

<span data-ttu-id="22602-296">In den ersten neun Zeilen wird die aktuelle Blockstruktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="22602-296">The first nine lines describe the current chunk structure.</span></span> <span data-ttu-id="22602-297">Die GUID und die PID entsprechen dem psguid \_ Storage/PID- \_ STG- \_ Inhalt.</span><span class="sxs-lookup"><span data-stu-id="22602-297">The GUID and the PID correspond to PSGUID\_STORAGE / PID\_STG\_CONTENTS.</span></span> <span data-ttu-id="22602-298">Dabei handelt es sich um einen Block, der Klartext enthält.</span><span class="sxs-lookup"><span data-stu-id="22602-298">This is a chunk containing plain text.</span></span> <span data-ttu-id="22602-299">Der Text befindet sich in der folgenden Blockstruktur:</span><span class="sxs-lookup"><span data-stu-id="22602-299">The text is in the following chunk structure:</span></span>

```
10. This is an HTML IFilter test page
```

<span data-ttu-id="22602-300">Der nächste Block, beginnend bei Zeile 11, verfügt über eine andere GUID, die der entspricht, `HTML IFilter` und eine andere PID, die einem HTML-href entspricht.</span><span class="sxs-lookup"><span data-stu-id="22602-300">The next chunk, starting at line 11, has a different GUID, corresponding to the `HTML IFilter`, and a different PID, corresponding to an HTML HREF.</span></span> <span data-ttu-id="22602-301">Dies ist eine interne Werttyp Eigenschaft, die von exportiert wird `HTML IFilter` .</span><span class="sxs-lookup"><span data-stu-id="22602-301">This is an internal value-type property, exported by the `HTML IFilter`.</span></span>

<span data-ttu-id="22602-302">Der nächste Block, beginnend bei Zeile 21, verfügt über die gleiche GUID und PID, aber der Segment Zustand ist `VALUE` anstelle von `TEXT` .</span><span class="sxs-lookup"><span data-stu-id="22602-302">The next chunk, starting at line 21, has the same GUID and PID, but its chunk state is `VALUE` instead of `TEXT`.</span></span> <span data-ttu-id="22602-303">Beachten Sie, dass der Text in den letzten beiden Blöcken mit dem des ersten Blocks identisch ist.</span><span class="sxs-lookup"><span data-stu-id="22602-303">Note that the text in these last two chunks is the same as for the first chunk.</span></span> <span data-ttu-id="22602-304">Da der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) für drei Attribute (nur-Text, HTML-href als Text und HTML href als Wert) entwickelt wurde, die auf diesen Ausdruck angewendet werden, werden die Ergebnisse in drei separaten Blöcken ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="22602-304">But because the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is designed for three attributes (plain text, HTML HREF as text, and HTML HREF as a value) to be applied to this phrase, the results are emitted in three separate chunks.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22602-305">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="22602-305">Additional Resources</span></span>

- <span data-ttu-id="22602-306">Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="22602-306">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="22602-307">Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="22602-307">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="22602-308">Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="22602-308">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="22602-309">Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".</span><span class="sxs-lookup"><span data-stu-id="22602-309">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="22602-310">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22602-310">Related topics</span></span>

[<span data-ttu-id="22602-311">Entwickeln von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="22602-311">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="22602-312">Informationen zu Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="22602-312">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="22602-313">Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="22602-313">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="22602-314">Zurückgeben von Eigenschaften aus einem Filter Handler</span><span class="sxs-lookup"><span data-stu-id="22602-314">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="22602-315">Filtern von Handlern, die mit Windows ausgeliefert werden</span><span class="sxs-lookup"><span data-stu-id="22602-315">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="22602-316">Implementieren von Filter Handlern in Windows Search</span><span class="sxs-lookup"><span data-stu-id="22602-316">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="22602-317">Registrieren von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="22602-317">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
