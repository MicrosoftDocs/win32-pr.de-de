---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1011 bis 1020.
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: Fehler 1011 bis 1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a73f90ce0fc161604d87672fb5b33f9708aa945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050265"
---
# <a name="errors-1011-through-1020"></a>Fehler 1011 bis 1020

Beschreibt die WMI-SNMP-Anbieter Fehler 1011 bis 1020.

[Schwerwiegender Fehler 1011](#fatal-error-1011)

[Schwerwiegender Fehler 1012](#fatal-error-1012)

[Schwerwiegender Fehler 1013](#fatal-error-1013)

[Warnung 1014](#warning-1014)

[Schwerwiegender Fehler 1015](#fatal-error-1015)

[Schwerwiegender Fehler 1016](#fatal-error-1016)

[Schwerwiegender Fehler 1018](#fatal-error-1018)

[Schwerwiegender Fehler 1020](#fatal-error-1020)

## <a name="fatal-error-1011"></a>Schwerwiegender Fehler 1011

<dl> <dt>

<span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, schwerwiegender>: " <fileName> : <Zeile \#> die Syntax des Members <identifier> der Sequenz unter <identifier> scheidet sich von der Syntax Klausel des Objekttyps"**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Ein Element einer Sequenz muss mit dem Typ in der Syntax Klausel der Objekttyp Definition identisch sein. Der <Zeile \#> Parameter ist die Zeile der Syntax Klausel der Objekttyp Definition.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1012"></a>Schwerwiegender Fehler 1012

<dl> <dt>

<span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012, schwerwiegender>: " <fileName> : <Zeile \#> eine Index-oder Erweiterungs Klausel ist nur für Sequenz Objekttypen erforderlich."**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Eine Index Klausel darf nur in einer Objekttyp Definition vorhanden sein, deren Syntax zu einem Sequenztyp aufgelöst wird.

Dieser Fehler kann auftreten, wenn ein SNMPv1-oder SNMPv2C-MIB kompiliert wird.

</dd> </dl>

## <a name="fatal-error-1013"></a>Schwerwiegender Fehler 1013

<dl> <dt>

<span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013, schwerwiegender>: " <fileName><line \#>: <identifier> sollte in einen Sequenztyp aufgelöst werden"**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Ein im "Sequence of"-Konstrukt verwendeter Typ muss in einen Sequenztyp aufgelöst werden.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="warning-1014"></a>Warnung 1014

<dl> <dt>

<span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, Warning>: " <fileName> : <line \#>: untergeordnete Kennung des Werts 0 wird in OIDs nicht empfohlen"**
</dt> <dd>

Semantik Warnung für **Objekttyp-** Makro Aufruf Modul. Es wird empfohlen, dass kein-Objekt in einem Internet Standard-MIB einen untergeordneten Bezeichner von NULL in seinem Objekt Bezeichner verwendet.

Diese Warnung kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1015"></a>Schwerwiegender Fehler 1015

<dl> <dt>

<span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015, schwerwiegender>: " <fileName> : <line \#>: OBJECT-TYPEs <identifier> from Module <identifier> and <identifier> from Module <identifier> werden die gleichen OID-Werte zugewiesen"**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Zwei **Objekttyp** aufrufen (im selben oder in unterschiedlichen Modulen) darf nicht der gleiche Objektbezeichnerwert zugewiesen werden.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1016"></a>Schwerwiegender Fehler 1016

<dl> <dt>

<span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, schwerwiegender>: " <fileName> : <line \#>: der Wert in der defval-Klausel stimmt nicht mit dem Typ in der Syntax Klausel überein."**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Ein Wert in einer defval-Klausel muss ein Wert des Typs sein, der in der Syntax Klausel angegeben ist.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1018"></a>Schwerwiegender Fehler 1018

<dl> <dt>

<span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018, schwerwiegender>: " <fileName><line \#>: <symbol> in der Enterprise-Klausel von Trap-Type wird nicht in einen OID-Wert aufgelöst"**
</dt> <dd>

**Trap-Type-** Makro Aufruf, SNMPv1-spezifischer Modul Semantik Fehler. Das in der Enterprise-Klausel eines **Trap-Type-** Makro aufzurufende Symbol muss zu einem Objektbezeichnerwert aufgelöst werden.

</dd> </dl>

## <a name="fatal-error-1020"></a>Schwerwiegender Fehler 1020

<dl> <dt>

<span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020, schwerwiegender>: " <fileName><line \#>: der Trap-Type zugewiesene Wert <identifier> wird nicht in eine positive ganze Zahl aufgelöst"**
</dt> <dd>

**Trap-Type-** Makro Aufruf, SNMPv1-spezifischer Modul Semantik Fehler. Ein Symbol, das zum Angeben des Trap-Werts verwendet wird, wird nicht in eine positive ganze Zahl aufgelöst.

</dd> </dl>

 

 



