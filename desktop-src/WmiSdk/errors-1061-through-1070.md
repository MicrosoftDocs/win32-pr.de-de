---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1061 bis 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Fehler 1061 bis 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a4bf0773ade1f62eb11f0c496aea340410c4a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356894"
---
# <a name="errors-1061-through-1070"></a>Fehler 1061 bis 1070

Beschreibt die WMI-SNMP-Anbieter Fehler 1061 bis 1070.

[Schwerwiegender Fehler 1063](#fatal-error-1063)

[Schwerwiegender Fehler 1064](#fatal-error-1064)

[Schwerwiegender Fehler 1070](#fatal-error-1070)

## <a name="fatal-error-1063"></a>Schwerwiegender Fehler 1063

<dl> <dt>

<span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, schwerwiegender>: " <fileName><line \#>: die obere Grenze der Größenangabe ist kleiner als die untere Grenze"**
</dt> <dd>

Modul Semantik Fehler in der Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C. Das in einer Größenangabe verwendete Symbol muss in eine Oktett-Zeichenfolge oder eine nicht transparente Zeichenfolge aufgelöst werden Die untere Grenze einer Bereichs-oder Größenangabe darf nicht größer als die obere Grenze sein.

</dd> </dl>

## <a name="fatal-error-1064"></a>Schwerwiegender Fehler 1064

<dl> <dt>

<span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, schwerwiegender>: " <fileName> : <line \#>: <identifier> das Sequenz Element wird nicht in einen Objekttyp aufgelöst."**
</dt> <dd>

Semantik Fehler des typzuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C. Alle einzelnen Elemente einer Sequenz Deklaration müssen in einen Objekttyp aufgelöst werden.

</dd> </dl>

## <a name="fatal-error-1070"></a>Schwerwiegender Fehler 1070

<dl> <dt>

<span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, schwerwiegender>: " <fileName><line \#>: MIB-Modul <moduleName> , von dem das Symbol <symbolName> importiert wird, ist nicht in der Eingabe vorhanden"**
</dt> <dd>

Modul Semantik Fehler in Querverweisen, spezifisch für weder SNMPv1 noch SNMPv2C. Wenn eines der Module im Imports-Abschnitt des Haupt Moduls oder eines Tochter Moduls nicht vorhanden ist und auf mindestens ein Symbol aus diesem Modul verwiesen wird, tritt dieser schwerwiegender Fehler auf.

</dd> </dl>

 

 



