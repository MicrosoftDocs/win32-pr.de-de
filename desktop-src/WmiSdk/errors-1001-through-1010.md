---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1001 bis 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Fehler 1001 bis 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348063"
---
# <a name="errors-1001-through-1010"></a>Fehler 1001 bis 1010

Beschreibt die WMI-SNMP-Anbieter Fehler 1001 bis 1010.

[Schwerwiegender Fehler 1001](#fatal-error-1001)

[Schwerwiegender Fehler 1002](#fatal-error-1002)

[Schwerwiegender Fehler 1003](#fatal-error-1003)

[Warnung 1004](#warning-1004)

[Warnung 1005](#warning-1005)

[Schwerwiegender Fehler 1006](#fatal-error-1006)

[Schwerwiegender Fehler 1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>Schwerwiegender Fehler 1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, schwerwiegender>: " <fileName> : <line \#>: Syntax Klausel des Objekttyps wird nicht in zulässige Typen aufgelöst"
</dt> <dd>

Semantik Fehler des Objekttyp-Makro Aufruf Moduls. Die Syntax Klausel des Objekttyp Makros muss in einen Typ oder einen Untertyp aufgelöst werden, der mit der Größen-oder Bereichs Spezifikation, die das SNMPv1-oder SNMPv2C SMI zulässt, gebildet wird. Wenn dies nicht der Fall ist, wird ein schwerwiegender Fehler 1001 gemeldet.

Dieser Fehler kann auftreten, wenn ein SNMPv1-oder SNMPv2C-MIB kompiliert wird.

Die SNMPv1 SMI erlaubt folgende Typen:

-   INTEGER
-   NULL
-   Oktett-Zeichenfolge
-   Objekt Bezeichner
-   NetworkAddress
-   IpAddress
-   Zähler
-   Maßstab
-   TimeTicks
-   Nicht transparent
-   DisplayString
-   Physaddress

Die SNMPv2C SMI erlaubt folgende Typen:

-   INTEGER
-   Oktett-Zeichenfolge
-   Objekt Bezeichner
-   BITS
-   Integer32
-   IpAddress
-   Counter32
-   TimeTicks
-   Nicht transparent
-   Counter64
-   Unsigned32
-   DisplayString
-   Physaddress
-   MacAddress
-   Wahrheitswert
-   Testandincr
-   Autonomoustype
-   Instancepointer
-   Variablepointer
-   Zeilen Zeiger
-   Rowstatus
-   TimeStamp
-   TimeInterval
-   DateAndTime
-   StorageType
-   Tdomäne
-   Taddress

</dd> </dl>

## <a name="fatal-error-1002"></a>Schwerwiegender Fehler 1002

<dl> <dt>

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, schwerwiegender>: " <fileName> : <line \#>: Ungültige Zugriffs Klausel <clause> "
</dt> <dd>

Semantik Fehler des Objekttyp-Makro Aufruf Moduls. Für SNMPv1 muss die Access-Klausel des Objekttyp Makros "schreibgeschützt", "schreibgeschützt", "Lesen/Schreiben" oder "nicht verfügbar" lauten.

Bei SNMPv2C muss die Max-Access-Klausel "schreibgeschützt", "Lesen/erstellen", "Lesen/Schreiben" oder "nicht verfügbar" lauten.

</dd> </dl>

## <a name="fatal-error-1003"></a>Schwerwiegender Fehler 1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, schwerwiegender>: " <fileName> : <line \#>: Ungültige Status Klausel <clause> "
</dt> <dd>

Semantik Fehler des Objekttyp-Makro Aufruf Moduls. Für SNMPv1 muss die Status-Klausel eines Objekttyp-Makro aufgabenaufes "obligatorisch", "optional", "veraltet" oder "veraltet" lauten.

Bei SNMPv2C muss die Status-Klausel eines Objekttyp-Makro auf-aufgabens "Current", "deprecated" oder "deprecated" lauten.

</dd> </dl>

## <a name="warning-1004"></a>Warnung 1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: " <fileName> : <line \#>: <identifier> Objekttyp, dessen Syntax zu einem der Counter-Typen aufgelöst wird, endet nicht mit dem Buchstaben" "
</dt> <dd>

Semantik Warnung für Objekttyp-Makro Aufruf Modul. Der Bezeichner für ein Objekt des Syntax Zählers (SNMPv1) oder Counter32 und Counter64 (SNMPv2C) muss den Plural aufweisen.

Diese Warnung kann auftreten, wenn Sie ein SNMPv1-oder SNMPv2C-MIB kompilieren.

</dd> </dl>

## <a name="warning-1005"></a>Warnung 1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Warning>: " <fileName> : <line \#>: Objekttyp mit der Syntax" Sequence of ", sollte über eine Access-Klausel verfügen, auf die nicht zugegriffen werden kann.
</dt> <dd>

Semantik Warnung für Objekttyp-Makro Aufruf Modul. Eine Tabelle oder konzeptionelle Zeile (Sequenz von bzw. Sequenz Objekttypen) muss "nicht zugänglich" sein.

Diese Warnung kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1006"></a>Schwerwiegender Fehler 1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, schwerwiegender>: " <fileName> : <Zeile \#> Objekttyp <identifier> , der eine Syntax Sequenz hat, verfügt nicht über eine Index-oder Erweiterungs Klausel"
</dt> <dd>

Semantik Fehler des Objekttyp-Makro Aufruf Moduls. Für SNMPv1 muss die Index-Klausel für eine Objekttyp Definition vorhanden sein, deren Syntax zu einem Sequenztyp aufgelöst wird.

Für SNMPv2C muss entweder die Index-oder die Augments-Klausel für eine konzeptionelle Zeilen Deklaration vorhanden sein.

</dd> </dl>

## <a name="fatal-error-1008"></a>Schwerwiegender Fehler 1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, schwerwiegender>: " <fileName> : <line \#>: der Objekttyp <identifier> , für den die Syntax" Sequenz "nicht referenziert wurde.
</dt> <dd>

Semantik Fehler des Objekttyp-Makro Aufruf Moduls. Ein Objekttyp mit der Syntax Klausel als Sequenztyp muss in der Syntax Klausel von genau einem Objekttyp Aufruf enthalten sein, der für eine Tabellen Deklaration steht, d. h. ein Objekt mit der Syntax Klausel als Sequenz vom Typ. Der <Zeilen \#> Parameter verweist auf den zweiten Verweis Punkt.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

 

 



