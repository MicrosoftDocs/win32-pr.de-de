---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 101 bis 110.
ms.assetid: baa64233-eb19-4f52-836b-5bdf4a23ae4f
ms.tgt_platform: multiple
title: Fehler 101 bis 110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21874ada13d15920e755e5061ec638ad51fa0f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343818"
---
# <a name="errors-101-through-110"></a>Fehler 101 bis 110

Beschreibt die WMI-SNMP-Anbieter Fehler 101 bis 110.

[Schwerwiegender Fehler 101](#fatal-error-101)

[Schwerwiegender Fehler 102](#fatal-error-102)

[Schwerwiegender Fehler 103](#fatal-error-103)

[Schwerwiegender Fehler 104](#fatal-error-104)

[Schwerwiegender Fehler 105](#fatal-error-105)

[Schwerwiegender Fehler 106](#fatal-error-106)

[Schwerwiegender Fehler 107](#fatal-error-107)

[Schwerwiegender Fehler 108](#fatal-error-108)

[Schwerwiegender Fehler 109](#fatal-error-109)

[Warnung 110](#warning-110)

## <a name="fatal-error-101"></a>Schwerwiegender Fehler 101

<dl> <dt>

<span id="_101__Fatal____Usage_"></span><span id="_101__fatal____usage_"></span><span id="_101__FATAL____USAGE_"></span>**<101, schwerwiegender>: "Verwendung:**
</dt> <dd></dd> <dt>

<span id="smi2smir__DiagnosticArgs___VersionArgs___CommandArgs_"></span><span id="smi2smir__diagnosticargs___versionargs___commandargs_"></span><span id="SMI2SMIR__DIAGNOSTICARGS___VERSIONARGS___COMMANDARGS_"></span>**Smi2smir <DiagnosticArgs> <VersionArgs><CommandArgs>**
</dt> <dd></dd> <dt>

<span id="smi2smir__DiagnosticArgs___RegistryArgs_"></span><span id="smi2smir__diagnosticargs___registryargs_"></span><span id="SMI2SMIR__DIAGNOSTICARGS___REGISTRYARGS_"></span>**Smi2smir <DiagnosticArgs><RegistryArgs>**
</dt> <dd></dd> <dt>

<span id="smi2smir__HelpArgs__"></span><span id="smi2smir__helpargs__"></span><span id="SMI2SMIR__HELPARGS__"></span>**Smi2smir <HelpArgs> "**
</dt> <dd>

Befehlszeilen-Syntax Fehler. Darauf folgt eine Erläuterung der Switches.

</dd> </dl>

## <a name="fatal-error-102"></a>Schwerwiegender Fehler 102

<dl> <dt>

<span id="_102__Fatal___Invalid_argument_on_command_line_after__last_correct_argument__"></span><span id="_102__fatal___invalid_argument_on_command_line_after__last_correct_argument__"></span><span id="_102__FATAL___INVALID_ARGUMENT_ON_COMMAND_LINE_AFTER__LAST_CORRECT_ARGUMENT__"></span>**<102, schwerwiegender>: "Ungültiges Argument in der Befehlszeile nach <last correct argument> " "**
</dt> <dd>

Befehlszeilen-Syntax Fehler. Es gibt einige zusätzliche Argumente, oder ein Switch ist nicht in der Befehlszeile gültig. Der <last correct argument> -Parameter verweist auf das letzte Argument, das in der Befehlszeile ordnungsgemäß gelesen wurde, und kann möglicherweise Smi2smir sein. Dies ist der Name der ausführbaren Datei für den SNMP-Modul Informations Compiler.

</dd> </dl>

## <a name="fatal-error-103"></a>Schwerwiegender Fehler 103

<dl> <dt>

<span id="_103__Fatal____Diagnostic_Level_not_specified_for_the__m_switch_"></span><span id="_103__fatal____diagnostic_level_not_specified_for_the__m_switch_"></span><span id="_103__FATAL____DIAGNOSTIC_LEVEL_NOT_SPECIFIED_FOR_THE__M_SWITCH_"></span>**<103, schwerwiegender>: "die Diagnose Ebene wurde für den/m-Schalter nicht angegeben."**
</dt> <dd>

Befehlszeilen-Syntax Fehler. Wenn Sie den **/m** -Schalter angeben, müssen Sie auch die Diagnose Ebene 0, 1 oder 2 angeben.

</dd> </dl>

## <a name="fatal-error-104"></a>Schwerwiegender Fehler 104

<dl> <dt>

<span id="_104__Fatal____Diagnostic_Level_must_be_0__1_or_2_for_the__m_switch_"></span><span id="_104__fatal____diagnostic_level_must_be_0__1_or_2_for_the__m_switch_"></span><span id="_104__FATAL____DIAGNOSTIC_LEVEL_MUST_BE_0__1_OR_2_FOR_THE__M_SWITCH_"></span>**<104, schwerwiegender>: "die Diagnose Ebene muss 0, 1 oder 2 für den Schalter"/m "lauten.**
</dt> <dd>

Befehlszeilen-Syntax Fehler. Wenn Sie den **/m** -Schalter angeben, müssen Sie auch die Diagnose Ebene 0, 1 oder 2 angeben.

</dd> </dl>

## <a name="fatal-error-105"></a>Schwerwiegender Fehler 105

<dl> <dt>

<span id="_105__Fatal____Maximum_diagnostic_count_missing_after_the__c_switch_"></span><span id="_105__fatal____maximum_diagnostic_count_missing_after_the__c_switch_"></span><span id="_105__FATAL____MAXIMUM_DIAGNOSTIC_COUNT_MISSING_AFTER_THE__C_SWITCH_"></span>**<105, schwerwiegender>: "die maximale Anzahl von Diagnosen fehlt nach dem/c-Switch".**
</dt> <dd>

Befehlszeilen-Syntax Fehler. Wenn Sie den **/c** -Schalter angeben, müssen Sie auch eine nicht negative ganze Zahl als maximale Anzahl angeben.

</dd> </dl>

## <a name="fatal-error-106"></a>Schwerwiegender Fehler 106

<dl> <dt>

<span id="_106__Fatal_____argument__is_not_a_valid_diagnostic_count_"></span><span id="_106__fatal_____argument__is_not_a_valid_diagnostic_count_"></span><span id="_106__FATAL_____ARGUMENT__IS_NOT_A_VALID_DIAGNOSTIC_COUNT_"></span>**<106, schwerwiegender>: " <argument> ist keine gültige Diagnose Anzahl"**
</dt> <dd>

Befehlszeilen-Syntax Fehler. Wenn Sie den **/c** -Schalter angeben, müssen Sie auch eine nicht negative ganze Zahl als maximale Anzahl angeben.

</dd> </dl>

## <a name="fatal-error-107"></a>Schwerwiegender Fehler 107

<dl> <dt>

<span id="_107__Fatal____File_Name_s__missing_"></span><span id="_107__fatal____file_name_s__missing_"></span><span id="_107__FATAL____FILE_NAME_S__MISSING_"></span>**<107, schwerwiegender>: "Dateiname (n) fehlt"**
</dt> <dd>

Semantik Fehler in der Befehlszeile. Mindestens ein Dateiname muss in der Befehlszeile für die angegebene Kombination von Switches angegeben werden.

</dd> </dl>

## <a name="fatal-error-108"></a>Schwerwiegender Fehler 108

<dl> <dt>

<span id="_108__Fatal____No_command_argument_specified_"></span><span id="_108__fatal____no_command_argument_specified_"></span><span id="_108__FATAL____NO_COMMAND_ARGUMENT_SPECIFIED_"></span>**<108, schwerwiegender>: "kein Befehls Argument angegeben"**
</dt> <dd>

Befehlszeilen-Syntax Fehler. Einige Aktionen müssen in der Befehlszeile angegeben werden.

</dd> </dl>

## <a name="fatal-error-109"></a>Schwerwiegender Fehler 109

<dl> <dt>

<span id="_109__Fatal____Module_name_missing_"></span><span id="_109__fatal____module_name_missing_"></span><span id="_109__FATAL____MODULE_NAME_MISSING_"></span>**<109, schwerwiegender>: "Modulname fehlt."**
</dt> <dd>

Befehlszeilen-Syntax Fehler.

</dd> </dl>

## <a name="warning-110"></a>Warnung 110

<dl> <dt>

<span id="_110__Warning____No_include_path_specified_after_the__i_switch_"></span><span id="_110__warning____no_include_path_specified_after_the__i_switch_"></span><span id="_110__WARNING____NO_INCLUDE_PATH_SPECIFIED_AFTER_THE__I_SWITCH_"></span>**<110, Warnung>: "kein Include-Pfad nach dem/i-Schalter angegeben"**
</dt> <dd>

Befehlszeilen Syntax-Warnung. Wenn Sie den **/i** -Schalter angeben, müssen Sie auch den Pfad zu den eingeschlossenen Dateien angeben.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



