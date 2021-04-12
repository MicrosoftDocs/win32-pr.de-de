---
description: In den folgenden Informationsmeldungen wird der compilervorgang beschrieben.
ms.assetid: 838e598d-871d-4015-a372-4d94cacf8048
ms.tgt_platform: multiple
title: Allgemeine Informationsmeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0997fad497299c7598fc1130edace49c20d7bb76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344909"
---
# <a name="general-information-messages"></a><span data-ttu-id="c718c-103">Allgemeine Informationsmeldungen</span><span class="sxs-lookup"><span data-stu-id="c718c-103">General Information Messages</span></span>

<span data-ttu-id="c718c-104">In den folgenden Informationsmeldungen wird der compilervorgang beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c718c-104">The following information messages describe the compiler operation.</span></span>

<dl> <dt>

<span data-ttu-id="c718c-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**Smi2smir: Version <Version \#> MIB-Definitionen, die aus kompiliert wurden <file name>**</span><span class="sxs-lookup"><span data-stu-id="c718c-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: Version <version \#> MIB definitions compiled from <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-106">Diese Meldung wird am Anfang jeder Datei Kompilierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c718c-106">This message appears at the beginning of every file compilation.</span></span> <span data-ttu-id="c718c-107">Dies bedeutet, dass die Datei möglicherweise explizit vom Benutzer in der Befehlszeile angegeben wurde, oder Sie wurde vom Compiler aus den Includeverzeichnissen der Registrierung oder den Includeverzeichnissen, die in der Befehlszeile angegeben sind, abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c718c-107">It means the file may have been explicitly specified on the command line by the user, or it may have been pulled in by the compiler from the registry include directories or the include directories mentioned on the command line.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**Smi2smir: Fehler beim Überprüfen der Syntax. <file name>**</span><span class="sxs-lookup"><span data-stu-id="c718c-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Syntax check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-109">Die spezifischen Fehlermeldungen, die dieser Meldung vorangestellt sind, haben die Art der Syntax Fehler.</span><span class="sxs-lookup"><span data-stu-id="c718c-109">The specific error messages that precede this message give the nature of the syntax errors.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**Smi2smir: Fehler beim Überprüfen der Semantik. <file name>**</span><span class="sxs-lookup"><span data-stu-id="c718c-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Semantic check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-111">Die spezifischen Fehlermeldungen, die dieser Meldung vorangestellt sind, haben die Art der Semantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="c718c-111">The specific error messages that precede this message give the nature of the semantic errors.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**Smi2smir: konnte nicht <file name> in SMIR geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="c718c-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: Could not load <file name> into the smir**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-113">Die Syntax-oder Semantik Überprüfung für das Modul ist fehlgeschlagen, oder die SMIR-Interaktion war nicht fertig.</span><span class="sxs-lookup"><span data-stu-id="c718c-113">Syntax or semantic check failed on the module, or SMIR interaction was not complete.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**Smi2smir: Syntax Überprüfung erfolgreich auf <file name>**</span><span class="sxs-lookup"><span data-stu-id="c718c-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Syntax check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c718c-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**Smi2smir: semantische Prüfung erfolgreich auf <file name>**</span><span class="sxs-lookup"><span data-stu-id="c718c-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Semantic check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c718c-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**Smi2smir: <file name> erfolgreich in SMIR geladen**</span><span class="sxs-lookup"><span data-stu-id="c718c-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: Loaded <file name> successfully into the smir**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c718c-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**Smi2smir: mindestens ein Symbol in konnte nicht aufgelöst werden. <module name>**</span><span class="sxs-lookup"><span data-stu-id="c718c-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: Could not resolve one or more symbols in <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-118">Die Module, die einem oder mehreren importierten Symbolen im angegebenen Modul entsprechen, wurden nicht gefunden oder konnten nicht kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="c718c-118">The modules corresponding to one or more of the imported symbols in the specified module were not found or could not be compiled.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**Smi2smir: Es konnte keine Verbindung mit dem SMIR hergestellt werden.**</span><span class="sxs-lookup"><span data-stu-id="c718c-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: Could not connect to the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-120">Stellen Sie sicher, dass Smir.dll vorhanden ist, mit dem regsvr32-Befehl registriert wurde und dass der WMI-Server (Windows-Verwaltungsinstrumentation) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c718c-120">Ensure that Smir.dll exists, has been registered using the regsvr32 command, and that the Windows Management Instrumentation (WMI) server is up and running.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**Smi2smir: Module in der SMIR: <Liste der Module, 1 in jeder Zeile>**</span><span class="sxs-lookup"><span data-stu-id="c718c-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: Modules in the SMIR: <list of modules, 1 on each line>**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-122">Dies ist die Ausgabe des **/l** -Schalters.</span><span class="sxs-lookup"><span data-stu-id="c718c-122">This is the output of the **/l** switch.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir konnte die Module in SMIR nicht auflisten.**</span><span class="sxs-lookup"><span data-stu-id="c718c-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir Could not list the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-124">Dies weist auf einen Fehler des **/l** -Schalters aufgrund einer SMIR-Verbindung hin.</span><span class="sxs-lookup"><span data-stu-id="c718c-124">This indicates a failure of the **/l** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**Smi2smir: Modul wurde <module name> erfolgreich gelöscht.**</span><span class="sxs-lookup"><span data-stu-id="c718c-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: Deleted module <module name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-126">Der Schalter " **/d** " war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c718c-126">The **/d** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**Smi2smir: Modul konnte nicht gelöscht werden. <module name>**</span><span class="sxs-lookup"><span data-stu-id="c718c-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: Could not delete module <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-128">Dies weist auf einen Fehler des **/d** -Schalters aufgrund einer SMIR-Verbindung hin.</span><span class="sxs-lookup"><span data-stu-id="c718c-128">This indicates a failure of the **/d** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir: alle Module in SMIR gelöscht**</span><span class="sxs-lookup"><span data-stu-id="c718c-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Deleted all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-130">Der Schalter " **/p** " war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c718c-130">The **/p** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir: alle Module in SMIR konnten nicht gelöscht werden.**</span><span class="sxs-lookup"><span data-stu-id="c718c-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Could not delete all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-132">Fehler beim **/p** -Switch, weil keine SMIR-Verbindung besteht.</span><span class="sxs-lookup"><span data-stu-id="c718c-132">The **/p** switch failed because there is no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**Smi2smir: <module name> das Modul ist nicht in SMIR vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="c718c-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: Module <module name> does not exist in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-134">Der **/d** -Schalter ist fehlgeschlagen, da das angegebene Modul nicht in SMIR angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c718c-134">The **/d** switch failed because the specified module is not in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**Smi2smir: MOF erfolgreich generiert**</span><span class="sxs-lookup"><span data-stu-id="c718c-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: Generated MOF successfully**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-136">Der Schalter " **/g** " oder " **/GC** " war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c718c-136">The **/g** or **/gc** switch worked successfully.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**Smi2smir: MOF konnte nicht generiert werden.**</span><span class="sxs-lookup"><span data-stu-id="c718c-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: Could not generate MOF**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-138">Der Schalter " **/g** " oder " **/GC** " konnte nicht erfolgreich ausgeführt werden, da keine SMIR-Verbindung besteht.</span><span class="sxs-lookup"><span data-stu-id="c718c-138">The **/g** or **/gc** switch did not work successfully due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**Smi2smir: Name des Moduls: <module name>**</span><span class="sxs-lookup"><span data-stu-id="c718c-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: Name of the module: <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-140">Dies ist die erfolgreiche Ausgabe des **/n** -Schalters.</span><span class="sxs-lookup"><span data-stu-id="c718c-140">This is the successful output of the **/n** switch.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**Smi2smir: konnte nicht erfolgreich analysiert werden. <file name>**</span><span class="sxs-lookup"><span data-stu-id="c718c-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: Could not parse <file name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-142">Dies weist auf einen Fehler des **/n** -oder **/NI** -Schalters hin, da die angegebene Datei keine gültige MIB-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="c718c-142">This indicates failure of the **/n** or **/ni** switch because the specified file is not a valid MIB file.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**Smi2smir: Dateien wurden erfolgreich verarbeitet. <number>**</span><span class="sxs-lookup"><span data-stu-id="c718c-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: Processed <number> files successfully**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-144">Gibt die Anzahl der Dateien an, die erfolgreich analysiert wurden, als der **/r** -oder **/Auto** -Schalter verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c718c-144">This specifies the number of files that were successfully parsed when the **/r** or the **/auto** switch were used.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**Smi2smir: wiederholte Dateien in der Eingabe für das Modul <module name> . Nur die Datei <file name> wird kompiliert.**</span><span class="sxs-lookup"><span data-stu-id="c718c-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: Repeated files in the input for module <module name>. Only the file <file name> will be compiled**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-146">Der Benutzer hat in der Befehlszeile explizit mehr als eine Datei angegeben, und mindestens zwei Dateien weisen das gleiche MIB-Modul auf.</span><span class="sxs-lookup"><span data-stu-id="c718c-146">The user has explicitly specified more than one file on the command line, and two or more of these files have the same MIB module.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**Smi2smir: Verzeichnis <directory name> zur Registrierung hinzugefügt**</span><span class="sxs-lookup"><span data-stu-id="c718c-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Added directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-148">Erfolg des **/PA** -Schalters.</span><span class="sxs-lookup"><span data-stu-id="c718c-148">Success of the **/pa** switch.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**Smi2smir: das Verzeichnis konnte nicht zur Registrierung hinzugefügt werden. <directory name>**</span><span class="sxs-lookup"><span data-stu-id="c718c-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Could not add directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-150">Fehler des **/PA** -Schalters. Dies geschieht nur, wenn die Registrierungs-API ausfällt.</span><span class="sxs-lookup"><span data-stu-id="c718c-150">Failure of the **/pa** switch, which happens only if the registry API fails.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**Smi2smir: Verzeichnis <directory name> aus der Registrierung gelöscht**</span><span class="sxs-lookup"><span data-stu-id="c718c-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Deleted directory <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-152">Erfolg des **/PD** -Schalters.</span><span class="sxs-lookup"><span data-stu-id="c718c-152">Success of the **/pd** switch.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**Smi2smir: <directory name> aus der Registrierung konnte nicht gelöscht werden.**</span><span class="sxs-lookup"><span data-stu-id="c718c-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Could not delete <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-154">Fehler beim **/PD** -Schalter.</span><span class="sxs-lookup"><span data-stu-id="c718c-154">Failure of the **/pd** switch.</span></span> <span data-ttu-id="c718c-155">Das angegebene Verzeichnis ist nicht in der Liste der Verzeichnisse in der Registrierung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c718c-155">The specified directory does not exist in the list of directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="c718c-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**Smi2smir: <file name> ist keine gültige MIB-Datei.**</span><span class="sxs-lookup"><span data-stu-id="c718c-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> is not a valid mib file**</span></span>
</dt> <dd>

<span data-ttu-id="c718c-157">In der Befehlszeile wurde mehr als eine Datei angegeben, von denen eine keine gültige MIB-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="c718c-157">More than one file has been specified on the command line, one of which is not a valid MIB file.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c718c-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c718c-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c718c-159">Einrichten der WMI-SNMP-Umgebung</span><span class="sxs-lookup"><span data-stu-id="c718c-159">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



