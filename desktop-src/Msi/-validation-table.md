---
description: Die \_ Validierungs Tabelle ist eine Systemtabelle, die die Spaltennamen und die Spaltenwerte für alle Tabellen in der Datenbank enthält.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: _Validation Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864543"
---
# <a name="_validation-table"></a>\_Validierungs Tabelle

Die \_ Validierungs Tabelle ist eine Systemtabelle, die die Spaltennamen und die Spaltenwerte für alle Tabellen in der Datenbank enthält. Sie wird während des Daten Bank Überprüfungsprozesses verwendet, um sicherzustellen, dass alle Spalten berücksichtigt werden und die richtigen Werte aufweisen. Diese Tabelle wird nicht mit der Installer-Datenbank ausgeliefert.

Die \_ Validierungs Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                               | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------------|-----|----------|
| Tabelle       | [Bezeichner](identifier.md)       | J   | N        |
| Column      | [Bezeichner](identifier.md)       | J   | N        |
| Nullwerte zulässig    | [Text](text.md)                   | N   | N        |
| MinValue    | [Doubleiteger](doubleinteger.md) | N   | J        |
| MaxValue    | [Doubleiteger](doubleinteger.md) | N   | J        |
| KeyTable    | [Bezeichner](identifier.md)       | N   | J        |
| KeyColumn   | [Integer](integer.md)             | N   | J        |
| Category    | [Text](text.md)                   | N   | J        |
| Set         | [Text](text.md)                   | N   | J        |
| BESCHREIBUNG | [Text](text.md)                   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub
</dt> <dd>

Wird verwendet, um eine bestimmte Tabelle zu identifizieren. Dieser Schlüssel und der Spalten Schlüssel bilden den Primärschlüssel der \_ Validierungs Tabelle.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Kolumne
</dt> <dd>

Wird verwendet, um eine bestimmte Spalte der Tabelle zu identifizieren. Dieser Schlüssel und der Tabellenschlüssel bilden den Primärschlüssel der \_ Validierungs Tabelle.

</dd> <dt>

<span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Werte zulässt
</dt> <dd>

Gibt an, ob die Spalte einen NULL-Wert enthalten kann.

Diese Spalte kann einen der folgenden Werte aufweisen.



| String | Bedeutung                                   |
|--------|-------------------------------------------|
| J      | Ja, die Spalte kann einen NULL-Wert aufweisen.    |
| N      | Nein, die Spalte darf keinen NULL-Wert aufweisen. |



 

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue
</dt> <dd>

Dieses Feld gilt für Spalten mit einem numerischen Wert. Das Feld enthält den minimal zulässigen Wert. Dies kann der Minimalwert für eine ganze Zahl oder der minimale Wert für eine Datums-oder Versions Zeichenfolge sein.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue
</dt> <dd>

Dieses Feld gilt für Spalten mit einem numerischen Wert. Das Feld ist der maximal zulässige Wert. Dies kann der Höchstwert für eine ganze Zahl oder der Höchstwert für eine Datums-oder Versions Zeichenfolge sein.

</dd> <dt>

<span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable
</dt> <dd>

Dieses Feld gilt für Spalten, bei denen es sich um externe Schlüssel handelt. Das in column identifizierte Feld muss mit der durch KeyColumn angegebenen Spaltennummer in der Tabelle in keytable verknüpft werden. Dabei kann es sich um eine durch Semikolons getrennte Liste von Tabellen handeln.

</dd> <dt>

<span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn
</dt> <dd>

Dieses Feld gilt für Tabellen Spalten, bei denen es sich um externe Schlüssel handelt. Das in column identifizierte Feld muss mit der durch KeyColumn angegebenen Spaltennummer in der Tabelle in keytable verknüpft werden. Der zulässige Bereich des KeyColumn-Felds ist 1-32.

</dd> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie
</dt> <dd>

Dies ist der Datentyp, der im Datenbankfeld enthalten ist, das in den Tabellen-und Spalten Spalten der \_ Validierungs Tabelle angegeben ist. Wenn dies ein Typ mit einem numerischen Wert ist, z. b. " [Integer](integer.md)", " [doubleinteger](doubleinteger.md) " oder " [time/date](time-date.md)", geben Sie in dieses Feld NULL ein, und geben Sie den Wertebereich mithilfe der Spalten MinValue und MaxValue an. Verwenden Sie die Spalte Kategorie, um die nicht numerischen Datentypen anzugeben, die in den [Spaltendatentypen](column-data-types.md)beschrieben werden.

</dd> <dt>

<span id="Set"></span><span id="set"></span><span id="SET"></span>Set
</dt> <dd>

Dies ist eine Liste zulässiger Werte für dieses Feld, die durch Semikolons getrennt sind. Dieses Feld wird in der Regel für Enumerationen verwendet.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Eine Beschreibung der Daten, die in der Spalte gespeichert sind.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

## <a name="remarks"></a>Bemerkungen

Das Kategoriefeld dieser Tabelle gilt nur für Zeichen folgen Daten. Wenn das Spalten Feld auf eine Spalte mit Binärdaten verweist, muss der binäre Datentyp im Feld "Category" angegeben werden. Ganzzahlige Datenspalten Typen ignorieren das Kategoriefeld während der Validierung.

 

 



