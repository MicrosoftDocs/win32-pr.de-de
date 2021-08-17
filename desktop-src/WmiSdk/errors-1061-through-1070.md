---
description: Beschreibt die Fehler 1061 bis 1070 des WMI-SNMP-Anbieters.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Fehler 1061 bis 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c0072f30c8daf584c1aaf2acf783b15d2d9498a3c1479264a1db361c3e3ce43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924571"
---
# <a name="errors-1061-through-1070"></a>Fehler 1061 bis 1070

Beschreibt die Fehler 1061 bis 1070 des WMI-SNMP-Anbieters.

[Schwerwiegender Fehler 1063](#fatal-error-1063)

[Schwerwiegender Fehler 1064](#fatal-error-1064)

[Schwerwiegender Fehler 1070](#fatal-error-1070)

## <a name="fatal-error-1063"></a>Schwerwiegender Fehler 1063

<dl> <dt>

<span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, Fatal>: <fileName> "<line \#>: Upper bound of SIZE specification is less than the lower bound"**
</dt> <dd>

Modulsemantikfehler in der SIZE-Spezifikation, der weder für SNMPv1 noch für SNMPv2C spezifisch ist. Das in einer SIZE-Spezifikation verwendete Symbol muss in OCTET STRING oder Opaque aufgelöst werden. Die untere Grenze eines Bereichs oder einer SIZE-Spezifikation darf nicht größer als die Obergrenze sein.

</dd> </dl>

## <a name="fatal-error-1064"></a>Schwerwiegender Fehler 1064

<dl> <dt>

<span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, Fatal>: <fileName> ":<line \#>: SEQUENCE item <identifier> does not resolve to an OBJECT-TYPE"**
</dt> <dd>

Semantischer Fehler des Typzuweisungsmoduls, der weder für SNMPv1 noch für SNMPv2C spezifisch ist. Alle einzelnen Elemente einer SEQUENCE-Deklaration müssen in einen OBJECT-TYPE aufgelöst werden.

</dd> </dl>

## <a name="fatal-error-1070"></a>Schwerwiegender Fehler 1070

<dl> <dt>

<span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, Fatal>: <fileName> "<line \#>: MIB Module <moduleName> , aus dem das Symbol importiert <symbolName> wird, ist in der Eingabe nicht vorhanden"**
</dt> <dd>

Modulsemantikfehler beim Querverweisen, der weder für SNMPv1 noch für SNMPv2C spezifisch ist. Wenn eines der Module im Imports-Abschnitt des Hauptmoduls oder eines untergeordneten Moduls nicht vorhanden ist und tatsächlich auf ein oder mehrere Symbole aus diesem Modul verwiesen wird, tritt dieser schwerwiegende Fehler auf.

</dd> </dl>

 

 



