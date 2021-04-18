---
description: Der Quell Server ermöglicht einem Client das Abrufen der exakten Version der Quelldateien, die zum Erstellen einer Anwendung verwendet wurden.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Quellserver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8d76c70b67c176126d8e424bd5b55b616697
ms.sourcegitcommit: bfb5d94f754d017307b4cc9d914a2716701331d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355083"
---
# <a name="source-server"></a><span data-ttu-id="4219f-103">Quellserver</span><span class="sxs-lookup"><span data-stu-id="4219f-103">Source Server</span></span>

<span data-ttu-id="4219f-104">Der Quell Server ermöglicht einem Client das Abrufen der exakten Version der Quelldateien, die zum Erstellen einer Anwendung verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="4219f-104">Source server enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="4219f-105">Da sich der Quellcode für ein Modul Zwischenversionen und im Laufe der Jahre ändern kann, ist es wichtig, sich den Quellcode anzusehen, wie er vorhanden war, als die Version des fraglichen Moduls erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4219f-105">Because the source code for a module can change between versions and over a course of years, it is important to look at the source code as it existed when the version of the module in question was built.</span></span>

<span data-ttu-id="4219f-106">Der Quell Server Ruft die entsprechenden Dateien aus der Quell Code Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="4219f-106">Source server retrieves the appropriate files from source control.</span></span> <span data-ttu-id="4219f-107">Um den Quell Server verwenden zu können, muss die Anwendung als Quell Indizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4219f-107">To use source server, the application must have been source indexed.</span></span>

## <a name="source-indexing"></a><span data-ttu-id="4219f-108">Quell Indizierung</span><span class="sxs-lookup"><span data-stu-id="4219f-108">Source Indexing</span></span>

<span data-ttu-id="4219f-109">Das Quell Indizierungs System ist eine Sammlung von ausführbaren Dateien und Perl-Skripts.</span><span class="sxs-lookup"><span data-stu-id="4219f-109">The source indexing system is a collection of executable files and Perl scripts.</span></span> <span data-ttu-id="4219f-110">Die Perl-Skripts erfordern perl 5,6 oder höher.</span><span class="sxs-lookup"><span data-stu-id="4219f-110">The Perl scripts require Perl 5.6 or greater.</span></span>

<span data-ttu-id="4219f-111">Im Allgemeinen sind Binärdateien während des Buildprozesses Quell indiziert, nachdem die Anwendung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4219f-111">Generally, binaries are source indexed during the build process after the application has been built.</span></span> <span data-ttu-id="4219f-112">Die vom Quell Server benötigten Informationen werden in den PDB-Dateien gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4219f-112">The information needed by source server is stored in the PDB files.</span></span>

<span data-ttu-id="4219f-113">Der Quell Server ist zurzeit mit Skripts ausgeliefert, die mit den folgenden Quell Code Verwaltungssystemen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="4219f-113">Source server currently ships with scripts that should work with the following source-control systems.</span></span>

-   <span data-ttu-id="4219f-114">Team Foundation Server</span><span class="sxs-lookup"><span data-stu-id="4219f-114">Team Foundation Server</span></span>
-   <span data-ttu-id="4219f-115">Perforce</span><span class="sxs-lookup"><span data-stu-id="4219f-115">Perforce</span></span>
-   <span data-ttu-id="4219f-116">Visual SourceSafe</span><span class="sxs-lookup"><span data-stu-id="4219f-116">Visual SourceSafe</span></span>
-   <span data-ttu-id="4219f-117">CVS</span><span class="sxs-lookup"><span data-stu-id="4219f-117">CVS</span></span>
-   <span data-ttu-id="4219f-118">Subversion</span><span class="sxs-lookup"><span data-stu-id="4219f-118">Subversion</span></span>

<span data-ttu-id="4219f-119">Sie können auch ein benutzerdefiniertes Skript erstellen, um den Code für ein anderes Quell Code Verwaltungssystem zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="4219f-119">You can also create a custom script to index your code for a different source-control system.</span></span>

<span data-ttu-id="4219f-120">In der folgenden Tabelle sind die Quell Server Tools aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4219f-120">The following table lists the source server tools.</span></span>



| <span data-ttu-id="4219f-121">Tool</span><span class="sxs-lookup"><span data-stu-id="4219f-121">Tool</span></span>        | <span data-ttu-id="4219f-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4219f-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4219f-123">Srcsrv.ini</span><span class="sxs-lookup"><span data-stu-id="4219f-123">Srcsrv.ini</span></span>  | <span data-ttu-id="4219f-124">Diese Datei ist die Masterliste aller Quell Code Verwaltungs Server.</span><span class="sxs-lookup"><span data-stu-id="4219f-124">This file is the master list of all source control servers.</span></span> <span data-ttu-id="4219f-125">Jeder Eintrag weist das folgende Format auf:*myserver* = *Server Info*</span><span class="sxs-lookup"><span data-stu-id="4219f-125">Each entry has the following format:*MYSERVER*=*serverinfo*</span></span><br/> <span data-ttu-id="4219f-126">Bei der Verwendung von Perforce bestehen die Server Informationen aus dem vollständigen Netzwerkpfad zum Server, gefolgt von einem Doppelpunkt und der verwendeten Portnummer.</span><span class="sxs-lookup"><span data-stu-id="4219f-126">When using Perforce, the server info consists of the full network path to the server, followed by a colon, followed by the port number it uses.</span></span> <span data-ttu-id="4219f-127">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4219f-127">For example:</span></span><br/> <span data-ttu-id="4219f-128">MyServer = Machine. Corp. Company. com: 1666</span><span class="sxs-lookup"><span data-stu-id="4219f-128">MYSERVER=machine.corp.company.com:1666</span></span><br/> <span data-ttu-id="4219f-129">Diese Datei kann auf dem Computer installiert werden, auf dem der Debugger ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4219f-129">This file can be installed on the computer running the debugger.</span></span> <span data-ttu-id="4219f-130">Wenn der Quell Server gestartet wird, wird Srcsrv.ini nach Werten untersucht. Diese Werte überschreiben die Informationen, die in der PDB-Datei enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4219f-130">When source server starts, it looks at Srcsrv.ini for values; these values will override the information contained in the PDB file.</span></span> <span data-ttu-id="4219f-131">Dadurch können Benutzer einen Debugger so konfigurieren, dass zur Debugzeit ein alternativer Quell Code Verwaltungs Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4219f-131">This enables users to configure a debugger to use an alternate source control server at debug time.</span></span><br/> <span data-ttu-id="4219f-132">Weitere Informationen finden Sie im Beispiel Srcsrv.ini, das mit den Quell Server Tools installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4219f-132">For more information, see the example Srcsrv.ini installed with the source server tools.</span></span><br/> |
| <span data-ttu-id="4219f-133">SSINDEX. cmd</span><span class="sxs-lookup"><span data-stu-id="4219f-133">Ssindex.cmd</span></span> | <span data-ttu-id="4219f-134">Mit diesem Skript wird die Liste der in die Quell Code Verwaltung eingecheckten Dateien zusammen mit den Versionsinformationen der einzelnen Dateien erstellt.</span><span class="sxs-lookup"><span data-stu-id="4219f-134">This script builds the list of files checked into source control along with the version information of each file.</span></span> <span data-ttu-id="4219f-135">Sie speichert eine Teilmenge dieser Informationen in den PDB-Dateien, die beim Erstellen der Anwendung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="4219f-135">It stores a subset of this information in the .pdb files generated when you built the application.</span></span> <span data-ttu-id="4219f-136">Das Skript verwendet eines der folgenden Perl-Module, um eine Schnittstelle mit der Quell Code Verwaltung zu erstellen: P4.pm (Perforce) oder VSS.pm (Visual Source Safe). Um weitere Informationen zu erhalten, führen Sie das Skript mit dem-? aus.</span><span class="sxs-lookup"><span data-stu-id="4219f-136">The script uses one of the following Perl modules to interface with source control: P4.pm (Perforce) or Vss.pm (Visual Source Safe).For more information, run the script with the -?</span></span> <span data-ttu-id="4219f-137">oder-??</span><span class="sxs-lookup"><span data-stu-id="4219f-137">or -??</span></span> <span data-ttu-id="4219f-138">(Ausführliche Hilfe) oder untersuchen Sie das Skript.</span><span class="sxs-lookup"><span data-stu-id="4219f-138">(verbose help) option or examine the script.</span></span><br/>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="4219f-139">Srctool.exe</span><span class="sxs-lookup"><span data-stu-id="4219f-139">Srctool.exe</span></span> | <span data-ttu-id="4219f-140">Dieses Hilfsprogramm listet alle Dateien auf, die in einer PDB-Datei indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4219f-140">This utility lists all files indexed within a .pdb file.</span></span> <span data-ttu-id="4219f-141">Für jede Datei werden der vollständige Pfad, der Quell Code Verwaltungs Server und die Versionsnummer der Datei aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4219f-141">For each file, it lists the full path, source control server, and version number of the file.</span></span> <span data-ttu-id="4219f-142">Sie können diese Informationen verwenden, um Dateien abzurufen, ohne den Quell Server zu verwenden. Um weitere Informationen zu erhalten, führen Sie das Hilfsprogramm mit dem/?</span><span class="sxs-lookup"><span data-stu-id="4219f-142">You can use this information to retrieve files without using the source server.For more information, run the utility with the /?</span></span> <span data-ttu-id="4219f-143">(Neuen Branch erstellen und Pull Request starten).</span><span class="sxs-lookup"><span data-stu-id="4219f-143">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="4219f-144">Pdbstr.exe</span><span class="sxs-lookup"><span data-stu-id="4219f-144">Pdbstr.exe</span></span>  | <span data-ttu-id="4219f-145">Dieses Hilfsprogramm wird von den Indizierungs Skripts verwendet, um die Versions Kontrollinformationen in den alternativen Stream "SRCSRV" der PDB-Ziel Datei einzufügen.</span><span class="sxs-lookup"><span data-stu-id="4219f-145">This utility is used by the indexing scripts to insert the version control information into the "srcsrv" alternate stream of the target .pdb file.</span></span> <span data-ttu-id="4219f-146">Außerdem kann jeder Stream aus einer PDB-Datei gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="4219f-146">It can also read any stream from a .pdb file.</span></span> <span data-ttu-id="4219f-147">Sie können diese Informationen verwenden, um zu überprüfen, ob die Indizierungs Skripts ordnungsgemäß funktionieren. Um weitere Informationen zu erhalten, führen Sie das Hilfsprogramm mit dem/?</span><span class="sxs-lookup"><span data-stu-id="4219f-147">You can use this information to verify that the indexing scripts are working properly.For more information, run the utility with the /?</span></span> <span data-ttu-id="4219f-148">(Neuen Branch erstellen und Pull Request starten).</span><span class="sxs-lookup"><span data-stu-id="4219f-148">option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a><span data-ttu-id="4219f-149">Abrufen der Quelldatei</span><span class="sxs-lookup"><span data-stu-id="4219f-149">Retrieving the Source File</span></span>

<span data-ttu-id="4219f-150">Die dbghelp-API ermöglicht den Zugriff auf die Quell Serverfunktionen über die [**symgetsourcefile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4219f-150">The DbgHelp API provides access to source server functionality through the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span> <span data-ttu-id="4219f-151">Um den Namen der abzurufenden Quelldatei abzurufen, rufen Sie die [**symenum SourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) -oder [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="4219f-151">To retrieve the name of the source file to be retrieved, call the [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) or [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) function.</span></span>

## <a name="using-source-server-with-a-debugger"></a><span data-ttu-id="4219f-152">Verwenden des Quell Servers mit einem Debugger</span><span class="sxs-lookup"><span data-stu-id="4219f-152">Using Source Server with a Debugger</span></span>

<span data-ttu-id="4219f-153">Um den Quell Server mit WinDbg, KD, NZD oder cdb zu verwenden, stellen Sie sicher, dass Sie eine aktuelle Version der Debugtools für Windows-Paket (Version 6,3 oder höher) installiert haben.</span><span class="sxs-lookup"><span data-stu-id="4219f-153">To use the source server with WinDbg, KD, NTSD, or CDB, ensure that you have installed a recent version of the Debugging Tools for Windows package (version 6.3 or later).</span></span> <span data-ttu-id="4219f-154">Fügen Sie dann SRV \* wie folgt in den SRCPATH-Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="4219f-154">Then, include srv\* in the .srcpath command as follows:</span></span>

<span data-ttu-id="4219f-155">**\. SRCPATH SRV \* ;** _c: \\ meinquelle_</span><span class="sxs-lookup"><span data-stu-id="4219f-155">**\.srcpath srv\*;**_c:\\mysource_</span></span>

<span data-ttu-id="4219f-156">Beachten Sie, dass dieses Beispiel auch einen herkömmlichen Quellpfad enthält.</span><span class="sxs-lookup"><span data-stu-id="4219f-156">Note that this example also includes a traditional source path.</span></span> <span data-ttu-id="4219f-157">Wenn der Debugger die Datei nicht vom Quell Server abrufen kann, wird der angegebene Pfad durchsucht.</span><span class="sxs-lookup"><span data-stu-id="4219f-157">If the debugger cannot retrieve the file from the source server, it will search the specified path.</span></span>

<span data-ttu-id="4219f-158">Wenn eine Quelldatei vom Quell Server abgerufen wird, bleibt Sie nach der Debugsitzung auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="4219f-158">If a source file is retrieved by the source server, it will remain on your hard drive after the debugging session is over.</span></span> <span data-ttu-id="4219f-159">Quelldateien werden lokal im Unterverzeichnis src des Installationsverzeichnisses Debugtools für Windows gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4219f-159">Source files are stored locally in the src subdirectory of the Debugging Tools for Windows installation directory.</span></span>

## <a name="source-server-data-blocks"></a><span data-ttu-id="4219f-160">Quell Server-Datenblöcke</span><span class="sxs-lookup"><span data-stu-id="4219f-160">Source Server Data Blocks</span></span>

<span data-ttu-id="4219f-161">Der Quell Server basiert auf zwei Datenblöcken in der PDB-Datei.</span><span class="sxs-lookup"><span data-stu-id="4219f-161">Source server relies on two blocks of data within the PDB file.</span></span>

-   <span data-ttu-id="4219f-162">Liste der Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="4219f-162">Source file list.</span></span> <span data-ttu-id="4219f-163">Beim Erstellen eines Moduls wird automatisch eine Liste der voll qualifizierten Pfade zu den Quelldateien erstellt, die zum Erstellen des Moduls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4219f-163">Building a module automatically creates a list of fully qualified paths to the source files used to build the module.</span></span>
-   <span data-ttu-id="4219f-164">Datenblock.</span><span class="sxs-lookup"><span data-stu-id="4219f-164">Data block.</span></span> <span data-ttu-id="4219f-165">Wenn Sie die Quelle wie zuvor beschrieben indizieren, wird der PDB-Datei mit dem Namen "SRCSRV" ein alternativer Datenstrom hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4219f-165">Indexing the source as described previously adds an alternate stream to the PDB file named "srcsrv".</span></span> <span data-ttu-id="4219f-166">Das Skript, das diese Daten einfügt, hängt vom jeweiligen Buildprozess und dem verwendeten Quell Code Verwaltungssystem ab.</span><span class="sxs-lookup"><span data-stu-id="4219f-166">The script that inserts this data is dependent on the specific build process and source control system in use.</span></span>

<span data-ttu-id="4219f-167">In der Sprachspezifikation Version 1 ist der Datenblock in drei Abschnitte unterteilt: ini, Variablen und Quelldateien.</span><span class="sxs-lookup"><span data-stu-id="4219f-167">In the language specification version 1, the data block is divided into three sections: ini, variables, and source files.</span></span> <span data-ttu-id="4219f-168">Sie weist die folgende Syntax auf.</span><span class="sxs-lookup"><span data-stu-id="4219f-168">It has the following syntax.</span></span>

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

<span data-ttu-id="4219f-169">Der gesamte Text wird buchstäblich interpretiert, mit Ausnahme von Text, der in Prozentzeichen (%) eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4219f-169">All text is interpreted literally, except for text enclosed in percent signs (%).</span></span> <span data-ttu-id="4219f-170">Text, der in Prozentzeichen eingeschlossen ist, wird als Variablenname behandelt, der rekursiv aufgelöst werden soll, es sei denn, er ist eine der folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="4219f-170">Text enclosed in percent signs is treated as a variable name to be resolved recursively, unless it is one of the following functions:</span></span>

<dl> <dt>

<span data-ttu-id="4219f-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>% fnvar%()</span><span class="sxs-lookup"><span data-stu-id="4219f-171"><span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()</span></span>
</dt> <dd>

<span data-ttu-id="4219f-172">Der Parameter Text muss in Prozentzeichen eingeschlossen und als zu erweiternde Variable behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="4219f-172">The parameter text should be enclosed in percent signs and treated as a variable to be expanded.</span></span>

</dd> <dt>

<span data-ttu-id="4219f-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%%() KSL</span><span class="sxs-lookup"><span data-stu-id="4219f-173"><span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()</span></span>
</dt> <dd>

<span data-ttu-id="4219f-174">Alle Schrägstriche (/) im Parameter Text sollten durch rückwärts Schrägstriche () ersetzt werden \\ .</span><span class="sxs-lookup"><span data-stu-id="4219f-174">All forward slashes (/) in the parameter text should be replaced with backward slashes (\\).</span></span>

</dd> <dt>

<span data-ttu-id="4219f-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>% fnfile%()</span><span class="sxs-lookup"><span data-stu-id="4219f-175"><span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()</span></span>
</dt> <dd>

<span data-ttu-id="4219f-176">Alle Pfadinformationen im Parameter Text sollten entfernt werden, sodass nur der Dateiname erhalten bleibt.</span><span class="sxs-lookup"><span data-stu-id="4219f-176">All path information in the parameter text should be stripped out, leaving only the file name.</span></span>

</dd> </dl>

<span data-ttu-id="4219f-177">Der ini-Abschnitt enthält Variablen, die die Anforderungen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4219f-177">The ini section contains variables that describe the requirements.</span></span> <span data-ttu-id="4219f-178">Das Indizierungs Skript kann diesem Abschnitt beliebig viele Variablen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4219f-178">The indexing script can add any number of variables to this section.</span></span> <span data-ttu-id="4219f-179">Hier finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="4219f-179">The following are examples:</span></span>

<dl> <dt>

<span data-ttu-id="4219f-180"><span id="VERSION"></span><span id="version"></span>Version</span><span class="sxs-lookup"><span data-stu-id="4219f-180"><span id="VERSION"></span><span id="version"></span>VERSION</span></span>
</dt> <dd>

<span data-ttu-id="4219f-181">Die Version der Sprachspezifikation.</span><span class="sxs-lookup"><span data-stu-id="4219f-181">The language specification version.</span></span> <span data-ttu-id="4219f-182">Diese Variable ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4219f-182">This variable is required.</span></span>

</dd> <dt>

<span data-ttu-id="4219f-183"><span id="VERCTL"></span><span id="verctl"></span>Verctl</span><span class="sxs-lookup"><span data-stu-id="4219f-183"><span id="VERCTL"></span><span id="verctl"></span>VERCTL</span></span>
</dt> <dd>

<span data-ttu-id="4219f-184">Eine Zeichenfolge, die das Produkt der Quell Code Verwaltung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4219f-184">A string that describes the source control product.</span></span> <span data-ttu-id="4219f-185">Diese Variable ist optional.</span><span class="sxs-lookup"><span data-stu-id="4219f-185">This variable is optional.</span></span>

</dd> <dt>

<span data-ttu-id="4219f-186"><span id="DATETIME"></span><span id="datetime"></span>DateTime</span><span class="sxs-lookup"><span data-stu-id="4219f-186"><span id="DATETIME"></span><span id="datetime"></span>DATETIME</span></span>
</dt> <dd>

<span data-ttu-id="4219f-187">Eine Zeichenfolge, die das Datum und die Uhrzeit der Verarbeitung der PDB-Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="4219f-187">A string that indicates the date and time the PDB file was processed.</span></span> <span data-ttu-id="4219f-188">Diese Variable ist optional.</span><span class="sxs-lookup"><span data-stu-id="4219f-188">This variable is optional.</span></span>

</dd> </dl>

<span data-ttu-id="4219f-189">Der Abschnitt Variablen enthält Variablen, die beschreiben, wie eine Datei aus der Quell Code Verwaltung extrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4219f-189">The variables section contains variables that describe how to extract a file from source control.</span></span> <span data-ttu-id="4219f-190">Sie kann auch verwendet werden, um häufig verwendeten Text als Variablen zu definieren, um die Größe des Datenblocks zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="4219f-190">It can also be used to define commonly used text as variables to reduce the size of the data block.</span></span>

<dl> <dt>

<span data-ttu-id="4219f-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>Srcsrvtrg</span><span class="sxs-lookup"><span data-stu-id="4219f-191"><span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG</span></span>
</dt> <dd>

<span data-ttu-id="4219f-192">Beschreibt, wie der Zielpfad für die extrahierte Datei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4219f-192">Describes how to build the target path for the extracted file.</span></span> <span data-ttu-id="4219f-193">Dies ist eine erforderliche Variable.</span><span class="sxs-lookup"><span data-stu-id="4219f-193">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="4219f-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>Srcsrvcmd</span><span class="sxs-lookup"><span data-stu-id="4219f-194"><span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD</span></span>
</dt> <dd>

<span data-ttu-id="4219f-195">Beschreibt, wie der Befehl zum Extrahieren der Datei aus der Quell Code Verwaltung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4219f-195">Describes how to build the command to extract the file from source control.</span></span> <span data-ttu-id="4219f-196">Dies schließt den Namen der ausführbaren Datei und der Befehlszeilenparameter ein.</span><span class="sxs-lookup"><span data-stu-id="4219f-196">This includes the name of the executable file and its command-line parameters.</span></span> <span data-ttu-id="4219f-197">Dies ist eine erforderliche Variable.</span><span class="sxs-lookup"><span data-stu-id="4219f-197">This is a required variable.</span></span>

</dd> <dt>

<span data-ttu-id="4219f-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>Srcsrvenv</span><span class="sxs-lookup"><span data-stu-id="4219f-198"><span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV</span></span>
</dt> <dd>

<span data-ttu-id="4219f-199">Eine Zeichenfolge, die Umgebungsvariablen auflistet, die während der Dateiextraktion erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4219f-199">A string that lists environment variables to be created during the file extraction.</span></span> <span data-ttu-id="4219f-200">Trennen Sie mehrere Einträge durch ein Rückraum Zeichen ( \\ b).</span><span class="sxs-lookup"><span data-stu-id="4219f-200">Separate multiple entries with a backspace character (\\b).</span></span> <span data-ttu-id="4219f-201">Dies ist eine optionale Variable.</span><span class="sxs-lookup"><span data-stu-id="4219f-201">This is an optional variable.</span></span>

</dd> </dl>

<span data-ttu-id="4219f-202">Der Abschnitt Quelldateien enthält einen Eintrag für jede Quelldatei, die indiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="4219f-202">The source files section contains an entry for each source file that has been indexed.</span></span> <span data-ttu-id="4219f-203">Die Inhalte der einzelnen Zeilen werden als Variablen mit den Namen var1, var2, var3 usw. bis VAR10 interpretiert.</span><span class="sxs-lookup"><span data-stu-id="4219f-203">The contents of each line are interpreted as variables with the names VAR1, VAR2, VAR3, and so on until VAR10.</span></span> <span data-ttu-id="4219f-204">Die Variablen werden durch Sternchen getrennt.</span><span class="sxs-lookup"><span data-stu-id="4219f-204">The variables are separated by asterisks.</span></span> <span data-ttu-id="4219f-205">Var1 muss den voll qualifizierten Pfad zur Quelldatei angeben, der an anderer Stelle in der PDB-Datei aufgelistet ist.</span><span class="sxs-lookup"><span data-stu-id="4219f-205">VAR1 must specify the fully qualified path to the source file as listed elsewhere in the PDB file.</span></span> <span data-ttu-id="4219f-206">Beispielsweise die folgende Zeile:</span><span class="sxs-lookup"><span data-stu-id="4219f-206">For example, the following line:</span></span>

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

<span data-ttu-id="4219f-207">wird wie folgt interpretiert:</span><span class="sxs-lookup"><span data-stu-id="4219f-207">is interpreted as follows:</span></span>

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

<span data-ttu-id="4219f-208">In diesem Beispiel ist VAR4 eine Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="4219f-208">In this example, VAR4 is a version number.</span></span> <span data-ttu-id="4219f-209">Die meisten Quell Code Verwaltungssysteme unterstützen jedoch das bezeichnen von Dateien so, dass der Quell Zustand für einen bestimmten Build wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4219f-209">However, most source control systems support labeling files in such a way that the source state for a given build can be restored.</span></span> <span data-ttu-id="4219f-210">Daher können Sie alternativ die Bezeichnung für den Build verwenden.</span><span class="sxs-lookup"><span data-stu-id="4219f-210">Therefore, you could alternately use the label for the build.</span></span> <span data-ttu-id="4219f-211">Der Beispiel Datenblock kann so geändert werden, dass er eine Variable wie die folgende enthält:</span><span class="sxs-lookup"><span data-stu-id="4219f-211">The sample data block could be modified to contain a variable such as the following:</span></span>

``` syntax
LABEL=BUILD47
```

<span data-ttu-id="4219f-212">Wenn Sie dann das Quell Code Verwaltungssystem verwenden, um eine Bezeichnung anzugeben, können Sie die srcsrvcmd-Variable wie folgt ändern:</span><span class="sxs-lookup"><span data-stu-id="4219f-212">Then, presuming the source control system uses the at sign (@) to indicate a label, you could modify the SRCSRVCMD variable as follows:</span></span>

<span data-ttu-id="4219f-213">**sd.exe-p% fnvar%(% var2%) Print-o% srcsrvtrg%-q% Depot%/%var3% @% Bezeichnung%**</span><span class="sxs-lookup"><span data-stu-id="4219f-213">**sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%@%label%**</span></span>

## <a name="how-source-server-works"></a><span data-ttu-id="4219f-214">Funktionsweise des Quell Servers</span><span class="sxs-lookup"><span data-stu-id="4219f-214">How Source Server Works</span></span>

<span data-ttu-id="4219f-215">Der Quell Server Client wird in Symsrv.dll implementiert.</span><span class="sxs-lookup"><span data-stu-id="4219f-215">The source server client is implemented in Symsrv.dll.</span></span> <span data-ttu-id="4219f-216">Der Client extrahiert keine Informationen direkt aus der PDB-Datei. Er verwendet einen Symbol Handler, z. b. den, der in Dbghelp.dll implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="4219f-216">The client does not extract information directly from the PDB file; it uses a symbol handler such as the one implemented in Dbghelp.dll.</span></span> <span data-ttu-id="4219f-217">Es handelt sich im Wesentlichen um eine rekursive Variablen Ersetzungs-Engine, die eine Befehlszeile erstellt, mit der die richtige Quelldatei aus dem Quell Code Verwaltungssystem extrahiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4219f-217">It is essentially a recursive variable substitution engine that creates a command line that can be used to extract the proper source file from the source control system.</span></span> <span data-ttu-id="4219f-218">Der Code sollte Symsrv.dll nicht direkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4219f-218">Your code should not call Symsrv.dll directly.</span></span> <span data-ttu-id="4219f-219">Verwenden Sie die [**symgetsourcefile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) -Funktion, um ihre Funktionalität in Ihre Anwendung zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="4219f-219">To integrate its functionality into your application, use the [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) function.</span></span>

<span data-ttu-id="4219f-220">Die erste Version des Quell Servers funktioniert wie folgt.</span><span class="sxs-lookup"><span data-stu-id="4219f-220">The first version of source server works as follows.</span></span> <span data-ttu-id="4219f-221">Dieses Verhalten kann sich in zukünftigen Versionen ändern.</span><span class="sxs-lookup"><span data-stu-id="4219f-221">This behavior may change in future versions.</span></span>

-   <span data-ttu-id="4219f-222">Der Client ruft die **srcsrvinit** -Funktion mit dem Zielpfad auf, der als Basis für alle Quelldatei Extraktionen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4219f-222">The client calls the **SrcSrvInit** function with the target path to be used as a base for all source file extractions.</span></span> <span data-ttu-id="4219f-223">Dieser Pfad wird in der Targ-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4219f-223">It stores this path in the TARG variable.</span></span>
-   <span data-ttu-id="4219f-224">Der Client extrahiert den SRCSRV-Datenstrom aus der PDB-Datei, wenn das PDB-Modul geladen wird, und ruft die **srcsrvloadmodule** -Funktion auf, um den Datenblock an den Quell Server zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="4219f-224">The client extracts the Srcsrv stream from the PDB when the module PDB is loaded and calls the **SrcSrvLoadModule** function to pass the data block to source server.</span></span>
-   <span data-ttu-id="4219f-225">Wenn dbghelp eine Quelldatei abruft, ruft der Client die **srcsrvgetfile** -Funktion auf, um die Quelldateien aus der Quell Code Verwaltung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4219f-225">When Dbghelp retrieves a source file, the client calls the **SrcSrvGetFile** function to retrieve the source files from source control.</span></span>
-   <span data-ttu-id="4219f-226">Der Quell Server durchsucht die Quelldatei Einträge im Datenblock nach einem Eintrag, der mit der angeforderten Datei übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4219f-226">Source server searches the source file entries in the data block for an entry that matches the requested file.</span></span> <span data-ttu-id="4219f-227">Es füllt var1 mit dem Inhalt des Quelldatei Eintrags in var *n* auf.</span><span class="sxs-lookup"><span data-stu-id="4219f-227">It fills VAR1 to VAR *n* with the contents of the source file entry.</span></span> <span data-ttu-id="4219f-228">Anschließend wird die srcsrvtrg-Variable mithilfe von var1 auf var *n* erweitert.</span><span class="sxs-lookup"><span data-stu-id="4219f-228">Next, it expands the SRCSRVTRG variable using VAR1 to VAR *n*.</span></span> <span data-ttu-id="4219f-229">Wenn sich die Datei bereits an diesem Speicherort befindet, wird der Speicherort an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4219f-229">If the file is already in this location, it returns the location to the caller.</span></span> <span data-ttu-id="4219f-230">Andernfalls wird die srcsrvcmd-Variable erweitert, um den Befehl zu erstellen, der erforderlich ist, um die Datei aus der Quell Code Verwaltung abzurufen und an den Ziel Speicherort zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="4219f-230">Otherwise, it expands the SRCSRVCMD variable to build the command needed to retrieve the file from source control and copy it to the target location.</span></span> <span data-ttu-id="4219f-231">Schließlich führt Sie diesen Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="4219f-231">Finally, it executes this command.</span></span>

## <a name="creating-a-source-control-provider-module"></a><span data-ttu-id="4219f-232">Erstellen eines Quellcodeverwaltungs-Anbieter Moduls</span><span class="sxs-lookup"><span data-stu-id="4219f-232">Creating a Source Control Provider Module</span></span>

<span data-ttu-id="4219f-233">Der Quell Server umfasst Anbieter Module für Perforce (P4.pm) und Visual Source Safe (VSS.pm).</span><span class="sxs-lookup"><span data-stu-id="4219f-233">The source server includes provider modules for Perforce (p4.pm) and Visual Source Safe (vss.pm).</span></span> <span data-ttu-id="4219f-234">Um ein eigenes Anbieter Modul zu erstellen, müssen Sie die folgenden Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="4219f-234">To create your own provider module, you must implement the following set of interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="4219f-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$Module:: simpleusage ()**</span><span class="sxs-lookup"><span data-stu-id="4219f-235"><span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module::SimpleUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="4219f-236">Zweck: zeigt die Informationen zu einfachen Modul Verwendungs Informationen für "stdout" an.</span><span class="sxs-lookup"><span data-stu-id="4219f-236">Purpose: Displays simple module usage information to STDOUT.</span></span>

<span data-ttu-id="4219f-237">Parameter: keine</span><span class="sxs-lookup"><span data-stu-id="4219f-237">Parameters: None</span></span>

<span data-ttu-id="4219f-238">Rückgabewert: None</span><span class="sxs-lookup"><span data-stu-id="4219f-238">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="4219f-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$Module:: verbosusage ()**</span><span class="sxs-lookup"><span data-stu-id="4219f-239"><span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module::VerboseUsage()**</span></span>
</dt> <dd>

<span data-ttu-id="4219f-240">Zweck: zeigt ausführliche Informationen zur Modul Verwendung an stdout an.</span><span class="sxs-lookup"><span data-stu-id="4219f-240">Purpose: Displays in-depth module usage information to STDOUT.</span></span>

<span data-ttu-id="4219f-241">Parameter: keine</span><span class="sxs-lookup"><span data-stu-id="4219f-241">Parameters: None</span></span>

<span data-ttu-id="4219f-242">Rückgabewert: None</span><span class="sxs-lookup"><span data-stu-id="4219f-242">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="4219f-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$ObjRef = $Module:: New ( \@ commandarguments)**</span><span class="sxs-lookup"><span data-stu-id="4219f-243"><span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module::new(\@CommandArguments)**</span></span>
</dt> <dd>

<span data-ttu-id="4219f-244">Zweck: Initialisiert eine Instanz des Anbieter Moduls.</span><span class="sxs-lookup"><span data-stu-id="4219f-244">Purpose: Initializes an instance of the provider module.</span></span>

<span data-ttu-id="4219f-245">Parameter: alle @ARGV Argumente, die von "SSINDEX. cmd" nicht als allgemeine Argumente erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="4219f-245">Parameters: All @ARGV arguments that were not recognized by SSIndex.cmd as being general arguments.</span></span>

<span data-ttu-id="4219f-246">Rückgabewert: ein Verweis, der in späteren Vorgängen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4219f-246">Return value: A reference that can be used in later operations.</span></span>

</dd> <dt>

<span data-ttu-id="4219f-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$ObjRef->gatherfileinformation ($SourcePath, $ServerHashReference)**</span><span class="sxs-lookup"><span data-stu-id="4219f-247"><span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation($SourcePath, $ServerHashReference)**</span></span>
</dt> <dd>

<span data-ttu-id="4219f-248">Zweck: ermöglicht dem Modul, die erforderlichen Quell Indizierungs Informationen für das vom $SourcePath-Parameter angegebene Verzeichnis zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="4219f-248">Purpose: Enables the module to gather the required source indexing information for the directory specified by the $SourcePath parameter.</span></span> <span data-ttu-id="4219f-249">Das Modul sollte nicht davon ausgehen, dass dieser Eintrag für jede Objektinstanz nur einmal aufgerufen wird, da SSINDEX. cmd ihn möglicherweise mehrmals für verschiedene Pfade aufruft.</span><span class="sxs-lookup"><span data-stu-id="4219f-249">The module should not assume that this entry will be called only once for each object instance, as SSIndex.cmd may call it multiple times for different paths.</span></span>

<span data-ttu-id="4219f-250">Parameter: (1) das lokale Verzeichnis, das die zu indizierende Quelle enthält.</span><span class="sxs-lookup"><span data-stu-id="4219f-250">Parameters: (1) The local directory containing the source to be indexed.</span></span> <span data-ttu-id="4219f-251">(2) ein Verweis auf einen Hash, der alle Einträge aus der angegebenen Srcsrv.ini Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="4219f-251">(2) A reference to a hash containing all of the entries from the specified Srcsrv.ini file.</span></span>

<span data-ttu-id="4219f-252">Rückgabewert: None</span><span class="sxs-lookup"><span data-stu-id="4219f-252">Return value: None</span></span>

</dd> <dt>

<span data-ttu-id="4219f-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $ObjRef->GetFileInfo ($LocalFile)**</span><span class="sxs-lookup"><span data-stu-id="4219f-253"><span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo($LocalFile)**</span></span>
</dt> <dd>

<span data-ttu-id="4219f-254">Zweck: stellt die erforderlichen Informationen bereit, um eine einzelne, bestimmte Datei aus dem Quell Code Verwaltungssystem zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="4219f-254">Purpose: Provides the necessary information to extract a single, specific file from the source control system.</span></span>

<span data-ttu-id="4219f-255">Parameter: ein voll qualifizierter Dateiname</span><span class="sxs-lookup"><span data-stu-id="4219f-255">Parameters: A fully qualified file name</span></span>

<span data-ttu-id="4219f-256">Rückgabewert: (1) ein Hash Verweis auf die Variablen, die zum Interpretieren der zurückgegebenen $FileEntry erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4219f-256">Return value: (1) A hash reference of the variables necessary to interpret the returned $FileEntry.</span></span> <span data-ttu-id="4219f-257">SSINDEX. cmd speichert diese Variablen für jede Quelldatei, die von einer einzelnen Debugdatei verwendet wird, um die Menge der Informationen zu reduzieren, die in den quellindexstream geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4219f-257">SSIndex.cmd caches these variables for every source file used by a single debug file to reduce the amount of information written to the source index stream.</span></span> <span data-ttu-id="4219f-258">(2) der Datei Eintrag, der in den quellindexstream geschrieben werden soll, damit SrcSrv.dll diese Datei aus der Quell Code Verwaltung extrahieren kann.</span><span class="sxs-lookup"><span data-stu-id="4219f-258">(2) The file entry to be written to the source index stream to allow SrcSrv.dll to extract this file from source control.</span></span> <span data-ttu-id="4219f-259">Das genaue Format dieser Zeile ist spezifisch für das Quell Code Verwaltungssystem.</span><span class="sxs-lookup"><span data-stu-id="4219f-259">The exact format of this line is specific to the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="4219f-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $ObjRef->longname ()**</span><span class="sxs-lookup"><span data-stu-id="4219f-260"><span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName()**</span></span>
</dt> <dd>

<span data-ttu-id="4219f-261">Zweck: stellt eine beschreibende Zeichenfolge bereit, um den Quell Code Verwaltungs Anbieter für den Endbenutzer zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4219f-261">Purpose: Provides a descriptive string to identify the source control provider to the end user.</span></span>

<span data-ttu-id="4219f-262">Parameter: keine</span><span class="sxs-lookup"><span data-stu-id="4219f-262">Parameters: None</span></span>

<span data-ttu-id="4219f-263">Rückgabewert: der beschreibende Name des Quell Code Verwaltungssystems.</span><span class="sxs-lookup"><span data-stu-id="4219f-263">Return value: The descriptive name of the source control system.</span></span>

</dd> <dt>

<span data-ttu-id="4219f-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $ObjRef->sourcestreamvariables ()**</span><span class="sxs-lookup"><span data-stu-id="4219f-264"><span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables()**</span></span>
</dt> <dd>

<span data-ttu-id="4219f-265">Zweck: ermöglicht dem Quell Code Verwaltungs Anbieter, dem Quellstream für jede Debugdatei Quell Code Verwaltungs spezifische Variablen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4219f-265">Purpose: Enables the source control provider to add source control specific variables to the source stream for each debug file.</span></span> <span data-ttu-id="4219f-266">Die Beispiel Module verwenden diese Methode zum Schreiben der erforderlichen Extract \_ cmd-und Extract \_ target-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4219f-266">The sample modules use this method for writing the required EXTRACT\_CMD and EXTRACT\_TARGET variables.</span></span>

<span data-ttu-id="4219f-267">Parameter: keine</span><span class="sxs-lookup"><span data-stu-id="4219f-267">Parameters: None</span></span>

<span data-ttu-id="4219f-268">Rückgabewert: die Liste der Einträge für die Quelldaten Strom Variablen.</span><span class="sxs-lookup"><span data-stu-id="4219f-268">Return value: The list of entries for the source stream variables.</span></span>

</dd> </dl>

 

 




