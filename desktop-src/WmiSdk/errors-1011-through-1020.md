---
description: Beschreibt die Fehler 1011 bis 1020 des WMI-SNMP-Anbieters.
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: Fehler 1011 bis 1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49642dd17180b32a683ec7937553dbe60c60584e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886975"
---
# <a name="errors-1011-through-1020"></a>Fehler 1011 bis 1020

Beschreibt die Fehler 1011 bis 1020 des WMI-SNMP-Anbieters.

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

<span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, Fatal>: " &lt; fileName &gt; :<line \#> the SYNTAX of member identifier of &lt; &gt; SEQUENCE, identifier , differs from the &lt; SYNTAX clause of the &gt; OBJECT-TYPE"**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Ein Element einer SEQUENCE muss mit dem Typ in der SYNTAX-Klausel der OBJECT-TYPE-Definition identisch sein. Die <Zeile \#> Parameter ist die Zeile der SYNTAX-Klausel der OBJECT-TYPE-Definition.

Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1012"></a>Schwerwiegender Fehler 1012

<dl> <dt>

<span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012, Fatal>: " &lt; fileName &gt; :<line \#> An INDEX or AUGMENTS clause is only for SEQUENCE OBJECT-TYPES"**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Eine INDEX-Klausel darf nur in einer OBJECT-TYPE-Definition vorhanden sein, deren SYNTAX in einen SEQUENCE-Typ aufgelöst wird.

Dieser Fehler kann beim Kompilieren einer SNMPv1- oder SNMPv2C-MIB auftreten.

</dd> </dl>

## <a name="fatal-error-1013"></a>Schwerwiegender Fehler 1013

<dl> <dt>

<span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013, Fatal>: " &lt; fileName<line>: identifier should resolve to a SEQUENCE type" (Dateiname &gt;<Zeile \#>: &lt; Bezeichner &gt; sollte in einen SEQUENCE-Typ aufgelöst werden)**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Ein im SEQUENCE OF-Konstrukt verwendeter Typ muss in einen SEQUENCE-Typ aufgelöst werden.

Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="warning-1014"></a>Warnung 1014

<dl> <dt>

<span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, Warning>: " &lt; fileName &gt; :<line>: Sub-identifier of value 0 not recommended in OIDs" (Dateiname :<Zeile \#>: Unterbezeichner des Werts 0 wird in OIDs nicht empfohlen)**
</dt> <dd>

Semantische Warnung des **OBJECT-TYPE-Makroaufrufmoduls.** Es wird empfohlen, dass kein Objekt in einer Internet Standard-MIB einen Unterbezeichner von 0 (null) in seinem OBJECT IDENTIFIER verwendet.

Diese Warnung kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1015"></a>Schwerwiegender Fehler 1015

<dl> <dt>

<span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015, Fatal>: " &lt; fileName &gt; :<line>: OBJECT-TYPEs identifier from module identifier and identifier from module identifier are assigned the same OID values" (Dateiname :<Zeile \#>: OBJECT-TYPEs &lt; Bezeichner &gt; aus &lt; Modulbezeichner &gt; und &lt; Bezeichner &gt; aus &lt; Modulbezeichner &gt; werden die gleichen OID-Werte zugewiesen.**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Zwei **OBJECT-TYPE-Aufrufen** (in denselben oder verschiedenen Modulen) darf nicht der gleiche Objektbezeichnerwert zugewiesen werden.

Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1016"></a>Schwerwiegender Fehler 1016

<dl> <dt>

<span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, Fatal>: " &lt; fileName &gt; :<line>: Value in the DEFVAL clause does not match the type in the SYNTAX clause" (Dateiname :<Zeile \#>: Der Wert in der DEFVAL-Klausel stimmt nicht mit dem Typ in der SYNTAX-Klausel überein.**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Ein Wert in einer DEFVAL-Klausel muss ein Wert des in der SYNTAX-Klausel erwähnten Typs sein.

Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1018"></a>Schwerwiegender Fehler 1018

<dl> <dt>

<span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018, Fatal>: " &lt; fileName &gt;<line \#>: symbol in ENTERPRISE clause of TRAP-TYPE does not resolve to an OID value" (Dateiname<Zeile>: &lt; Symbol in der &gt; ENTERPRISE-Klausel von TRAP-TYPE wird nicht in einen OID-Wert aufgelöst)**
</dt> <dd>

**TRAP-TYPE-Makroaufruf,** semantischer SNMPv1-spezifischer Modulfehler. Das symbol, das in der **ENTERPRISE-Klausel eines TRAP-TYPE-Makroaufrufs** verwendet wird, muss in einen Objektbezeichnerwert aufgelöst werden.

</dd> </dl>

## <a name="fatal-error-1020"></a>Schwerwiegender Fehler 1020

<dl> <dt>

<span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020, Fatal>: " &lt; fileName &gt;<line \#>: Value assigned to TRAP-TYPE &lt; identifier does not resolve to a positive &gt; integer"**
</dt> <dd>

**TRAP-TYPE-Makroaufruf,** semantischer SNMPv1-spezifischer Modulfehler. Ein Symbol, das zum Angeben des Trapwerts verwendet wird, wird nicht in eine positive ganze Zahl aufgelöst.

</dd> </dl>

 

 



