---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1071 bis 1080.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Fehler 1071 bis 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277aa7dd69d674ebc16bc0a2b4d104c349e593a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359594"
---
# <a name="errors-1071-through-1080"></a>Fehler 1071 bis 1080

Beschreibt die WMI-SNMP-Anbieter Fehler 1071 bis 1080.

[Warnung 1071](#warning-1071)

[Warnung 1072](#warning-1072)

[Schwerwiegender Fehler 1074](#fatal-error-1074)

[Schwerwiegender Fehler 1075](#fatal-error-1075)

[Schwerwiegender Fehler 1077](#fatal-error-1077)

[Schwerwiegender Fehler 1079](#fatal-error-1079)

[Warnung 1080](#warning-1080)

## <a name="warning-1071"></a>Warnung 1071

<dl> <dt>

<span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, Warning>: " <fileName><line \#>: Symbol <identifier> nicht im importierten Modul vorhanden <identifier> "**
</dt> <dd>

Modul Semantik Warnung für Querverweise, spezifisch für weder SNMPv1 noch SNMPv2C. Ein Symbol, das aus einem Modul importiert wird, wird in nichts in diesem Modul aufgelöst. Obwohl dieses Modul in der Eingabe angegeben ist, wird diese Warnung angezeigt.

</dd> </dl>

## <a name="warning-1072"></a>Warnung 1072

<dl> <dt>

<span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, Warnung>: " <fileName> : <Zeile \#> Objekttyp <name> ist ein Nachfolger vom Objekttyp <name> des Moduls <name> "**
</dt> <dd>

Semantik Warnung für **Objekttyp-** Makro Aufruf Modul. Ein skalare Objekt darf keine untergeordneten Objekte aufweisen.

Diese Warnung kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1074"></a>Schwerwiegender Fehler 1074

<dl> <dt>

<span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074, schwerwiegender>: " <fileName> : <\# der Zeile> Sequenz (konzeptionelle Zeile)"-Objekttyp <name> weist keine Sequenz des Objekttyps (konzeptionelle Tabelle) als übergeordnetes Element auf.**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Jedes Row-Objekt muss über ein Table-Objekt als übergeordnetes Element verfügen.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1075"></a>Schwerwiegender Fehler 1075

<dl> <dt>

<span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, schwerwiegender>: " <fileName> : <line \#>: der Objekttyp darf kein untergeordnetes Element <name> des Table-Objekt Typs <name> " Module "sein, es <name> sei denn, er befindet sich in der Sequenz der letzteren"**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Jedes Sequenz Objekt muss genau die gleichen Objekte aufweisen, die in der Sequenztyp Definition als untergeordnete Elemente angegeben sind. Ebenso muss jede Objekt Sequenz genau ein untergeordnetes Element aufweisen.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1077"></a>Schwerwiegender Fehler 1077

<dl> <dt>

<span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, schwerwiegender>: " <fileName> : <line \#>: die Syntax des Table Object-Type <name> ist nicht die Sequenz der Syntax des untergeordneten Objekt Typs <name> des Moduls <name> "**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Die Syntax Klausel eines Table-Objekts muss die "Sequenz von" der Syntax des Row-Objekts sein.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1079"></a>Schwerwiegender Fehler 1079

<dl> <dt>

<span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079, schwerwiegender>: "Dateiname>: <Zeile \#>: Objekttyp <name> ist ein zusätzliches untergeordnetes Element des Objekttyp <name> Moduls <name> "**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Jede Objekt Sequenz muss genau ein untergeordnetes Element aufweisen.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="warning-1080"></a>Warnung 1080

<dl> <dt>

<span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, Warning>: " <fileName><line \#>: MIB-Modul <moduleName> , von dem das Symbol <symbolName> importiert wird, ist nicht in der Eingabe vorhanden"**
</dt> <dd>

Modul Semantik Warnung für Querverweise, spezifisch für weder SNMPv1 noch SNMPv2C. Wenn eines der Module im Imports-Abschnitt des Haupt Moduls oder eines Tochter Systems nicht vorhanden ist, aber keine Symbole aus diesem Modul referenziert werden, wird diese Warnung angezeigt.

</dd> </dl>

 

 



