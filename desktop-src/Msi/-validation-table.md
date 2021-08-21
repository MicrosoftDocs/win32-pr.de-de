---
description: Die \_ Validierungstabelle ist eine Systemtabelle, die die Spaltennamen und Spaltenwerte für alle Tabellen in der Datenbank enthält.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: _Validation-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a42fbe2a2f8da4abceb04912eee2a12edd708ff88d979fbf45f7de8051dc80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640445"
---
# <a name="_validation-table"></a>\_Validierungstabelle

Die \_ Validierungstabelle ist eine Systemtabelle, die die Spaltennamen und Spaltenwerte für alle Tabellen in der Datenbank enthält. Sie wird während des Datenbankvalidierungsprozesses verwendet, um sicherzustellen, dass alle Spalten berücksichtigt werden und die richtigen Werte aufweisen. Diese Tabelle ist nicht im Lieferumfang der Installer-Datenbank enthalten.

Die \_ Tabelle Validation enthält die folgenden Spalten.



| Spalte      | Typ                               | Key | Nullwerte zulässig |
|-------------|------------------------------------|-----|----------|
| Tabelle       | [Identifier](identifier.md)       | J   | N        |
| Spalte      | [Identifier](identifier.md)       | J   | N        |
| Nullwerte zulässig    | [Text](text.md)                   | N   | N        |
| Minvalue    | [DoubleInteger](doubleinteger.md) | N   | J        |
| MaxValue    | [DoubleInteger](doubleinteger.md) | N   | J        |
| KeyTable    | [Identifier](identifier.md)       | N   | J        |
| KeyColumn   | [Integer](integer.md)             | N   | J        |
| Category    | [Text](text.md)                   | N   | J        |
| Set         | [Text](text.md)                   | N   | J        |
| BESCHREIBUNG | [Text](text.md)                   | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabelle
</dt> <dd>

Wird verwendet, um eine bestimmte Tabelle zu identifizieren. Dieser Schlüssel und der Spaltenschlüssel bilden den Primärschlüssel der \_ Validierungstabelle.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Spalte
</dt> <dd>

Wird verwendet, um eine bestimmte Spalte der Tabelle zu identifizieren. Dieser Schlüssel und der Tabellenschlüssel bilden den Primärschlüssel der \_ Validierungstabelle.

</dd> <dt>

<span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable
</dt> <dd>

Gibt an, ob die Spalte einen NULL-Wert enthalten kann.

Diese Spalte kann einen der folgenden Werte aufweisen.



| String | Bedeutung                                   |
|--------|-------------------------------------------|
| J      | Ja, die Spalte kann einen NULL-Wert aufweisen.    |
| N      | Nein, die Spalte hat möglicherweise keinen NULL-Wert. |



 

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>Minvalue
</dt> <dd>

Dieses Feld gilt für Spalten mit einem numerischen Wert. Das Feld enthält den minimal zulässigen Wert. Dies kann der Mindestwert für eine ganze Zahl oder der Mindestwert für eine Datums- oder Versionszeichenfolge sein.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>Maxvalue
</dt> <dd>

Dieses Feld gilt für Spalten mit einem numerischen Wert. Das Feld ist der maximal zulässige Wert. Dies kann der Höchstwert für eine ganze Zahl oder der Höchstwert für eine Datums- oder Versionszeichenfolge sein.

</dd> <dt>

<span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable
</dt> <dd>

Dieses Feld gilt für Spalten, die externe Schlüssel sind. Das in Spalte identifizierte Feld muss mit der Spaltennummer verknüpft werden, die von KeyColumn in der In KeyTable benannten Tabelle angegeben wird. Dies kann eine Durch Semikolon getrennte Liste von Tabellen sein.

</dd> <dt>

<span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>Keycolumn
</dt> <dd>

Dieses Feld gilt für Tabellenspalten, die externe Schlüssel sind. Das in Spalte identifizierte Feld muss mit der Spaltennummer verknüpft werden, die von KeyColumn in der In KeyTable benannten Tabelle angegeben wird. Der zulässige Bereich des KeyColumn-Felds ist 1-32.

</dd> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie
</dt> <dd>

Dies ist der Datentyp, der in dem Datenbankfeld enthalten ist, das von den Spalten Tabelle und Spalte der Tabelle Validation angegeben \_ wird. Wenn es sich um einen Typ mit einem numerischen Wert handelt, z. B. [Integer,](integer.md) [DoubleInteger](doubleinteger.md) oder [Time/Date,](time-date.md)geben Sie NULL in dieses Feld ein, und geben Sie den Bereich des Werts mithilfe der Spalten MinValue und MaxValue an. Verwenden Sie die Spalte Kategorie, um die unter [Spaltendatentypen](column-data-types.md)beschriebenen nicht numerischen Datentypen anzugeben.

</dd> <dt>

<span id="Set"></span><span id="set"></span><span id="SET"></span>Festgelegt
</dt> <dd>

Dies ist eine Liste zulässiger Werte für dieses Feld, die durch Semikolons getrennt sind. Dieses Feld wird normalerweise für Enumerationen verwendet.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Eine Beschreibung der Daten, die in der Spalte gespeichert sind.

</dd> </dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

## <a name="remarks"></a>Hinweise

Das Feld Kategorie dieser Tabelle gilt nur für Zeichenfolgendaten. Wenn das Feld Spalte auf eine Spalte mit Binärdaten verweist, muss der binäre Datentyp im Feld Category angegeben werden. Integerdaten Spaltentypen ignorieren das Feld Category während der Überprüfung.

 

 



