---
description: Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung von Tools zur Patcherstellung, wie z. b. Msimsp.exe und Patchwiz.dll. Das Msimsp.exe Tool ist nur in den Windows SDK Komponenten für Windows Installer Entwickler verfügbar.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106364301"
---
# <a name="msimspexe"></a><span data-ttu-id="a7529-104">Msimsp.exe</span><span class="sxs-lookup"><span data-stu-id="a7529-104">Msimsp.exe</span></span>

<span data-ttu-id="a7529-105">Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung von Tools zur Patcherstellung, wie z. b. Msimsp.exe und [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a7529-105">The recommended method for generating a patch package is to use patch creation tools such as Msimsp.exe and [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="a7529-106">Das Msimsp.exe Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7529-106">The Msimsp.exe tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="a7529-107">Msimsp.exe ist eine ausführbare Datei, die [Patchwiz.dll](patchwiz-dll.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="a7529-107">Msimsp.exe is a executable file that calls [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="a7529-108">Das Tool kann zum Erstellen eines Patchpakets verwendet werden, indem der Pfad zur Eigenschaften Datei für die Patcherstellung (PCP-Datei) und der Pfad zum Patchpaket, das erstellt wird, übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a7529-108">The tool can be used to create a patch package by passing in the path to a patch creation properties file (.pcp file) and the path to the patch package that is being created.</span></span> <span data-ttu-id="a7529-109">Msimsp. Ex kann auch verwendet werden, um eine Protokolldatei zu erstellen und einen temporären Ordner anzugeben, in dem die Transformationen, Schränke und Dateien, die zum Erstellen des Patchpakets verwendet werden, gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a7529-109">Msimsp.ex can also be used to create a log file and to specify a temporary folder in which the transforms, cabinets, and files that are used to create the patch package are saved.</span></span>

<span data-ttu-id="a7529-110">Die Befehlszeilen Syntax für Msimsp.exe lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a7529-110">The command-line syntax for Msimsp.exe is:</span></span>

<span data-ttu-id="a7529-111">**Msimsp.exe-s-Pfad** *\[ zu pcp- \] Datei* **-p** *\[ Pfad zur MSP- \] Datei* **{Optionen}**</span><span class="sxs-lookup"><span data-stu-id="a7529-111">**Msimsp.exe -s** *\[path to .pcp file\]* **-p** *\[path to .msp file\]* **{options}**</span></span>

<span data-ttu-id="a7529-112">Bei den Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet, und es können Schrägstriche anstelle eines Bindestrichs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7529-112">The command-line options are not case-sensitive, and slash delimiters can be used instead of a dash.</span></span> <span data-ttu-id="a7529-113">Wenn keine Optionen angegeben sind, zeigt Msimsp.exe die aktuellen Werte der Eigenschaften der Zusammenfassungs Informationen an.</span><span class="sxs-lookup"><span data-stu-id="a7529-113">If no options are specified, Msimsp.exe displays the current values of the summary Information properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7529-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ Pfad zur PCP-Datei \]_</span><span class="sxs-lookup"><span data-stu-id="a7529-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[path to .pcp file\]_</span></span>
</dt> <dd>

<span data-ttu-id="a7529-115">Dies ist erforderlich, und es muss der Pfad zur Eigenschaften Datei für die Patcherstellung (PCP-Erweiterung) befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="a7529-115">This is required and must be followed by the path to the patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="a7529-116">Weitere Informationen finden Sie unter [PatchWiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a7529-116">For more information, see [PatchWiz.dll](patchwiz-dll.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7529-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_Pfad zur MSP-Datei_</span><span class="sxs-lookup"><span data-stu-id="a7529-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_path to .msp file_</span></span>
</dt> <dd>

<span data-ttu-id="a7529-118">Dies ist erforderlich, und es folgt der Pfad zum Patchpaket, das erstellt wird (Erweiterung. msp).</span><span class="sxs-lookup"><span data-stu-id="a7529-118">This is required and followed by the path to patch package that is being created (.msp extension).</span></span>

</dd> <dt>

<span data-ttu-id="a7529-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_Pfad zum temporären Ordner_</span><span class="sxs-lookup"><span data-stu-id="a7529-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_path to temporary folder_</span></span>
</dt> <dd>

<span data-ttu-id="a7529-120">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a7529-120">Optional.</span></span> <span data-ttu-id="a7529-121">Gefolgt vom Pfad zum temporären Ordner.</span><span class="sxs-lookup"><span data-stu-id="a7529-121">Followed by path to temporary folder.</span></span> <span data-ttu-id="a7529-122">Der Standard Speicherort ist% tmp% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="a7529-122">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="a7529-123"><span id="-k"></span><span id="-K"></span>**-k**</span><span class="sxs-lookup"><span data-stu-id="a7529-123"><span id="-k"></span><span id="-K"></span>**-k**</span></span>
</dt> <dd>

<span data-ttu-id="a7529-124">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a7529-124">Optional.</span></span> <span data-ttu-id="a7529-125">Schlägt fehl, wenn der temporäre Ordner bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7529-125">Fail if the temporary folder already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a7529-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_Pfad zur Protokolldatei_</span><span class="sxs-lookup"><span data-stu-id="a7529-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_path to log file_</span></span>
</dt> <dd>

<span data-ttu-id="a7529-127">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a7529-127">Optional.</span></span> <span data-ttu-id="a7529-128">Gefolgt vom Pfad zur Protokolldatei, in der der patcherstellungs Prozess und die Fehler beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a7529-128">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="a7529-129">Weitere Informationen finden Sie unter [Rückgabewerte für uikreatepatchpackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="a7529-129">For more information, see [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7529-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-LP**_Pfad zur Protokolldatei mit Leistungsdaten_</span><span class="sxs-lookup"><span data-stu-id="a7529-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp**_path to log file with performance data_</span></span>
</dt> <dd>

<span data-ttu-id="a7529-131">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a7529-131">Optional.</span></span> <span data-ttu-id="a7529-132">Gefolgt vom Pfad zur Protokolldatei, in der der patcherstellungs Prozess und die Fehler beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a7529-132">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="a7529-133">Mit dieser Option werden Leistungsdaten in die Protokolldatei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="a7529-133">This option writes performance data to log file.</span></span> <span data-ttu-id="a7529-134">Diese Option erfordert Version 4,0 von Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="a7529-134">This option requires version 4.0 of Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="a7529-135"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="a7529-135"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="a7529-136">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a7529-136">Optional.</span></span> <span data-ttu-id="a7529-137">Zeigt ein Dialogfeld an, wenn die Patcherstellung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a7529-137">Displays a dialog if the patch creation completes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="a7529-138"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="a7529-138"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="a7529-139">Mit diesem Befehl wird die Befehlszeilenhilfe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a7529-139">Displays command-line help.</span></span>

</dd> </dl>

> [!Note]
> <span data-ttu-id="a7529-140">Msimsp.exe kann bei der Aufruf Makecab.exe einen Fehler verursachen, wenn in der Datei Spalte der [Dateitabelle](file-table.md) des Installationspakets Werte vorhanden sind, die sich nur in der Groß-/Kleinschreibung unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a7529-140">Msimsp.exe can fail when it calls Makecab.exe if there are values in the File column of the [File table](file-table.md) of the installation package that differ only by case.</span></span> <span data-ttu-id="a7529-141">Bei Windows Installer wird die Groß-/Kleinschreibung beachtet, und es wird nur ein Installationspaket wie in der folgenden Tabelle zugelassen, wenn Comp1 und Comp2 in verschiedenen Verzeichnissen installiert sind.</span><span class="sxs-lookup"><span data-stu-id="a7529-141">Windows Installer is case-sensitive and allows an installation package such as in the table below only when Comp1 and Comp2 are installed into different directories.</span></span> <span data-ttu-id="a7529-142">In diesem Szenario können Sie jedoch Msimsp.exe oder [Patchwiz.dll](patchwiz-dll.md) nicht verwenden, um einen Patch für das Paket zu generieren, da Msimsp.exe und Patchwiz.dll Makecab.exe, die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a7529-142">However, in this scenario you cannot use Msimsp.exe or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package, because Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive.</span></span>
> 
> <span data-ttu-id="a7529-143">Vermeiden Sie das Erstellen eines Installationspakets, z. b. der folgenden partiellen [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="a7529-143">Avoid authoring an installation package such as the following partial [File table](file-table.md).</span></span>
> 
> | <span data-ttu-id="a7529-144">File</span><span class="sxs-lookup"><span data-stu-id="a7529-144">File</span></span>       | <span data-ttu-id="a7529-145">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="a7529-145">Component\_</span></span> | <span data-ttu-id="a7529-146">FileName</span><span class="sxs-lookup"><span data-stu-id="a7529-146">FileName</span></span>   |
> |------------|-------------|------------|
> | <span data-ttu-id="a7529-147">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="a7529-147">readme.txt</span></span> | <span data-ttu-id="a7529-148">Comp1</span><span class="sxs-lookup"><span data-stu-id="a7529-148">Comp1</span></span>       | <span data-ttu-id="a7529-149">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="a7529-149">readme.txt</span></span> |
> | <span data-ttu-id="a7529-150">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="a7529-150">ReadMe.txt</span></span> | <span data-ttu-id="a7529-151">Comp2</span><span class="sxs-lookup"><span data-stu-id="a7529-151">Comp2</span></span>       | <span data-ttu-id="a7529-152">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="a7529-152">readme.txt</span></span> |


## <a name="related-topics"></a><span data-ttu-id="a7529-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a7529-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7529-154">Erstellen eines Patchpakets</span><span class="sxs-lookup"><span data-stu-id="a7529-154">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="a7529-155">Beispiel für ein kleines Update-Patching</span><span class="sxs-lookup"><span data-stu-id="a7529-155">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)
</dt> <dt>

[<span data-ttu-id="a7529-156">Entwicklungs Tools für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a7529-156">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="a7529-157">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="a7529-157">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



