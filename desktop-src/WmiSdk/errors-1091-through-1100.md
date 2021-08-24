---
description: Beschreibt die WMI-SNMP-Anbieterfehler 1091 bis 1100.
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: Fehler 1091 bis 1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cedd1fc12fa5f547e041201f5411a262ddb3a3958ef58e8bed3bfcf8270d7058
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244320"
---
# <a name="errors-1091-through-1100"></a>Fehler 1091 bis 1100

Beschreibt die WMI-SNMP-Anbieterfehler 1091 bis 1100.

[Warnung 1091](#warning-1091)

[Schwerwiegender Fehler 1092](#fatal-error-1092)

[Schwerwiegender Fehler 1093](#fatal-error-1093)

[Schwerwiegender Fehler 1094](#fatal-error-1094)

[Schwerwiegender Fehler 1095](#fatal-error-1095)

[Schwerwiegender Fehler 1097](#fatal-error-1097)

[Schwerwiegender Fehler 1098](#fatal-error-1098)

[Schwerwiegender Fehler 1099](#fatal-error-1099)

## <a name="warning-1091"></a>Warnung 1091

<dl> <dt>

<span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, Warning>: " <fileName> :<line \#> IMPLIED clause is not allowed for fixed size objects"**
</dt> <dd>

**OBJECT-TYPE-Makroaufruf:** Semantikwarnung für SNMPv2C-spezifisches Modul. Das IMPLIED-Schlüsselwort kann nur für ein Objekt mit einer Syntax variabler Länge, z. B. OBJECT IDENTIFIER oder OCTET STRING variabler Länge, in der INDEX-Klausel vorhanden sein.

</dd> </dl>

## <a name="fatal-error-1092"></a>Schwerwiegender Fehler 1092

<dl> <dt>

<span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, Fatal>: " <fileName> :<line \#> IMPLIED clause not allowed for potentially zero-length objects"**
</dt> <dd>

**OBJECT-TYPE-Makroaufruf** SNMPv2C-spezifischer Modulsemantikfehler. Die IMPLIED-Klausel kann nicht für ein Objekt variabler Länge verwendet werden, wenn dieses Objekt eine Länge von 0 (null) haben kann.

</dd> </dl>

## <a name="fatal-error-1093"></a>Schwerwiegender Fehler 1093

<dl> <dt>

<span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Schwerwiegende>: "<Zeile>: Nur der Typ "INTEGER" kann gemäß der <fileName> \# V1-SMI aufzählt werden.**
</dt> <dd>

Typzuweisung, SNMPv1-spezifischer Modulsemantikfehler. Eine SNMPv1 MIB-Enumeration kann nur den Typ INTEGER verwenden.

</dd> </dl>

## <a name="fatal-error-1094"></a>Schwerwiegender Fehler 1094

<dl> <dt>

<span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094. Schwerwiegende>: "<Zeile>: Der in der Enumeration verwendete Typ wird nicht in einen <fileName> \# der zulässigen Typen auflösen.**
</dt> <dd>

Typzuweisung, SNMPv2C-spezifischer Modulsemantikfehler. Der in einer Enumeration verwendete Typ muss INTEGER oder ein äquivalenter Typ oder eine andere Enumeration sein.

</dd> </dl>

## <a name="fatal-error-1095"></a>Schwerwiegender Fehler 1095

<dl> <dt>

<span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095. Schwerwiegende>: " <fileName><Zeile \#>: Enumerationsmember ist kein Member der übergeordneten Enumeration"**
</dt> <dd>

Typzuweisung, SNMPv2C-spezifischer Modulsemantikfehler. Wenn eine andere Enumeration verwendet wird, muss ihr Satz von Elementen eine Teilmenge der Elemente der übergeordneten Enumeration sein.

</dd> </dl>

## <a name="fatal-error-1097"></a>Schwerwiegender Fehler 1097

<dl> <dt>

<span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, Fatal>: " <fileName><line \#>: identifier does not resolve to <name> an integer value"**
</dt> <dd>

Typzuweisung, SNMPv2C-spezifischer Modulsemantikfehler. Die Werte im BITS-Typ müssen ganzzahlige Werte sein.

</dd> </dl>

## <a name="fatal-error-1098"></a>Schwerwiegender Fehler 1098

<dl> <dt>

<span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, Fatal>: " <fileName><line \#>: Duplicate value in <value> BITS construct"**
</dt> <dd>

Typzuweisung, SNMPv2C-spezifischer Modulsemantikfehler. In einem BITS-Konstrukt dürfen keine doppelten Namen und Werte vorhanden sein. Die <Zeile> Parameter ist die Position der Wiederholung \# des Namens/Werts.

</dd> </dl>

## <a name="fatal-error-1099"></a>Schwerwiegender Fehler 1099

<dl> <dt>

<span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, Fatal>: " <fileName><line \#>: Duplicate name <identifier> in BITS construct"**
</dt> <dd>

Typzuweisung, SNMPv2C-spezifischer Modulsemantikfehler. In einem BITS-Konstrukt dürfen keine doppelten Namen und Werte vorhanden sein. Die <Zeile> Parameter ist die Position der Wiederholung \# des Namens/Werts.

</dd> </dl>

 

 



