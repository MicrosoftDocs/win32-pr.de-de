---
description: Beschreibt die Fehler 1031 bis 1040 des WMI-SNMP-Anbieters.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Fehler 1031 bis 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2378ec70aa39a8560a11df8fa9027f97960d4720f89e1f6cac271496e432362
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568610"
---
# <a name="errors-1031-through-1040"></a>Fehler 1031 bis 1040

Beschreibt die Fehler 1031 bis 1040 des WMI-SNMP-Anbieters.

[Warnung 1031](#warning-1031)

[Schwerwiegender Fehler 1032](#fatal-error-1032)

[Schwerwiegender Fehler 1033](#fatal-error-1033)

[Warnung 1034](#warning-1034)

[Warnung 1036](#warning-1036)

[Schwerwiegender Fehler 1037](#fatal-error-1037)

[Schwerwiegender Fehler 1038](#fatal-error-1038)

[Schwerwiegender Fehler 1039](#fatal-error-1039)

[Schwerwiegender Fehler 1040](#fatal-error-1040)

## <a name="warning-1031"></a>Warnung 1031

<dl> <dt>

<span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Warning>: " <fileName> :<line \#>: Standardsymbol <identifier> should be imported from module <identifier> . Angenommen, die Standarddefinition."**
</dt> <dd>

Semantische Warnung des IMPORTS-Abschnittsmoduls, die weder für SNMPv1 noch für SNMPv2C spezifisch ist. Wenn sich ein SNMP-Bezeichner, der dem Compiler bekannt ist, im Imports-Abschnitt befindet, muss das Modul, aus dem er importiert wird, eines der Standardmodule sein.

Bei bestimmten häufig verwendeten IMPORTS handelt es sich um "angenommenes Wissen" des Compilers. Es ist nicht erforderlich, dass der Compiler Zugriff auf andere Informationsmodule benötigt, um diese aufzulösen.

Die integrierten Importe von SNMPv1 und SNMPv2C werden in den folgenden Tabellen beschrieben.

</dd> </dl>

**Integrierte SNMPv1-IMPORTE**



| Import-Klasse | Modul      | Instanzen                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| ASN.1-Wert  | RFC1155-SMI | Internet, Verzeichnis, Verwaltung, experimentell, privat, Unternehmen |
|              | RFC1213-MIB | MIB-II und IP, Schnittstellen, Übertragung                             |
| ASN.1-Typ   | RFC1155-SMI | NetworkAddress, IpAddress, Counter, Gauge, TimeTicks, Opaque        |
|              | RFC1213-MIB | DisplayString, PhysAddress                                          |
| ASN.1-Makro  | RFC-1212    | OBJECT-TYPE                                                         |
|              | RFC-1215    | TRAP-TYP                                                           |



 

**Integrierte SNMPv2C-IMPORTE**



| Import-Klasse       | Modul      | Instanzen                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASN.1-Wert        | SNMPv2-SMI  | org, dod, Internet, directory, mgmt, mib-2, transmission, experimental, private, enterprises, security, snmpv2, snmpDomains, snmpProxys, snmpModules                                                           |
|                    | SNMPv2-TM   | rfc1157Proxy                                                                                                                                                                                                   |
| Objektidentität    | SNMPv2-SMI  | zeroDotZero                                                                                                                                                                                                    |
|                    | SNMPv2-TM   | snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain                                                                                                                     |
| ASN.1-Typ         | SNMPv2-SMI  | Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32                                                                                                                             |
| ASN.1-Makro        | SNMPv2-SMI  | MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE                                                                                                                                               |
|                    | SNMPv2-CONF | OBJECT-GROUP, NOTIFICATION-GROUP, MODULE-COMPLIANCE, AGENT-CAPABILITIES                                                                                                                                        |
|                    | SNMPv2-TC   | TEXTUAL-CONVENTION                                                                                                                                                                                             |
| Textkonvention | SNMPv2-TC   | DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain,Laufdress |
|                    | SNMPv2-TM   | SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a>Schwerwiegender Fehler 1032

<dl> <dt>

<span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Fatal>: <fileName> "<line \#>: Duplicate value in <value> enumeration"**
</dt> <dd>

Modulsemantikfehler in einer Enumeration, der weder für SNMPv1 noch für SNMPv2C spezifisch ist. Es dürfen keine doppelten Werte vorhanden sein. Die <Zeile \#>-Parameters ist die Position der Wiederholung des Namens/Werts.

</dd> </dl>

## <a name="fatal-error-1033"></a>Schwerwiegender Fehler 1033

<dl> <dt>

<span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Fatal>: <fileName> "<line \#>: Duplicate name <identifier> in enumeration"**
</dt> <dd>

Modulsemantikfehler in einer Enumeration, der weder für SNMPv1 noch für SNMPv2C spezifisch ist. Es dürfen keine doppelten Namen vorhanden sein. Die <Zeile \#>-Parameters ist die Position der Wiederholung des Namens/Werts.

</dd> </dl>

## <a name="warning-1034"></a>Warnung 1034

<dl> <dt>

<span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning>: <fileName> "<line \#>: A value of 0 disallowed in an enumeration"**
</dt> <dd>

Modulsemantikwarnung in einer Enumeration, die weder für SNMPv1 noch für SNMPv2C spezifisch ist. Es wird empfohlen, den benannten Wert 0 (null) nicht in einer Enumeration zu verwenden.

</dd> </dl>

## <a name="warning-1036"></a>Warnung 1036

<dl> <dt>

<span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036: Warning> <fileName> "<line>: Value in enumeration does not resolve to a positive integer" (<Zeile \#>: Der Wert in der Enumeration wird nicht in eine positive ganze Zahl aufgelöst)**
</dt> <dd>

Modulsemantikwarnung in einer Enumeration, die weder für SNMPv1 noch für SNMPv2C spezifisch ist. Ein negativer Wert ist in einer Enumeration nicht zulässig.

</dd> </dl>

## <a name="fatal-error-1037"></a>Schwerwiegender Fehler 1037

<dl> <dt>

<span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Fatal>: <fileName> "<line>: Identifier does not resolve to OCTET STRING or Opaque types" (<Zeile \#>: Bezeichner <identifier> wird nicht in OCTET STRING- oder Opaque-Typen aufgelöst)**
</dt> <dd>

Modulsemantikfehler in der SIZE-Spezifikation, der weder für SNMPv1 noch für SNMPv2C spezifisch ist. Das in einer SIZE-Spezifikation verwendete Symbol muss in OCTET STRING oder Opaque aufgelöst werden.

</dd> </dl>

## <a name="fatal-error-1038"></a>Schwerwiegender Fehler 1038

<dl> <dt>

<span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Fatal>: <fileName> "<line>: Identifier does not resolve an INTEGER or Gauge type" (<Zeile \#>: Bezeichner <identifier> löst keinen INTEGER- oder Messgerättyp auf.**
</dt> <dd>

Modulsemantikfehler in Bereichsspezifikation. Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

In SNMPv1 muss das in einer Bereichsspezifikation verwendete Symbol in INTEGER oder Gauge aufgelöst werden.

In SNMPv2C muss das in einer Bereichsspezifikation verwendete Symbol in INTEGER, Gauge32, Integer32 oder Unsigned32 aufgelöst werden.

</dd> </dl>

## <a name="fatal-error-1039"></a>Schwerwiegender Fehler 1039

<dl> <dt>

<span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Fatal>:<<fileName> line \#>: Negative value used in SIZE specification"**
</dt> <dd>

Modulsemantikfehler in der SIZE-Spezifikation, der weder für SNMPv1 noch für SNMPv2C spezifisch ist. Jeder Wert, der zum Angeben der GRÖßE verwendet wird, muss nicht negativ sein.

</dd> </dl>

## <a name="fatal-error-1040"></a>Schwerwiegender Fehler 1040

<dl> <dt>

<span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Fatal>: <fileName> "<line \#>: Identifier <identifier> in SIZE specification does not resolve to a non-negative integral value"**
</dt> <dd>

Modulsemantikfehler in Bereichs- oder Größenangabe, der weder für SNMPv1 noch für SNMPv2C spezifisch ist. Jedes Symbol, das zum Angeben eines Werts in einer SIZE-Spezifikation verwendet wird, wird in einen nicht negativen Wert aufgelöst.

</dd> </dl>

 

 



