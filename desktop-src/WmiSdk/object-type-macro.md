---
description: Das Object-Type-Makro enthält obligatorische und optionale Klauseln, die die grundlegenden Merkmale eines MIB-Objekts beschreiben. Der SNMP-Anbieter konvertiert ein MIB in die entsprechenden Teile des ObjektType-Makros.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Object-Type-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128077"
---
# <a name="object-type-macro"></a>Object-Type-Makro

Das Object-Type-Makro enthält obligatorische und optionale Klauseln, die die grundlegenden Merkmale eines MIB-Objekts beschreiben. Der SNMP-Anbieter konvertiert ein MIB in die entsprechenden Teile des ObjektType-Makros.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Komponenten

<dl> <dt>

<span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB-Objekt
</dt> <dd>

Objekt, das den größten Teil der fraglichen Daten enthält.

</dd> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Objekt Deskriptor
</dt> <dd>

Eindeutiger Name oder Objekt Deskriptor, der jedes MIB-Objekt identifiziert. Jeder MIB-Objekt Deskriptor ist exakt einem CIM-Eigenschaftsnamen zugeordnet. **Ifindex** beispielsweise wird in **ifindex** übersetzt.

</dd> <dt>

<span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Syntax Klausel](syntax-clause.md)
</dt> <dd>

Definiert die Daten und den Typ eines MIB-Objekts.

</dd> <dt>

<span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[Index-Klausel](index-clause.md)
</dt> <dd>

Definiert einen Schlüssel zum Auswählen einer eindeutigen Tabellenzeile.

</dd> <dt>

<span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>Augments-Klausel
</dt> <dd>

Gibt an, dass die von Ihnen festgelegten Tabellen Auflistung als Erweiterung einer anderen Tabellen Auflistung angesehen werden kann, und kann die Index Klausel in SNMPv2 ersetzen. Die Auflistungen, auf die durch die Erweiterungs Klausel verwiesen wird, können mit der anderen Tabellen Auflistung kombiniert werden, um eine Sammlung zu bilden. Die resultierende Auflistung gibt die in der letzten Tabellen Auflistung in der Kette angegebenen Primärschlüssel Eigenschaften frei.

In diesem Fall werden die zuvor für die Index-Klausel angegebenen Zustellungs Regeln auf die letzte Tabellen Auflistung in der Kette angewendet. Die Auflistung von-Objekten wird dann einer CIM-Klassendefinition zugeordnet.

</dd> <dt>

<span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>Object-Identifier-Klausel
</dt> <dd>

Enthält einen eindeutigen Objekt Bezeichner für ein MIB-Objekt. Dieser Objekt Bezeichner wird dem **Objekt \_ Bezeichner** des CIM-Eigenschaften Qualifizierers zugeordnet.

</dd> <dt>

<span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Access-und Max-Access-Klauseln](access-and-max-access-clauses.md)
</dt> <dd>

Definieren Sie die Zugriffsrechte für das MIB-Objekt.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Description-Klausel
</dt> <dd>

Stellt eine Textbeschreibung des-Objekts bereit, das der CIM-Eigenschaften **qualifiziererbeschreibung** zugeordnet ist. Diese Klausel ist möglicherweise leer.

Jede **Tabelle** und jedes **Eingabe** Objekt in einer SNMP-Tabellendefinition enthält auch eine Beschreibungs Klausel, die auch leer sein kann. Die Tabellen-und Eintrags Beschreibungs Klauseln werden verkettet, und das Ergebnis wird der **Beschreibung** der CIM-Klassen Qualifizierer zugeordnet.

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Status-Klausel
</dt> <dd>

Gibt an, ob das Objekt unterstützt werden muss. Wenn der Wert der Status-Klausel **veraltet** ist, verwirft der Anbieter das MIB-Objekt aus der Zuordnung. Andernfalls wird die Status-Klausel dem CIM-Eigenschaften **qualifiziererstatus** zugeordnet.

Der bevorzugte **Wert für SNMPv1 ist entweder** **obligatorisch** oder **optional**, aber der Qualifizierer kann einen anderen Wert enthalten. Der bevorzugte **Wert für SNMPv2C ist entweder** **Current** oder **veraltet**, aber der Qualifizierer kann einen anderen Wert enthalten.

</dd> <dt>

<span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>Defval-Klausel
</dt> <dd>

Weist einer Variablen in einer logischen Tabellenzeile einen Standardwert zu und wird dem Zeichen folgen-CIM-Eigenschafts Qualifizierer **defval** zugeordnet.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Reference-Klausel
</dt> <dd>

Verweist auf ein anderes Dokument, das weitere Informationen zum-Objekt enthält. Diese Klausel wird dem CIM-Eigenschafts **qualifiziererverweis** zugeordnet, der vom Typ "String" ist.

</dd> <dt>

<span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>Units-Klausel
</dt> <dd>

Stellt eine genaue Definition der Darstellung des-Objekts bereit. Diese Klausel ist den CIM-Eigenschaften **qualifizierereinheiten** zugeordnet, die den Typ "String" haben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Object-Type-Makro beschreibt die Grundmerkmale eines einzelnen MIB-Objekts. Ein Satz von Objekttyp Makros kann als Gruppe verwandter Objekte betrachtet werden. Verwenden Sie in SNMPv2C das Objektgruppen Makro, um Sätze verwandter Objekte formal in eine Auflistung zu gruppieren. Es ist jedoch kein formaler Mechanismus zum Erstellen von Sammlungen in SNMPv1 vorhanden. Für den SNMP-Anbieter wird das Objektgruppen Makro ignoriert, Sie können jedoch Gruppierungs Beziehungen und fabrizieren von Auflistungen erfinden.

 

 



