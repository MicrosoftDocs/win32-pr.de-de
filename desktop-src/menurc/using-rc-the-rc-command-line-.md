---
title: Verwenden des Ressourcencompilers (RC-Befehlszeile)
description: Um RC zu starten, verwenden Sie den folgenden Befehl.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948668"
---
# <a name="using-rc-the-rc-command-line"></a><span data-ttu-id="885f6-103">Verwenden des Ressourcencompilers (RC-Befehlszeile)</span><span class="sxs-lookup"><span data-stu-id="885f6-103">Using RC (The RC Command Line)</span></span>

<span data-ttu-id="885f6-104">Um RC zu starten, verwenden Sie den folgenden Befehl.</span><span class="sxs-lookup"><span data-stu-id="885f6-104">To start RC, use the following command.</span></span>

<span data-ttu-id="885f6-105">**RC** \[ *Optionen* \] *Skriptdatei*</span><span class="sxs-lookup"><span data-stu-id="885f6-105">**RC** \[*options*\] *script-file*</span></span>

<span data-ttu-id="885f6-106">Der *Skriptdatei* Parameter gibt den Namen der Ressourcen Definitionsdatei an, die die Namen, Typen, Dateinamen und Beschreibungen der zu kompilierenden Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="885f6-106">The *script-file* parameter specifies the name of the resource-definition file that contains the names, types, filenames, and descriptions of the resources to be compiled.</span></span>

<span data-ttu-id="885f6-107">RC kann separate Ressourcen Dateien für Anwendungen generieren, die sowohl sprachneutrale als auch sprachspezifische Ressourcen haben.</span><span class="sxs-lookup"><span data-stu-id="885f6-107">RC can generate separate resource files for applications that have both language-neutral and language-specific resources.</span></span> <span data-ttu-id="885f6-108">Entwickler können eine [Ressourcen Konfigurationsdatei](/windows/desktop/Intl/preparing-resources) verwenden oder Befehlszeilenoptionen festlegen, um auszuwählen, welche Ressourcentypen und-Elemente nicht lokalisierbare Ressourcen der [sprach neutralen Datei (LN)](/windows/desktop/Intl/mui-resource-management) sind und welche lokalisierbare Ressourcen von sprachspezifischen MUI-Dateien sind.</span><span class="sxs-lookup"><span data-stu-id="885f6-108">Developers can use a [resource configuration file](/windows/desktop/Intl/preparing-resources) or set command-line options to select which resource types and items are non-localizable resources of the [language-neutral (LN) file](/windows/desktop/Intl/mui-resource-management) and which are localizable resources of language-specific MUI files.</span></span> <span data-ttu-id="885f6-109">Weitere Informationen finden Sie unter [mehrsprachige Benutzeroberfläche](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="885f6-109">For more information, see the [Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="885f6-110">Der *options* -Parameter kann eine oder mehrere der folgenden Befehlszeilenoptionen sein.</span><span class="sxs-lookup"><span data-stu-id="885f6-110">The *options* parameter can be one or more of the following command-line options.</span></span>

## <a name="options"></a><span data-ttu-id="885f6-111">Optionen</span><span class="sxs-lookup"><span data-stu-id="885f6-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="885f6-112"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="885f6-112"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-113">Zeigt eine Liste der Befehlszeilenoptionen an.</span><span class="sxs-lookup"><span data-stu-id="885f6-113">Displays a list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-114"><span id="_c"></span><span id="_C"></span>**/c**</span><span class="sxs-lookup"><span data-stu-id="885f6-114"><span id="_c"></span><span id="_C"></span>**/c**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-115">Definiert eine Codepage, die von der NLS-Konvertierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="885f6-115">Defines a code page used by NLS conversion.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-116"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="885f6-116"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-117">Definiert ein Symbol für den Präprozessor, der mit der [**\# ifdef**](-ifdef.md) -Direktive getestet werden kann.</span><span class="sxs-lookup"><span data-stu-id="885f6-117">Defines a symbol for the preprocessor that you can test with the [**\#ifdef**](-ifdef.md) directive.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/FM** - *mresname*</span><span class="sxs-lookup"><span data-stu-id="885f6-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*</span></span>
</dt> <dd>

<span data-ttu-id="885f6-119">RC erstellt eine sprachneutrale. RES-Datei und eine sprachabhängige (MUI). RES-Datei mithilfe der *Skriptdatei*.</span><span class="sxs-lookup"><span data-stu-id="885f6-119">RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file using *script-file*.</span></span> <span data-ttu-id="885f6-120">Diese Option muss in Verbindung mit der Option **/FO** *Resname* verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="885f6-120">This option must be used together with the **/fo** *resname* option.</span></span> <span data-ttu-id="885f6-121">RC benennt den sprach neutralen Namen. Res file *Resname. res* und benennt die sprachabhängige (MUI). Res-Datei ( *mresname. res*).</span><span class="sxs-lookup"><span data-stu-id="885f6-121">RC names the language-neutral .RES file *resname.res* and names the language-dependent (MUI) .RES file *mresname.res*.</span></span>

<span data-ttu-id="885f6-122">**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die [**loadmuilibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) -Funktion und die [**fremuilibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) -Funktion in einem aktualisierten System zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="885f6-122">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/FO** *Resname*</span><span class="sxs-lookup"><span data-stu-id="885f6-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*</span></span>
</dt> <dd>

<span data-ttu-id="885f6-124">RC erstellt einen. RES Datei mit dem *Namen Resname* unter Verwendung der *Skriptdatei*.</span><span class="sxs-lookup"><span data-stu-id="885f6-124">RC creates a .RES file named *resname* using *script-file*.</span></span>

<span data-ttu-id="885f6-125">Wenn die Option **/FM** *mresname* ebenfalls festgelegt ist, erstellt RC eine sprachneutrale. RES-Datei und eine sprachabhängige (MUI). RES-Datei.</span><span class="sxs-lookup"><span data-stu-id="885f6-125">If the **/fm** *mresname* option is also set, RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file.</span></span>

<span data-ttu-id="885f6-126">**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die [**loadmuilibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) -Funktion und die [**fremuilibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) -Funktion in einem aktualisierten System zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="885f6-126">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-127"><span id="_g1"></span><span id="_G1"></span>**/G1**</span><span class="sxs-lookup"><span data-stu-id="885f6-127"><span id="_g1"></span><span id="_G1"></span>**/g1**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-128">Wenn/G1 festgelegt ist, generiert RC eine MUI-Datei, wenn die einzige lokalisierbare Ressource, die in der MUI-Datei enthalten ist, eine Versions Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="885f6-128">If /g1, is set, RC generates a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span> <span data-ttu-id="885f6-129">Wenn/G1 nicht festgelegt ist, generiert RC keine MUI-Datei, wenn die einzige lokalisierbare Ressource, die in der MUI-Datei enthalten ist, eine Versions Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="885f6-129">If /g1 is not set, RC will not generate a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-130"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="885f6-130"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-131">Zeigt die Liste der Befehlszeilenoptionen an.</span><span class="sxs-lookup"><span data-stu-id="885f6-131">Displays the list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-132"><span id="_I"></span><span id="_i"></span>**/I**</span><span class="sxs-lookup"><span data-stu-id="885f6-132"><span id="_I"></span><span id="_i"></span>**/I**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-133">Durchsucht das angegebene Verzeichnis, bevor die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="885f6-133">Searches the specified directory before searching the directories specified by the INCLUDE environment variable.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span><span class="sxs-lookup"><span data-stu-id="885f6-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span></span>
</dt> <dd>

<span data-ttu-id="885f6-135">Lokalisierbare Ressourcentypen RC stellt die sprachabhängige (MUI) dar. RES-Datei.</span><span class="sxs-lookup"><span data-stu-id="885f6-135">Localizable resource types RC places into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="885f6-136">Wenn die **/q** -Option ebenfalls festgelegt ist, wird diese Option ignoriert, und die Informationen in der RC-Konfigurationsdatei haben Vorrang.</span><span class="sxs-lookup"><span data-stu-id="885f6-136">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="885f6-137">**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die [**loadmuilibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) -Funktion und die [**fremuilibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) -Funktion in einem aktualisierten System zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="885f6-137">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *über Schreib*</span><span class="sxs-lookup"><span data-stu-id="885f6-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *overtype*</span></span>
</dt> <dd>

<span data-ttu-id="885f6-139">Überlappende Ressourcentypen, die RC in beide Sprachen neutral stellen. RES und die sprachabhängige (MUI). RES-Dateien.</span><span class="sxs-lookup"><span data-stu-id="885f6-139">Overlapping resource types that RC places into both the language-neutral .RES and the language-dependent (MUI).RES files.</span></span> <span data-ttu-id="885f6-140">Die von der **/k** -Option angegebenen Ressourcentypen müssen eine Teilmenge der von der **/j** -Option angegebenen Ressourcentypen sein.</span><span class="sxs-lookup"><span data-stu-id="885f6-140">The resource types that are specified by the **/k** option must be a subset of those that are specified by the **/j** option.</span></span> <span data-ttu-id="885f6-141">Zum Beispiel? J2? J3? "K3" gibt an, dass RC den Ressourcentyp 3 in den sprach neutralen und sprach abhängigen Dateien (MUI) platziert.</span><span class="sxs-lookup"><span data-stu-id="885f6-141">For example, ?J2 ?J3 ?K3 specifies that RC places resource type 3 in both the language-neutral and language-dependent (MUI) files.</span></span> <span data-ttu-id="885f6-142">Wenn die **/q** -Option ebenfalls festgelegt ist, wird diese Option ignoriert, und die Informationen in der RC-Konfigurationsdatei haben Vorrang.</span><span class="sxs-lookup"><span data-stu-id="885f6-142">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="885f6-143">**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die [**loadmuilibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) -Funktion und die [**fremuilibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) -Funktion in einem aktualisierten System zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="885f6-143">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *LangID*</span><span class="sxs-lookup"><span data-stu-id="885f6-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*</span></span>
</dt> <dd>

<span data-ttu-id="885f6-145">Gibt die Standardsprache für die Kompilierung an.</span><span class="sxs-lookup"><span data-stu-id="885f6-145">Specifies the default language for compilation.</span></span> <span data-ttu-id="885f6-146">Beispielsweise entspricht-L409 dem einschließen der folgenden-Anweisung am Anfang der Ressourcen Skriptdatei: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span><span class="sxs-lookup"><span data-stu-id="885f6-146">For example, -l409 is equivalent to including the following statement at the top of the resource script file: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span></span>

<span data-ttu-id="885f6-147">Weitere Informationen finden Sie unter [sprach](/windows/desktop/Intl/language-identifiers)Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="885f6-147">For more information, see [Language Identifiers](/windows/desktop/Intl/language-identifiers).</span></span>

</dd> <dt>

<span data-ttu-id="885f6-148"><span id="_n"></span><span id="_N"></span>**/n**</span><span class="sxs-lookup"><span data-stu-id="885f6-148"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-149">Null beendet alle Zeichen folgen in der Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="885f6-149">Null terminates all strings in the string table.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *MUI. rcconfig*</span><span class="sxs-lookup"><span data-stu-id="885f6-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *Mui.RCConfig*</span></span>
</dt> <dd>

<span data-ttu-id="885f6-151">Eine RC-Konfigurationsdatei, die dem Format der RC-Konfigurationsdatei folgt.</span><span class="sxs-lookup"><span data-stu-id="885f6-151">An RC configuration file that follows the RC Configuration File format.</span></span> <span data-ttu-id="885f6-152">Das Format der RC-Konfigurationsdatei ermöglicht es Komponenten, Ressourcen Informationen, wie z. b. Ressourcen Versionsverwaltung, MUI-Dateipfad, Ressourcentypen und Elemente, selbst zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="885f6-152">The RC Configuration File format enables components to self-describe resource information such as resource versioning, MUI file path, resource types and items.</span></span> <span data-ttu-id="885f6-153">Mit dieser Datei wird angegeben, welche Ressourcen in die sprachneutrale Sprache gelangen. RES-Datei und welche Ressourcen in den sprach abhängigen (MUI). RES-Datei.</span><span class="sxs-lookup"><span data-stu-id="885f6-153">This file specifies which resources go into the language-neutral .RES file and which resources go into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="885f6-154">Diese Option und die Informationen in der RC-Konfigurationsdatei überschreiben die Befehlszeilenoptionen **/j** und **/k**.</span><span class="sxs-lookup"><span data-stu-id="885f6-154">This option, and the information provided in the RC Configuration file, override the command line options **/j** and **/k**.</span></span>

<span data-ttu-id="885f6-155">**Windows Server 2003 und Windows XP/2000:** Diese Option ist nicht verfügbar, ohne auch die [**loadmuilibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) -Funktion und die [**fremuilibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) -Funktion in einem aktualisierten System zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="885f6-155">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-156"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="885f6-156"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-157">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="885f6-157">Ignored.</span></span> <span data-ttu-id="885f6-158">Wird aus Gründen der Kompatibilität mit vorhandenen Makefiles bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="885f6-158">Provided for compatibility with existing makefiles.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-159"><span id="_u"></span><span id="_U"></span>**/u**</span><span class="sxs-lookup"><span data-stu-id="885f6-159"><span id="_u"></span><span id="_U"></span>**/u**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-160">Definiert ein Symbol für den Präprozessor.</span><span class="sxs-lookup"><span data-stu-id="885f6-160">Undefines a symbol for the preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-161"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="885f6-161"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-162">Zeigt Meldungen an, die den Fortschritt des Compilers melden.</span><span class="sxs-lookup"><span data-stu-id="885f6-162">Displays messages that report on the progress of the compiler.</span></span>

</dd> <dt>

<span data-ttu-id="885f6-163"><span id="_x"></span><span id="_X"></span>**/x**</span><span class="sxs-lookup"><span data-stu-id="885f6-163"><span id="_x"></span><span id="_X"></span>**/x**</span></span>
</dt> <dd>

<span data-ttu-id="885f6-164">Verhindert, dass RC die include-Umgebungsvariable bei der Suche nach Header Dateien oder Ressourcen Dateien prüft.</span><span class="sxs-lookup"><span data-stu-id="885f6-164">Prevents RC from checking the INCLUDE environment variable when searching for header files or resource files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="885f6-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="885f6-165">Remarks</span></span>

<span data-ttu-id="885f6-166">Bei den Optionen wird die Groß-/Kleinschreibung nicht beachtet, und ein Bindestrich (-) kann anstelle eines Schrägstrichs (/) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="885f6-166">Options are not case sensitive, and a hyphen (-) can be used in place of a slash mark (/).</span></span> <span data-ttu-id="885f6-167">Sie können Optionen für einzelne Buchstaben kombinieren, wenn Sie keine zusätzlichen Parameter benötigen.</span><span class="sxs-lookup"><span data-stu-id="885f6-167">You can combine single-letter options if they do not require any additional parameters.</span></span>

<span data-ttu-id="885f6-168">RC generiert in den folgenden Fällen keine MUI-Datei.</span><span class="sxs-lookup"><span data-stu-id="885f6-168">RC will not generate a MUI file in the following cases.</span></span>

-   <span data-ttu-id="885f6-169">In der RC-Datei sind keine lokalisierbaren Ressourcen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="885f6-169">No localizable resources exist in the .rc file.</span></span>
-   <span data-ttu-id="885f6-170">Die einzige in der RC-Datei angegebene Ressourcen Sprachen-ID ist neutral (0x0).</span><span class="sxs-lookup"><span data-stu-id="885f6-170">The only resource language id specified in the .rc file is neutral (0x0).</span></span>
-   <span data-ttu-id="885f6-171">Die RC-Datei verfügt über Ressourcen, die in mehr als einer Sprache angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="885f6-171">The .rc file has resources that are specified in more than one language.</span></span> <span data-ttu-id="885f6-172">Die Ausnahme besteht darin, dass die RC-Datei zwei Sprachen enthält und eine Sprache neutral (0x0) ist, dass RC eine MUI-Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="885f6-172">The exception is if the .rc file contains two languages, and one language is neutral (0x0), RC generates a MUI file.</span></span>

<span data-ttu-id="885f6-173">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="885f6-173">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="885f6-174">Definieren von Namen für den Präprozessor</span><span class="sxs-lookup"><span data-stu-id="885f6-174">Defining Names for the Preprocessor</span></span>](defining-names-for-the-preprocessor.md)
-   [<span data-ttu-id="885f6-175">Umbenennen der kompilierten Ressourcen Datei</span><span class="sxs-lookup"><span data-stu-id="885f6-175">Renaming the Compiled Resource File</span></span>](renaming-the-compiled-resource-file.md)
-   [<span data-ttu-id="885f6-176">Dateien werden gesucht</span><span class="sxs-lookup"><span data-stu-id="885f6-176">Searching for Files</span></span>](searching-for-files.md)
-   [<span data-ttu-id="885f6-177">Anzeigen von Statusmeldungen</span><span class="sxs-lookup"><span data-stu-id="885f6-177">Displaying Progress Messages</span></span>](displaying-progress-messages.md)
-   [<span data-ttu-id="885f6-178">RC-Diagnosemeldungen</span><span class="sxs-lookup"><span data-stu-id="885f6-178">RC Diagnostic Messages</span></span>](rc-diagnostic-messages.md)

## <a name="related-topics"></a><span data-ttu-id="885f6-179">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="885f6-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="885f6-180">Multilingual User Interface</span><span class="sxs-lookup"><span data-stu-id="885f6-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 