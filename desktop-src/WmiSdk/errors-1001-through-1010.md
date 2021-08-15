---
description: Beschreibt die WMI-SNMP-Anbieterfehler 1001 bis 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Fehler 1001 bis 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fac32553e345dfe2f011d6294ff045db58c681b49dc127bd0da8e5afabf0757
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411940"
---
# <a name="errors-1001-through-1010"></a>Fehler 1001 bis 1010

Beschreibt die WMI-SNMP-Anbieterfehler 1001 bis 1010.

[Schwerwiegender Fehler 1001](#fatal-error-1001)

[Schwerwiegender Fehler 1002](#fatal-error-1002)

[Schwerwiegender Fehler 1003](#fatal-error-1003)

[Warnung 1004](#warning-1004)

[Warnung 1005](#warning-1005)

[Schwerwiegender Fehler 1006](#fatal-error-1006)

[Schwerwiegender Fehler 1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>Schwerwiegender Fehler 1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Fatal>: " <fileName> :<line \#>: SYNTAX clause of OBJECT-TYPE does not resolve to allowed types"
</dt> <dd>

Semantikfehler des OBJECT-TYPE-Makroaufrufmoduls. Die SYNTAX-Klausel des OBJECT-TYPE-Makros muss in einen Typ oder Untertyp auflösen, der mithilfe der SIZE- oder Bereichsspezifikation gebildet wird, die die SNMPv1- oder SNMPv2C-SMI zulässt. Wenn dies nicht der Fall ist, wird der schwerwiegende Fehler 1001 gemeldet.

Dieser Fehler kann beim Kompilieren eines SNMPv1- oder SNMPv2C-MIB auftreten.

Vom SNMPv1-SMI zulässige Typen sind:

-   INTEGER
-   NULL
-   OKTETT-ZEICHENFOLGE
-   OBJEKTBEZEICHNER
-   Networkaddress
-   IpAddress
-   Leistungsindikator
-   Maßstab
-   TimeTicks
-   Nicht transparent
-   DisplayString
-   PhysAddress

Vom SNMPv2C-SMI zulässige Typen sind:

-   INTEGER
-   OKTETT-ZEICHENFOLGE
-   OBJEKTBEZEICHNER
-   BITS
-   Integer32
-   IpAddress
-   Counter32
-   TimeTicks
-   Nicht transparent
-   Counter64
-   Unsigned32
-   DisplayString
-   PhysAddress
-   MacAddress
-   TruthValue
-   TestAndIncr
-   AutonomousType
-   InstancePointer
-   VariablePointer
-   RowPointer
-   RowStatus
-   TimeStamp
-   TimeInterval
-   DateAndTime
-   StorageType
-   Tdomain
-   Gegenst du

</dd> </dl>

## <a name="fatal-error-1002"></a>Schwerwiegender Fehler 1002

<dl> <dt>

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Fatal>: " <fileName> :<line \#>: Invalid ACCESS clause <clause> "
</dt> <dd>

Semantikfehler des OBJECT-TYPE-Makroaufrufmoduls. Für SNMPv1 muss die ACCESS-Klausel des OBJECT-TYPE-Makros "schreibgeschützt", "schreibgeschützt", "lesen/schreiben" oder "nicht zugänglich" sein.

Für SNMPv2C muss die MAX-ACCESS-Klausel "schreibgeschützt", "read-create", "read/write" oder "nicht zugänglich" sein.

</dd> </dl>

## <a name="fatal-error-1003"></a>Schwerwiegender Fehler 1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Fatal>: " <fileName> :<line \#>: Invalid STATUS clause <clause> "
</dt> <dd>

Semantikfehler des OBJECT-TYPE-Makroaufrufmoduls. Für SNMPv1 muss die STATUS-Klausel eines OBJECT-TYPE-Makroaufrufs "obligatorisch", "optional", "veraltet" oder "veraltet" sein.

Für SNMPv2C muss die STATUS-Klausel eines OBJECT-TYPE-Makroaufrufs "current", "deprecated" oder "obsolete" sein.

</dd> </dl>

## <a name="warning-1004"></a>Warnung 1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: " <fileName> :<line>: OBJECT-TYPE , dessen Syntax in einen der Indikatortypen auflöset, endet nicht mit dem Buchstaben \# <identifier> 's' "
</dt> <dd>

OBJECT-TYPE-Makroaufrufmodulsemantische Warnung. Der Bezeichner für ein Objekt von SYNTAX Counter (SNMPv1) oder Counter32 und Counter64 (SNMPv2C) muss plural sein.

Diese Warnung kann beim Kompilieren eines SNMPv1- oder SNMPv2C-MIB auftreten.

</dd> </dl>

## <a name="warning-1005"></a>Warnung 1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Warning>: " <fileName> :<line \#>: OBJECT-TYPE with SYNTAX "SEQUENCE OF", should have an ACCESS clause "not-accessible"
</dt> <dd>

OBJECT-TYPE-Makroaufrufmodulsemantische Warnung. Eine Tabelle oder konzeptionelle Zeile (SEQUENCE OF- bzw. SEQUENCE-Objekttypen) muss "nicht zugänglich" sein.

Diese Warnung kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1006"></a>Schwerwiegender Fehler 1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Fatal>: " <fileName> :<line> OBJECT-TYPE , which is of SYNTAX SEQUENCE, does not have an INDEX or \# <identifier> AUGMENTS clause"
</dt> <dd>

Semantikfehler des OBJECT-TYPE-Makroaufrufmoduls. Für SNMPv1 muss die INDEX-Klausel für eine OBJECT-TYPE-Definition vorhanden sein, deren SYNTAX in einen SEQUENCE-Typ auflöset.

Für SNMPv2C muss entweder die INDEX- oder die AUGMENTS-Klausel für eine konzeptionelle Zeilendeklaration vorhanden sein.

</dd> </dl>

## <a name="fatal-error-1008"></a>Schwerwiegender Fehler 1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Fatal>: " <fileName> :<line>: OBJECT-TYPE , which is \# of SYNTAX "SEQUENCE" has not <identifier> referenced"
</dt> <dd>

Semantikfehler des OBJECT-TYPE-Makroaufrufmoduls. Ein OBJECT-TYPE mit der SYNTAX-Klausel als SEQUENCE-Typ muss in der SYNTAX-Klausel genau eines OBJECT-TYPE-Aufrufs enthalten sein, der für eine Tabellendeklaration steht, also ein Objekt mit der SYNTAX-Klausel als SEQUENCE OF-Typ. Der <zeile \#> verweist auf den zweiten Bezugspunkt.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

 

 



