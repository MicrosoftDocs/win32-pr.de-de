---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1041 bis 1050.
ms.assetid: e7e70fb3-12c6-40b1-91a4-c550e8210c09
ms.tgt_platform: multiple
title: Fehler 1041 bis 1050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ef466d1b1226b14d895fef81be24baee45354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042056"
---
# <a name="errors-1041-through-1050"></a>Fehler 1041 bis 1050

Beschreibt die WMI-SNMP-Anbieter Fehler 1041 bis 1050.

[Schwerwiegender Fehler 1041](#fatal-error-1041)

[Schwerwiegender Fehler 1042](#fatal-error-1042)

[Warnung 1043](#warning-1043)

[Schwerwiegender Fehler 1044](#fatal-error-1044)

[Warnung 1045](#warning-1045)

[Warnung 1046](#warning-1046)

[Warnung 1047](#warning-1047)

[Warnung 1048](#warning-1048)

[Schwerwiegender Fehler 1049](#fatal-error-1049)

## <a name="fatal-error-1041"></a>Schwerwiegender Fehler 1041

<dl> <dt>

<span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, schwerwiegender>: " <fileName><line \#>: Bezeichner <identifier> in Bereichs Spezifikation wird nicht in einen integralen Wert aufgelöst"**
</dt> <dd>

Modul Semantik Fehler in Bereichs-oder Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C. Das in einer Größenangabe verwendete Symbol muss in eine Oktett-Zeichenfolge oder eine nicht transparente Zeichenfolge aufgelöst werden Jeder Wert, der zum Angeben eines Bereichs verwendet wird, muss eine ganze Zahl sein.

</dd> </dl>

## <a name="fatal-error-1042"></a>Schwerwiegender Fehler 1042

<dl> <dt>

<span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, schwerwiegender>: " <fileName><line \#>: obere Grenze der Bereichs Spezifikation ist kleiner als die untere Grenze"**
</dt> <dd>

Modul Semantik Fehler in Bereichs-oder Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C. Das in einer Größenangabe verwendete Symbol muss in eine Oktett-Zeichenfolge oder eine nicht transparente Zeichenfolge aufgelöst werden Die untere Grenze einer Bereichs-oder Größenangabe darf nicht größer als die obere Grenze sein.

</dd> </dl>

## <a name="warning-1043"></a>Warnung 1043

<dl> <dt>

<span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, Warning>: " <fileName> : <line \#>: Objekttyp mit der Syntax" Sequence ", sollte über eine Access-Klausel verfügen, auf die nicht zugegriffen werden kann.**
</dt> <dd>

Semantik Warnung für **Objekttyp-** Makro Aufruf Modul. Eine Tabelle oder konzeptionelle Zeile (Sequenz von bzw. Sequenz Objekttypen) muss "nicht zugänglich" sein.

Diese Warnung kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1044"></a>Schwerwiegender Fehler 1044

<dl> <dt>

<span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, schwerwiegender>: " <fileName><line \#>: Neudefinition des Symbols <identifier> "**
</dt> <dd>

Modul Semantik Fehler, spezifisch für weder SNMPv1 noch SNMPv2C. Neudefinition von Objekt Deskriptoren, Makro aufrufen und ASN. 1-Typen führt zu einem Fehler.

</dd> </dl>

## <a name="warning-1045"></a>Warnung 1045

<dl> <dt>

<span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, Warning>: " <fileName><linereferenzierung zum Standard Symbol <symbolName> wird für die Definition als in angenommen <moduleName> . Verwenden Sie die "Module. Symbol"-Notationen, wenn Sie auf die Definition im aktuellen Modul verweisen möchten.**
</dt> <dd>

Modul Semantik Warnung, spezifisch für weder SNMPv1 noch SNMPv2C. Ein Symbol, das dem Compiler bekannt ist, wurde neu definiert, und es wird darauf verwiesen. Der Compiler nimmt die Standard Definition des Symbols an. Daher müssen Sie die Notation "Module. Symbol" verwenden, um eine Neudefinition des Standard Symbols zu verwenden.

</dd> </dl>

## <a name="warning-1046"></a>Warnung 1046

<dl> <dt>

<span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, Warnung>: " <fileName><Zeilen \#>: nicht <symbol> definiert. Annahme der Standard Definition "**
</dt> <dd>

Modul Semantik Warnung, spezifisch für weder SNMPv1 noch SNMPv2C. Ein Symbol, das dem Compiler bekannt ist, darf nicht neu definiert oder verwendet werden, ohne importiert zu werden.

</dd> </dl>

## <a name="warning-1047"></a>Warnung 1047

<dl> <dt>

<span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, Warning>: " <fileName><line \#>: Typdefinition <symbol> definiert, aber nicht referenziert"**
</dt> <dd>

Modul Semantik Warnung, spezifisch für weder SNMPv1 noch SNMPv2C. Auf alle Wert Zuweisungen und Typdefinitionen muss irgendwo verwiesen werden.

</dd> </dl>

## <a name="warning-1048"></a>Warnung 1048

<dl> <dt>

<span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, Warning>: " <fileName><line \#>: Definition von Werten <symbol> definiert, aber nicht referenziert"**
</dt> <dd>

Modul Semantik Warnung, spezifisch für weder SNMPv1 noch SNMPv2C. Auf alle Wert Zuweisungen und Typdefinitionen muss irgendwo verwiesen werden.

</dd> </dl>

## <a name="fatal-error-1049"></a>Schwerwiegender Fehler 1049

<dl> <dt>

<span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, schwerwiegender>: " <fileName> : <line \#>: defval-Klausel für Objekttyp mit Syntax Network Address" nicht zulässig.**
</dt> <dd>

**Objekttyp-** Makro Aufruf SNMPv1-spezifischer modulsemantik Fehler. Die defval-Klausel ist für einen Objekttyp, dessen Syntax Klausel in Network Address aufgelöst wird, nicht zulässig.

</dd> </dl>

 

 



