---
description: In diesem Thema werden zwei Hilfsprogramme zum Erstellen von MUI-Anwendungen beschrieben.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Ressourcen Hilfsprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960354"
---
# <a name="resource-utilities"></a><span data-ttu-id="96245-103">Ressourcen Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="96245-103">Resource Utilities</span></span>

<span data-ttu-id="96245-104">In diesem Thema werden zwei Hilfsprogramme zum Erstellen von MUI-Anwendungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="96245-104">This topic describes two utilities used to build MUI applications.</span></span> <span data-ttu-id="96245-105">Obwohl MUI ein MUI-spezifisches Tool ist, nutzt MUI auch das standardmäßige Windows RC-Compilerdienstprogramm.</span><span class="sxs-lookup"><span data-stu-id="96245-105">While MUIRCT is a MUI-specific tool, MUI also makes use of the standard Windows RC Compiler utility.</span></span> <span data-ttu-id="96245-106">Anweisungen zum Verwenden dieser Hilfsprogramme finden Sie unter [Lokalisieren von Ressourcen und entwickeln der Anwendung](localizing-resources-and-building-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="96245-106">Instructions for using these utilities are provided in [Localizing Resources and Building the Application](localizing-resources-and-building-the-application.md).</span></span>

## <a name="muirct-utility"></a><span data-ttu-id="96245-107">Muject-Hilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="96245-107">MUIRCT Utility</span></span>

<span data-ttu-id="96245-108">Muunct (Muirct.exe) ist ein Befehlszeilenprogramm zum Aufteilen einer standardmäßigen ausführbaren Datei in eine ln-Datei und sprachspezifische (lokalisierbare) Ressourcen Dateien.</span><span class="sxs-lookup"><span data-stu-id="96245-108">MUIRCT (Muirct.exe) is a command line utility for splitting a standard executable file into an LN file and language-specific (that is, localizable) resource files.</span></span> <span data-ttu-id="96245-109">Jede der resultierenden Dateien enthält Ressourcen Konfigurationsdaten für die Datei Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="96245-109">Each of the resulting files contains resource configuration data for file association.</span></span> <span data-ttu-id="96245-110">Muunct ist im Microsoft Windows SDK für Windows Vista enthalten.</span><span class="sxs-lookup"><span data-stu-id="96245-110">MUIRCT is included in the Microsoft Windows SDK for Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="96245-111">Ab Windows Vista wird das Win32-Ressourcen Lade Modul aktualisiert, um Ressourcen aus sprachspezifischen Dateien und aus LN-Dateien zu laden.</span><span class="sxs-lookup"><span data-stu-id="96245-111">Starting with Windows Vista, the Win32 resource loader is updated to load resources from language-specific files as well as from LN files.</span></span>

 

### <a name="muirct-usages"></a><span data-ttu-id="96245-112">Mumuct-Verwendungen</span><span class="sxs-lookup"><span data-stu-id="96245-112">MUIRCT Usages</span></span>

1.  <span data-ttu-id="96245-113">Binäre Binärdatei und MUI-Datei auf Grundlage der RC- \_ Konfigurationsdatei aufteilen.</span><span class="sxs-lookup"><span data-stu-id="96245-113">Split binary into main binary and mui file based on rc\_config file.</span></span>

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  <span data-ttu-id="96245-114">Extrahieren Sie Prüfsumme aus der Prüfsummen \_ Datei, und fügen Sie Sie in die Ausgabe \_ Datei ein.</span><span class="sxs-lookup"><span data-stu-id="96245-114">Extract checksum from checksum\_file and insert it in output\_file.</span></span>

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  <span data-ttu-id="96245-115">Berechnen Sie die Prüfsumme basierend auf der Prüfsummen \_ Datei, und fügen Sie Sie in die Ausgabe \_ Datei ein.</span><span class="sxs-lookup"><span data-stu-id="96245-115">Calculate checksum based on checksum\_file and insert it in output\_file.</span></span>

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  <span data-ttu-id="96245-116">Speichern Sie den Inhalt der Ressourcen Konfigurationsdaten aus der Eingabe \_ Datei.</span><span class="sxs-lookup"><span data-stu-id="96245-116">Dump resource configuration data contents from input\_file.</span></span>

    `Muirct -d input_file`

### <a name="muirct-syntax"></a><span data-ttu-id="96245-117">Mumuct-Syntax</span><span class="sxs-lookup"><span data-stu-id="96245-117">MUIRCT Syntax</span></span>

<span data-ttu-id="96245-118">Mumuct kann die Richtung von Befehls zeilenschaltern und/oder aus einer Ressourcen Konfigurationsdatei annehmen, die mithilfe des Schalters "-q" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="96245-118">MUIRCT can take direction from command line switches and/or from a resource configuration file, specified using the -q switch.</span></span>


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



<span data-ttu-id="96245-119">**Switches und Argumente**</span><span class="sxs-lookup"><span data-stu-id="96245-119">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96245-120">-h |-?</span><span class="sxs-lookup"><span data-stu-id="96245-120">-h|-?</span></span></td>
<td><span data-ttu-id="96245-121">Zeigt den Hilfe Bildschirm an.</span><span class="sxs-lookup"><span data-stu-id="96245-121">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-122">-c</span><span class="sxs-lookup"><span data-stu-id="96245-122">-c</span></span></td>
<td><span data-ttu-id="96245-123">Gibt die Eingabe checksum_file an, aus der die Ressourcen Prüfsumme extrahiert oder berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96245-123">Specifies the input checksum_file from which to extract or calculate the resource checksum.</span></span> <span data-ttu-id="96245-124">Checksum_file muss eine Win32-Binärdatei sein, die lokalisierbare Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="96245-124">Checksum_file must be a Win32 binary file containing localizable resources.</span></span> <span data-ttu-id="96245-125">Wenn checksum_file Ressourcen für mehr als eine Sprache enthält, muss der Schalter-b verwendet werden, um anzugeben, welche dieser verwendet werden soll, andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="96245-125">If checksum_file contains resources for more than one language, the -b switch must be used to specify which of these should be used otherwise MUIRCT fails.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-126">-b</span><span class="sxs-lookup"><span data-stu-id="96245-126">-b</span></span></td>
<td><span data-ttu-id="96245-127">Gibt die Sprache an, die verwendet werden soll, wenn die mit-c angegebene checksum_file Ressourcen in mehreren Sprachen enthält.</span><span class="sxs-lookup"><span data-stu-id="96245-127">Specifies the language to be used when the checksum_file specified with -c contains resources in multiple languages.</span></span> <span data-ttu-id="96245-128">Dieser Switch kann nur in Verbindung mit dem Schalter-c verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96245-128">This switch can only be used in conjunction with the -c switch.</span></span> <span data-ttu-id="96245-129">Der sprach Bezeichner kann im Dezimal-oder Hexadezimal Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="96245-129">The language identifier can be in decimal or hexadecimal format.</span></span> <span data-ttu-id="96245-130">Muunct schlägt fehl, wenn die checksum_file Ressourcen in mehreren Sprachen enthält und-b nicht angegeben ist oder wenn die durch den Schalter-b angegebene Sprache im checksum_file nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="96245-130">MUIRCT fails if the checksum_file contains resources in multiple language and the -b is not specified or if the language specified by the -b switch cannot be found in the checksum_file.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-131">-g</span><span class="sxs-lookup"><span data-stu-id="96245-131">-g</span></span></td>
<td><span data-ttu-id="96245-132">Gibt die Sprach-ID an, die als ultimative Fall Back Sprache im Abschnitt mit den Ressourcen Konfigurationsdaten der LN-Datei enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="96245-132">Specifies the language ID to be included as the ultimate fallback language in the resource configuration data section of the LN file.</span></span> <span data-ttu-id="96245-133">Wenn das Ressourcen Lade Modul eine angeforderte MUI-Datei nicht von den bevorzugten Benutzeroberflächen Sprachen des Threads lädt, wird als letzter Versuch die endgültige Fall Back Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="96245-133">If the resource loader fails to load a requested .mui file from the thread preferred UI languages, it uses the ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="96245-134">Der langid-Wert kann im Dezimal-oder Hexadezimal Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="96245-134">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="96245-135">Beispielsweise kann Englisch (USA) durch-g 0x409 oder-g 1033 angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="96245-135">For example English (United States) can be specified by -g 0x409 or -g 1033.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-136">-q</span><span class="sxs-lookup"><span data-stu-id="96245-136">-q</span></span></td>
<td><span data-ttu-id="96245-137">Gibt an, dass die source_file in den output_LN_file und die output_MUI_file entsprechend dem Layout der rc_config Datei aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="96245-137">Specifies that the source_file is to be split into the output_LN_file and the output_MUI_file according to the rc_config file layout.</span></span> <span data-ttu-id="96245-138">Bei der rc_config-Datei handelt es sich um eine XML-formatierte Datei, die angibt, welche Ressourcen in die MUI-Datei extrahiert werden und in der LN-Datei verbleiben.</span><span class="sxs-lookup"><span data-stu-id="96245-138">The rc_config file is an XML formatted file that specifies which resources will be extracted to the .mui file and which will be left in the LN file.</span></span> <span data-ttu-id="96245-139">Der rc_config kann die Verteilung von Ressourcentypen und einzelnen benannten Elementen zwischen dem output_LN_file und output_MUI_file angeben.</span><span class="sxs-lookup"><span data-stu-id="96245-139">The rc_config can specify the distribution of resource types and individual named items between the output_LN_file and output_MUI_file.</span></span> <span data-ttu-id="96245-140">Der source_file muss eine Win32-Binärdatei sein, die Ressourcen in einer einzelnen Sprache enthält, andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="96245-140">The source_file must be a Win32 binary that contains resources in a single language otherwise MUIRCT fails.</span></span> <span data-ttu-id="96245-141">Muunct teilt die Datei nicht, wenn Sie sprachneutral ist. Dies wird durch den Sprach-ID-Wert 0 in der Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="96245-141">MUIRCT does not split the file if it is language neutral which is indicated by having only language ID value 0 in the file.</span></span> <span data-ttu-id="96245-142">Bei den output_LN_file und output_mui_file handelt es sich um die Namen der sprach neutralen Datei und der MUI-Datei, in die der source_file aufgeteilt ist.</span><span class="sxs-lookup"><span data-stu-id="96245-142">The output_LN_file and output_mui_file are the names of the language neutral and .mui file into which the source_file is split.</span></span> <span data-ttu-id="96245-143">Diese Dateinamen sind optional.</span><span class="sxs-lookup"><span data-stu-id="96245-143">These file names are optional.</span></span> <span data-ttu-id="96245-144">Wenn Sie nicht angegeben werden, fügt muunct die Erweiterungen. ln und. MUI an source_file an.</span><span class="sxs-lookup"><span data-stu-id="96245-144">If they are not specified, MUIRCT appends the extensions .ln and .mui to source_file.</span></span> <span data-ttu-id="96245-145">Normalerweise sollten Sie die &quot; Erweiterung ". ln" entfernen, &quot; bevor Sie die Datei bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="96245-145">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span> <span data-ttu-id="96245-146">Muunct verknüpft die output_LN_file und output_MUI_file, indem eine Prüfsumme basierend auf dem source_file Namen und der Dateiversion berechnet und das Ergebnis in den Ressourcen Konfigurations Abschnitt jeder Ausgabedatei eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="96245-146">MUIRCT associates the output_LN_file and output_MUI_file by calculating a checksum based on the source_file name and file version and inserting the result into the resource configuration section of each output file.</span></span> <span data-ttu-id="96245-147">Bei Verwendung in Verbindung mit dem Schalter-c hat der Schalter-q Vorrang.</span><span class="sxs-lookup"><span data-stu-id="96245-147">When used in conjunction with the -c switch, the -q switch takes precedence.</span></span> <span data-ttu-id="96245-148">Wenn die mit dem Schalter-q bereitgestellte rc_config Datei eine Prüfsumme enthält, ignoriert den Schalter-c und fügt den Prüfsummen Wert aus dem Wert rc_config Datei in die LN-und MUI-Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="96245-148">If the rc_config file supplied with the -q switch contains a checksum MUIRCT ignores the -c switch and inserts the checksum value from the value, rc_config file into the LN and.mui files.</span></span> <span data-ttu-id="96245-149">Wenn im rc_config kein Prüfsummen Wert gefunden wird, berechnet muunct die Ressourcen Prüfsumme basierend auf dem Verhalten des Schalters-c.</span><span class="sxs-lookup"><span data-stu-id="96245-149">If no checksum value is found in the rc_config, MUIRCT calculates the resource checksum based on the behavior of the -c switch.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-150">-v</span><span class="sxs-lookup"><span data-stu-id="96245-150">-v</span></span></td>
<td><span data-ttu-id="96245-151">Gibt die Ebene der Ausführlichkeit für die Protokollierung an.</span><span class="sxs-lookup"><span data-stu-id="96245-151">Specifies the level of verboseness for logging.</span></span> <span data-ttu-id="96245-152">Geben Sie 1 an, um alle grundlegenden Fehlermeldungen und Vorgangs Ergebnisse zu drucken.</span><span class="sxs-lookup"><span data-stu-id="96245-152">Specify 1 to print all basic error messages and operation results.</span></span> <span data-ttu-id="96245-153">Geben Sie 2 an, um auch die in der MUI-Datei und der LN-Datei enthaltenen Ressourcen Informationen (Typ, Name, sprach Bezeichner) einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="96245-153">Specify 2 to also include the resource information (type, name, language identifier) included in the .mui file and LN file.</span></span> <span data-ttu-id="96245-154">Der Standardwert ist-v 1.</span><span class="sxs-lookup"><span data-stu-id="96245-154">The default is -v 1</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-155">-X</span><span class="sxs-lookup"><span data-stu-id="96245-155">-x</span></span></td>
<td><span data-ttu-id="96245-156">Gibt die Sprachen-ID an, mit der muunct alle Ressourcentypen markiert, die dem Ressourcenabschnitt der MUI-Datei hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="96245-156">Specifies the language ID with which MUIRCT marks all resource types added to the resource section of the .mui file.</span></span> <span data-ttu-id="96245-157">Der langid-Wert kann im Dezimal-oder Hexadezimal Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="96245-157">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="96245-158">Beispielsweise kann Englisch (USA) durch-x 0x409 oder-x 1033 angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="96245-158">For example English (United States) can be specified by -x 0x409 or -x 1033.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-159">-E</span><span class="sxs-lookup"><span data-stu-id="96245-159">-e</span></span></td>
<td><span data-ttu-id="96245-160">Extrahiert die Ressourcen Prüf Summe aus dem-checksum_file, die mit dem Schalter "-c" bereitgestellt wird, und fügt Sie in die angegebene output_file ein.</span><span class="sxs-lookup"><span data-stu-id="96245-160">Extracts the resource checksum contained in the checksum_file provided with the -c switch and inserts it in the specified output_file.</span></span> <span data-ttu-id="96245-161">Wenn-e angegeben ist, ignoriert muunct alle Switches außer dem Schalter-c.</span><span class="sxs-lookup"><span data-stu-id="96245-161">When -e is specified, MUIRCT ignores all switches other than the -c switch.</span></span> <span data-ttu-id="96245-162">In diesem Fall muss die checksum_file eine Win32-Binärdatei sein, die einen Ressourcen Konfigurationsdaten Abschnitt mit einem Prüfsummen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="96245-162">In this case the checksum_file must be a Win32 binary file that contains a resource configuration data section with a checksum value.</span></span> <span data-ttu-id="96245-163">Der output_file muss eine vorhandene LN-Datei oder MUI-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="96245-163">The output_file must be an existing LN file or .mui file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-164">-Z</span><span class="sxs-lookup"><span data-stu-id="96245-164">-z</span></span></td>
<td><span data-ttu-id="96245-165">Berechnet und fügt Ressourcen Prüfsummen Daten in die angegebene Ausgabedatei ein.</span><span class="sxs-lookup"><span data-stu-id="96245-165">Calculates and inserts resource checksum data in the specified output file.</span></span> <span data-ttu-id="96245-166">Mumuct-Prüfsummenberechnung für die Eingabe, die mit dem Schalter "-c" bereitgestellt wird, und optional-b-Schalter.</span><span class="sxs-lookup"><span data-stu-id="96245-166">MUIRCT bases checksum calculation on the input provided with the -c switch, and the optional -b switch.</span></span> <span data-ttu-id="96245-167">Wenn Sie eine Ausgabedatei für den nicht vorhandenen-z-Schalter angeben, wird muunct mit einem Fehler beendet.</span><span class="sxs-lookup"><span data-stu-id="96245-167">If you specify an output file for the -z switch that does not exist, MUIRCT exits with a failure.</span></span><br/> <span data-ttu-id="96245-168">Beispiel: berechnet die Prüfsumme auf der Grundlage Lokalisier barer Ressourcen in Notepad.exe und fügt die Prüfsumme in die Ausgabedatei Notepad2.exe ein.</span><span class="sxs-lookup"><span data-stu-id="96245-168">Example: Calculates the checksum based on localizable resources in Notepad.exe and inserts the checksum into the output file Notepad2.exe.</span></span><br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-169">-f</span><span class="sxs-lookup"><span data-stu-id="96245-169">-f</span></span></td>
<td><span data-ttu-id="96245-170">Ermöglicht das Erstellen einer MUI-Datei, wobei die Versions Ressource die einzige lokalisierbare Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="96245-170">Enables creating a .mui file with the version resource being the only localizable resource.</span></span> <span data-ttu-id="96245-171">Standardmäßig ist dies nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="96245-171">By default, MUIRCT does not allow this.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-172">-d</span><span class="sxs-lookup"><span data-stu-id="96245-172">-d</span></span></td>
<td><span data-ttu-id="96245-173">Hiermit werden eingebettete Ressourcen Konfigurationsdaten in der Quelldatei angezeigt und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96245-173">Locates and displays embedded resource configuration data in the source file.</span></span> <span data-ttu-id="96245-174">Wenn Sie diesen Schalter angeben, ignoriert muunct alle anderen Befehlszeilenoptionen.</span><span class="sxs-lookup"><span data-stu-id="96245-174">When you specify this switch, MUIRCT ignores all other command line options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-175">-M</span><span class="sxs-lookup"><span data-stu-id="96245-175">-m</span></span></td>
<td><span data-ttu-id="96245-176">Gibt die Versionsnummer an, die beim Berechnen der Prüfsumme zum Zuordnen der output_LN_file und output_MUI_file verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96245-176">Specifies the version number to use when calculating the checksum for associating the output_LN_file and output_MUI_file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-177">source_filename</span><span class="sxs-lookup"><span data-stu-id="96245-177">source_filename</span></span></td>
<td><span data-ttu-id="96245-178">Der Name der lokalisierten binären Quelldatei. Platzhalter können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96245-178">Name of the localized binary source file; wildcards cannot be used.</span></span> <span data-ttu-id="96245-179">Diese Datei kann nur Ressourcen in einer Sprache enthalten.</span><span class="sxs-lookup"><span data-stu-id="96245-179">This file can only contain resources in one language.</span></span> <span data-ttu-id="96245-180">Wenn sich in der Datei Ressourcen in mehreren Sprachen befinden, schlägt muunct fehl, es sei denn, der Schalter "-b" wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="96245-180">If there are resources in multiple languages in the file, MUIRCT fails, unless the -b switch is used.</span></span> <span data-ttu-id="96245-181">Wenn die Datei Ressourcen mit sprach Bezeichnern enthält, die nur den Wert 0 haben, teilt muunct die Datei nicht, da eine Sprach-ID von 0 eine neutrale Sprache angibt.</span><span class="sxs-lookup"><span data-stu-id="96245-181">If the file contains resources with language identifiers having value 0 only, MUIRCT does not split the file because a language identifier of 0 indicates a neutral language.</span></span><br/> <span data-ttu-id="96245-182">Für den Schalter "-d" ist source_filename entweder eine ln-Datei oder eine sprachspezifische Ressourcen Datei, für die die Daten der Ressourcen Konfiguration angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="96245-182">For the -d switch, source_filename is either an LN file or a language-specific resource file for which MUIRCT is to display resource configuration data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-183">language_neutral_filename</span><span class="sxs-lookup"><span data-stu-id="96245-183">language_neutral_filename</span></span></td>
<td><span data-ttu-id="96245-184">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="96245-184">Optional.</span></span> <span data-ttu-id="96245-185">Name der LN-Datei.</span><span class="sxs-lookup"><span data-stu-id="96245-185">Name of LN file.</span></span> <span data-ttu-id="96245-186">Wenn Sie den Namen dieser Datei nicht angeben, fügt muunct eine zweite Erweiterung &quot; . ln &quot; an den Quell Dateinamen an, der als sprach neutraler Dateiname verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96245-186">If you do not specify the name of this file, MUIRCT appends a second extension &quot;.ln&quot; to the source file name to use as the language-neutral file name.</span></span> <span data-ttu-id="96245-187">Normalerweise sollten Sie die &quot; Erweiterung ". ln" entfernen, &quot; bevor Sie die Datei bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="96245-187">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="96245-188">Die LN-Datei darf keine Zeichen folgen oder Menüs enthalten.</span><span class="sxs-lookup"><span data-stu-id="96245-188">The LN file should not contain strings or menus.</span></span> <span data-ttu-id="96245-189">Sie sollten Sie manuell entfernen.</span><span class="sxs-lookup"><span data-stu-id="96245-189">You should remove them manually.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-190">mui_filename</span><span class="sxs-lookup"><span data-stu-id="96245-190">mui_filename</span></span></td>
<td><span data-ttu-id="96245-191">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="96245-191">Optional.</span></span> <span data-ttu-id="96245-192">Name der sprachspezifischen Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="96245-192">Name of language-specific resource file.</span></span> <span data-ttu-id="96245-193">Wenn Sie keinen Namen angeben, fügt muunct eine zweite Erweiterung &quot; . MUI &quot; an den Quell Dateinamen an, der als Dateiname verwendet werden soll. Normalerweise erstellt muunct eine sprachspezifische Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="96245-193">If you do not specify a name, MUIRCT appends a second extension &quot;.mui&quot; to the source file name to use as the file name.Normally, MUIRCT creates a language-specific resource file.</span></span> <span data-ttu-id="96245-194">Es wird jedoch keine Ressourcen Datei erstellt, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="96245-194">However, it does not create a resource file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="96245-195">In der ursprünglichen Binärdatei befinden sich keine lokalisierbaren Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="96245-195">No localizable resources are in the original binary file.</span></span></li>
<li><span data-ttu-id="96245-196">Die einzige in der ursprünglichen Binärdatei gefundene Ressourcen Sprache ist die neutrale Sprache.</span><span class="sxs-lookup"><span data-stu-id="96245-196">The only resource language found in the original binary file is the neutral language.</span></span></li>
<li><span data-ttu-id="96245-197">Die ursprüngliche Binärdatei enthält Ressourcen für mehr als eine Sprache, ohne die neutrale Sprache zu zählen.</span><span class="sxs-lookup"><span data-stu-id="96245-197">The original binary file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="96245-198">Wenn die Binärdatei Ressourcen für zwei Sprachen enthält und eine von Ihnen die neutrale Sprache ist, wird die Datei vom Hilfsprogramm als monolingual betrachtet und eine sprachspezifische Ressourcen Datei erstellt, wenn lokalisierbare Ressourcen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="96245-198">If the binary file contains resources for two languages, and one of them is the neutral language, the utility considers the file to be monolingual and creates a language-specific resource file if there are localizable resources.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a><span data-ttu-id="96245-199">Muout-Sprachausgabe</span><span class="sxs-lookup"><span data-stu-id="96245-199">MUIRCT Language Output</span></span>

<span data-ttu-id="96245-200">Muunct wählt den Wert des Attributs "ultimatefallbacklanguage" aus, der auf der Grundlage der folgenden Reihenfolge in die Konfigurationsdaten der LN-Datei Ressource eingefügt werden soll, von der höchsten Priorität bis zum niedrigsten:</span><span class="sxs-lookup"><span data-stu-id="96245-200">MUIRCT chooses the "UltimateFallbackLanguage" attribute value to insert in the LN file resource configuration data based on the following order, from highest priority to lowest:</span></span>

1.  <span data-ttu-id="96245-201">"Ultimatefallbacklanguage"-Attribut in der Quell Ressourcen-Konfigurationsdatei, wenn eine Eingabe als Eingabe übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="96245-201">"UltimateFallbackLanguage" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="96245-202">Die mit dem Schalter "-g" angegebene Sprache.</span><span class="sxs-lookup"><span data-stu-id="96245-202">The language specified with the -g switch.</span></span>
3.  <span data-ttu-id="96245-203">Sprache der Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="96245-203">Input file language.</span></span>

<span data-ttu-id="96245-204">Muzict wählt den "language"-Attribut Wert aus, der auf der Grundlage der folgenden Reihenfolge in die MUI-Datei Ressourcen-Konfigurationsdaten eingefügt werden soll:</span><span class="sxs-lookup"><span data-stu-id="96245-204">MUIRCT picks the "language" attribute value to insert in the .mui file resource configuration data based on the following order:</span></span>

1.  <span data-ttu-id="96245-205">"language"-Attribut in der Quell Ressourcen-Konfigurationsdatei, wenn eine Eingabe als Eingabe erfolgt.</span><span class="sxs-lookup"><span data-stu-id="96245-205">"language" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="96245-206">Die durch den Schalter-x angegebene Sprache (Force Language).</span><span class="sxs-lookup"><span data-stu-id="96245-206">The language specified by the -x switch (force language).</span></span>
3.  <span data-ttu-id="96245-207">Sprache der Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="96245-207">Input file language.</span></span>

### <a name="muirct-checksum-handling"></a><span data-ttu-id="96245-208">Verarbeitung von Mudo-Prüfsummen</span><span class="sxs-lookup"><span data-stu-id="96245-208">MUIRCT Checksum Handling</span></span>

<span data-ttu-id="96245-209">Das Betriebssystem berechnet die Prüfsumme normalerweise über die sprachspezifischen Ressourcen in einer Datei, es sei denn, Sie geben die Prüfsumme über eine Ressourcen Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="96245-209">The operating system normally calculates the checksum over the language-specific resources in a file unless you specify the checksum through a resource configuration file.</span></span> <span data-ttu-id="96245-210">Solange die Prüfsumme für die LN-Datei und alle zugeordneten sprachspezifischen Ressourcen Dateien und das Language-Attribut in der Ressourcen Konfiguration in den LN und der sprach abhängigen Übereinstimmung identisch ist, kann das Ressourcen Lade Modul Ressourcen erfolgreich laden.</span><span class="sxs-lookup"><span data-stu-id="96245-210">As long as the checksum is the same for the LN file and all associated language-specific resource files, and the language attribute in the resource configuration in the LN and language dependent match, the resource loader can successfully load resources.</span></span>

<span data-ttu-id="96245-211">Muunct unterstützt mehrere Methoden zum Platzieren geeigneter Prüfsummen in den Ressourcen Konfigurationsdaten:</span><span class="sxs-lookup"><span data-stu-id="96245-211">MUIRCT supports several methods for placing appropriate checksums in the resource configuration data:</span></span>

1.  <span data-ttu-id="96245-212">Erstellen Sie eine ausführbare Datei für jede Sprache, die sowohl Code als auch Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="96245-212">Build an executable for each language, containing both code and resources.</span></span> <span data-ttu-id="96245-213">Verwenden Sie anschließend muunct, um jede dieser Dateien in eine ln-Datei und eine sprachspezifische Ressourcen Datei aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="96245-213">After this, use MUIRCT to split each of these files into an LN file and a language-specific resource file.</span></span> <span data-ttu-id="96245-214">Muunct wird mehrmals ausgeführt, um eine Ressourcen Datei für jede Sprache zu generieren.</span><span class="sxs-lookup"><span data-stu-id="96245-214">MUIRCT runs multiple times, once to generate a resource file for each language.</span></span> <span data-ttu-id="96245-215">Sie können den Build wie folgt ausführen:</span><span class="sxs-lookup"><span data-stu-id="96245-215">You can perform the build in the following ways:</span></span>
    1.  <span data-ttu-id="96245-216">Verwenden Sie den Schalter-q, um einen Prüfsummen Wert in der Ressourcen Konfigurationsdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="96245-216">Use the -q switch to specify a checksum value in the resource configuration file.</span></span> <span data-ttu-id="96245-217">Diese Werte werden in alle LN-Dateien und sprachspezifischen Ressourcen Dateien eingefügt, die erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="96245-217">MUIRCT places this value in all the LN files and language-specific resource files produced.</span></span> <span data-ttu-id="96245-218">Sie müssen eine Strategie zum Auswählen dieses Werts anwenden, wie weiter unten in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="96245-218">You need to adopt a strategy for choosing this value, as described later in this topic.</span></span>
    2.  <span data-ttu-id="96245-219">Verwenden Sie den Schalter-c (und optional auch den Schalter-b), um eine einzelne Sprache mit Ressourcen auszuwählen, von denen muunct die Prüfsumme extrahiert.</span><span class="sxs-lookup"><span data-stu-id="96245-219">Use the -c switch (and, optionally, the -b switch) to choose a single language having resources from which MUIRCT extracts the checksum.</span></span>
    3.  <span data-ttu-id="96245-220">Verwenden Sie den Schalter-z, um eine einzelne Sprache mit Ressourcen auszuwählen, von denen die Prüfsumme immer extrahiert wird.</span><span class="sxs-lookup"><span data-stu-id="96245-220">Use the -z switch to choose a single language having resources from which MUIRCT always extracts the checksum.</span></span> <span data-ttu-id="96245-221">Wenden Sie diese Prüfsumme an, nachdem die Dateien mit anderen Methoden erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="96245-221">Apply this checksum after the files have been built using other methods.</span></span>
2.  <span data-ttu-id="96245-222">Erstellen Sie eine ausführbare Datei, die sowohl Code als auch Ressourcen für eine einzelne Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="96245-222">Build an executable containing both code and resources for a single language.</span></span> <span data-ttu-id="96245-223">Verwenden Sie danach muunct, um die Ressourcen zwischen der LN-Datei und der sprachspezifischen Ressourcen Datei aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="96245-223">After this, use MUIRCT to split the resources between the LN file and the language-specific resource file.</span></span> <span data-ttu-id="96245-224">Verwenden Sie abschließend ein binäres Lokalisierungs Tool, um die sich ergebende Ressourcen Datei für jede Sprache zu ändern.</span><span class="sxs-lookup"><span data-stu-id="96245-224">Finally, use a binary localization tool to modify the resulting resource file for each language.</span></span>

<span data-ttu-id="96245-225">Die häufigste Konvention für die Prüfsummen Behandlung besteht darin, die Prüfsumme auf den englischen Ressourcen (USA) zu basieren.</span><span class="sxs-lookup"><span data-stu-id="96245-225">The most common convention for checksum handling is to base the checksum on the English (United States) resources.</span></span> <span data-ttu-id="96245-226">Sie können eine andere Konvention anwenden, solange Sie für jede LN-Datei konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="96245-226">You are free to adopt a different convention, as long as it is consistent for each LN file.</span></span> <span data-ttu-id="96245-227">Beispielsweise ist es für ein Unternehmen der Softwareentwicklung durchaus akzeptabel, dass die Prüfsummen in der Software basieren, die auf französischen Ressourcen (Frankreich) statt auf englischen (USA) Ressourcen aufbaut, solange alle Anwendungen über französische Ressourcen (Frankreich) verfügen, auf denen die Prüfsummen basieren.</span><span class="sxs-lookup"><span data-stu-id="96245-227">For example, it is perfectly acceptable for a software development enterprise to base its checksums in the software it builds on French (France) resources instead of English (United States) resources, as long as all the applications have French (France) resources on which to base the checksums.</span></span> <span data-ttu-id="96245-228">Es ist auch zulässig, die Ressourcen Konfigurationsdatei zu verwenden, um einen beliebigen hexadezimalen Wert von bis zu 16 hexadezimal Ziffern als Prüfsumme zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="96245-228">It is also acceptable to use the resource configuration file to assign an arbitrary hexadecimal value of up to 16 hexadecimal digits as a checksum.</span></span> <span data-ttu-id="96245-229">Diese letzte Strategie verhindert die effektive Verwendung der Schalter "-z", "-c" und "-b" von muunct.</span><span class="sxs-lookup"><span data-stu-id="96245-229">This last strategy precludes the effective use of the -z, -c, and -b switches of MUIRCT.</span></span> <span data-ttu-id="96245-230">Hierfür ist es erforderlich, eine Methode zu verwenden, die entweder [**GUIDGEN**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) oder ein anderes Tool verwendet, um Prüfsummen Werte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="96245-230">It requires adoption of a method using either [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) or some other tool to generate checksum values.</span></span> <span data-ttu-id="96245-231">Diese Strategie erfordert auch, dass Sie eine Richtlinie einrichten, um zu bestimmen, wann der Wert beim Hinzufügen neuer Lokalisier barer Ressourcen geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="96245-231">This strategy also requires you to set up a policy for determining when to modify the value when adding new localizable resources.</span></span>

<span data-ttu-id="96245-232">Wenn Sie die englische Prüfsumme (USA) auf alle Dateien anwenden möchten, können Sie eine der oben beschriebenen Prüfsummen Behandlungsmethoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="96245-232">To apply the English (United States) checksum to all files, you can use any of the checksum handling methods described above.</span></span> <span data-ttu-id="96245-233">Sie können z. b. die Datei "ln" und die sprachspezifische Ressourcen Datei für Englisch (USA) generieren und dann mit dem Schalter "muunct-d" die resultierende Prüfsumme abrufen.</span><span class="sxs-lookup"><span data-stu-id="96245-233">For example, you can generate the LN file and language-specific resource file for English (United States), then use the MUIRCT -d switch to obtain the resulting checksum.</span></span> <span data-ttu-id="96245-234">Sie können diese Prüfsumme in ihre Ressourcen Konfigurationsdatei kopieren und den Schalter-q mit muunct verwenden, um die Prüfsumme auf alle anderen Dateien anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="96245-234">You can copy this checksum into your resource configuration file and use the -q switch with MUIRCT to apply the checksum to all other files.</span></span>

### <a name="use-of-a-resource-configuration-file-with-muirct"></a><span data-ttu-id="96245-235">Verwendung einer Ressourcen Konfigurationsdatei mit muesct</span><span class="sxs-lookup"><span data-stu-id="96245-235">Use of a Resource Configuration File with MUIRCT</span></span>

<span data-ttu-id="96245-236">Bei der Verwendung von muunct können Sie Ressourcen Konfigurationsdaten angeben.</span><span class="sxs-lookup"><span data-stu-id="96245-236">You can specify resource configuration data when using MUIRCT.</span></span> <span data-ttu-id="96245-237">Unabhängig davon, ob Sie explizit eine Ressourcen Konfigurationsdatei angeben, enthält jede sprachspezifische Ressourcen Datei Ressourcen Konfigurationsdaten, ebenso wie jede andere Datei mit einer zugeordneten Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="96245-237">Whether or not you explicitly supply a resource configuration file, every language-specific resource file has resource configuration data, as does any LN file with an associated resource file.</span></span> <span data-ttu-id="96245-238">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="96245-238">For example:</span></span>

-   <span data-ttu-id="96245-239">Wenn Sie den Schalter-q zum Angeben einer Ressourcen Konfigurationsdatei verwenden, aber keine lokalisierbaren Ressourcen in der Eingabe Quelldatei vorhanden sind, wird keine sprachspezifische Ressourcen Datei generiert, und die resultierende LN-Datei enthält keine Ressourcen Konfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="96245-239">If you use the -q switch to specify a resource configuration file, but there are no localizable resources in your input source file, no language-specific resource file is generated and the resulting LN file does not contain resource configuration data.</span></span> <span data-ttu-id="96245-240">Wenn die Eingabe Quelldatei über mehrsprachige Ressourcen verfügt, wird die Datei von muzct nicht geteilt.</span><span class="sxs-lookup"><span data-stu-id="96245-240">Also, if the input source file has multilingual resources, then MUIRCT won't split the file.</span></span>

> [!Note]  
> <span data-ttu-id="96245-241">Das Verhalten von muunct ist derzeit nicht konsistent, wenn das neutralresources-Element der Ressourcen Konfigurationsdatei keine ResourceType-Elemente enthält und das localizedresources-Element z. b. Zeichen folgen und Menüs enthält.</span><span class="sxs-lookup"><span data-stu-id="96245-241">Currently the behavior of MUIRCT is inconsistent when the neutralResources element of the resource configuration file contains no resourceType elements and the localizedResources element contains strings and menus, for example.</span></span> <span data-ttu-id="96245-242">In einem solchen Fall teilt muunct die Ressourcen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="96245-242">In such a case, MUIRCT splits the resources as follows:</span></span>
>
> -   <span data-ttu-id="96245-243">Alle Ressourcen in der ursprünglichen Binärdatei (einschließlich Zeichen folgen und Menüs) sowie die MUI-Ressourcen werden in der LN-Datei abgelegt.</span><span class="sxs-lookup"><span data-stu-id="96245-243">All resources in the original binary (including strings and menus), plus the MUI resources, are placed in the LN file.</span></span>
> -   <span data-ttu-id="96245-244">Zeichen folgen, Menüs und MUI-Ressourcen werden in die entsprechende sprachspezifische Ressourcen Datei eingefügt.</span><span class="sxs-lookup"><span data-stu-id="96245-244">Strings, menus, and MUI resources are placed in the appropriate language-specific resource file.</span></span>

 

### <a name="examples-for-using-muirct"></a><span data-ttu-id="96245-245">Beispiele für die Verwendung von muunct</span><span class="sxs-lookup"><span data-stu-id="96245-245">Examples for Using MUIRCT</span></span>

<span data-ttu-id="96245-246">**Beispiele für die Standard Verwendung**</span><span class="sxs-lookup"><span data-stu-id="96245-246">**Examples of Standard Usage**</span></span>


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



<span data-ttu-id="96245-247">**Beispiel für Ausgabe der LN-Datei mit dem Schalter "-d"**</span><span class="sxs-lookup"><span data-stu-id="96245-247">**Example of LN File Output Using -d Switch**</span></span>

<span data-ttu-id="96245-248">Im folgenden finden Sie ein Beispiel für die Ausgabe der Ressourcen Konfigurationsdaten aus einer LN-Datei Shell32.dll, wobei der Schalter-d mit muunct verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="96245-248">Here is an example of the resource configuration data output from an LN file, Shell32.dll, using the -d switch with MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



<span data-ttu-id="96245-249">**Beispiel für Language-Specific Ausgabe der Ressourcen Datei mit dem Schalter "-d"**</span><span class="sxs-lookup"><span data-stu-id="96245-249">**Example of Language-Specific Resource File Output Using -d Switch**</span></span>

<span data-ttu-id="96245-250">Im folgenden finden Sie ein Beispiel für die Ausgabe der Ressourcen Konfigurationsdaten aus einer MUI-Datei (Shell32.dll. MUI), wobei der Schalter "-d" für muunct verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="96245-250">Here is an example of the resource configuration data output from a .mui file, Shell32.dll.mui, using the -d switch for MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a><span data-ttu-id="96245-251">RC Compiler Utility</span><span class="sxs-lookup"><span data-stu-id="96245-251">RC Compiler Utility</span></span>

<span data-ttu-id="96245-252">Der RC-Compiler (Rc.exe) ist ein Befehlszeilenprogramm zum Kompilieren einer Ressourcen Definitions Skriptdatei (RC-Erweiterung) in Ressourcen Dateien (Erweiterung ". res").</span><span class="sxs-lookup"><span data-stu-id="96245-252">RC Compiler (Rc.exe) is a command line utility for compiling a resource definition script file (.rc extension) into resource files (.res extension).</span></span> <span data-ttu-id="96245-253">Der RC-Compiler ist in der Windows SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="96245-253">RC Compiler is included in the Windows SDK.</span></span> <span data-ttu-id="96245-254">In diesem Dokument wird nur die Verwendung des RC-Compilers mit MUI-bezogenen Funktionen des Ressourcen Laders erläutert.</span><span class="sxs-lookup"><span data-stu-id="96245-254">This document only explains the use of RC Compiler with MUI-related capabilities of the resource loader.</span></span> <span data-ttu-id="96245-255">Ausführliche Informationen zum Compiler finden Sie unter Informationen [zu Ressourcen Dateien](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="96245-255">For complete information about the compiler, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="96245-256">Der RC-Compiler ermöglicht das Erstellen aus einem einzelnen Satz von Quellen, einer LN-Datei und einer separaten sprachspezifischen Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="96245-256">RC Compiler allows you to build, from a single set of sources, an LN file and a separate language-specific resource file.</span></span> <span data-ttu-id="96245-257">Die Dateien werden in Bezug auf die Daten mithilfe von Ressourcen Konfigurationsdaten verknüpft.</span><span class="sxs-lookup"><span data-stu-id="96245-257">As for MUIRCT, the files are associated by resource configuration data.</span></span>

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a><span data-ttu-id="96245-258">RC-compilersyntax wie für MUI-Ressourcen verwendet</span><span class="sxs-lookup"><span data-stu-id="96245-258">RC Compiler Syntax as Used for MUI Resources</span></span>

<span data-ttu-id="96245-259">RC-Compilerschalter werden ausführlich in [mithilfe von RC](../menurc/using-rc-the-rc-command-line-.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="96245-259">RC Compiler switches are defined in detail in [Using RC](../menurc/using-rc-the-rc-command-line-.md).</span></span> <span data-ttu-id="96245-260">In diesem Abschnitt werden nur die Schalter definiert, mit denen MUI-Ressourcen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="96245-260">This section only defines the switches used to build MUI resources.</span></span> <span data-ttu-id="96245-261">Denken Sie daran, dass bei jedem Switch die Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="96245-261">Remember that each switch is case-insensitive.</span></span> <span data-ttu-id="96245-262">Es wird angenommen, dass Ressourcentypen sprachneutral sind, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="96245-262">Resource types are assumed to be language-neutral unless otherwise indicated.</span></span>


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



<span data-ttu-id="96245-263">**Switches und Argumente**</span><span class="sxs-lookup"><span data-stu-id="96245-263">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96245-264">-h |-?</span><span class="sxs-lookup"><span data-stu-id="96245-264">-h|-?</span></span></td>
<td><span data-ttu-id="96245-265">Zeigt den Hilfe Bildschirm an.</span><span class="sxs-lookup"><span data-stu-id="96245-265">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-266">-FM</span><span class="sxs-lookup"><span data-stu-id="96245-266">-fm</span></span></td>
<td><span data-ttu-id="96245-267">Verwendet die angegebene Ressourcen Datei für sprachspezifische Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="96245-267">Uses the specified resource file for language-specific resources.</span></span> <span data-ttu-id="96245-268">Normalerweise erstellt der Ressourcen Compiler eine sprachspezifische Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="96245-268">Normally the resource compiler creates a language-specific resource file.</span></span> <span data-ttu-id="96245-269">Die Datei wird jedoch nicht erstellt, wenn eine der folgenden Bedingungen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="96245-269">However, it does not create the file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="96245-270">Es sind keine lokalisierbaren Ressourcen in der RC-Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="96245-270">There are no localizable resources in the .rc file.</span></span></li>
<li><span data-ttu-id="96245-271">Die einzige in der RC-Datei gefundene Ressourcen Sprache ist die neutrale Sprache.</span><span class="sxs-lookup"><span data-stu-id="96245-271">The only resource language found in the .rc file is the neutral language.</span></span></li>
<li><span data-ttu-id="96245-272">Die RC-Datei enthält Ressourcen für mehr als eine Sprache, ohne die neutrale Sprache zu zählen.</span><span class="sxs-lookup"><span data-stu-id="96245-272">The .rc file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="96245-273">Wenn die RC-Datei Ressourcen für zwei Sprachen enthält und eine von Ihnen die neutrale Sprache ist, betrachtet der Compiler die Datei als monolingual.</span><span class="sxs-lookup"><span data-stu-id="96245-273">If the .rc file contains resources for two languages, and one of them is the neutral language, the compiler considers the file to be monolingual.</span></span> <span data-ttu-id="96245-274">Wenn lokalisierbare Ressourcen vorhanden sind, erstellt der Compiler eine sprachspezifische Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="96245-274">If there are any localizable resources, the compiler creates a language-specific resource file.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-275">-q</span><span class="sxs-lookup"><span data-stu-id="96245-275">-q</span></span></td>
<td><span data-ttu-id="96245-276">Verwendet die angegebene Ressourcen Konfigurationsdatei zum Abrufen der Ressourcentypen, die in der sprachspezifischen Ressourcen Datei und der LN-Datei platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96245-276">Uses the specified resource configuration file to obtain the resource types to place in the language-specific resource file and the LN file.</span></span> <span data-ttu-id="96245-277">Weitere Informationen finden Sie unter <a href="preparing-a-resource-configuration-file.md">Vorbereiten einer Ressourcen Konfigurationsdatei</a>.</span><span class="sxs-lookup"><span data-stu-id="96245-277">For more information, see <a href="preparing-a-resource-configuration-file.md">Preparing a Resource Configuration File</a>.</span></span> <span data-ttu-id="96245-278">Als Alternative zu diesem Switch können Sie die Schalter-j und-k verwenden, aber es wird empfohlen, eine Ressourcen Konfigurationsdatei zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="96245-278">As an alternative to this switch, you can use the -j and -k switches, but it is preferred to use a resource configuration file.</span></span> <br/> <span data-ttu-id="96245-279">Wenn Sie den Schalter-q mit einer Ressourcen Konfigurationsdatei verwenden, können Sie eine Element basierte Teilung implementieren und Attribute bereitstellen, für die die binäre Ressourcen Konfiguration in der LN-und sprachspezifischen Ressourcen Datei enden soll.</span><span class="sxs-lookup"><span data-stu-id="96245-279">By using the -q switch with a resource configuration file, you can implement an item-based split and provide attributes that will end up with the binary resource configuration in the LN and language-specific resource file.</span></span> <span data-ttu-id="96245-280">Diese Aufteilung ist mit den Switches-j und-k nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="96245-280">This split is not possible using the -j and -k switches.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="96245-281">Der RC-compilersplit-Prozess funktioniert nicht ordnungsgemäß, wenn Sie Ressourcen und Versionsinformationen in verschiedenen Ressourcen Konfigurationsdateien speichern.</span><span class="sxs-lookup"><span data-stu-id="96245-281">The RC Compiler split process does not work properly if you store resources and version information in different resource configuration files.</span></span> <span data-ttu-id="96245-282">In diesem Fall teilt der RC-Compiler die Versionsinformationen nicht.</span><span class="sxs-lookup"><span data-stu-id="96245-282">In this case, RC Compiler does not split the version information.</span></span> <span data-ttu-id="96245-283">Daher tritt beim Verknüpfen der sprachspezifischen Ressourcen Datei ein linker-Fehler auf, da die Datei nicht über Versions Ressourcen verfügt.</span><span class="sxs-lookup"><span data-stu-id="96245-283">Therefore a linker error occurs during linking of the language-specific resource file because the file does not have version resources.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-284">-g</span><span class="sxs-lookup"><span data-stu-id="96245-284">-g</span></span></td>
<td><span data-ttu-id="96245-285">Gibt die endgültige <a href="language-identifiers.md">Fall Back Sprachen</a> -ID im Hexadezimal Format an.</span><span class="sxs-lookup"><span data-stu-id="96245-285">Specifies the ultimate <a href="language-identifiers.md">fallback language</a> identifier in hexadecimal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-286">-G1</span><span class="sxs-lookup"><span data-stu-id="96245-286">-g1</span></span></td>
<td><span data-ttu-id="96245-287">Erstellt eine MUI. res-Datei, auch wenn die Versions Ressource der einzige lokalisierbare Inhalt ist.</span><span class="sxs-lookup"><span data-stu-id="96245-287">Creates a MUI .res file even if the VERSION resource is the only localizable content.</span></span> <span data-ttu-id="96245-288">Standardmäßig erzeugt der RC-Compiler keine res-Datei, wenn die Version die einzige lokalisierbare Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="96245-288">By default, RC Compiler does not produce a .res file if VERSION is the only localizable resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-289">-g2</span><span class="sxs-lookup"><span data-stu-id="96245-289">-g2</span></span></td>
<td><span data-ttu-id="96245-290">Gibt die benutzerdefinierte Versionsnummer an, die beim Berechnen der Prüfsumme verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96245-290">Specifies the custom version number to use when calculating the checksum.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-291">mui_res_name</span><span class="sxs-lookup"><span data-stu-id="96245-291">mui_res_name</span></span></td>
<td><span data-ttu-id="96245-292">Ressourcen Datei für sprachspezifische Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="96245-292">Resource file for language-specific resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-293">rc_config_file_name</span><span class="sxs-lookup"><span data-stu-id="96245-293">rc_config_file_name</span></span></td>
<td><span data-ttu-id="96245-294">Ressourcen Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="96245-294">Resource configuration file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96245-295">langid</span><span class="sxs-lookup"><span data-stu-id="96245-295">langid</span></span></td>
<td><span data-ttu-id="96245-296">Der Sprachen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="96245-296">Language identifier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96245-297">version</span><span class="sxs-lookup"><span data-stu-id="96245-297">version</span></span></td>
<td><span data-ttu-id="96245-298">Benutzerdefinierte Versionsnummer in einem Format wie z &quot; &quot; . b. 6.2.0.0.</span><span class="sxs-lookup"><span data-stu-id="96245-298">Custom version number, in a format such as &quot;6.2.0.0&quot;.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a><span data-ttu-id="96245-299">Beispiel für die Verwendung von RC-Compiler zum Erstellen von MUI-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="96245-299">Example for Using RC Compiler to Build MUI Resources</span></span>

<span data-ttu-id="96245-300">Um den RC-compilervorgang mit MUI-Ressourcen zu veranschaulichen, betrachten wir die folgende Befehlszeile für die Ressourcen Datei "MyFile. RC":</span><span class="sxs-lookup"><span data-stu-id="96245-300">To illustrate RC Compiler operation with MUI resources, let's examine the following command line, for the resource file Myfile.rc:</span></span>


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



<span data-ttu-id="96245-301">Diese Befehlszeile bewirkt, dass der RC-Compiler folgende Aktionen durchführen kann:</span><span class="sxs-lookup"><span data-stu-id="96245-301">This command line causes RC Compiler to do the following:</span></span>

-   <span data-ttu-id="96245-302">Erstellen Sie die sprachspezifische Ressourcen Datei "MyFile \_ Res. res" und eine sprachneutrale Ressourcen Datei, die standardmäßig auf "MyFile. res" basiert, basierend auf dem Namen der RC-Datei.</span><span class="sxs-lookup"><span data-stu-id="96245-302">Create the language-specific resource file Myfile\_res.res and a language-neutral resource file that defaults to Myfile.res, based on the name of the .rc file.</span></span>
-   <span data-ttu-id="96245-303">Fügen Sie die Ressourcentypen 2 (Item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 \_ Type der sprachspezifischen res-Datei hinzu, wenn Sie sich in der RC-Datei befinden.</span><span class="sxs-lookup"><span data-stu-id="96245-303">Add the 2 (item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY\_TYPE resource types to the language-specific .res file if they are in the .rc file.</span></span>
-   <span data-ttu-id="96245-304">Fügen Sie den Ressourcentyp 16 sowie alle anderen Ressourcentypen, die in der Ressourcen Datei beschrieben werden, der sprach neutralen res-Datei und der sprachspezifischen res-Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="96245-304">Add resource type 16, along with any other resource types described in the resource file to the language-neutral .res file and to the language-specific .res file.</span></span> <span data-ttu-id="96245-305">Beachten Sie, dass in diesem Beispiel der Ressourcentyp 16 an zwei Stellen hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="96245-305">Note that, in this example, resource type 16 is being added in two places.</span></span>
-   <span data-ttu-id="96245-306">Wählen Sie den Attribut Wert "ultimatefallbacklanguage" aus, der auf der Grundlage der folgenden Kriterien in die Konfigurationsdaten der LN-Datei Ressource eingefügt werden soll:</span><span class="sxs-lookup"><span data-stu-id="96245-306">Choose the "UltimateFallbackLanguage" attribute value to insert into the LN file resource configuration data based on the following criteria, ordered from highest priority to lowest:</span></span>
    -   <span data-ttu-id="96245-307">Das Attribut "ultimatefallbacklanguage" in der Ressourcen Konfigurationsdatei, wenn eines als Eingabe übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="96245-307">"UltimateFallbackLanguage" attribute in the resource configuration file if one is passed in as input.</span></span>
    -   <span data-ttu-id="96245-308">Der sprach Attribut Wert, der basierend auf der RC-compilersprachreihenfolge (sprachneutrale Sprache und sprachspezifische Ressourcen Datei Sprache) in die Ressourcen Konfigurationsdaten eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="96245-308">Language attribute value to insert in the resource configuration data based on the RC Compiler language order (language-neutral and language-specific resource file language).</span></span> <span data-ttu-id="96245-309">Zu den Überlegungen zählen die Sprache in der RC-Datei, der sprach Wert des Schalters-GL und der Bezeichner 0x0409 für Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="96245-309">Considerations include language in the .rc file, language value of the -gl switch, and identifier 0x0409 for English (United States).</span></span>

## <a name="remarks"></a><span data-ttu-id="96245-310">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96245-310">Remarks</span></span>

<span data-ttu-id="96245-311">Wenn Sie ein beliebiges Symbol (3), einen Dialog (5), einen Zeichen folgen-(6) oder einen Versions (16) Ressourcentyp im neutralresources-Element enthalten, müssen Sie diesen Eintrag im localizedresources-Element in der Ressourcen Konfigurationsdatei duplizieren.</span><span class="sxs-lookup"><span data-stu-id="96245-311">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element in the resource configuration file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96245-312">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="96245-312">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96245-313">Mehrsprachige Benutzeroberflächen Referenz</span><span class="sxs-lookup"><span data-stu-id="96245-313">Multilingual User Interface Reference</span></span>](multilingual-user-interface-reference.md)
</dt> <dt>

[<span data-ttu-id="96245-314">MUI-Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="96245-314">MUI Resource Management</span></span>](mui-resource-management.md)
</dt> <dt>

[<span data-ttu-id="96245-315">Lokalisieren von Ressourcen und entwickeln der Anwendung</span><span class="sxs-lookup"><span data-stu-id="96245-315">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
