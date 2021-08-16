---
description: Dies ist eine schreibgeschützte temporäre Tabelle, die zum Anzeigen von Transformationen im Transformationsansichtsmodus verwendet wird. Diese Tabelle wird vom Installationsprogramm nie beibehalten.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: _TransformView-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b3254c7419ed5d4964377a466ecd557429a22450a9ba84fdd892822fca86c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640465"
---
# <a name="_transformview-table"></a>\_TransformView-Tabelle

Dies ist eine schreibgeschützte temporäre Tabelle, die zum Anzeigen von Transformationen im Transformationsansichtsmodus verwendet wird. Diese Tabelle wird vom Installationsprogramm nie beibehalten.

Rufen Sie zum Aufrufen des Transformationsansichtsmodus ein Handle ab, und öffnen Sie die Verweisdatenbank. Weitere Informationen finden [Sie unter Abrufen eines Datenbankhandle.](obtaining-a-database-handle.md) Rufen Sie [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) mit MSITRANSFORM \_ ERROR \_ VIEWTRANSFORM auf. Dadurch wird verhindert, dass die Transformation auf die Datenbank angewendet wird, und der Transformationsinhalt wird in der \_ Tabelle TransformView gespeichert. Auf die Daten in der Tabelle kann mithilfe SQL Abfragen zugegriffen werden. Weitere Informationen finden Sie unter [Arbeiten mit Abfragen.](working-with-queries.md)

Die \_ TransformView-Tabelle wird nicht gelöscht, wenn eine andere Transformation angewendet wird. Die Tabelle spiegelt die kumulativen Auswirkungen aufeinander folgender Anwendungen wider. Um die Transformationen separat anzuzeigen, müssen Sie die Tabelle freigeben.

Die \_ TransformView-Tabelle enthält die folgenden Spalten.



| Spalte  | Typ                         | Key | Nullwerte zulässig |
|---------|------------------------------|-----|----------|
| Tabelle   | [Identifier](identifier.md) | J   | N        |
| Column  | [Text](text.md)             | J   | N        |
| Zeile     | [Text](text.md)             | J   | J        |
| Daten    | [Text](text.md)             | N   | J        |
| Aktuell | [Text](text.md)             | N   | J        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabelle
</dt> <dd>

Name einer geänderten Datenbanktabelle.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Spalte
</dt> <dd>

Name einer geänderten Tabellenspalte oder INSERT, DELETE, CREATE oder DROP.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Zeile
</dt> <dd>

Eine Liste der Primärschlüsselwerte, die durch Registerkarten getrennt sind. NULL-Primärschlüsselwerte werden durch ein einzelnes Leerzeichen dargestellt. Ein NULL-Wert in dieser Spalte gibt eine Schemaänderung an.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Daten
</dt> <dd>

Daten, Name eines Datenstroms oder einer Spaltendefinition.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Aktuellen
</dt> <dd>

Aktueller Wert aus der Verweisdatenbank oder Spalte einer Zahl.

</dd> </dl>

## <a name="remarks"></a>Hinweise

\_TransformView wird durch eine Sperre im Arbeitsspeicher gespeichert, die mit dem folgenden Befehl SQL freigegeben werden kann.

"ALTER TABLE \_ TransformView FREE".

Auf die Daten in der Tabelle kann mithilfe SQL Abfragen zugegriffen werden. Die SQL-Sprache verfügt über zwei Hauptbereiche: DDL (Data Definition Language), die zum Definieren aller Objekte in einer SQL Datenbank verwendet wird, und Data Manipulation Language (DML), die zum Auswählen, Einfügen, Aktualisieren und Löschen von Daten in den mit DDL definierten Objekten verwendet wird.

Die DmL-Transformationsvorgänge (Data Manipulation Language) sind wie folgt angegeben. Die Datenbearbeitungssprache (Data Manipulation Language, DML) sind anweisungen in SQL, die Daten bearbeiten, anstatt sie zu definieren.



| Transformationsvorgang | SQL Ergebnis                                    |
|---------------------|-----------------------------------------------|
| Ändern von Daten         | {table} {column} {row} {data} {aktueller Wert} |
| Zeile einfügen          | {table} "INSERT" {row} NULL NULL              |
| Zeile löschen          | {table} "DELETE" {row} NULL NULL              |



 

Die DDL-Transformationsvorgänge (Data Definition Language) sind wie folgt angegeben. Die Datendefinitionssprache (Data Definition Language, DDL) sind die Anweisungen in SQL, die Daten definieren, anstatt sie zu bearbeiten.



| Transformationsvorgang | SQL Ergebnis                                   |
|---------------------|----------------------------------------------|
| Hinzufügen einer Spalte          | {table} {column} NULL {defn} {Spaltennummer} |
| Tabelle hinzufügen           | {table} "CREATE" NULL NULL NULL              |
| Löschen einer Tabelle          | {table} "DROP" NULL NULL NULL                |



 

Wenn die Anwendung einer Transformation diese Tabelle hinzufügt, empfängt das Datenfeld Text, der als 16-Bit-Ganzzahlwert interpretiert werden kann. Der Wert beschreibt die Spalte mit dem Namen im Feld Spalte. Sie können den ganzzahligen Wert mit den Konstanten in der folgenden Tabelle vergleichen, um die Definition der geänderten Spalte zu bestimmen.



| bit                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7<br/>         | Hexadezimal: 0x0000 0x0100<br/> Dezimal: 0 255<br/> Spaltenbreite<br/>                                                                                                                                                                                                                                  |
| <span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8<br/>                  | Hexadezimal: 0x0100<br/> Dezimal: 256<br/> Eine persistente Spalte. 0 (null) bedeutet eine temporäre Spalte. <br/>                                                                                                                                                                                                   |
| <span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9<br/>                  | Hexadezimal: 0x0200<br/> Dezimal: 1023<br/> Eine lokalisierbare Spalte. Null bedeutet, dass die Spalte nicht lokalisiert werden kann.<br/>                                                                                                                                                                                      |
| <span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11<br/> | Hexadezimal: 0x0000<br/> Dezimal: 0<br/> Lange ganze Zahl<br/> Hexadezimal: 0x0400<br/> Decimal: 1024<br/> Kurze ganze Zahl<br/> Hexadezimal: 0x0800<br/> Decimal: 2048<br/> Binäres Objekt<br/> Hexadezimal: 0x0C00<br/> Dezimalzahl: 3072<br/> String<br/> |
| <span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12<br/>              | Hexadezimal: 0x1000<br/> Decimal: 4096<br/> Nullable-Spalte. 0 (null) bedeutet, dass die Spalte nicht NULL-Werte zugibt.<br/>                                                                                                                                                                                               |
| <span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13<br/>              | Hexadezimal: 0x2000<br/> Dezimalzahl: 8192<br/> Primärschlüsselspalte. Null bedeutet, dass diese Spalte kein Primärschlüssel ist.<br/>                                                                                                                                                                                      |
| <span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15<br/> | Hexadezimal: 0x4000 0x8000<br/> Decimal: 16384 32768<br/> Reserviert<br/>                                                                                                                                                                                                                                |



 

Ein Skriptbeispiel, das die \_ TransformView-Tabelle veranschaulicht, finden Sie unter [Anzeigen einer Transformation.](view-a-transform.md)

 

 




