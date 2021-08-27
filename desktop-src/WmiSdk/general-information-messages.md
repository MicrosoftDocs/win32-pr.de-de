---
description: Die folgenden Informationsmeldungen beschreiben den Compilervorgang.
ms.assetid: 838e598d-871d-4015-a372-4d94cacf8048
ms.tgt_platform: multiple
title: Allgemeine Informationsmeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680bcf7c2b9cbea5e60d13a7dd2aa6be93d9fad0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882731"
---
# <a name="general-information-messages"></a>Allgemeine Informationsmeldungen

Die folgenden Informationsmeldungen beschreiben den Compilervorgang.

<dl> <dt>

<span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: Version <version \#> MIB definitions compiled from <file name>**
</dt> <dd>

Diese Meldung wird am Anfang jeder Dateikompilierung angezeigt. Dies bedeutet, dass die Datei möglicherweise explizit vom Benutzer in der Befehlszeile angegeben wurde oder vom Compiler aus den Includeverzeichnissen der Registrierung oder den include-Verzeichnissen, die in der Befehlszeile erwähnt werden, per Pull in die Datei gezogen wurde.

</dd> <dt>

<span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Syntaxprüfung fehlgeschlagen <file name>**
</dt> <dd>

Die spezifischen Fehlermeldungen vor dieser Meldung geben die Art der Syntaxfehler an.

</dd> <dt>

<span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Semantic check failed on (Semantikprüfung fehlgeschlagen) <file name>**
</dt> <dd>

Die spezifischen Fehlermeldungen vor dieser Meldung geben die Art der semantischen Fehler an.

</dd> <dt>

<span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: Could not load <file name> into the Smir**
</dt> <dd>

Die Syntax- oder Semantikprüfung für das Modul ist fehlgeschlagen, oder die SMIR-Interaktion war nicht abgeschlossen.

</dd> <dt>

<span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Syntaxprüfung erfolgreich am <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Semantikprüfung erfolgreich am <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: Erfolgreich <file name> in den Smir geladen**
</dt> <dd></dd> <dt>

<span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: Ein oder mehrere Symbole in konnten nicht behoben werden. <module name>**
</dt> <dd>

Die Module, die mindestens einem der importierten Symbole im angegebenen Modul entspricht, wurden nicht gefunden oder konnten nicht kompiliert werden.

</dd> <dt>

<span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: Es konnte keine Verbindung mit SMIR hergestellt werden.**
</dt> <dd>

Stellen Sie sicher, Smir.dll vorhanden ist, mit dem Befehl regsvr32 registriert wurde und dass der WMI-Server (Windows Management Instrumentation) ausgeführt wird.

</dd> <dt>

<span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: Modules in the SMIR: <list of modules, 1 on each line>**
</dt> <dd>

Dies ist die Ausgabe des **Schalters /l.**

</dd> <dt>

<span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir Could not list the modules in the SMIR (smi2smir Konnte die Module im SMIR nicht auflisten)**
</dt> <dd>

Dies weist auf einen Fehler des **Schalters /l** hin, weil keine SMIR-Verbindung besteht.

</dd> <dt>

<span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: Das Modul wurde erfolgreich <module name> gelöscht.**
</dt> <dd>

Der **Schalter /d** war erfolgreich.

</dd> <dt>

<span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: Das Modul konnte nicht gelöscht werden. <module name>**
</dt> <dd>

Dies weist auf einen Fehler des **Schalters /d** hin, weil keine SMIR-Verbindung besteht.

</dd> <dt>

<span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Alle Module im SMIR gelöscht**
</dt> <dd>

Der **Schalter /p** war erfolgreich.

</dd> <dt>

<span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Alle Module im SMIR konnten nicht gelöscht werden.**
</dt> <dd>

Fehler **beim /p-Schalter,** da keine SMIR-Verbindung besteht.

</dd> <dt>

<span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: Das <module name> Modul ist im SMIR nicht vorhanden.**
</dt> <dd>

Fehler **beim /d-Schalter,** da sich das angegebene Modul nicht im SMIR befindet.

</dd> <dt>

<span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: Mof erfolgreich generiert**
</dt> <dd>

Der **Schalter /g** oder **/gc** hat erfolgreich funktioniert.

</dd> <dt>

<span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: MOF konnte nicht generiert werden.**
</dt> <dd>

Der **Schalter /g** oder **/gc** funktionierte aufgrund einer SMIR-Verbindung nicht erfolgreich.

</dd> <dt>

<span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: Name des Moduls: <module name>**
</dt> <dd>

Dies ist die erfolgreiche Ausgabe des **Schalters /n.**

</dd> <dt>

<span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: Die Analyse konnte nicht erfolgreich <file name> ausgeführt werden.**
</dt> <dd>

Dies weist auf einen Fehler des **Schalters /n** oder **/ni** hin, da die angegebene Datei keine gültige MIB-Datei ist.

</dd> <dt>

<span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: &lt; Zahlendateien &gt; wurden erfolgreich verarbeitet.**
</dt> <dd>

Dies gibt die Anzahl der Dateien an, die erfolgreich analysiert wurden, als der Schalter **/r** oder **/auto** verwendet wurde.

</dd> <dt>

<span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: Wiederholte Dateien in der Eingabe für das Modul <module name> . Nur die <file name> Datei wird kompiliert.**
</dt> <dd>

Der Benutzer hat explizit mehr als eine Datei in der Befehlszeile angegeben, und mindestens zwei dieser Dateien verfügen über das gleiche MIB-Modul.

</dd> <dt>

<span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Verzeichnis zur <directory name> Registrierung hinzugefügt**
</dt> <dd>

Erfolg des **Schalters /pa.**

</dd> <dt>

<span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Das Verzeichnis konnte der Registrierung <directory name> nicht hinzugefügt werden.**
</dt> <dd>

Fehler beim **/pa-Schalter,** der nur auftritt, wenn die Registrierungs-API fehlschlägt.

</dd> <dt>

<span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Verzeichnis aus <directory name> der Registrierung gelöscht**
</dt> <dd>

Erfolg des **Schalters /pd.**

</dd> <dt>

<span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Could not delete from the registry (smi2smir: Aus der <directory name> Registrierung konnte nicht gelöscht werden)**
</dt> <dd>

Fehler des Schalters **/pd.** Das angegebene Verzeichnis ist in der Liste der Verzeichnisse in der Registrierung nicht vorhanden.

</dd> <dt>

<span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> ist keine gültige mib-Datei.**
</dt> <dd>

In der Befehlszeile wurde mehr als eine Datei angegeben, von denen eine keine gültige MIB-Datei ist.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



