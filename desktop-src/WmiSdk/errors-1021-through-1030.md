---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1021 bis 1033.
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: Fehler 1021 bis 1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8bce9c7c4d70250fa63ad0100cf93c8d5b26984
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347095"
---
# <a name="errors-1021-through-1030"></a>Fehler 1021 bis 1030

Beschreibt die WMI-SNMP-Anbieter Fehler 1021 bis 1033.

[Schwerwiegender Fehler 1021](#fatal-error-1021)

[Schwerwiegender Fehler 1022](#fatal-error-1022)

[Schwerwiegender Fehler 1023](#fatal-error-1023)

[Schwerwiegender Fehler 1024](#fatal-error-1024)

[Schwerwiegender Fehler 1025](#fatal-error-1025)

[Schwerwiegender Fehler 1026](#fatal-error-1026)

[Warnung 1027](#warning-1027)

[Schwerwiegender Fehler 1028](#fatal-error-1028)

[Schwerwiegender Fehler 1029](#fatal-error-1029)

[Schwerwiegender Fehler 1030](#fatal-error-1030)

## <a name="fatal-error-1021"></a>Schwerwiegender Fehler 1021

<dl> <dt>

<span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, schwerwiegender>: " <fileName><line \#>: der <identifier> Bezeichner in der Variables-Klausel von Trap-Type wird nicht in einen skalaren Objekttyp aufgelöst."**
</dt> <dd>

**Trap-Type-** Makro Aufruf, SNMPv1-spezifischer Modul Semantik Fehler. Jedes Element in der Liste der Variablen, das in der Variables-Klausel eines **Trap-Type-** Makro Aufrufs verwendet wird, muss in den Namen einer Instanz des skalaren Objekt Typs aufgelöst werden.

</dd> </dl>

## <a name="fatal-error-1022"></a>Schwerwiegender Fehler 1022

<dl> <dt>

<span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, schwerwiegender>: " <fileName><line \#>: Wert wird nicht in Typ aufgelöst <type> "**
</dt> <dd>

Semantik Fehler des Wert Zuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C. Der Wert für die RHS einer Ganzzahl, **null**, Oktett-Zeichenfolge oder Objekt-ID-Wert Zuweisung weist den falschen Typ auf.

</dd> </dl>

## <a name="fatal-error-1023"></a>Schwerwiegender Fehler 1023

<dl> <dt>

<span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, schwerwiegender>: " <fileName><line \#>: Bezeichner <identifier> wird nicht in den Typ aufgelöst <identifier> "**
</dt> <dd>

Semantik Fehler des Wert Zuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C. Ein Symbol (Werte Verweis) für die RHS einer Ganzzahl, **null**, Oktett-Zeichenfolge oder Objekt-ID-Wert Zuweisung wird nicht in den richtigen Typ aufgelöst.

</dd> </dl>

## <a name="fatal-error-1024"></a>Schwerwiegender Fehler 1024

<dl> <dt>

<span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, schwerwiegender>: " <fileName><line \#>: negative Ganzzahl in OID-Werte Definition"**
</dt> <dd>

Semantik Fehler des Wert Zuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C. Alle Werte in einer OID-Komponentenliste müssen nicht negative (vorzugsweise positive) ganze Zahlen sein.

</dd> </dl>

## <a name="fatal-error-1025"></a>Schwerwiegender Fehler 1025

<dl> <dt>

<span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, schwerwiegender>: "Bezeichner <identifier> in OID-Wert wird nicht in eine positive ganze Zahl aufgelöst"**
</dt> <dd>

Semantik Fehler des Wert Zuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C. Alle Werte in einer OID-Komponentenliste müssen nicht negative (vorzugsweise positive) ganze Zahlen sein.

</dd> </dl>

## <a name="fatal-error-1026"></a>Schwerwiegender Fehler 1026

<dl> <dt>

<span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, schwerwiegender>: " <fileName><line \#>: der Bezeichner <identifier> in OID-Wert wird weder in einen OID-Wert noch in eine positive ganze Zahl aufgelöst"**
</dt> <dd>

Semantik Fehler des Wert Zuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C. Die erste Komponente, die in einem OID-Wert verwendet wird, muss in einen OID-oder eine ganze Zahl aufgelöst werden.

</dd> </dl>

## <a name="warning-1027"></a>Warnung 1027

<dl> <dt>

<span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, Warning>: " <fileName><line \#>: importiertes Symbol nicht <identifier> verwendet."**
</dt> <dd>

Gibt eine Semantik Warnung für das Abschnitts Modul aus, die spezifisch für weder SNMPv1 noch SNMPv2C. Für jedes nicht verwendete importierte Symbol wird eine Warnung ausgegeben.

</dd> </dl>

## <a name="fatal-error-1028"></a>Schwerwiegender Fehler 1028

<dl> <dt>

<span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, schwerwiegender>: "Modul wurde <identifier> nicht in den Imports-Abschnitt importiert"**
</dt> <dd>

Der Code für die Modul Semantik der Importe ist spezifisch für weder SNMPv1 noch SNMPv2C. Ein Modulname, der zum Verweisen auf ein Symbol verwendet wird, muss entweder in der Imports-Klausel vorhanden sein oder der Name des aktuellen Moduls sein.

</dd> </dl>

## <a name="fatal-error-1029"></a>Schwerwiegender Fehler 1029

<dl> <dt>

<span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, schwerwiegender>: " <fileName><line \#>: das aktuelle Modul <identifier> kann nicht importiert werden"**
</dt> <dd>

Der Code für die Modul Semantik der Importe ist spezifisch für weder SNMPv1 noch SNMPv2C. Der Name des aktuellen Moduls ist auch in der Liste der Importe enthalten.

</dd> </dl>

## <a name="fatal-error-1030"></a>Schwerwiegender Fehler 1030

<dl> <dt>

<span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, schwerwiegender>: " <fileName><line \#>: Symbol <identifier> nicht aus Modul importiert <identifier> "**
</dt> <dd>

Der Code für die Modul Semantik der Importe ist spezifisch für weder SNMPv1 noch SNMPv2C. Sie haben die Notation "Module. Symbol" verwendet, aber das Symbol wurde nicht aus dem angegebenen Modul im Abschnitt Imports importiert.

</dd> </dl>

 

 



