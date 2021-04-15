---
description: Dies ist eine schreibgeschützte temporäre Tabelle, die zum Anzeigen von Transformationen mit dem Transformations Ansichtsmodus verwendet wird. Diese Tabelle wird nie vom Installationsprogramm persistent gespeichert.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: _TransformView Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528883"
---
# <a name="_transformview-table"></a>\_Transformview-Tabelle

Dies ist eine schreibgeschützte temporäre Tabelle, die zum Anzeigen von Transformationen mit dem Transformations Ansichtsmodus verwendet wird. Diese Tabelle wird nie vom Installationsprogramm persistent gespeichert.

Um den Transformations Ansichtsmodus aufzurufen, rufen Sie ein Handle ab, und öffnen Sie die Verweis Datenbank. Siehe Abrufen [eines Daten Bank Handles](obtaining-a-database-handle.md). [**Msidatabaseapplytransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) mit msitransform- \_ Fehler \_ viewtransform abrufen. Dadurch wird verhindert, dass die Transformation auf die Datenbank angewendet wird, und der Transformations Inhalt wird in die \_ transformview-Tabelle integriert. Auf die Daten in der Tabelle kann mithilfe von SQL-Abfragen zugegriffen werden. Siehe [Arbeiten mit Abfragen](working-with-queries.md).

Die \_ transformview-Tabelle wird nicht gelöscht, wenn eine andere Transformation angewendet wird. Die Tabelle spiegelt die kumulative Auswirkung aufeinander folgender Anwendungen wider. Um die Transformationen separat anzuzeigen, müssen Sie die Tabelle freigeben.

Die \_ transformview-Tabelle weist die folgenden Spalten auf.



| Spalte  | Typ                         | Schlüssel | Nullwerte zulässig |
|---------|------------------------------|-----|----------|
| Tabelle   | [Bezeichner](identifier.md) | J   | N        |
| Column  | [Text](text.md)             | J   | N        |
| Zeile     | [Text](text.md)             | J   | J        |
| Daten    | [Text](text.md)             | N   | J        |
| Aktuell | [Text](text.md)             | N   | J        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub
</dt> <dd>

Der Name einer geänderten Datenbanktabelle.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Kolumne
</dt> <dd>

Der Name einer geänderten Tabellenspalte oder INSERT, DELETE, CREATE oder Drop.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Zeile
</dt> <dd>

Eine Liste der Primärschlüssel Werte, die durch Registerkarten getrennt sind. NULL-Primärschlüssel Werte werden durch ein einzelnes Leerzeichen dargestellt. Ein NULL-Wert in dieser Spalte gibt eine Schema Änderung an.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats
</dt> <dd>

Daten, Name eines Datenstroms oder Spaltendefinition.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Strömung
</dt> <dd>

Aktueller Wert aus Verweis Datenbank oder Spalte a-Nummer.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die \_ transformview wird durch eine Sperr Anzahl im Arbeitsspeicher gespeichert, die mit dem folgenden SQL-Befehl freigegeben werden kann.

"Alter Table \_ transformview Free".

Auf die Daten in der Tabelle kann mithilfe von SQL-Abfragen zugegriffen werden. Die SQL-Sprache verfügt über zwei Hauptbereiche: Datendefinitionssprache (Data Definition Language, DDL), die zum Definieren aller Objekte in einer SQL-Datenbank verwendet wird, und DML (Data Manipulation Language), die zum auswählen, einfügen, aktualisieren und Löschen von Daten in den Objekten verwendet werden, die mithilfe von DDL definiert wurden.

Die Transformations Vorgänge der Daten Bearbeitungs Sprache (DML) werden wie folgt angegeben. DML (Data Manipulation Language) sind die Anweisungen in SQL, die im Gegensatz zum Definieren von Daten bearbeitet werden.



| Transformations Vorgang | SQL-Ergebnis                                    |
|---------------------|-----------------------------------------------|
| Ändern von Daten         | glaub Kolumne Zeile Vorrats {Aktueller Wert} |
| Zeile einfügen          | glaub "Insert" {Row} NULL NULL              |
| Zeile löschen          | glaub "Delete" {Row} NULL NULL              |



 

Die DDL-Transformations Vorgänge (Data Definition Language, Datendefinitionssprache) werden wie folgt angegeben. DDL (Data Definition Language) sind die Anweisungen in SQL, die definieren, dass Daten nicht bearbeitet werden können.



| Transformations Vorgang | SQL-Ergebnis                                   |
|---------------------|----------------------------------------------|
| Hinzufügen einer Spalte          | glaub Kolumne NULL {DEFN} {Spaltennummer} |
| Tabelle hinzufügen           | glaub "Create" Null Null Null              |
| Löschen einer Tabelle          | glaub "Drop" Null Null Null                |



 

Wenn die Anwendung einer Transformation diese Tabelle hinzufügt, empfängt das Datenfeld Text, der als 16-Bit-Ganzzahl interpretiert werden kann. Der Wert beschreibt die Spalte mit dem Namen im Feld Spalte. Sie können den ganzzahligen Wert mit den Konstanten in der folgenden Tabelle vergleichen, um die Definition der geänderten Spalte zu bestimmen.



| bit                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7<br/>         | Hexadezimalwert: 0x0000 0x0100<br/> Dezimalzahl: 0 255<br/> Spaltenbreite<br/>                                                                                                                                                                                                                                  |
| <span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8<br/>                  | Hexadezimalwert: 0x0100<br/> Dezimalzahl: 256<br/> Eine persistente Spalte. NULL bedeutet eine temporäre Spalte. <br/>                                                                                                                                                                                                   |
| <span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9<br/>                  | Hexadezimalwert: 0x0200<br/> Dezimalzahl: 1023<br/> Eine lokalisierbare Spalte. NULL bedeutet, dass die Spalte nicht lokalisiert werden kann.<br/>                                                                                                                                                                                      |
| <span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11<br/> | Hexadezimalwert: 0x0000<br/> Dezimalwert: 0<br/> Lange ganze Zahl<br/> Hexadezimalwert: 0x0400<br/> Dezimalzahl: 1024<br/> Kurze Ganzzahl<br/> Hexadezimalwert: 0x0800<br/> Dezimalzahl: 2048<br/> Binary-Objekt<br/> Hexadezimal: 0x0c00<br/> Dezimalzahl: 3072<br/> String<br/> |
| <span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12<br/>              | Hexadezimalwert: 0x1000<br/> Dezimalzahl: 4096<br/> Nullable-Spalte. NULL bedeutet, dass die Spalte keine NULL-Werte zulässt.<br/>                                                                                                                                                                                               |
| <span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13<br/>              | Hexadezimalwert: 0x2000<br/> Dezimalzahl: 8192<br/> Primärschlüssel Spalte. NULL bedeutet, dass diese Spalte kein Primärschlüssel ist.<br/>                                                                                                                                                                                      |
| <span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15<br/> | Hexadezimalwert: 0x4000 0X8000<br/> Dezimalzahl: 16384 32768<br/> Reserviert<br/>                                                                                                                                                                                                                                |



 

Ein Skript Beispiel, in dem die \_ transformview-Tabelle veranschaulicht wird, finden Sie unter [View a Transform](view-a-transform.md).

 

 




