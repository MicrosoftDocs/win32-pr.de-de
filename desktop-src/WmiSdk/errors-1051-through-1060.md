---
description: Beschreibt die Fehler 1051 bis 1060 des WMI-SNMP-Anbieters.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Fehler 1051 bis 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3405a799d71b33fa1dabd7c84964b8d1726d2e27
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882590"
---
# <a name="errors-1051-through-1060"></a>Fehler 1051 bis 1060

Beschreibt die Fehler 1051 bis 1060 des WMI-SNMP-Anbieters.

[Schwerwiegender Fehler 1051](#fatal-error-1051)

[Schwerwiegender Fehler 1054](#fatal-error-1054)

[Schwerwiegender Fehler 1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>Schwerwiegender Fehler 1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Fatal>: " &lt; fileName &gt; :<line \#>: Ambiguous reference to symbol &lt; identifier &gt; "**
</dt> <dd>

Semantischer Fehler des IMPORTS-Abschnittmoduls, der weder für SNMPv1 noch für SNMPv2C spezifisch ist. Jeder Objektdeskriptor, der einem Objekt in einer Internet Standard-MIB entspricht, muss eindeutig sein. Da Unternehmens-MIBs über allgemeine Objektdeskriptoren verfügen können, müssen solche aus zwei Modulen importierten Deskriptoren eindeutig im MIB-Modul verwendet werden, indem die Notation "module.descriptor" verwendet wird.

</dd> </dl>

## <a name="fatal-error-1054"></a>Schwerwiegender Fehler 1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Fatal>: " &lt; fileName &gt; :<line \#>: identifier &lt; in &gt; INDEX clause does not resolve to one of the allowed types"**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Der Typ eines Objekts in der INDEX-Klausel oder ein beliebiger in der INDEX-Klausel angegebener Typ muss in einen Skalartyp aufgelöst werden, d. h. in einen Nicht-SEQUENCE- oder Nicht-SEQUENCE OF-Typ. Jeder in der INDEX-Klausel angegebene Typ muss ebenfalls in einen dieser Typen aufgelöst werden.

Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1055"></a>Schwerwiegender Fehler 1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Fatal>:" &lt; fileName &gt; :<line \#>: SYNTAX of INDEX OBJECT-TYPE &lt; identifier &gt; , does not resolve to one of the allowed types"**
</dt> <dd>

Semantischer Fehler des **OBJECT-TYPE-Makroaufrufmoduls.** Der Typ eines Objekts in der INDEX-Klausel oder ein beliebiger in der INDEX-Klausel angegebener Typ muss in einen Skalartyp aufgelöst werden, d. h. in einen Nicht-SEQUENCE- oder Nicht-SEQUENCE OF-Typ.

Dieser Fehler kann in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

 

 



