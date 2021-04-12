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
# <a name="general-information-messages"></a>Allgemeine Informationsmeldungen

In den folgenden Informationsmeldungen wird der compilervorgang beschrieben.

<dl> <dt>

<span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**Smi2smir: Version <Version \#> MIB-Definitionen, die aus kompiliert wurden <file name>**
</dt> <dd>

Diese Meldung wird am Anfang jeder Datei Kompilierung angezeigt. Dies bedeutet, dass die Datei möglicherweise explizit vom Benutzer in der Befehlszeile angegeben wurde, oder Sie wurde vom Compiler aus den Includeverzeichnissen der Registrierung oder den Includeverzeichnissen, die in der Befehlszeile angegeben sind, abgerufen.

</dd> <dt>

<span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**Smi2smir: Fehler beim Überprüfen der Syntax. <file name>**
</dt> <dd>

Die spezifischen Fehlermeldungen, die dieser Meldung vorangestellt sind, haben die Art der Syntax Fehler.

</dd> <dt>

<span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**Smi2smir: Fehler beim Überprüfen der Semantik. <file name>**
</dt> <dd>

Die spezifischen Fehlermeldungen, die dieser Meldung vorangestellt sind, haben die Art der Semantik Fehler.

</dd> <dt>

<span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**Smi2smir: konnte nicht <file name> in SMIR geladen werden.**
</dt> <dd>

Die Syntax-oder Semantik Überprüfung für das Modul ist fehlgeschlagen, oder die SMIR-Interaktion war nicht fertig.

</dd> <dt>

<span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**Smi2smir: Syntax Überprüfung erfolgreich auf <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**Smi2smir: semantische Prüfung erfolgreich auf <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**Smi2smir: <file name> erfolgreich in SMIR geladen**
</dt> <dd></dd> <dt>

<span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**Smi2smir: mindestens ein Symbol in konnte nicht aufgelöst werden. <module name>**
</dt> <dd>

Die Module, die einem oder mehreren importierten Symbolen im angegebenen Modul entsprechen, wurden nicht gefunden oder konnten nicht kompiliert werden.

</dd> <dt>

<span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**Smi2smir: Es konnte keine Verbindung mit dem SMIR hergestellt werden.**
</dt> <dd>

Stellen Sie sicher, dass Smir.dll vorhanden ist, mit dem regsvr32-Befehl registriert wurde und dass der WMI-Server (Windows-Verwaltungsinstrumentation) ausgeführt wird.

</dd> <dt>

<span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**Smi2smir: Module in der SMIR: <Liste der Module, 1 in jeder Zeile>**
</dt> <dd>

Dies ist die Ausgabe des **/l** -Schalters.

</dd> <dt>

<span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir konnte die Module in SMIR nicht auflisten.**
</dt> <dd>

Dies weist auf einen Fehler des **/l** -Schalters aufgrund einer SMIR-Verbindung hin.

</dd> <dt>

<span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**Smi2smir: Modul wurde <module name> erfolgreich gelöscht.**
</dt> <dd>

Der Schalter " **/d** " war erfolgreich.

</dd> <dt>

<span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**Smi2smir: Modul konnte nicht gelöscht werden. <module name>**
</dt> <dd>

Dies weist auf einen Fehler des **/d** -Schalters aufgrund einer SMIR-Verbindung hin.

</dd> <dt>

<span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir: alle Module in SMIR gelöscht**
</dt> <dd>

Der Schalter " **/p** " war erfolgreich.

</dd> <dt>

<span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**Smi2smir: alle Module in SMIR konnten nicht gelöscht werden.**
</dt> <dd>

Fehler beim **/p** -Switch, weil keine SMIR-Verbindung besteht.

</dd> <dt>

<span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**Smi2smir: <module name> das Modul ist nicht in SMIR vorhanden.**
</dt> <dd>

Der **/d** -Schalter ist fehlgeschlagen, da das angegebene Modul nicht in SMIR angegeben ist.

</dd> <dt>

<span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**Smi2smir: MOF erfolgreich generiert**
</dt> <dd>

Der Schalter " **/g** " oder " **/GC** " war erfolgreich.

</dd> <dt>

<span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**Smi2smir: MOF konnte nicht generiert werden.**
</dt> <dd>

Der Schalter " **/g** " oder " **/GC** " konnte nicht erfolgreich ausgeführt werden, da keine SMIR-Verbindung besteht.

</dd> <dt>

<span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**Smi2smir: Name des Moduls: <module name>**
</dt> <dd>

Dies ist die erfolgreiche Ausgabe des **/n** -Schalters.

</dd> <dt>

<span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**Smi2smir: konnte nicht erfolgreich analysiert werden. <file name>**
</dt> <dd>

Dies weist auf einen Fehler des **/n** -oder **/NI** -Schalters hin, da die angegebene Datei keine gültige MIB-Datei ist.

</dd> <dt>

<span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**Smi2smir: Dateien wurden erfolgreich verarbeitet. <number>**
</dt> <dd>

Gibt die Anzahl der Dateien an, die erfolgreich analysiert wurden, als der **/r** -oder **/Auto** -Schalter verwendet wurde.

</dd> <dt>

<span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**Smi2smir: wiederholte Dateien in der Eingabe für das Modul <module name> . Nur die Datei <file name> wird kompiliert.**
</dt> <dd>

Der Benutzer hat in der Befehlszeile explizit mehr als eine Datei angegeben, und mindestens zwei Dateien weisen das gleiche MIB-Modul auf.

</dd> <dt>

<span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**Smi2smir: Verzeichnis <directory name> zur Registrierung hinzugefügt**
</dt> <dd>

Erfolg des **/PA** -Schalters.

</dd> <dt>

<span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**Smi2smir: das Verzeichnis konnte nicht zur Registrierung hinzugefügt werden. <directory name>**
</dt> <dd>

Fehler des **/PA** -Schalters. Dies geschieht nur, wenn die Registrierungs-API ausfällt.

</dd> <dt>

<span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**Smi2smir: Verzeichnis <directory name> aus der Registrierung gelöscht**
</dt> <dd>

Erfolg des **/PD** -Schalters.

</dd> <dt>

<span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**Smi2smir: <directory name> aus der Registrierung konnte nicht gelöscht werden.**
</dt> <dd>

Fehler beim **/PD** -Schalter. Das angegebene Verzeichnis ist nicht in der Liste der Verzeichnisse in der Registrierung vorhanden.

</dd> <dt>

<span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**Smi2smir: <file name> ist keine gültige MIB-Datei.**
</dt> <dd>

In der Befehlszeile wurde mehr als eine Datei angegeben, von denen eine keine gültige MIB-Datei ist.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



