---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1051 bis 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Fehler 1051 bis 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170eddf3126a40f929aa36899259b731fa244941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352446"
---
# <a name="errors-1051-through-1060"></a>Fehler 1051 bis 1060

Beschreibt die WMI-SNMP-Anbieter Fehler 1051 bis 1060.

[Schwerwiegender Fehler 1051](#fatal-error-1051)

[Schwerwiegender Fehler 1054](#fatal-error-1054)

[Schwerwiegender Fehler 1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>Schwerwiegender Fehler 1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, schwerwiegender>: " <fileName> : <line \#>: mehrdeutiger Verweis auf Symbol <identifier> "**
</dt> <dd>

Der Code für die Modul Semantik der Importe ist spezifisch für weder SNMPv1 noch SNMPv2C. Jeder Objekt Deskriptor, der einem Objekt in einer Internet Standard-MIB entspricht, muss eindeutig sein. Da Enterprise-MIBs allgemeine Objekt Deskriptoren haben können, müssen solche Deskriptoren, die aus zwei Modulen importiert werden, im MIB-Modul mithilfe der Notation "Module. Descriptor" eindeutig verwendet werden.

</dd> </dl>

## <a name="fatal-error-1054"></a>Schwerwiegender Fehler 1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, schwerwiegender>: " <fileName> : <line \#>: <identifier> in einer Index Klausel wird nicht in einen der zulässigen Typen aufgelöst."**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Der Typ eines Objekts in der Index Klausel oder ein beliebiger Typ, der in der Index-Klausel angegeben ist, muss in einen skalaren Typ aufgelöst werden, d. h. eine nicht-Sequenz oder eine nicht-Sequenz vom Typ. Jeder in der Index-Klausel angegebene Typ muss ebenfalls in einen dieser Typen aufgelöst werden.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

## <a name="fatal-error-1055"></a>Schwerwiegender Fehler 1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, schwerwiegender>: " <fileName> : <line \#>: Syntax des Index Objekt Typs <identifier> wird nicht in einen der zulässigen Typen aufgelöst"**
</dt> <dd>

Semantik Fehler des **Objekttyp-** Makro Aufruf Moduls. Der Typ eines Objekts in der Index Klausel oder ein beliebiger Typ, der in der Index-Klausel angegeben ist, muss in einen skalaren Typ aufgelöst werden, d. h. eine nicht-Sequenz oder eine nicht-Sequenz vom Typ.

Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.

</dd> </dl>

 

 



