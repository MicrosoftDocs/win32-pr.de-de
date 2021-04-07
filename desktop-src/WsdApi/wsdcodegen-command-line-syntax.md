---
description: 'Wsdcodegen verfügt über zwei Funktionen: das Erstellen von Konfigurationsdateien und das Erstellen von Quellcode für WSDAPI-Client-und-Host Anwendungen.'
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: Wsdcodegen-Befehlszeilen Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863751"
---
# <a name="wsdcodegen-command-line-syntax"></a><span data-ttu-id="a9543-103">Wsdcodegen-Befehlszeilen Syntax</span><span class="sxs-lookup"><span data-stu-id="a9543-103">WsdCodeGen Command Line Syntax</span></span>

<span data-ttu-id="a9543-104">Wsdcodegen verfügt über zwei Funktionen: das Erstellen von Konfigurationsdateien und das Erstellen von Quellcode für WSDAPI-Client-und-Host Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a9543-104">WsdCodeGen has two functions: generating configuration files and generating source code for WSDAPI client and host applications.</span></span> <span data-ttu-id="a9543-105">Dieses Thema enthält die Befehlszeilen Syntax, die zum Ausführen der einzelnen Aufgaben verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9543-105">This topic gives the command line syntax used to perform each task.</span></span>

## <a name="generating-a-configuration-file"></a><span data-ttu-id="a9543-106">Erstellen einer Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="a9543-106">Generating a Configuration File</span></span>

### <a name="syntax"></a><span data-ttu-id="a9543-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9543-107">Syntax</span></span>

<span data-ttu-id="a9543-108">**WSDCODEGEN.EXE** **/generateconfig:**{**Client** \| **Host** \| **all**} **\[ /OutputFile:**_configfilename_ *_\]_* *wsdlfilename amelist*</span><span class="sxs-lookup"><span data-stu-id="a9543-108">**WSDCODEGEN.EXE** **/generateconfig:**{**client**\|**host**\|**all**} **\[/outputfile:**_ConfigFileName_*_\]_* *WSDLFileNameList*</span></span>

### <a name="parameters"></a><span data-ttu-id="a9543-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9543-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9543-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig: {Client \| Host \| alle}**</span><span class="sxs-lookup"><span data-stu-id="a9543-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig:{client \| host \| all}**</span></span>
</dt> <dd>

<span data-ttu-id="a9543-111">Der Codetyp, der von der Ausgabe Konfigurationsdatei generiert wird.</span><span class="sxs-lookup"><span data-stu-id="a9543-111">The type of code that the output configuration file will generate.</span></span> <span data-ttu-id="a9543-112">**/generateconfig: Client** wird verwendet, um eine Konfigurationsdatei zum Generieren von Client Code zu generieren, **/generateconfig: der Host** wird zum Generieren einer Konfigurationsdatei zum Generieren des Host Codes verwendet, und **/generateconfig: all** wird verwendet, um eine Konfigurationsdatei zum Generieren von Client-und Hostcode zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a9543-112">**/generateconfig:client** is used to generate a configuration file for generating client code, **/generateconfig:host** is used to generate a configuration file for generating host code, and **/generateconfig:all** is used to generate a configuration file for generating both client and host code.</span></span>

</dd> <dt>

<span data-ttu-id="a9543-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/OutputFile:**_configfilename_</span><span class="sxs-lookup"><span data-stu-id="a9543-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile:**_ConfigFileName_</span></span>
</dt> <dd>

<span data-ttu-id="a9543-114">Dieser optionale Parameter wird verwendet, um den Dateinamen der Ausgabe Konfigurationsdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a9543-114">This optional parameter is used to specify the file name of the output configuration file.</span></span> <span data-ttu-id="a9543-115">Wenn dieser Parameter ausgeschlossen wird, wird der Name der Ausgabe Konfigurationsdatei codegen.config.</span><span class="sxs-lookup"><span data-stu-id="a9543-115">If this parameter is excluded, the name of the output configuration file is codegen.config.</span></span>

</dd> <dt>

<span data-ttu-id="a9543-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span><span class="sxs-lookup"><span data-stu-id="a9543-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span></span>
</dt> <dd>

<span data-ttu-id="a9543-117">Fügen Sie eine PnP-X-Vorlage in die Konfigurationsdatei ein.</span><span class="sxs-lookup"><span data-stu-id="a9543-117">Include a PnP-X template in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="a9543-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*Wsdldatamelist*</span><span class="sxs-lookup"><span data-stu-id="a9543-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span></span>
</dt> <dd>

<span data-ttu-id="a9543-119">Eine durch Leerzeichen getrennte Liste der WSDL-Dateien, die von wsdcodegen verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9543-119">A space-delimited list of the WSDL file(s) to be processed by WsdCodeGen.</span></span>

</dd> </dl>

## <a name="generating-source-code"></a><span data-ttu-id="a9543-120">Quellcode wird erzeugt</span><span class="sxs-lookup"><span data-stu-id="a9543-120">Generating Source Code</span></span>

### <a name="syntax"></a><span data-ttu-id="a9543-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9543-121">Syntax</span></span>

<span data-ttu-id="a9543-122">**WSDCODEGEN.EXE** **/GenerateCode** **\[ /Download \]** **\[ /GBC \]** **\[ outputroot:**_path_ *_\]_* **\[ /writeaccess:**_Befehl_ *_\]_* *configfilename*</span><span class="sxs-lookup"><span data-stu-id="a9543-122">**WSDCODEGEN.EXE** **/generatecode** **\[/download\]** **\[/gbc\]** **\[outputroot:**_path_*_\]_* **\[/writeaccess:**_command_*_\]_* *ConfigFileName*</span></span>

### <a name="parameters"></a><span data-ttu-id="a9543-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9543-123">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9543-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span><span class="sxs-lookup"><span data-stu-id="a9543-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span></span>
</dt> <dd>

<span data-ttu-id="a9543-125">Weist wsdcodegen an, Quellcode zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a9543-125">Directs WsdCodeGen to generate source code.</span></span> <span data-ttu-id="a9543-126">Dies ist der Standardmodus, wenn kein Modus angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a9543-126">This is the default mode if no mode is specified.</span></span>

</dd> <dt>

<span data-ttu-id="a9543-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/Download**</span><span class="sxs-lookup"><span data-stu-id="a9543-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/download**</span></span>
</dt> <dd>

<span data-ttu-id="a9543-128">Herunterladen importierter Dokumente, auf die von der Konfigurationsdatei verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="a9543-128">Downloads imported documents referenced by the configuration file.</span></span> <span data-ttu-id="a9543-129">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a9543-129">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a9543-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span><span class="sxs-lookup"><span data-stu-id="a9543-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span></span>
</dt> <dd>

<span data-ttu-id="a9543-131">Fügt dem Quellcode Kommentare hinzu, die angeben, dass der Code generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a9543-131">Adds comments to the source code that indicates the code was generated.</span></span> <span data-ttu-id="a9543-132">Diesen Kommentaren wird der Ausdruck "generiert von" vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="a9543-132">These comments are prefixed with the phrase "Generated by".</span></span> <span data-ttu-id="a9543-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a9543-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a9543-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_Pfad_</span><span class="sxs-lookup"><span data-stu-id="a9543-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_path_</span></span>
</dt> <dd>

<span data-ttu-id="a9543-135">Der Ausgabe Speicherort für generierte Dateien.</span><span class="sxs-lookup"><span data-stu-id="a9543-135">The output location for generated files.</span></span> <span data-ttu-id="a9543-136">der *Pfad* kann ein absoluter oder relativer Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="a9543-136">*path* can be an absolute or relative path.</span></span> <span data-ttu-id="a9543-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a9543-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a9543-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_Befehl_</span><span class="sxs-lookup"><span data-stu-id="a9543-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_command_</span></span>
</dt> <dd>

<span data-ttu-id="a9543-139">Weist wsdcodegen an, den angegebenen Befehl auszuführen, bevor vorhandene Dateien auf dem Datenträger geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a9543-139">Directs WsdCodeGen to execute the specified command before it modifies any existing files on disk.</span></span> <span data-ttu-id="a9543-140">Ausgabedateien, die mit den Daten auf dem Datenträger identisch sind, erhalten diesen Befehl nicht, und Sie werden auch nicht in geschrieben.</span><span class="sxs-lookup"><span data-stu-id="a9543-140">Output files that are identical to those on disk will not receive this command, nor will they be written to.</span></span> <span data-ttu-id="a9543-141">Wenn der Befehl die Sequenz " {0} " enthält, wird diese Sequenz durch den Dateinamen der Datei ersetzt, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9543-141">If the command contains the sequence "{0}", this sequence will be replaced with the filename of the file to be modified.</span></span> <span data-ttu-id="a9543-142">Wenn dies nicht der Fall ist, wird der Dateiname an den Befehl angehängt.</span><span class="sxs-lookup"><span data-stu-id="a9543-142">If not, the filename will be appended to the command.</span></span>

<span data-ttu-id="a9543-143">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="a9543-143">Examples:</span></span>

<span data-ttu-id="a9543-144">**/writeaccess: "atungb-r"**</span><span class="sxs-lookup"><span data-stu-id="a9543-144">**/writeaccess:"attrib -r"**</span></span>

<span data-ttu-id="a9543-145">**/writeaccess: "atungb-r {0} "**</span><span class="sxs-lookup"><span data-stu-id="a9543-145">**/writeaccess:"attrib -r {0}"**</span></span>

<span data-ttu-id="a9543-146">**/writeaccess: "kopieren {0} .. \\ Sichern \\ "**</span><span class="sxs-lookup"><span data-stu-id="a9543-146">**/writeaccess:"copy {0} ..\\backup\\"**</span></span>

</dd> <dt>

<span data-ttu-id="a9543-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*Configfilename*</span><span class="sxs-lookup"><span data-stu-id="a9543-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*ConfigFileName*</span></span>
</dt> <dd>

<span data-ttu-id="a9543-148">Der Name der Konfigurationsdatei, die vor dem Erstellen von Code verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9543-148">The name of the configuration file to process before generating code.</span></span>

</dd> </dl>

## <a name="formatting-legend"></a><span data-ttu-id="a9543-149">Formatierungslegende</span><span class="sxs-lookup"><span data-stu-id="a9543-149">Formatting Legend</span></span>



| <span data-ttu-id="a9543-150">Format</span><span class="sxs-lookup"><span data-stu-id="a9543-150">Format</span></span>                                                                    | <span data-ttu-id="a9543-151">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a9543-151">Meaning</span></span>                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a9543-152">*Kursiv*</span><span class="sxs-lookup"><span data-stu-id="a9543-152">*Italic*</span></span>                                                                  | <span data-ttu-id="a9543-153">Informationen, die der Benutzer bereitstellen muss</span><span class="sxs-lookup"><span data-stu-id="a9543-153">Information that the user must provide</span></span>                  |
| <span data-ttu-id="a9543-154">**Fett**</span><span class="sxs-lookup"><span data-stu-id="a9543-154">**Bold**</span></span>                                                                  | <span data-ttu-id="a9543-155">Elemente, die der Benutzer genau so eingeben muss, wie sie angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="a9543-155">Elements that the user must type exactly as shown</span></span>       |
| <span data-ttu-id="a9543-156">Zwischen eckigen Klammern ( \[ \] )</span><span class="sxs-lookup"><span data-stu-id="a9543-156">Between brackets (\[\])</span></span>                                                   | <span data-ttu-id="a9543-157">Optionale Elemente</span><span class="sxs-lookup"><span data-stu-id="a9543-157">Optional items</span></span>                                          |
| <span data-ttu-id="a9543-158">Zwischen geschweiften Klammern ( {} ); durch Pipe getrennte Optionen ( \| ).</span><span class="sxs-lookup"><span data-stu-id="a9543-158">Between braces ({}); choices separated by pipe (\|).</span></span> <span data-ttu-id="a9543-159">Beispiel: {Even \| Odd}</span><span class="sxs-lookup"><span data-stu-id="a9543-159">Example: {even\|odd}</span></span> | <span data-ttu-id="a9543-160">Satz von Auswahlmöglichkeiten, von denen der Benutzer nur eine auswählen muss</span><span class="sxs-lookup"><span data-stu-id="a9543-160">Set of choices from which the user must choose only one</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a9543-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9543-161">Requirements</span></span>



| <span data-ttu-id="a9543-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9543-162">Requirement</span></span> | <span data-ttu-id="a9543-163">Wert</span><span class="sxs-lookup"><span data-stu-id="a9543-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a9543-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9543-164">Minimum supported client</span></span><br/> | <span data-ttu-id="a9543-165">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9543-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a9543-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9543-166">Minimum supported server</span></span><br/> | <span data-ttu-id="a9543-167">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9543-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9543-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9543-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9543-169">Wsdcodegen-Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="a9543-169">WsdCodeGen Configuration File</span></span>](wsdcodegen-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="a9543-170">Verwenden von wsdcodegen</span><span class="sxs-lookup"><span data-stu-id="a9543-170">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 




