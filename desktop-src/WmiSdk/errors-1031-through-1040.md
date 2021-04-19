---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1031 bis 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Fehler 1031 bis 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34079c2cbdb8e50aef04e8c364ba99abee760fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350003"
---
# <a name="errors-1031-through-1040"></a>Fehler 1031 bis 1040

Beschreibt die WMI-SNMP-Anbieter Fehler 1031 bis 1040.

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

<span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Warning>: " <fileName> : <line \#>: das Standard Symbol <identifier> sollte aus dem Modul importiert werden <identifier> . Angenommen, die Standard Definition. "**
</dt> <dd>

Gibt eine Semantik Warnung für das Abschnitts Modul aus, die spezifisch für weder SNMPv1 noch SNMPv2C. Wenn sich ein SNMP-Bezeichner, der dem Compiler bekannt ist, im Imports-Abschnitt befindet, muss das Modul, aus dem es importiert wird, eines der Standardmodule sein.

Bestimmte häufig verwendete Importe werden im Rahmen des Compilers "angenommen". Es ist nicht erforderlich, dass der Compiler Zugriff auf andere Informationsmodule benötigt, um diese zu beheben.

Die integrierten SNMPv1-und SNMPv2C-Importe werden in den folgenden Tabellen beschrieben.

</dd> </dl>

**Integrierte SNMPv1-Importe**



| Import Klasse | Modul      | Instanzen                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| ASN. 1-Wert  | RFC1155-SMI | Internet, Verzeichnis, Verwaltung, experimentell, privat, Unternehmen |
|              | RFC1213-MIB | MIB-II und IP, Schnittstellen, Übertragung                             |
| ASN. 1-Typ   | RFC1155-SMI | Network Address, IPAddress, Counter, Messgerät, TimeTicks, undurchsichtig        |
|              | RFC1213-MIB | Display String, physaddress                                          |
| ASN. 1-Makro  | RFC-1212    | Objekttyp                                                         |
|              | RFC-1215    | Trap-Typ                                                           |



 

**Integrierte SNMPv2C-Importe**



| Import Klasse       | Modul      | Instanzen                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASN. 1-Wert        | SNMPv2-SMI  | org, DoD, Internet, Verzeichnis, Mgmt, MIB-2, Übertragung, experimentell, privat, Unternehmen, Sicherheit, SNMPv2, snmpdomains, snmpproxys, snmpModules                                                           |
|                    | SNMPv2-TM   | rfc1157Proxy                                                                                                                                                                                                   |
| Objektidentität    | SNMPv2-SMI  | zerodotzero                                                                                                                                                                                                    |
|                    | SNMPv2-TM   | snmpudpdomain, snmpclnsdomain, smnpmsdomain, snmpddpdomain, snmpipxdomain, rfc1157Domain                                                                                                                     |
| ASN. 1-Typ         | SNMPv2-SMI  | Integer32, IPAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32                                                                                                                             |
| ASN. 1-Makro        | SNMPv2-SMI  | Modul Identität, Objekt Identität, Objekttyp, Benachrichtigungstyp                                                                                                                                               |
|                    | SNMPv2-conf | Objektgruppe, Benachrichtigungs Gruppe, Modul Konformität, Agentfunktionen                                                                                                                                        |
|                    | SNMPv2-TC   | Text Konvention                                                                                                                                                                                             |
| Text Konvention | SNMPv2-TC   | Display String, physaddress, MACAddress, Wahrheitswert, testandincr, autonomoustype, instancepointer, variablepointer, rowpointer, rowstatus, timestamp, TimeInterval, DateAndTime, StorageType, tdomain, taddress |
|                    | SNMPv2-TM   | Snmpudpaddress, snmposiaddress, snmpnbpaddress, snmpipxaddress                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a>Schwerwiegender Fehler 1032

<dl> <dt>

<span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, schwerwiegender>: " <fileName><line \#>: doppelter Wert <value> in der Enumeration"**
</dt> <dd>

Modul Semantik Fehler in einer Enumeration, spezifisch für weder SNMPv1 noch SNMPv2C. Es dürfen keine doppelten Werte vorhanden sein. Der <Zeile \#> Parameter ist die Position der Wiederholung des Namens/Werts.

</dd> </dl>

## <a name="fatal-error-1033"></a>Schwerwiegender Fehler 1033

<dl> <dt>

<span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, schwerwiegender>: " <fileName><line \#>: Doppelter Name <identifier> in Enumeration"**
</dt> <dd>

Modul Semantik Fehler in einer Enumeration, spezifisch für weder SNMPv1 noch SNMPv2C. Es dürfen keine doppelten Namen vorhanden sein. Der <Zeile \#> Parameter ist die Position der Wiederholung des Namens/Werts.

</dd> </dl>

## <a name="warning-1034"></a>Warnung 1034

<dl> <dt>

<span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning>: " <fileName><line \#>: der Wert 0 ist in einer Enumeration unzulässig."**
</dt> <dd>

Modul Semantik Warnung in einer Enumeration, spezifisch für weder SNMPv1 noch SNMPv2C. Es wird empfohlen, dass ein benannter Wert von NULL nicht in einer Enumeration verwendet wird.

</dd> </dl>

## <a name="warning-1036"></a>Warnung 1036

<dl> <dt>

<span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036 wird die Warnung> " <fileName><Zeilen \#>: Wert in der Enumeration nicht in eine positive ganze Zahl aufgelöst"**
</dt> <dd>

Modul Semantik Warnung in einer Enumeration, spezifisch für weder SNMPv1 noch SNMPv2C. Ein negativer Wert ist in einer Enumeration nicht zulässig.

</dd> </dl>

## <a name="fatal-error-1037"></a>Schwerwiegender Fehler 1037

<dl> <dt>

<span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, schwerwiegender>: " <fileName><line \#>: Bezeichner <identifier> wird nicht in Oktett-Zeichen folgen oder nicht transparente Typen aufgelöst"**
</dt> <dd>

Modul Semantik Fehler in der Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C. Das in einer Größenangabe verwendete Symbol muss in eine Oktett-Zeichenfolge oder eine nicht transparente Zeichenfolge aufgelöst werden

</dd> </dl>

## <a name="fatal-error-1038"></a>Schwerwiegender Fehler 1038

<dl> <dt>

<span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, schwerwiegender>: " <fileName><line \#>: Bezeichner <identifier> löst keine Ganzzahl oder keinen Mess Zeichentyp aus."**
</dt> <dd>

Modul Semantik Fehler in Bereichs Spezifikation. Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

In SNMPv1 muss das Symbol, das in einer Bereichs Spezifikation verwendet wird, in eine ganze Zahl oder ein Messgerät aufgelöst werden.

In SNMPv2C muss das in einer Bereichs Spezifikation verwendete Symbol in "Integer", "Gauge32", "Integer32" oder "Unsigned32" aufgelöst werden.

</dd> </dl>

## <a name="fatal-error-1039"></a>Schwerwiegender Fehler 1039

<dl> <dt>

<span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, schwerwiegender>: <fileName><Zeilen \#>: negativer Wert, der in der Größenangabe verwendet wird. "**
</dt> <dd>

Modul Semantik Fehler in der Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C. Jeder Wert, der zum Angeben der Größe verwendet wird, muss nicht negativ sein.

</dd> </dl>

## <a name="fatal-error-1040"></a>Schwerwiegender Fehler 1040

<dl> <dt>

<span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, schwerwiegender>: " <fileName><line \#>: Bezeichner <identifier> in der Größenangabe wird nicht in einen nicht negativen integralen Wert aufgelöst"**
</dt> <dd>

Modul Semantik Fehler in Bereichs-oder Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C. Jedes Symbol, das verwendet wird, um einen Wert in einer Größenangabe anzugeben, wird in einen nicht negativen Wert aufgelöst.

</dd> </dl>

 

 



