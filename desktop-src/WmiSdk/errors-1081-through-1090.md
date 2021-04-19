---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1081 bis 1090.
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: Fehler 1081 bis 1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a80399ef61bce644813447559a76bf9710873be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348547"
---
# <a name="errors-1081-through-1090"></a>Fehler 1081 bis 1090

Beschreibt die WMI-SNMP-Anbieter Fehler 1081 bis 1090.

[Schwerwiegender Fehler 1081](#fatal-error-1081)

[Schwerwiegender Fehler 1082](#fatal-error-1082)

[Schwerwiegender Fehler 1084](#fatal-error-1084)

[Warnung 1085](#warning-1085)

[Warnung 1086](#warning-1086)

[Schwerwiegender Fehler 1087](#fatal-error-1087)

[Schwerwiegender Fehler 1089](#fatal-error-1089)

[Schwerwiegender Fehler 1090](#fatal-error-1090)

## <a name="fatal-error-1081"></a>Schwerwiegender Fehler 1081

<dl> <dt>

<span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, schwerwiegender>: " <fileName> line \#>: Symbol <identifier> nicht im importierten Modul vorhanden <identifier> "**
</dt> <dd>

Modul Semantik Fehler in Querverweisen, spezifisch für weder SNMPv1 noch SNMPv2C. Ein Symbol, das aus einem Modul importiert wird, wird in nichts in diesem Modul aufgelöst. Wenn im MIB tatsächlich auf dieses Symbol verwiesen wird, tritt dieser Fehler auf.

</dd> </dl>

## <a name="fatal-error-1082"></a>Schwerwiegender Fehler 1082

<dl> <dt>

<span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, schwerwiegender>: " <fileName> : <line \#>: Ungültige Status Klausel <clause> "**
</dt> <dd>

**Objekt-Identitäts** -Makro Aufruf, SNMPv2C-spezifischer Modul Semantik Fehler. Die Status-Klausel eines **Objekt Identitäts aufbilden** muss "Current", "deprecated" oder "deprecated" lauten.

</dd> </dl>

## <a name="fatal-error-1084"></a>Schwerwiegender Fehler 1084

<dl> <dt>

<span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, schwerwiegender>: "Dateiname><Zeile \#>: erforderliche Module-Identity nach dem Import Abschnitt für alle SNMPv2-Module"**
</dt> <dd>

**Modul-Identity-** Makro Aufruf, SNMPv2C-spezifischer Modul Semantik Fehler. Es darf nur ein **Modul Identitäts** Aufruf in einem SNMPv2C MIB vorhanden sein, unmittelbar nach dem Import Abschnitt.

</dd> </dl>

## <a name="warning-1085"></a>Warnung 1085

<dl> <dt>

<span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, Warning>: " <fileName><line \#>: im Modul wurden keine Gruppen gefunden <name> . Die Modul Identität konnte nicht fabriziert werden. Der Versuch, das Modul in SMIR zu laden, schlägt fehl.**
</dt> <dd>

Modul Semantik SNMPv1 spezifische Warnung. Dieser Fehler wird generiert, wenn in einem Modul keine Objektgruppen gefunden werden.

</dd> </dl>

## <a name="warning-1086"></a>Warnung 1086

<dl> <dt>

<span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, Warning>: " <fileName><line \#>: im Modul wurden keine Gruppen gefunden <name> "**
</dt> <dd>

Modul Semantik SNMPv1 spezifische Warnung. Dieser Fehler wird generiert, wenn in einem Modul keine Objektgruppen gefunden werden.

</dd> </dl>

## <a name="fatal-error-1087"></a>Schwerwiegender Fehler 1087

<dl> <dt>

<span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Schwerwiegender>: " <fileName><line \#>: Ungültige Status Klausel <clause> für ein Textkonventionen-Makro"**
</dt> <dd>

Typzuweisung, SNMPv2C-spezifischer modulsemantik Fehler. Die Status-Klausel eines **Textkonventionen-Makro Aufrufes** muss "Current", "deprecated" oder "deprecated" lauten.

</dd> </dl>

## <a name="fatal-error-1089"></a>Schwerwiegender Fehler 1089

<dl> <dt>

<span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, schwerwiegender>: " <fileName> : <line \#>: <identifier> das Symbol in der Augments-Klausel wird nicht in einen Row-Objekttyp aufgelöst."**
</dt> <dd>

**Objekttyp-** Makro Aufruf SNMPv2C-spezifischer modulsemantik Fehler. Wenn eine Erweiterungs Klausel vorhanden ist, muss der Bezeichner in der Augments-Klausel in einen Table-Objekttyp aufgelöst werden.

</dd> </dl>

## <a name="fatal-error-1090"></a>Schwerwiegender Fehler 1090

<dl> <dt>

<span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, schwerwiegender>: " <fileName> : <line \#> implizierte Klausel ist nur für das letzte Index Objekt nützlich."**
</dt> <dd>

**Objekttyp-** Makro Aufruf SNMPv2C-spezifischer modulsemantik Fehler. Die implizierte Klausel kann nur mit dem letzten Objekt in der Index Klausel verknüpft werden.

</dd> </dl>

 

 



