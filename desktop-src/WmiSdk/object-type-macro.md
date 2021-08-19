---
description: Das OBJECT-TYPE-Makro enthält obligatorische und optionale Klauseln, die die grundlegenden Merkmale eines MIB-Objekts beschreiben. Der SNMP-Anbieter konvertiert einen MIB in die entsprechenden Teile des OBJECT-TYPE-Makros.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: OBJECT-TYPE-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef71bcdd915dfaa59ace008c28a5d63a323c2cd1d0f119b9d91e5a0720e192e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818006"
---
# <a name="object-type-macro"></a>OBJECT-TYPE-Makro

Das OBJECT-TYPE-Makro enthält obligatorische und optionale Klauseln, die die grundlegenden Merkmale eines MIB-Objekts beschreiben. Der SNMP-Anbieter konvertiert einen MIB in die entsprechenden Teile des OBJECT-TYPE-Makros.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

## <a name="components"></a>Komponenten

<dl> <dt>

<span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB-Objekt
</dt> <dd>

Objekt, das die meisten der in Frage gestellten Daten enthält.

</dd> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Objektdeskriptor
</dt> <dd>

Eindeutiger Name oder Objektdeskriptor, der jedes MIB-Objekt identifiziert. Jeder MIB-Objektdeskriptor wird genau einem CIM-Eigenschaftennamen zuordnen. IfIndex **wird z. B.** in **ifIndex übersetzt.**

</dd> <dt>

<span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[SYNTAX-Klausel](syntax-clause.md)
</dt> <dd>

Definiert die Daten und den Typ eines MIB-Objekts.

</dd> <dt>

<span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX-Klausel](index-clause.md)
</dt> <dd>

Definiert einen Schlüssel zum Auswählen einer eindeutigen Tabellenzeile.

</dd> <dt>

<span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUGMENTS-Klausel
</dt> <dd>

Gibt an, dass die von ihm angegebenen Tabellensammlungen als Erweiterung einer anderen Tabellensammlung betrachtet werden können und die INDEX-Klausel in SNMPv2 ersetzen kann. Die Auflistungen, auf die durch die AUGMENTS-Klausel verwiesen wird, können mit der anderen Tabellensammlung kombiniert werden, um eine Sammlung zu bilden. Die resultierende Auflistung verwendet die Primärschlüsseleigenschaften, die in der letzten Tabellensammlung in der Kette angegeben sind.

In diesem Fall werden die vorherigen Zuordnungsregeln, die für die INDEX-Klausel angegeben wurden, auf die letzte Tabellensammlung in der Kette angewendet. Die Auflistung von -Objekten wird dann einer CIM-Klassendefinition zuordnungen.

</dd> <dt>

<span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT-IDENTIFIER-Klausel
</dt> <dd>

Enthält einen eindeutigen Objektbezeichner für ein MIB-Objekt. Dieser Objektbezeichner wird dem CIM-Eigenschaftenqualifizierer-Objektbezeichner **\_ zu.**

</dd> <dt>

<span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[ACCESS- und MAX-ACCESS-Klauseln](access-and-max-access-clauses.md)
</dt> <dd>

Definieren Sie die Zugriffsrechte für das MIB-Objekt.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION-Klausel
</dt> <dd>

Stellt eine Textbeschreibung des -Objekts zur Verfügung, das dem CIM-Eigenschaftenqualifizierer **Description zu ordnet.** Diese Klausel ist möglicherweise leer.

Jedes **TABLE-** **und ENTRY-Objekt** in einer SNMP-Tabellendefinition enthält auch eine DESCRIPTION-Klausel, die ebenfalls leer sein kann. Die TABLE- und ENTRY DESCRIPTION-Klauseln werden verkettet, und das Ergebnis wird dem CIM-Klassenqualifizierer **Description angezeigt.**

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS-Klausel
</dt> <dd>

Gibt an, ob das Objekt unterstützt werden muss. Wenn der Wert der STATUS-Klausel **veraltet ist,** verwirft der Anbieter das MIB-Objekt aus der Zuordnung. Andernfalls wird die STATUS-Klausel der CIM-Eigenschaft qualifizierer **Status zu.**

Für SNMPv1 ist der bevorzugte  Wert von **Status** entweder obligatorisch oder **optional,** aber der Qualifizierer kann einen anderen Wert enthalten. Für SNMPv2C ist der bevorzugte Wert von **Status** entweder **aktuell** oder veraltet, aber der Qualifizierer kann einen anderen Wert enthalten.

</dd> <dt>

<span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL-Klausel
</dt> <dd>

Weist einer Variablen in einer logischen Tabellenzeile einen Standardwert zu und wird der Zeichenfolge CIM-Eigenschaftenqualifizierer **Defval zugeordnet.**

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE-Klausel
</dt> <dd>

Verweist auf ein anderes Dokument, das weitere Informationen zum -Objekt enthält. Diese Klausel wird dem CIM-Eigenschaftenqualifizierer Reference (CIM-Eigenschaftsqualifiziererverweis) vom Typ string (Zeichenfolge) zu. 

</dd> <dt>

<span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITS-Klausel
</dt> <dd>

Stellt eine genaue Definition dessen dar, was das -Objekt darstellt. Diese Klausel wird der CIM-Eigenschaft qualifizierer **Units (Einheiten)** vom Typ string (Zeichenfolge) zu.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das OBJECT-TYPE-Makro beschreibt die grundlegenden Merkmale eines einzelnen MIB-Objekts. Ein Satz von OBJECT-TYPE-Makros kann als Gruppe verwandter Objekte betrachtet werden. Verwenden Sie in SNMPv2C das OBJECT-GROUP-Makro, um Sätze verwandter Objekte formell in einer Auflistung zu gruppieren. Es gibt jedoch keinen formalen Mechanismus zum Erstellen von Sammlungen in SNMPv1. Für den SNMP-Anbieter wird das OBJECT-GROUP-Makro ignoriert, aber Sie können Gruppierungsbeziehungen erstellen und Sammlungen erstellen.

 

 



