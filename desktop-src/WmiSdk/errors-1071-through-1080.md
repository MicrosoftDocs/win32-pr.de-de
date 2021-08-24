---
description: Beschreibt die Fehler 1071 bis 1080 des WMI-SNMP-Anbieters.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Fehler 1071 bis 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c92cfd1c79b5bedd070229adcbc4c663d209903428073fc976cd575022e9ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679620"
---
# <a name="errors-1071-through-1080"></a>Fehler 1071 bis 1080

Beschreibt die Fehler 1071 bis 1080 des WMI-SNMP-Anbieters.

[Warnung 1071](#warning-1071)

[Warnung 1072](#warning-1072)

[Schwerwiegender Fehler 1074](#fatal-error-1074)

[Schwerwiegender Fehler 1075](#fatal-error-1075)

[Schwerwiegender Fehler 1077](#fatal-error-1077)

[Schwerwiegender Fehler 1079](#fatal-error-1079)

[Warnung 1080](#warning-1080)

## <a name="warning-1071"></a>Warnung 1071

<dl> <dt>

<span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, Warning>: " <fileName><line \#>: Symbol <identifier> not present in imported module <identifier> "**
</dt> <dd>

Modulsemantikwarnung zu Querverweisen, spezifisch für weder SNMPv1 noch SNMPv2C. Ein aus einem Modul importiertes Symbol wird in diesem Modul nicht aufgelöst. Obwohl dieses Modul in der Eingabe angegeben ist, wird diese Warnung angezeigt.

</dd> </dl>

## <a name="warning-1072"></a>Warnung 1072

<dl> <dt>

<span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, Warning>: " <fileName> :<line \#> OBJECT-TYPE <name> is a descendant of OBJECT-TYPE of module <name> <name> "**
</dt> <dd>

Semantische Warnung des **OBJECT-TYPE-Makroaufrufmoduls.** Ein Skalarobjekt darf keine Nachfolgerobjekte aufweisen.

Diese Warnung kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1074"></a>Schwerwiegender Fehler 1074

<dl> <dt>

<span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074, Fatal>: " <fileName> :<line> \# SEQUENCE (Conceptual row) OBJECT-TYPE does not have a SEQUENCE OF (Conceptual table) OBJECT-TYPE as its parent" (:<line> SEQUENCE (Conceptual row) OBJECT-TYPE <name> does not have a SEQUENCE OF (Conceptual table) OBJECT-TYPE as its parent"**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Jedes Zeilenobjekt muss über ein Tabellenobjekt als übergeordnetes Objekt verfügen.

Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1075"></a>Schwerwiegender Fehler 1075

<dl> <dt>

<span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, Fatal>:" <fileName> :<line \#>: OBJECT-TYPE <name> cannot be a child of table OBJECT-TYPE of module <name> <name> unless it is in the SEQUENCE of the latter"**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Jedes SEQUENCE-Objekt muss genau die gleichen Objekte aufweisen, die in der SEQUENCE-Typdefinition wie seine untergeordneten Elemente erwähnt werden. Ebenso muss jedes SEQUENCE OF-Objekt genau ein untergeordnetes Objekt aufweisen.

Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1077"></a>Schwerwiegender Fehler 1077

<dl> <dt>

<span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, Fatal>: " <fileName> :<line \#>: The syntax of table OBJECT-TYPE <name> is not the SEQUENCE OF the syntax of the child OBJECT-TYPE <name> of module <name> "**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Die Syntaxklausel eines Tabellenobjekts muss die "SEQUENCE OF" der Syntax des Zeilenobjekts sein.

Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1079"></a>Schwerwiegender Fehler 1079

<dl> <dt>

<span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079, Fatal>:"fileName>:<line \#>: OBJECT-TYPE <name> is an extra child of OBJECT-TYPE of module <name> <name> "**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Jedes SEQUENCE OF-Objekt muss genau ein untergeordnetes Objekt aufweisen.

Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="warning-1080"></a>Warnung 1080

<dl> <dt>

<span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, Warning>: <fileName> "<line \#>: MIB Module <moduleName> , from which symbol is not present in <symbolName> input"**
</dt> <dd>

Modulsemantikwarnung zu Querverweisen, spezifisch für weder SNMPv1 noch SNMPv2C. Wenn eines der Module im Imports-Abschnitt des Hauptmoduls oder eines untergeordneten Moduls nicht vorhanden ist, aber auf Symbole aus diesem Modul nicht verwiesen wird, wird diese Warnung angezeigt.

</dd> </dl>

 

 



