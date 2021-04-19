---
title: Syntax
description: Hier ist die Syntax zum Aufrufen von FXC.exe, dem Effekt-Compiler-Tool. Ein Beispiel finden Sie unter Offline Kompilierung.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- FXC, Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106337474"
---
# <a name="syntax"></a><span data-ttu-id="46b7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46b7c-105">Syntax</span></span>

<span data-ttu-id="46b7c-106">Hier ist die Syntax zum Aufrufen von FXC.exe, dem Effekt-Compiler-Tool.</span><span class="sxs-lookup"><span data-stu-id="46b7c-106">Here is the syntax for calling FXC.exe, the effect-compiler tool.</span></span> <span data-ttu-id="46b7c-107">Ein Beispiel finden Sie unter [Offline Kompilierung](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="46b7c-107">For an example, see [Offline Compiling](dx-graphics-tools-fxc-using.md).</span></span>

-   [<span data-ttu-id="46b7c-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="46b7c-108">Usage</span></span>](#usage)
-   [<span data-ttu-id="46b7c-109">Argumente</span><span class="sxs-lookup"><span data-stu-id="46b7c-109">Arguments</span></span>](#arguments)
-   [<span data-ttu-id="46b7c-110">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="46b7c-110">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="46b7c-111">Profiles</span><span class="sxs-lookup"><span data-stu-id="46b7c-111">Profiles</span></span>](#profiles)
-   [<span data-ttu-id="46b7c-112">Versions Hinweise</span><span class="sxs-lookup"><span data-stu-id="46b7c-112">Version notes</span></span>](#version-notes)
-   [<span data-ttu-id="46b7c-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46b7c-113">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="46b7c-114">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="46b7c-114">Usage</span></span>

<span data-ttu-id="46b7c-115">**FXC** *switchoptions* - *Datei* Namen</span><span class="sxs-lookup"><span data-stu-id="46b7c-115">**fxc** *SwitchOptions* *Filenames*</span></span>

## <a name="arguments"></a><span data-ttu-id="46b7c-116">Argumente</span><span class="sxs-lookup"><span data-stu-id="46b7c-116">Arguments</span></span>
<span data-ttu-id="46b7c-117">Trennen Sie jede Switch-Option durch ein Leerzeichen oder einen Doppelpunkt.</span><span class="sxs-lookup"><span data-stu-id="46b7c-117">Separate each switch option with a space or a colon.</span></span>

### <a name="switchoptions"></a><span data-ttu-id="46b7c-118">*Switchoptions*</span><span class="sxs-lookup"><span data-stu-id="46b7c-118">*SwitchOptions*</span></span>
<span data-ttu-id="46b7c-119">\[in \] Kompilierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-119">\[in\] Compile options.</span></span> <span data-ttu-id="46b7c-120">Es gibt nur eine erforderliche Option und vieles mehr, das optional ist.</span><span class="sxs-lookup"><span data-stu-id="46b7c-120">There is just one required option, and many more that are optional.</span></span> <span data-ttu-id="46b7c-121">Trennen Sie jede durch ein Leerzeichen oder einen Doppelpunkt.</span><span class="sxs-lookup"><span data-stu-id="46b7c-121">Separate each with a space or colon.</span></span>

#### <a name="required-option"></a><span data-ttu-id="46b7c-122">Erforderliche Option</span><span class="sxs-lookup"><span data-stu-id="46b7c-122">Required option</span></span>
##### <a name="t-profile"></a><span data-ttu-id="46b7c-123">/T <*Profil*></span><span class="sxs-lookup"><span data-stu-id="46b7c-123">/T <*profile*></span></span>
<span data-ttu-id="46b7c-124">Shadermodell (siehe [profile](#profiles)).</span><span class="sxs-lookup"><span data-stu-id="46b7c-124">Shader model (see [Profiles](#profiles)).</span></span>

#### <a name="optional-options"></a><span data-ttu-id="46b7c-125">Optionale Optionen</span><span class="sxs-lookup"><span data-stu-id="46b7c-125">Optional options</span></span>
##### <a name="-help"></a><span data-ttu-id="46b7c-126">/?, /help</span><span class="sxs-lookup"><span data-stu-id="46b7c-126">/?, /help</span></span>
<span data-ttu-id="46b7c-127">Hilfe zum Drucken von `FXC.exe` .</span><span class="sxs-lookup"><span data-stu-id="46b7c-127">Print help for `FXC.exe`.</span></span>

##### <a name="commandoptionfile"></a><span data-ttu-id="46b7c-128">@<*Command. Option. file*></span><span class="sxs-lookup"><span data-stu-id="46b7c-128">@<*command.option.file*></span></span>
<span data-ttu-id="46b7c-129">Eine Datei, die zusätzliche Kompilierungsoptionen enthält.</span><span class="sxs-lookup"><span data-stu-id="46b7c-129">File that contains additional compile options.</span></span> <span data-ttu-id="46b7c-130">Diese Option kann mit anderen Kompilierungsoptionen für die Befehlszeile gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="46b7c-130">This option can be mixed with other command line compile options.</span></span> <span data-ttu-id="46b7c-131">Der *Befehl. Option. File* darf nur eine Option pro Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="46b7c-131">The *command.option.file* must contain only one option per line.</span></span> <span data-ttu-id="46b7c-132">Der *Befehl. Option. File* darf keine leeren Zeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="46b7c-132">The *command.option.file* cannot contain any blank lines.</span></span> <span data-ttu-id="46b7c-133">Die in der Datei angegebenen Optionen dürfen keine führenden oder nachfolgenden Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="46b7c-133">Options specified in the file must not contain any leading or trailing spaces.</span></span>

##### <a name="all_resources_bound"></a><span data-ttu-id="46b7c-134">/all_resources_bound</span><span class="sxs-lookup"><span data-stu-id="46b7c-134">/all_resources_bound</span></span>
<span data-ttu-id="46b7c-135">Aktivieren Sie aggressive Vereinfachung in SM 5.1 und höher.</span><span class="sxs-lookup"><span data-stu-id="46b7c-135">Enable aggressive flattening in SM5.1+.</span></span> <span data-ttu-id="46b7c-136">Neu für Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="46b7c-136">New for Direct3D 12.</span></span>

##### <a name="cc"></a><span data-ttu-id="46b7c-137">/CC</span><span class="sxs-lookup"><span data-stu-id="46b7c-137">/Cc</span></span>
<span data-ttu-id="46b7c-138">Ausgabe Farbe codierte Assembly.</span><span class="sxs-lookup"><span data-stu-id="46b7c-138">Output color-coded assembly.</span></span>

##### <a name="compress"></a><span data-ttu-id="46b7c-139">/compress</span><span class="sxs-lookup"><span data-stu-id="46b7c-139">/compress</span></span>
<span data-ttu-id="46b7c-140">Komprimieren des DX10-Shader-Bytecode aus Dateien.</span><span class="sxs-lookup"><span data-stu-id="46b7c-140">Compress DX10 shader bytecode from files.</span></span>

##### <a name="d-idtext"></a><span data-ttu-id="46b7c-141">/D <*ID*- >=< *Text*></span><span class="sxs-lookup"><span data-stu-id="46b7c-141">/D <*id*>=<*text*></span></span>
<span data-ttu-id="46b7c-142">Definieren Sie das Makro.</span><span class="sxs-lookup"><span data-stu-id="46b7c-142">Define macro.</span></span>

##### <a name="decompress"></a><span data-ttu-id="46b7c-143">/decompress</span><span class="sxs-lookup"><span data-stu-id="46b7c-143">/decompress</span></span>
<span data-ttu-id="46b7c-144">Dekomprimieren von DX10-Shader-Bytecode aus der ersten Datei.</span><span class="sxs-lookup"><span data-stu-id="46b7c-144">Decompress DX10 shader bytecode from first file.</span></span> <span data-ttu-id="46b7c-145">Ausgabedateien müssen in der Reihenfolge aufgelistet werden, in der Sie sich während der Komprimierung befanden.</span><span class="sxs-lookup"><span data-stu-id="46b7c-145">Output files should be listed in the order they were in during compression.</span></span>

##### <a name="dumpbin"></a><span data-ttu-id="46b7c-146">/dumpbin</span><span class="sxs-lookup"><span data-stu-id="46b7c-146">/dumpbin</span></span>
<span data-ttu-id="46b7c-147">Lädt eine Binärdatei, anstatt einen Shader zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="46b7c-147">Loads a binary file rather than compiling a shader.</span></span>

##### <a name="e-name"></a><span data-ttu-id="46b7c-148">/E <name></span><span class="sxs-lookup"><span data-stu-id="46b7c-148">/E <name></span></span>
<span data-ttu-id="46b7c-149">Shader-Einstiegspunkt.</span><span class="sxs-lookup"><span data-stu-id="46b7c-149">Shader entry point.</span></span> <span data-ttu-id="46b7c-150">Wenn kein Einstiegspunkt angegeben wird, wird **Main** als Shader-Eintrags Name betrachtet.</span><span class="sxs-lookup"><span data-stu-id="46b7c-150">If no entry point is given, **main** is considered to be the shader entry name.</span></span>

##### <a name="enable_unbounded_descriptor_tables"></a><span data-ttu-id="46b7c-151">/enable_unbounded_descriptor_tables</span><span class="sxs-lookup"><span data-stu-id="46b7c-151">/enable_unbounded_descriptor_tables</span></span>
<span data-ttu-id="46b7c-152">Aktiviert ungebundene deskriptortabellen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-152">Enables unbounded descriptor tables.</span></span> <span data-ttu-id="46b7c-153">Neu für Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="46b7c-153">New for Direct3D 12.</span></span>

##### <a name="extractrootsignature-file"></a><span data-ttu-id="46b7c-154">/extractrootsignature <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-154">/extractrootsignature <*file*></span></span>
<span data-ttu-id="46b7c-155">Extrahieren Sie die Stamm Signatur aus Shader-Bytecode.</span><span class="sxs-lookup"><span data-stu-id="46b7c-155">Extract root signature from shader bytecode.</span></span> <span data-ttu-id="46b7c-156">Neu für Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="46b7c-156">New for Direct3D 12.</span></span>

##### <a name="fc-file"></a><span data-ttu-id="46b7c-157">/FC <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-157">/Fc <*file*></span></span>
<span data-ttu-id="46b7c-158">Ausgabeassembly-Codelisten Datei.</span><span class="sxs-lookup"><span data-stu-id="46b7c-158">Output assembly code listing file.</span></span>

##### <a name="fd-file"></a><span data-ttu-id="46b7c-159">/FD <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-159">/Fd <*file*></span></span>
<span data-ttu-id="46b7c-160">Extrahieren Sie die Informationen der Shader-Programmdatenbank (PDB), und schreiben Sie Sie in die angegebene Datei. Wenn Sie den Shader kompilieren, verwenden Sie/FD, um eine PDB-Datei mit shaderdebuginformationen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="46b7c-160">Extract shader program database (PDB) info and write to the given file.When you compile the shader, use /Fd to generate a PDB file with shader debugging info.</span></span>

##### <a name="fe-file"></a><span data-ttu-id="46b7c-161">/FE <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-161">/Fe <*file*></span></span>
<span data-ttu-id="46b7c-162">Gibt Warnungen und Fehler in der angegebenen Datei aus.</span><span class="sxs-lookup"><span data-stu-id="46b7c-162">Output warnings and errors to the given file.</span></span>

##### <a name="fh-file"></a><span data-ttu-id="46b7c-163">/FH <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-163">/Fh <*file*></span></span>
<span data-ttu-id="46b7c-164">Ausgabe Header Datei, die den Objektcode enthält.</span><span class="sxs-lookup"><span data-stu-id="46b7c-164">Output header file containing object code.</span></span>

##### <a name="fl-file"></a><span data-ttu-id="46b7c-165">/FL <*Datei*</span><span class="sxs-lookup"><span data-stu-id="46b7c-165">/Fl <*file*</span></span>
<span data-ttu-id="46b7c-166">Gibt eine Bibliothek aus.</span><span class="sxs-lookup"><span data-stu-id="46b7c-166">Output a library.</span></span> <span data-ttu-id="46b7c-167">Erfordert den D3dcompiler- \_47.dll oder eine spätere Version der dll.</span><span class="sxs-lookup"><span data-stu-id="46b7c-167">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="fo-file"></a><span data-ttu-id="46b7c-168">/FO <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-168">/Fo <*file*></span></span>
<span data-ttu-id="46b7c-169">Ausgabe Objektdatei.</span><span class="sxs-lookup"><span data-stu-id="46b7c-169">Output object file.</span></span> <span data-ttu-id="46b7c-170">Häufig wird die Erweiterung &quot; . FXC &quot; verwendet, obwohl andere Erweiterungen verwendet werden, wie z &quot; . b.. o &quot; , &quot; . obj &quot; oder &quot; . dxbc &quot; .</span><span class="sxs-lookup"><span data-stu-id="46b7c-170">Often given the extension &quot;.fxc&quot;, though other extensions are used, such as &quot;.o&quot;, &quot;.obj&quot; or &quot;.dxbc&quot;.</span></span>

##### <a name="fx-file"></a><span data-ttu-id="46b7c-171">/FX <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-171">/Fx <*file*></span></span>
<span data-ttu-id="46b7c-172">Ausgabeassemblycode und Hex-Listen Datei</span><span class="sxs-lookup"><span data-stu-id="46b7c-172">Output assembly code and hex listing file.</span></span>

##### <a name="gch"></a><span data-ttu-id="46b7c-173">/Gch</span><span class="sxs-lookup"><span data-stu-id="46b7c-173">/Gch</span></span>
<span data-ttu-id="46b7c-174">Als untergeordneten Effekt für fx_4_x profile kompilieren.</span><span class="sxs-lookup"><span data-stu-id="46b7c-174">Compile as a child effect for fx_4_x profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="46b7c-175">Die Unterstützung für Legacy Effekt Profile ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="46b7c-175">Support for legacy Effects profiles is deprecated.</span></span>

##### <a name="gdp"></a><span data-ttu-id="46b7c-176">/Gdp</span><span class="sxs-lookup"><span data-stu-id="46b7c-176">/Gdp</span></span>
<span data-ttu-id="46b7c-177">Deaktivieren Sie den Leistungsmodus des Effekts.</span><span class="sxs-lookup"><span data-stu-id="46b7c-177">Disable effect performance mode.</span></span>

##### <a name="gec"></a><span data-ttu-id="46b7c-178">/Gec</span><span class="sxs-lookup"><span data-stu-id="46b7c-178">/Gec</span></span>
<span data-ttu-id="46b7c-179">Aktivieren Sie den abwärts Kompatibilitätsmodus.</span><span class="sxs-lookup"><span data-stu-id="46b7c-179">Enable backward compatibility mode.</span></span>

##### <a name="ges"></a><span data-ttu-id="46b7c-180">/Ges</span><span class="sxs-lookup"><span data-stu-id="46b7c-180">/Ges</span></span>
<span data-ttu-id="46b7c-181">Aktivieren Sie den Strict-Modus.</span><span class="sxs-lookup"><span data-stu-id="46b7c-181">Enable strict mode.</span></span>

##### <a name="getprivate-file"></a><span data-ttu-id="46b7c-182">/getprivate <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-182">/getprivate <*file*></span></span>
<span data-ttu-id="46b7c-183">Speichert private Daten aus dem Shader-BLOB (kompilierte Shader-Binärdatei) in der angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="46b7c-183">Save private data from the shader blob (compiled shader binary) to the given file.</span></span> <span data-ttu-id="46b7c-184">Extrahiert private Daten, die zuvor durch/setprivate eingebettet wurden, aus dem Shader-BLOB.</span><span class="sxs-lookup"><span data-stu-id="46b7c-184">Extracts private data, previously embedded by /setprivate, from the shader blob.</span></span>

<span data-ttu-id="46b7c-185">Sie müssen die/dumpbin-Option mit/getprivate. angeben.</span><span class="sxs-lookup"><span data-stu-id="46b7c-185">You must specify the /dumpbin option with /getprivate.</span></span> <span data-ttu-id="46b7c-186">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="46b7c-186">For example:</span></span>

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a><span data-ttu-id="46b7c-187">/Gfa</span><span class="sxs-lookup"><span data-stu-id="46b7c-187">/Gfa</span></span>
<span data-ttu-id="46b7c-188">Vermeiden Sie flowsteuerungskonstrukte.</span><span class="sxs-lookup"><span data-stu-id="46b7c-188">Avoid flow control constructs.</span></span>

##### <a name="gfp"></a><span data-ttu-id="46b7c-189">/GFP</span><span class="sxs-lookup"><span data-stu-id="46b7c-189">/Gfp</span></span>
<span data-ttu-id="46b7c-190">Flow-steuerungskonstrukte bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-190">Prefer flow control constructs.</span></span>

##### <a name="gis"></a><span data-ttu-id="46b7c-191">/Gis</span><span class="sxs-lookup"><span data-stu-id="46b7c-191">/Gis</span></span>
<span data-ttu-id="46b7c-192">Erzwingen der IEEE-strenge.</span><span class="sxs-lookup"><span data-stu-id="46b7c-192">Force IEEE strictness.</span></span>

##### <a name="gpp"></a><span data-ttu-id="46b7c-193">/Gpp</span><span class="sxs-lookup"><span data-stu-id="46b7c-193">/Gpp</span></span>
<span data-ttu-id="46b7c-194">Partielle Genauigkeit erzwingen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-194">Force partial precision.</span></span>
    
##### <a name="i-include"></a><span data-ttu-id="46b7c-195">/I <*einschließen*></span><span class="sxs-lookup"><span data-stu-id="46b7c-195">/I <*include*></span></span>
<span data-ttu-id="46b7c-196">Zusätzlicher Include-Pfad.</span><span class="sxs-lookup"><span data-stu-id="46b7c-196">Additional include path.</span></span>

##### <a name="lx"></a><span data-ttu-id="46b7c-197">/Lx</span><span class="sxs-lookup"><span data-stu-id="46b7c-197">/Lx</span></span>
<span data-ttu-id="46b7c-198">Ausgabe hexadezimal Literale.</span><span class="sxs-lookup"><span data-stu-id="46b7c-198">Output hexadecimal literals.</span></span> <span data-ttu-id="46b7c-199">Erfordert den D3dcompiler- \_47.dll oder eine spätere Version der dll.</span><span class="sxs-lookup"><span data-stu-id="46b7c-199">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="matchuavs"></a><span data-ttu-id="46b7c-200">/matchUAVs</span><span class="sxs-lookup"><span data-stu-id="46b7c-200">/matchUAVs</span></span>
<span data-ttu-id="46b7c-201">Entsprechung für Vorlagen-Shader-UAV-Slot-Zuweisungen im aktuellen Shader.</span><span class="sxs-lookup"><span data-stu-id="46b7c-201">Match template shader UAV slot allocations in the current shader.</span></span> <span data-ttu-id="46b7c-202">Weitere Informationen finden Sie unter " <a href="#remarks">Hinweise</a>".</span><span class="sxs-lookup"><span data-stu-id="46b7c-202">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="mergeuavs"></a><span data-ttu-id="46b7c-203">/mergeUAVs</span><span class="sxs-lookup"><span data-stu-id="46b7c-203">/mergeUAVs</span></span>
<span data-ttu-id="46b7c-204">UAV-Slot-Zuordnungen von Vorlagen-Shader und dem aktuellen Shader zusammenführen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-204">Merge UAV slot allocations of template shader and the current shader.</span></span> <span data-ttu-id="46b7c-205">Weitere Informationen finden Sie unter " <a href=""></a> <a href="#remarks">Hinweise</a>".</span><span class="sxs-lookup"><span data-stu-id="46b7c-205">For more info, see <a href=""></a><a href="#remarks">Remarks</a>.</span></span>

##### <a name="ni"></a><span data-ttu-id="46b7c-206">/Ni</span><span class="sxs-lookup"><span data-stu-id="46b7c-206">/Ni</span></span>
<span data-ttu-id="46b7c-207">Ausgabe Anweisungs Nummern in assemblyauflistungen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-207">Output instruction numbers in assembly listings.</span></span>

##### <a name="no"></a><span data-ttu-id="46b7c-208">/No</span><span class="sxs-lookup"><span data-stu-id="46b7c-208">/No</span></span>
<span data-ttu-id="46b7c-209">Byte Offset der Ausgabe Anweisung in Assemblylisten.</span><span class="sxs-lookup"><span data-stu-id="46b7c-209">Output instruction byte offset in assembly listings.</span></span> <span data-ttu-id="46b7c-210">Wenn Sie eine Assembly entwickeln, verwenden Sie/No, um Sie mit dem Byte Offset für jede Anweisung zu kommentieren.</span><span class="sxs-lookup"><span data-stu-id="46b7c-210">When you produce assembly, use /No to annotate it with the byte offset for each instruction.</span></span>

##### <a name="nologo"></a><span data-ttu-id="46b7c-211">/nologo</span><span class="sxs-lookup"><span data-stu-id="46b7c-211">/nologo</span></span>
<span data-ttu-id="46b7c-212">Copyrightmeldung unterdrücken</span><span class="sxs-lookup"><span data-stu-id="46b7c-212">Suppress copyright message.</span></span>

##### <a name="od"></a><span data-ttu-id="46b7c-213">/Od</span><span class="sxs-lookup"><span data-stu-id="46b7c-213">/Od</span></span>
<span data-ttu-id="46b7c-214">Deaktiviert Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-214">Disable optimizations.</span></span> <span data-ttu-id="46b7c-215">/Od impliziert/GFP, aber die Ausgabe ist möglicherweise nicht identisch mit/od/GFP.</span><span class="sxs-lookup"><span data-stu-id="46b7c-215">/Od implies /Gfp, though output may not be identical to /Od /Gfp.</span></span>

##### <a name="op"></a><span data-ttu-id="46b7c-216">/Op</span><span class="sxs-lookup"><span data-stu-id="46b7c-216">/Op</span></span>
<span data-ttu-id="46b7c-217">Deaktivieren Sie preshaders (veraltet).</span><span class="sxs-lookup"><span data-stu-id="46b7c-217">Disable preshaders (deprecated).</span></span>

##### <a name="o0-o1-o2-o3"></a><span data-ttu-id="46b7c-218">/O0/O1,/O2,/O3</span><span class="sxs-lookup"><span data-stu-id="46b7c-218">/O0 /O1, /O2, /O3</span></span>
<span data-ttu-id="46b7c-219">Optimierungs Ebenen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-219">Optimization levels.</span></span> <span data-ttu-id="46b7c-220">O1 ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="46b7c-220">O1 is the default setting.</span></span>
- <span data-ttu-id="46b7c-221">O0: deaktiviert die Neuanordnung von Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-221">O0 - Disables instruction reordering.</span></span> <span data-ttu-id="46b7c-222">Dies trägt zur Verringerung der Register Last bei und ermöglicht eine schnellere Schleifen Simulation.</span><span class="sxs-lookup"><span data-stu-id="46b7c-222">This helps reduce register load and enables faster loop simulation.</span></span>
- <span data-ttu-id="46b7c-223">O1: deaktiviert die Neuanordnen der Anweisung für ps_3_0 und aufwärts.</span><span class="sxs-lookup"><span data-stu-id="46b7c-223">O1 - Disables instruction reordering for ps_3_0 and up.</span></span>
- <span data-ttu-id="46b7c-224">O2-identisch mit O1.</span><span class="sxs-lookup"><span data-stu-id="46b7c-224">O2 - Same as O1.</span></span> <span data-ttu-id="46b7c-225">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="46b7c-225">Reserved for future use.</span></span>
- <span data-ttu-id="46b7c-226">O3-identisch mit O1.</span><span class="sxs-lookup"><span data-stu-id="46b7c-226">O3 - Same as O1.</span></span> <span data-ttu-id="46b7c-227">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="46b7c-227">Reserved for future use.</span></span>

##### <a name="p-file"></a><span data-ttu-id="46b7c-228">/P <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-228">/P <*file*></span></span>
<span data-ttu-id="46b7c-229">In Datei Vorverarbeiten (muss alleine verwendet werden).</span><span class="sxs-lookup"><span data-stu-id="46b7c-229">Preprocess to file (must be used alone).</span></span>

##### <a name="qstrip_debug"></a><span data-ttu-id="46b7c-230">/Qstrip_debug</span><span class="sxs-lookup"><span data-stu-id="46b7c-230">/Qstrip_debug</span></span>
<span data-ttu-id="46b7c-231">Entfernen Sie Debugdaten aus Shader-Bytecode für 4_0 +-Profile.</span><span class="sxs-lookup"><span data-stu-id="46b7c-231">Strip debug data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_priv"></a><span data-ttu-id="46b7c-232">/Qstrip_priv</span><span class="sxs-lookup"><span data-stu-id="46b7c-232">/Qstrip_priv</span></span>
<span data-ttu-id="46b7c-233">Entfernen Sie die privaten Daten aus 4_0 + Shader-Bytecode.</span><span class="sxs-lookup"><span data-stu-id="46b7c-233">Strip the private data from 4_0+ shader bytecode.</span></span> <span data-ttu-id="46b7c-234">Entfernt private Daten (beliebige Bytefolge) aus dem Shader-BLOB (kompilierter Shader-Binärdatei), die Sie zuvor mit der Option eingebettet haben `/setprivate <file>` .</span><span class="sxs-lookup"><span data-stu-id="46b7c-234">Removes private data (arbitrary sequence of bytes) from the shader blob (compiled shader binary) that you previously embedded with the `/setprivate <file>` option.</span></span>

<span data-ttu-id="46b7c-235">Sie müssen die/dumpbin-Option mit/Qstrip_priv angeben.</span><span class="sxs-lookup"><span data-stu-id="46b7c-235">You must specify the /dumpbin option with /Qstrip_priv.</span></span> <span data-ttu-id="46b7c-236">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="46b7c-236">For example:</span></span>

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a><span data-ttu-id="46b7c-237">/Qstrip_reflect</span><span class="sxs-lookup"><span data-stu-id="46b7c-237">/Qstrip_reflect</span></span>
<span data-ttu-id="46b7c-238">Entfernen Sie reflektionsdaten aus Shader-Bytecode für 4_0 +-Profile.</span><span class="sxs-lookup"><span data-stu-id="46b7c-238">Strip reflection data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_rootsignature"></a><span data-ttu-id="46b7c-239">/Qstrip_rootsignature</span><span class="sxs-lookup"><span data-stu-id="46b7c-239">/Qstrip_rootsignature</span></span>
<span data-ttu-id="46b7c-240">Stamm Signatur aus Shader-Bytecode entfernen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-240">Strip root signature from shader bytecode.</span></span> <span data-ttu-id="46b7c-241">Neu für Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="46b7c-241">New for Direct3D 12.</span></span>

##### <a name="res_may_alias"></a><span data-ttu-id="46b7c-242">/res_may_alias</span><span class="sxs-lookup"><span data-stu-id="46b7c-242">/res_may_alias</span></span>
<span data-ttu-id="46b7c-243">Angenommen, UAVs/Srvs können für cs_5_0 + Alias Alias sein.</span><span class="sxs-lookup"><span data-stu-id="46b7c-243">Assume that UAVs/SRVs may alias for cs_5_0+.</span></span> <span data-ttu-id="46b7c-244">Erfordert den D3dcompiler- \_47.dll oder eine spätere Version der dll.</span><span class="sxs-lookup"><span data-stu-id="46b7c-244">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="setprivate-file"></a><span data-ttu-id="46b7c-245">/setprivate <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-245">/setprivate <*file*></span></span>
<span data-ttu-id="46b7c-246">Fügen Sie dem kompilierten Shader-BLOB private Daten in der angegebenen Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="46b7c-246">Add private data in the given file to the compiled shader blob.</span></span> <span data-ttu-id="46b7c-247">Bettet die angegebene Datei, die als rohpuffer behandelt wird, in das Shader-BLOB ein.</span><span class="sxs-lookup"><span data-stu-id="46b7c-247">Embeds the given file, which is treated as a raw buffer, to the shader blob.</span></span> <span data-ttu-id="46b7c-248">Verwenden Sie/setprivate, um beim Kompilieren eines Shaders private Daten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-248">Use /setprivate to add private data when you compile a shader.</span></span> <span data-ttu-id="46b7c-249">Sie können auch die/dumpbin-Option mit/setprivate verwenden, um ein vorhandenes Shader-Objekt zu laden, und nachdem sich das Objekt im Arbeitsspeicher befindet, um das private dateiblob hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-249">Or, use the /dumpbin option with /setprivate to load an existing shader object, and then after the object is in memory, to add the private data blob.</span></span> <span data-ttu-id="46b7c-250">Verwenden Sie z. b. entweder einen einzelnen Befehl mit/setprivate, um einem kompilierten Shader-BLOB private Daten hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="46b7c-250">For example, use either a single command with /setprivate to add private data to a compiled shader blob:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
<span data-ttu-id="46b7c-251">Oder verwenden Sie zwei Befehle, bei denen der zweite Befehl ein Shader-Objekt lädt und dann private Daten hinzufügt:</span><span class="sxs-lookup"><span data-stu-id="46b7c-251">Or, use two commands where the second command loads a shader object and then adds private data:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a><span data-ttu-id="46b7c-252">/setrootsignature <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-252">/setrootsignature <*file*></span></span>
<span data-ttu-id="46b7c-253">Fügt die Stammsignatur an Shader-Bytecode an.</span><span class="sxs-lookup"><span data-stu-id="46b7c-253">Attach root signature to shader bytecode.</span></span> <span data-ttu-id="46b7c-254">Neu für Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="46b7c-254">New for Direct3D 12.</span></span>

##### <a name="shtemplate-file"></a><span data-ttu-id="46b7c-255">/shtemplate <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-255">/shtemplate <*file*></span></span>
<span data-ttu-id="46b7c-256">Verwenden Sie die angegebene Vorlagen-shaderdatei zum Zusammenführen (/mergeUAVs) und zum Abgleichen von (/matchUAVs) Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-256">Use given template shader file for merging (/mergeUAVs) and matching (/matchUAVs) resources.</span></span> <span data-ttu-id="46b7c-257">Weitere Informationen finden Sie unter " <a href="#remarks">Hinweise</a>".</span><span class="sxs-lookup"><span data-stu-id="46b7c-257">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="vd"></a><span data-ttu-id="46b7c-258">/VD</span><span class="sxs-lookup"><span data-stu-id="46b7c-258">/Vd</span></span>
<span data-ttu-id="46b7c-259">Deaktivieren Sie die Validierung.</span><span class="sxs-lookup"><span data-stu-id="46b7c-259">Disable validation.</span></span>

##### <a name="verifyrootsignature-file"></a><span data-ttu-id="46b7c-260">/verifyrootsignature <*Datei*></span><span class="sxs-lookup"><span data-stu-id="46b7c-260">/verifyrootsignature <*file*></span></span>
<span data-ttu-id="46b7c-261">Überprüfen Sie den Shader-Bytecode anhand der Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="46b7c-261">Verify shader bytecode against root signature.</span></span> <span data-ttu-id="46b7c-262">Neu für Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="46b7c-262">New for Direct3D 12.</span></span>

##### <a name="vi"></a><span data-ttu-id="46b7c-263">/Vi</span><span class="sxs-lookup"><span data-stu-id="46b7c-263">/Vi</span></span>
<span data-ttu-id="46b7c-264">Zeigt Details zum include-Prozess an.</span><span class="sxs-lookup"><span data-stu-id="46b7c-264">Display details about the include process.</span></span>

##### <a name="vn-name"></a><span data-ttu-id="46b7c-265">/VN <*Name*></span><span class="sxs-lookup"><span data-stu-id="46b7c-265">/Vn <*name*></span></span>
<span data-ttu-id="46b7c-266">Verwenden Sie den Namen als Variablennamen in der Header Datei.</span><span class="sxs-lookup"><span data-stu-id="46b7c-266">Use name as variable name in header file.</span></span>

##### <a name="wx"></a><span data-ttu-id="46b7c-267">/WX</span><span class="sxs-lookup"><span data-stu-id="46b7c-267">/WX</span></span>
<span data-ttu-id="46b7c-268">Behandeln Sie Warnungen als Fehler.</span><span class="sxs-lookup"><span data-stu-id="46b7c-268">Treat warnings as errors.</span></span>

##### <a name="zi"></a><span data-ttu-id="46b7c-269">/ZI</span><span class="sxs-lookup"><span data-stu-id="46b7c-269">/Zi</span></span>
<span data-ttu-id="46b7c-270">Aktiviert Debuginformationen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-270">Enable debugging information.</span></span>

##### <a name="zpc"></a><span data-ttu-id="46b7c-271">/Zpc</span><span class="sxs-lookup"><span data-stu-id="46b7c-271">/Zpc</span></span>
<span data-ttu-id="46b7c-272">Paket Matrizen in der Spalte-Haupt Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="46b7c-272">Pack matrices in column-major order.</span></span>

##### <a name="zpr"></a><span data-ttu-id="46b7c-273">/Zpr</span><span class="sxs-lookup"><span data-stu-id="46b7c-273">/Zpr</span></span>
<span data-ttu-id="46b7c-274">Paket Matrizen in Zeilen-Haupt Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="46b7c-274">Pack matrices in row-major order.</span></span>

### <a name="filenames"></a><span data-ttu-id="46b7c-275">*Dateinamen*</span><span class="sxs-lookup"><span data-stu-id="46b7c-275">*Filenames*</span></span>

<span data-ttu-id="46b7c-276">\[in \] den Dateien, die die Shader (s) und/oder die Auswirkung (e) enthalten.</span><span class="sxs-lookup"><span data-stu-id="46b7c-276">\[in\] The files that contains the shader(s) and/or the effect(s).</span></span>

## <a name="remarks"></a><span data-ttu-id="46b7c-277">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46b7c-277">Remarks</span></span>

<span data-ttu-id="46b7c-278">Verwenden `/mergeUAVs` Sie die `/matchUAVs` Optionen, und `/shtemplate` , um die UAV-Bindungs Slots für eine Kette von Shadern auszurichten.</span><span class="sxs-lookup"><span data-stu-id="46b7c-278">Use the `/mergeUAVs`, `/matchUAVs`, and `/shtemplate` options to align the UAV binding slots for a chain of shaders.</span></span>

<span data-ttu-id="46b7c-279">Angenommen, Sie verfügen über Shader A. FX, B. FX und C. fx.</span><span class="sxs-lookup"><span data-stu-id="46b7c-279">Suppose you have shaders A.fx, B.fx, and C.fx.</span></span> <span data-ttu-id="46b7c-280">Um die UAV-Bindungs Slots für diese Kette von Shader auszurichten, benötigen Sie zwei durch Führungen der Kompilierung:</span><span class="sxs-lookup"><span data-stu-id="46b7c-280">To align the UAV binding slots for this chain of shaders, you need two passes of compilation:</span></span>

<span data-ttu-id="46b7c-281">**So richten Sie die UAV-Bindungs Slots für eine Kette von Shadern aus**</span><span class="sxs-lookup"><span data-stu-id="46b7c-281">**To align the UAV binding slots for a chain of shaders**</span></span>

1.  <span data-ttu-id="46b7c-282">Verwenden Sie/mergeUAVs, um Shader zu kompilieren, und geben Sie ein zuvor kompiliertes Shader-BLOB mit/shtemplate. an.</span><span class="sxs-lookup"><span data-stu-id="46b7c-282">Use /mergeUAVs to compile shaders, and specify a previously-compiled shader blob with /shtemplate.</span></span> <span data-ttu-id="46b7c-283">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="46b7c-283">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  <span data-ttu-id="46b7c-284">Verwenden Sie/matchUAVs, um Shader zu kompilieren, und geben Sie das letzte Shader-BLOB aus dem ersten Durchlauf mit/shtemplate. an.</span><span class="sxs-lookup"><span data-stu-id="46b7c-284">Use /matchUAVs to compile shaders, and specify the last shader blob from the first pass with /shtemplate.</span></span> <span data-ttu-id="46b7c-285">Sie können in beliebiger Reihenfolge kompilieren.</span><span class="sxs-lookup"><span data-stu-id="46b7c-285">You can compile in any order.</span></span> <span data-ttu-id="46b7c-286">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="46b7c-286">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
<span data-ttu-id="46b7c-287">C. FX muss im zweiten Durchlauf nicht neu kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="46b7c-287">You don't have to recompile C.fx in the second pass.</span></span>

<span data-ttu-id="46b7c-288">Nachdem Sie die vorherigen beiden Kompilierungs Durchläufen durchgeführt haben, können Sie A. o, B. o und C. o als abschließende Shader-BLOBs mit ausgerichteten UAV-Slots verwenden.</span><span class="sxs-lookup"><span data-stu-id="46b7c-288">After you perform the preceding two compilation passes, you can use A.o, B.o, and C.o as final shader blobs with aligned UAV slots.</span></span>

## <a name="profiles"></a><span data-ttu-id="46b7c-289">Profiles</span><span class="sxs-lookup"><span data-stu-id="46b7c-289">Profiles</span></span>

<span data-ttu-id="46b7c-290">Jedes Shader-Modell wird mit einem HLSL-Profil bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="46b7c-290">Each shader model is labeled with an HLSL profile.</span></span> <span data-ttu-id="46b7c-291">Um einen Shader für ein bestimmtes Shader-Modell zu kompilieren, wählen Sie das entsprechende Shader-Profil aus der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="46b7c-291">To compile a shader against a particular shader model, choose the appropriate shader profile from the following table.</span></span>

<table><thead><tr class="header"><th><span data-ttu-id="46b7c-292">Shadertyp</span><span class="sxs-lookup"><span data-stu-id="46b7c-292">Shader Type</span></span></th><th><span data-ttu-id="46b7c-293">Profiles</span><span class="sxs-lookup"><span data-stu-id="46b7c-293">Profiles</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="46b7c-294">Compute-Shader</span><span class="sxs-lookup"><span data-stu-id="46b7c-294">Compute Shader</span></span></td><td><dl> <span data-ttu-id="46b7c-295">cs_4_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-295">cs_4_0</span></span><br />
<span data-ttu-id="46b7c-296">cs_4_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-296">cs_4_1</span></span><br />
<span data-ttu-id="46b7c-297">cs_5_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-297">cs_5_0</span></span><br />
<span data-ttu-id="46b7c-298">cs_5_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-298">cs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="46b7c-299">Domain-Shader</span><span class="sxs-lookup"><span data-stu-id="46b7c-299">Domain Shader</span></span></td><td><dl> <span data-ttu-id="46b7c-300">ds_5_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-300">ds_5_0</span></span><br />
<span data-ttu-id="46b7c-301">ds_5_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-301">ds_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="46b7c-302">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="46b7c-302">Geometry Shader</span></span></td><td><dl> <span data-ttu-id="46b7c-303">gs_4_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-303">gs_4_0</span></span><br />
<span data-ttu-id="46b7c-304">gs_4_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-304">gs_4_1</span></span><br />
<span data-ttu-id="46b7c-305">gs_5_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-305">gs_5_0</span></span><br />
<span data-ttu-id="46b7c-306">gs_5_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-306">gs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="46b7c-307">HLSL-Shader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="46b7c-307">HLSL shader linking</span></span> </td><td><dl> <span data-ttu-id="46b7c-308">lib_4_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-308">lib_4_0</span></span><br />
<span data-ttu-id="46b7c-309">lib_4_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-309">lib_4_1</span></span><br />
<span data-ttu-id="46b7c-310">lib_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-310">lib_4_0_level_9_1</span></span><br />
<span data-ttu-id="46b7c-311">lib_4_0_level_9_1_vs_only</span><span class="sxs-lookup"><span data-stu-id="46b7c-311">lib_4_0_level_9_1_vs_only</span></span><br />
<span data-ttu-id="46b7c-312">lib_4_0_level_9_1_ps_only</span><span class="sxs-lookup"><span data-stu-id="46b7c-312">lib_4_0_level_9_1_ps_only</span></span><br />
<span data-ttu-id="46b7c-313">lib_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="46b7c-313">lib_4_0_level_9_3</span></span><br />
<span data-ttu-id="46b7c-314">lib_4_0_level_9_3_vs_only</span><span class="sxs-lookup"><span data-stu-id="46b7c-314">lib_4_0_level_9_3_vs_only</span></span><br />
<span data-ttu-id="46b7c-315">lib_4_0_level_9_3_ps_only</span><span class="sxs-lookup"><span data-stu-id="46b7c-315">lib_4_0_level_9_3_ps_only</span></span><br />
<span data-ttu-id="46b7c-316">lib_5_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-316">lib_5_0</span></span><br />
</dl> <span data-ttu-id="46b7c-317">Weitere Informationen zum Verknüpfen von Shader finden Sie unter <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> und <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="46b7c-317">For more info about shader linking, see <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> and <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span></span> <br/></td></tr><tr class="odd"><td><span data-ttu-id="46b7c-318">Rumpf-Shader</span><span class="sxs-lookup"><span data-stu-id="46b7c-318">Hull Shader</span></span></td><td><dl> <span data-ttu-id="46b7c-319">hs_5_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-319">hs_5_0</span></span><br />
<span data-ttu-id="46b7c-320">hs_5_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-320">hs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="46b7c-321">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="46b7c-321">Pixel Shader</span></span></td><td><dl> <span data-ttu-id="46b7c-322">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-322">ps_2_0</span></span><br />
<span data-ttu-id="46b7c-323">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="46b7c-323">ps_2_a</span></span><br />
<span data-ttu-id="46b7c-324">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="46b7c-324">ps_2_b</span></span><br />
<span data-ttu-id="46b7c-325">ps_2_sw</span><span class="sxs-lookup"><span data-stu-id="46b7c-325">ps_2_sw</span></span><br />
<span data-ttu-id="46b7c-326">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-326">ps_3_0</span></span><br />
<span data-ttu-id="46b7c-327">ps_3_sw</span><span class="sxs-lookup"><span data-stu-id="46b7c-327">ps_3_sw</span></span><br />
<span data-ttu-id="46b7c-328">ps_4_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-328">ps_4_0</span></span><br />
<span data-ttu-id="46b7c-329">ps_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-329">ps_4_0_level_9_0</span></span><br />
<span data-ttu-id="46b7c-330">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-330">ps_4_0_level_9_1</span></span><br />
<span data-ttu-id="46b7c-331">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="46b7c-331">ps_4_0_level_9_3</span></span><br />
<span data-ttu-id="46b7c-332">ps_4_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-332">ps_4_1</span></span><br />
<span data-ttu-id="46b7c-333">ps_5_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-333">ps_5_0</span></span><br />
<span data-ttu-id="46b7c-334">ps_5_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-334">ps_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="46b7c-335">Stamm Signatur</span><span class="sxs-lookup"><span data-stu-id="46b7c-335">Root Signature</span></span></td><td><dl> <span data-ttu-id="46b7c-336">rootsig_1_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-336">rootsig_1_0</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="46b7c-337">Textur-Shader</span><span class="sxs-lookup"><span data-stu-id="46b7c-337">Texture Shader</span></span></td><td><dl> <span data-ttu-id="46b7c-338">tx_1_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-338">tx_1_0</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="46b7c-339">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="46b7c-339">Vertex Shader</span></span></td><td><dl> <span data-ttu-id="46b7c-340">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-340">vs_1_1</span></span><br />
<span data-ttu-id="46b7c-341">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-341">vs_2_0</span></span><br />
<span data-ttu-id="46b7c-342">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="46b7c-342">vs_2_a</span></span><br />
<span data-ttu-id="46b7c-343">vs_2_sw</span><span class="sxs-lookup"><span data-stu-id="46b7c-343">vs_2_sw</span></span><br />
<span data-ttu-id="46b7c-344">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-344">vs_3_0</span></span><br />
<span data-ttu-id="46b7c-345">vs_3_sw</span><span class="sxs-lookup"><span data-stu-id="46b7c-345">vs_3_sw</span></span><br />
<span data-ttu-id="46b7c-346">vs_4_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-346">vs_4_0</span></span><br />
<span data-ttu-id="46b7c-347">vs_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-347">vs_4_0_level_9_0</span></span><br />
<span data-ttu-id="46b7c-348">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-348">vs_4_0_level_9_1</span></span><br />
<span data-ttu-id="46b7c-349">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="46b7c-349">vs_4_0_level_9_3</span></span><br />
<span data-ttu-id="46b7c-350">vs_4_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-350">vs_4_1</span></span><br />
<span data-ttu-id="46b7c-351">vs_5_0</span><span class="sxs-lookup"><span data-stu-id="46b7c-351">vs_5_0</span></span><br />
<span data-ttu-id="46b7c-352">vs_5_1</span><span class="sxs-lookup"><span data-stu-id="46b7c-352">vs_5_1</span></span><br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a><span data-ttu-id="46b7c-353">Versions Hinweise</span><span class="sxs-lookup"><span data-stu-id="46b7c-353">Version notes</span></span>

<span data-ttu-id="46b7c-354">Direct3D 12 finden Sie unter [Angeben von Stamm Signaturen in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Ressourcen Bindung in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) und [dynamischer Indizierung mit HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span><span class="sxs-lookup"><span data-stu-id="46b7c-354">For Direct3D 12 refer to [Specifying Root Signatures in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Resource Binding in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) and [Dynamic Indexing using HLSL 5.1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span></span>

<span data-ttu-id="46b7c-355">Verwenden Sie in Direct3D 10 die API, um das Vertex-, Geometrie-und Pixel-Shader-Profil zu erhalten, das für ein bestimmtes Gerät am besten geeignet ist, indem Sie die folgenden Funktionen aufrufen: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)und [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="46b7c-355">In Direct3D 10 use the API to get the vertex, geometry, and pixel-shader profile best suited to a given device by calling these functions: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile), and [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span></span>

<span data-ttu-id="46b7c-356">In Direct3D 9 verwenden Sie die [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) -Methode oder die [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) -Methode, um die von einem Gerät unterstützten Scheitelpunkt-und Pixel-Shader-Profile abzurufen.</span><span class="sxs-lookup"><span data-stu-id="46b7c-356">In Direct3D 9 use the [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) or [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) methods to retrieve the vertex and pixel-shader profiles supported by a device.</span></span> <span data-ttu-id="46b7c-357">Die von diesen Methoden zurückgegebene [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) -Struktur gibt die Vertex-und Pixel-Shader-Profile an, die von einem Gerät in seinen **VertexShaderVersion** -und **PixelShaderVersion** -Membern unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="46b7c-357">The [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure returned by those methods indicates the vertex and pixel-shader profiles supported by a device in its **VertexShaderVersion** and **PixelShaderVersion** members.</span></span>

<span data-ttu-id="46b7c-358">Beispiele finden Sie unter [Kompilieren mit dem aktuellen Compiler](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="46b7c-358">For examples, see [Compiling with the Current Compiler](dx-graphics-tools-fxc-using.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46b7c-359">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46b7c-359">Related topics</span></span>

* [<span data-ttu-id="46b7c-360">Effekt-Compilertool</span><span class="sxs-lookup"><span data-stu-id="46b7c-360">Effect-Compiler Tool</span></span>](fxc.md)