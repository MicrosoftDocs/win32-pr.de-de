---
description: In diesem Abschnitt wird erläutert, wie ein benutzerdefiniertes Wörterbuch für die Handschrifterkennung erstellt
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Erstellen von benutzerdefinierten Wörterbüchern für die Handschrifterkennung in Windows 7 und Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b9b7b5a1d9dfadddd83825aea7d6f676439999
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345649"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="9b34f-103">Erstellen von benutzerdefinierten Wörterbüchern für die Handschrifterkennung in Windows 7 und Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b34f-103">Creating Custom Dictionaries for Handwriting Recognition in Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="9b34f-104">In diesem Abschnitt wird erläutert, wie ein benutzerdefiniertes Wörterbuch für die Handschrifterkennung erstellt</span><span class="sxs-lookup"><span data-stu-id="9b34f-104">This section explains how to create a custom dictionary for handwriting recognition.</span></span>

<span data-ttu-id="9b34f-105">Im Betriebssystem Windows 7 und unter dem Betriebssystem Windows Server 2008 R2 kann die Genauigkeit der Handschrifterkennung durch die Verwendung von benutzerdefinierten Wörterbüchern erheblich verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-105">In the Windows 7 operating system and the Windows Server 2008 R2 operating system, the accuracy of handwriting recognition can be significantly improved through the use of custom dictionaries.</span></span> <span data-ttu-id="9b34f-106">Diese Wörterbücher ergänzen oder ersetzen System Wörterbücher für die Handschrift.</span><span class="sxs-lookup"><span data-stu-id="9b34f-106">These dictionaries supplement or replace system dictionaries used for handwriting.</span></span> <span data-ttu-id="9b34f-107">Die Unterstützung für die Handschrifterkennung wird über das Freihand-und Handschriftdienste Feature bereitgestellt, das über Server-Manager aktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="9b34f-107">Support for handwriting recognition is provided through the Ink and Handwriting Services feature that needs to be enabled through Server Manager.</span></span>

> [!Note]  
> <span data-ttu-id="9b34f-108">Benutzerdefinierte Wörterbücher können nur für eine Sprache installiert werden, wenn die Handschrifterkennung für diese Sprache installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9b34f-108">Custom dictionaries can be installed for a language only if the handwriting recognizer for that language is installed.</span></span>

 

<span data-ttu-id="9b34f-109">Es gibt zwei grundlegende Schritte zum Einrichten eines benutzerdefinierten Wörterbuchs für die Handschrift:</span><span class="sxs-lookup"><span data-stu-id="9b34f-109">There are two basic steps to setting up a custom dictionary for handwriting:</span></span>

-   <span data-ttu-id="9b34f-110">Kompilieren Sie eine Wort Liste.</span><span class="sxs-lookup"><span data-stu-id="9b34f-110">Compile a word list.</span></span> <span data-ttu-id="9b34f-111">Die Kompilierung erstellt eine kompilierte benutzerdefinierte Wörterbuchdatei (. hwrdict).</span><span class="sxs-lookup"><span data-stu-id="9b34f-111">The compilation creates a compiled custom dictionary (.hwrdict) file.</span></span>
-   <span data-ttu-id="9b34f-112">Installieren Sie das kompilierte Benutzerwörterbuch.</span><span class="sxs-lookup"><span data-stu-id="9b34f-112">Install the compiled custom dictionary.</span></span>

## <a name="compiling-a-word-list"></a><span data-ttu-id="9b34f-113">Kompilieren einer Word-Liste</span><span class="sxs-lookup"><span data-stu-id="9b34f-113">Compiling a Word List</span></span>

<span data-ttu-id="9b34f-114">Die zu kompilierende Wort Liste muss im nur-Text-Format vorliegen und muss mit einer Unicode-Codierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-114">The word list to be compiled must be in plain-text format and should be saved using a Unicode encoding.</span></span> <span data-ttu-id="9b34f-115">Andere Codierungen können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-115">Other encodings will not work.</span></span> <span data-ttu-id="9b34f-116">Jede Zeile der Textdatei wird als einzelner Eintrag im Wörterbuch verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b34f-116">Each line of the text file is taken as a single entry in the dictionary.</span></span> <span data-ttu-id="9b34f-117">Multiword-Einheiten Einträge, die ein oder mehrere Leerzeichen enthalten, sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="9b34f-117">Multiword units entries containing one or more spaces are allowed.</span></span> <span data-ttu-id="9b34f-118">Leerzeichen am Anfang oder Ende einer Zeile werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9b34f-118">Spaces at the beginning or end of a line are ignored.</span></span>

<span data-ttu-id="9b34f-119">Ein benutzerdefiniertes Wörterbuch wird von einer Befehlszeile aus kompiliert.</span><span class="sxs-lookup"><span data-stu-id="9b34f-119">A custom dictionary is compiled from a command line.</span></span> <span data-ttu-id="9b34f-120">Öffnen Sie zum Kompilieren eines Wörterbuchs ein Befehlsfenster, navigieren Sie zu dem Ordner, der die Wort Liste enthält, und führen Sie HwrComp.exe mit den Befehlszeilenoptionen aus, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9b34f-120">To compile a dictionary, open a command window, navigate to the folder containing the word list, and then run HwrComp.exe with the command-line options you want to use.</span></span>

<span data-ttu-id="9b34f-121">Das folgende Beispiel zeigt die Verwendungs Syntax für die Befehlszeilenoptionen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-121">The following example shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a><span data-ttu-id="9b34f-122">Erklärung der Optionen</span><span class="sxs-lookup"><span data-stu-id="9b34f-122">Explanation of Options</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b34f-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b34f-123">Parameter</span></span></th>
<th><span data-ttu-id="9b34f-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b34f-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b34f-125">-lang <localename></span><span class="sxs-lookup"><span data-stu-id="9b34f-125">-lang <localename></span></span></td>
<td><span data-ttu-id="9b34f-126">Der angegebene Gebiets Schema Name, der der kompilierten benutzerdefinierten Wörterbuchdatei zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9b34f-126">The specified locale name assigned to the compiled custom dictionary file.</span></span> <span data-ttu-id="9b34f-127">Das <localename> -Argument hat die Form Language-Region.</span><span class="sxs-lookup"><span data-stu-id="9b34f-127">The argument <localename> has the form language-REGION.</span></span> <span data-ttu-id="9b34f-128">Ein Beispiel hierfür ist "en-US", das die englische Sprache in der USA Region angibt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-128">An example of this is en-US, which signifies the English language in the United States region.</span></span> <span data-ttu-id="9b34f-129">Beispiele für dieses Formular finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-129">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <span data-ttu-id="9b34f-130">Die folgenden Sprachen werden für Windows 7 und Windows Server 2008 R2 durch dieses Feature unterstützt: en-US, en-GB, en-ca, en-au, de-de, de-ch, fr-FR, es-es, es-MX, es-ar, IT-IT, nl-nl, NL-BE, pt-br, pt-pt, da-DK, SV-SE, nb-no, nn-no, fi-fi, PL-PL, CS-CZ, ru-ru, RO-RO, SR-LATN-CS, SR-Cyrl-CS, ca-es und HR-HR.</span><span class="sxs-lookup"><span data-stu-id="9b34f-130">The following languages are supported for Windows 7 and Windows Server 2008 R2 by this feature: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, cs-CZ, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES and hr-HR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b34f-131">-Typ <type></span><span class="sxs-lookup"><span data-stu-id="9b34f-131">-type <type></span></span></td>
<td><span data-ttu-id="9b34f-132">Das Option-Argument <type> ist eine Verkettung einer einzelnen Zeichenfolge für die Verwendung der Ressource als Haupt Wort Liste (primär) oder als Ergänzung zur Haupt Wort Liste (sekundär), gefolgt von dem Namen der eigentlichen Wort Liste, auf die die Ressource angewendet wird (z. b. Wörterbuch oder Nachname).</span><span class="sxs-lookup"><span data-stu-id="9b34f-132">The option argument <type> is a single-string concatenation of the resource's use as either the main word list (PRIMARY) or as a supplement to the main word list (SECONDARY) followed by the actual word list name to which the resource is applied (such as DICTIONARY or SURNAME).</span></span> <span data-ttu-id="9b34f-133">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="9b34f-133">The following are possible values:</span></span>
<ul>
<li><span data-ttu-id="9b34f-134">Primary-CityName-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-134">PRIMARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-135">Primary-CountryName-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-135">PRIMARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-136">Primary-countryshortname-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-136">PRIMARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-137">primär-Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="9b34f-137">PRIMARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="9b34f-138">primär-givenName-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-138">PRIMARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-139">Primary-StateOrProvince-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-139">PRIMARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="9b34f-140">Primary-streetname-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-140">PRIMARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-141">primär-Nachname-Liste</span><span class="sxs-lookup"><span data-stu-id="9b34f-141">PRIMARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-142">Sekundär-CityName-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-142">SECONDARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-143">Sekundär-CountryName-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-143">SECONDARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-144">Sekundär-countryshortname-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-144">SECONDARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-145">Sekundär Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="9b34f-145">SECONDARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="9b34f-146">Sekundär-emailsmtp-Liste</span><span class="sxs-lookup"><span data-stu-id="9b34f-146">SECONDARY-EMAILSMTP-LIST</span></span></li>
<li><span data-ttu-id="9b34f-147">Sekundär-emailusername-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-147">SECONDARY-EMAILUSERNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-148">Sekundär-givenName-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-148">SECONDARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-149">Sekundär-StateOrProvince-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-149">SECONDARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="9b34f-150">Sekundär-streetname-List</span><span class="sxs-lookup"><span data-stu-id="9b34f-150">SECONDARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-151">Sekundär-Nachname-Liste</span><span class="sxs-lookup"><span data-stu-id="9b34f-151">SECONDARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="9b34f-152">Sekundär-URL-Liste</span><span class="sxs-lookup"><span data-stu-id="9b34f-152">SECONDARY-URL-LIST</span></span></li>
</ul>
<span data-ttu-id="9b34f-153">Wenn ein Typwert mit dem Präfix Primary beginnt, wird das kompilierte Wörterbuch nach der Installation durch das System Wörterbuch für diese Sprache ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-153">If a type value starts with the prefix PRIMARY, the compiled dictionary, after it is installed, will replace the system dictionary for that language.</span></span> <span data-ttu-id="9b34f-154">Der Wert Primary-Dictionary stellt das Hauptsystem Wörterbuch für eine Sprache dar.</span><span class="sxs-lookup"><span data-stu-id="9b34f-154">The value PRIMARY-DICTIONARY represents the main system dictionary for a language.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9b34f-155">Das Ersetzen eines System Wörterbuchs führt nicht zum ursprünglichen Inhalt des System Wörterbuchs, da der Austausch nur wirksam ist, bis das benutzerdefinierte Wörterbuch entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="9b34f-155">Replacing a system dictionary does nothing to the original system dictionary content, as the replacement is in effect only until the custom dictionary has been removed.</span></span>
</blockquote>
<br/> <span data-ttu-id="9b34f-156">Wenn ein Typwert mit dem Präfix Sekundär beginnt, ergänzt das kompilierte Wörterbuch Das System Wörterbuch, ohne es zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-156">If a type value starts with the prefix SECONDARY, the compiled dictionary will supplement the system dictionary without replacing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b34f-157">-Kommentar</span><span class="sxs-lookup"><span data-stu-id="9b34f-157">-comment</span></span> <comment></td>
<td><span data-ttu-id="9b34f-158">Der angegebene Kommentar wird in die Wörterbuchdatei kompiliert.</span><span class="sxs-lookup"><span data-stu-id="9b34f-158">The specified comment is compiled into the dictionary file.</span></span> <span data-ttu-id="9b34f-159">Der Kommentar muss eine einzelne Zeichenfolge und nicht länger als 64 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="9b34f-159">The comment must be a single string and no longer than 64 characters.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b34f-160">-o <dictfile.hwrdict></span><span class="sxs-lookup"><span data-stu-id="9b34f-160">-o <dictfile.hwrdict></span></span></td>
<td><span data-ttu-id="9b34f-161">Die Ausgabe wird in den Dateinamen geschrieben, der durch angegeben wird <dictfile.hwrdict> .</span><span class="sxs-lookup"><span data-stu-id="9b34f-161">Output is written to the file name specified by <dictfile.hwrdict>.</span></span><br/> <span data-ttu-id="9b34f-162">Wenn diese Option fehlt, wird der Name der Ausgabedatei vom ursprünglichen Eingabe Dateinamen abgeleitet, wobei die Eingabedatei Erweiterung durch. hwrdict ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="9b34f-162">If this option is missing, the output file name is derived from the original input file name, with the input file extension replaced by .hwrdict.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a><span data-ttu-id="9b34f-163">Standardeinstellungen</span><span class="sxs-lookup"><span data-stu-id="9b34f-163">Defaults</span></span>

<span data-ttu-id="9b34f-164">Wenn keine Parameter angegeben werden, lauten die Standard Optionswerte</span><span class="sxs-lookup"><span data-stu-id="9b34f-164">If no parameters are specified, the default option values are</span></span>

<span data-ttu-id="9b34f-165">-lang <current input language> -Typ Sekundär-Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="9b34f-165">-lang <current input language> -type SECONDARY-DICTIONARY</span></span>

### <a name="examples"></a><span data-ttu-id="9b34f-166">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b34f-166">Examples</span></span>

<span data-ttu-id="9b34f-167">Im folgenden wird die Eingabedatei mylist1.txt kompiliert, die Standard Optionswerte angewendet und die Ausgabedatei mylist1. hwrdict erstellt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-167">The following compiles the input file mylist1.txt, applies the default option values, and creates the output file mylist1.hwrdict.</span></span>

``` syntax
hwrcomp mylist1.txt
```

<span data-ttu-id="9b34f-168">Im Gegensatz dazu kompiliert der folgende mylist1.txt in myrsrc1. hwrdict, weist jedoch "English (US)" (en-US) als Sprache und das sekundäre Wörterbuch als Typ zu.</span><span class="sxs-lookup"><span data-stu-id="9b34f-168">In contrast, the following compiles mylist1.txt into myrsrc1.hwrdict, but assigns "English (US)" (en-US) as the language and SECONDARY-DICTIONARY as the type.</span></span>

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a><span data-ttu-id="9b34f-169">Installieren eines kompilierten Benutzer Wörterbuchs</span><span class="sxs-lookup"><span data-stu-id="9b34f-169">Installing a Compiled Custom Dictionary</span></span>

<span data-ttu-id="9b34f-170">HwrComp.exe erstellt eine hwrdict-Datei, die in einem Binärformat vorliegt, das von einer Handschrifterkennung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b34f-170">HwrComp.exe creates a .hwrdict file, which is in a binary format usable by a handwriting recognizer.</span></span> <span data-ttu-id="9b34f-171">Diese Datei kann auf jedem Computer installiert werden, auf dem Windows 7 oder Windows Server 2008 R2 ausgeführt wird und der die Handschrifterkennung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-171">This file can be installed on any computer running Windows 7 or Windows Server 2008 R2 that supports handwriting recognition.</span></span> <span data-ttu-id="9b34f-172">Ein Wörterbuch wird entweder nur für den aktuellen Benutzer oder für alle Benutzer auf einem Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="9b34f-172">A dictionary is installed either for just the current user or for all users on a machine.</span></span>

<span data-ttu-id="9b34f-173">Eine kompilierte benutzerdefinierte Wörterbuchdatei kann über die Befehlszeile mit dem Tool HwrReg.exe installiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-173">A compiled custom dictionary file can be installed from the command line using the tool HwrReg.exe.</span></span> <span data-ttu-id="9b34f-174">Dieses Tool ist nützlich, wenn Sie einige der Konfigurationswerte außer Kraft setzen möchten, die in die Datei kompiliert werden, oder die Standardwerte sind.</span><span class="sxs-lookup"><span data-stu-id="9b34f-174">This tool is useful if you wish to override some of the configuration values that either are compiled into the file or are the default values.</span></span> <span data-ttu-id="9b34f-175">Es gibt zwei Möglichkeiten, HwrReg.exe auszuführen: im Modus "überprüfen/installieren" und im Listen-/Entfernungs Modus.</span><span class="sxs-lookup"><span data-stu-id="9b34f-175">There are two ways to run HwrReg.exe: in check/install mode and in list/remove mode.</span></span>

### <a name="running-hwrregexe-in-checkinstall-mode"></a><span data-ttu-id="9b34f-176">Ausführen von HwrReg.exe im Modus "überprüfen/installieren"</span><span class="sxs-lookup"><span data-stu-id="9b34f-176">Running HwrReg.exe in Check/Install Mode</span></span>

<span data-ttu-id="9b34f-177">Dieser Modus ist für benutzerdefinierte Wörterbuchdateien vorgesehen, die noch nicht installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-177">This mode is for custom dictionary files that have not yet been installed.</span></span> <span data-ttu-id="9b34f-178">Das folgende Beispiel zeigt die Verwendungs Syntax für die Befehlszeilenoptionen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-178">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a><span data-ttu-id="9b34f-179">Erklärung der Optionen</span><span class="sxs-lookup"><span data-stu-id="9b34f-179">Explanation of Options</span></span>



| <span data-ttu-id="9b34f-180">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b34f-180">Parameter</span></span>                | <span data-ttu-id="9b34f-181">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b34f-181">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b34f-182">-Überprüfen</span><span class="sxs-lookup"><span data-stu-id="9b34f-182">-check</span></span>                   | <span data-ttu-id="9b34f-183">Die Wörterbuchdatei wird überprüft, ohne installiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-183">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="9b34f-184">Die Option "Check" zeigt den Kommentar der Datei sowie die Registrierungsinformationen an, die zum Installieren der Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-184">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="9b34f-185">Diese Option ist nützlich, um Registrierungsinformationen vor der Installation zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-185">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="9b34f-186">Wenn diese Option fehlt, installiert HwrReg.exe das benutzerdefinierte Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="9b34f-186">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span><br/>  |
|  <span data-ttu-id="9b34f-187">Wochen <localename></span><span class="sxs-lookup"><span data-stu-id="9b34f-187">lang <localename></span></span> | <span data-ttu-id="9b34f-188">Die Wörterbuchdatei wird überprüft, ohne installiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-188">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="9b34f-189">Die Option "Check" zeigt den Kommentar der Datei sowie die Registrierungsinformationen an, die zum Installieren der Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-189">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="9b34f-190">Diese Option ist nützlich, um Registrierungsinformationen vor der Installation zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-190">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="9b34f-191">Wenn diese Option fehlt, installiert HwrReg.exe das benutzerdefinierte Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="9b34f-191">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span> <br/> |
|  <span data-ttu-id="9b34f-192">Bereich "{All \| Me}"</span><span class="sxs-lookup"><span data-stu-id="9b34f-192">scope {all\|me}</span></span>         | <span data-ttu-id="9b34f-193">Das benutzerdefinierte Wörterbuch wird entweder für alle Benutzer (Bereich alle) oder nur für den aktuellen Benutzer (Bereich "Me") installiert.</span><span class="sxs-lookup"><span data-stu-id="9b34f-193">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="9b34f-194">Die Installation mit dem Bereich "All" erfordert, dass der Befehl an einer Eingabeaufforderung mit erhöhten Rechten ausgeführt wird. Andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b34f-194">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="9b34f-195">Wenn diese Option fehlt, wird die Installation nur auf den aktuellen Benutzer beschränkt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-195">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                          |
|  <span data-ttu-id="9b34f-196">noprompt</span><span class="sxs-lookup"><span data-stu-id="9b34f-196">noprompt</span></span>                | <span data-ttu-id="9b34f-197">HwrReg.exe wird nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="9b34f-197">HwrReg.exe does not prompt for confirmation.</span></span> <span data-ttu-id="9b34f-198">Dies kann nützlich sein, wenn hwrReg.exe aus einem Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b34f-198">This can be useful when running hwrReg.exe from a script.</span></span> <br/>                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="9b34f-199">Im folgenden Beispiel wird das benutzerdefinierte Wörterbuch myrsrc1. hwrdict für die Sprache "Danish (Dänemark)" (da DK) mit dem Standardbereich nur des aktuellen Benutzers installiert.</span><span class="sxs-lookup"><span data-stu-id="9b34f-199">The following example installs the custom dictionary myrsrc1.hwrdict for language "Danish (Denmark)" (da DK), with the default scope of just the current user.</span></span>

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a><span data-ttu-id="9b34f-200">Ausführen von HwrReg.exe im Listen-/Entfernungs Modus</span><span class="sxs-lookup"><span data-stu-id="9b34f-200">Running HwrReg.exe in List/Remove Mode</span></span>

<span data-ttu-id="9b34f-201">In diesem Modus werden installierte benutzerdefinierte Wörterbücher aufgelistet oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-201">This mode either lists or removes installed custom dictionaries.</span></span> <span data-ttu-id="9b34f-202">Das folgende Beispiel zeigt die Verwendungs Syntax für die Befehlszeilenoptionen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-202">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a><span data-ttu-id="9b34f-203">Erklärung der Optionen</span><span class="sxs-lookup"><span data-stu-id="9b34f-203">Explanation of Options</span></span>



| <span data-ttu-id="9b34f-204">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b34f-204">Parameter</span></span>                | <span data-ttu-id="9b34f-205">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b34f-205">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="9b34f-206">Wochen <localename></span><span class="sxs-lookup"><span data-stu-id="9b34f-206">lang <localename></span></span> | <span data-ttu-id="9b34f-207">Die Wörterbücher, die nur für diesen Gebiets Schema Namen registriert sind, werden aufgelistet oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-207">The dictionaries registered for only this locale name are listed or removed.</span></span> <span data-ttu-id="9b34f-208">Das-Argument <localename> hat den Formular Sprachbereich.</span><span class="sxs-lookup"><span data-stu-id="9b34f-208">The argument <localename> has the form language REGION.</span></span> <span data-ttu-id="9b34f-209">Beispiele für dieses Formular finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-209">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <br/> <span data-ttu-id="9b34f-210">Wenn diese Option fehlt, werden Wörterbücher für alle Sprachen aufgelistet oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-210">If this option is missing, dictionaries for all languages are listed or removed.</span></span><br/> |
|  <span data-ttu-id="9b34f-211">Bereich "{All \| Me}"</span><span class="sxs-lookup"><span data-stu-id="9b34f-211">scope {all\|me}</span></span>         | <span data-ttu-id="9b34f-212">Das benutzerdefinierte Wörterbuch wird entweder für alle Benutzer (Bereich alle) oder nur für den aktuellen Benutzer (Bereich "Me") installiert.</span><span class="sxs-lookup"><span data-stu-id="9b34f-212">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="9b34f-213">Die Installation mit dem Bereich "All" erfordert, dass der Befehl an einer Eingabeaufforderung mit erhöhten Rechten ausgeführt wird. Andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b34f-213">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="9b34f-214">Wenn diese Option fehlt, wird die Installation nur auf den aktuellen Benutzer beschränkt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-214">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                      |
|  <span data-ttu-id="9b34f-215">Sorte <type></span><span class="sxs-lookup"><span data-stu-id="9b34f-215">type <type></span></span>       | <span data-ttu-id="9b34f-216">Listet oder entfernt nur Wörterbücher, die mit dem angegebenen Typ registriert sind.</span><span class="sxs-lookup"><span data-stu-id="9b34f-216">Lists or removes only dictionaries that are registered with the specified type.</span></span><br/> <span data-ttu-id="9b34f-217">Wenn diese Option fehlt, werden alle Wörterbuchtypen aufgelistet oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-217">If this option is missing, all dictionary types are listed or removed.</span></span> <span data-ttu-id="9b34f-218">Das Installieren oder Entfernen eines Benutzer Wörterbuchs eines anderen Typs (z. b. Primary-CountryName-List) kann die Handschrifterkennung in anderen Kontexten beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-218">Installing or removing a custom dictionary of another type (such as PRIMARY-COUNTRYNAME-LIST) may affect handwriting recognition in other contexts.</span></span> <br/>                                              |
|  <span data-ttu-id="9b34f-219">list</span><span class="sxs-lookup"><span data-stu-id="9b34f-219">list</span></span>                    | <span data-ttu-id="9b34f-220">Listet alle installierten Wörterbücher auf, die den anderen Optionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-220">Lists all installed dictionaries that match the other options.</span></span><br/> <span data-ttu-id="9b34f-221">Wenn diese Option fehlt, muss die Option remove angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-221">If this option is missing, the option  remove must be specified.</span></span><br/>                                                                                                                                                                                                                          |
|  <span data-ttu-id="9b34f-222">remove</span><span class="sxs-lookup"><span data-stu-id="9b34f-222">remove</span></span>                  | <span data-ttu-id="9b34f-223">Fordert zum Entfernen eines beliebigen Wörterbuchs auf, das mit den anderen Optionen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9b34f-223">Prompts for removal of any dictionary that matches the other options.</span></span><br/> <span data-ttu-id="9b34f-224">Wenn diese Option fehlt, muss die Optionsliste angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-224">If this option is missing, the option  list must be specified.</span></span><br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="9b34f-225">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b34f-225">Examples</span></span>

<span data-ttu-id="9b34f-226">Im folgenden finden Sie Wörterbücher mit der Sprache "English (US)" (en US) und dem primären Wörterbuch "Typ", die nur für den aktuellen Benutzer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b34f-226">The following lists dictionaries that have language "English (US)" (en US) and type PRIMARY DICTIONARY and that are installed for just the current user.</span></span>

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

<span data-ttu-id="9b34f-227">Ebenso werden mit dem folgenden Wörterbücher entfernt, die denselben Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9b34f-227">Similarly, the following removes dictionaries that match the same criteria.</span></span>

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a><span data-ttu-id="9b34f-228">Allgemeine Hinweise zu benutzerdefinierten Wörterbüchern</span><span class="sxs-lookup"><span data-stu-id="9b34f-228">General Notes on Custom Dictionaries</span></span>

-   <span data-ttu-id="9b34f-229">Wenn Sie zwei benutzerdefinierte Wörterbücher mit dem gleichen Typ, der gleichen Sprache und dem gleichen Gültigkeitsbereich installieren, wird die erste Installation durch die zweite Installation überschrieben.</span><span class="sxs-lookup"><span data-stu-id="9b34f-229">If you install two custom dictionaries that have the same type, language, and scope, the second installation will overwrite the first.</span></span>
-   <span data-ttu-id="9b34f-230">Wenn Sie zwei benutzerdefinierte Wörterbücher mit demselben Typ und derselben Sprache installieren, aber mit unterschiedlichen Bereichen (eines für alle Benutzer und eines für den aktuellen Benutzer), hat das für den aktuellen Benutzer installierte Wörterbuch Vorrang, und das für alle Benutzer installierte Wörterbuch wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9b34f-230">If you install two custom dictionaries with the same type and language, but with different scopes (one for all users, and one for the current user), the dictionary installed for the current user takes precedence, and the dictionary installed for all users is ignored.</span></span>

 

