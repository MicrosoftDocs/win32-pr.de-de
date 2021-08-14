---
description: Die IniLocator-Tabelle enthält die Informationen, die zum Suchen nach einer Datei oder eines Verzeichnisses mithilfe einer .ini-Datei oder zum Suchen nach einem bestimmten .ini Eintrag selbst erforderlich sind. Die .ini-Datei muss im Standardverzeichnis von Microsoft Windows vorhanden sein.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: IniLocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5fae106340a953c59358c7c4108991d1510d49ea6d8940bcef72c538b7165ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946540"
---
# <a name="inilocator-table"></a>IniLocator-Tabelle

Die IniLocator-Tabelle enthält die Informationen, die zum Suchen nach einer Datei oder eines Verzeichnisses mithilfe einer .ini-Datei oder zum Suchen nach einem bestimmten .ini Eintrag selbst erforderlich sind. Die .ini-Datei muss im Standardverzeichnis von Microsoft Windows vorhanden sein.

Die IniLocator-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Signatur\_ | [Identifier](identifier.md) | J   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| `Section`     | [Text](text.md)             | N   | N        |
| Key         | [Text](text.md)             | N   | N        |
| Feld       | [Integer](integer.md)       | N   | J        |
| Typ        | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatur\_
</dt> <dd>

Ein externer Schlüssel in der ersten Spalte der [Signaturtabelle](signature-table.md). Die Signatur \_ stellt eine eindeutige Signatur dar und ist auch der externe Schlüssel in Spalte 1 der Signaturtabelle. Wenn diese Signatur in der Signaturtabelle vorhanden ist, wird nach einer Datei gesucht. Wenn dieser Schlüssel in der Signature-Tabelle nicht vorhanden ist und der Wert der Spalte Type **msidbLocatorTypeRawValue** lautet, wird nach dem .ini Eintrag gesucht, der von der IniLocator-Tabelle angegeben wird. Andernfalls wird nach einem Verzeichnis gesucht, das von der IniLocator-Tabelle angegeben wird.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Dateiname
</dt> <dd>

Der .ini Dateiname.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Abschnitt
</dt> <dd>

Abschnittsname in der .ini-Datei.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Schlüssel
</dt> <dd>

Schlüsselwert innerhalb des Abschnitts.

</dd> <dt>

<span id="Field"></span><span id="field"></span><span id="FIELD"></span>Feld
</dt> <dd>

Das Feld in der .ini Zeile. Wenn Field NULL oder 0 ist, wird die gesamte Zeile gelesen. Dies muss eine nicht negative Zahl sein.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Typ
</dt> <dd>

Ein -Wert, der bestimmt, ob der .ini Wert ein Dateispeicherort, ein Verzeichnisspeicherort oder ein roher .ini Wert ist.

In der folgenden Tabelle sind gültige Werte aufgeführt. Falls nicht vorhanden, wird Type auf 1 festgelegt.



| Konstante                      | Hexadezimal | Decimal | BESCHREIBUNG           |
|-------------------------------|-------------|---------|-----------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Ein Verzeichnisspeicherort. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Ein Dateispeicherort.      |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | Ein unformatiertes .ini Wert.     |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.

Die Spalten dieser Tabelle sind im Allgemeinen nicht lokalisiert. Wenn ein Autor entscheidet, nach Produkten in mehreren Sprachen zu suchen, kann die Tabelle für jede Sprache einen separaten Eintrag enthalten.

Zugeordneter lokalisierter Text für die Statusanzeige oder Protokollierung wird in der [ActionText-Tabelle](actiontext-table.md)angegeben.

Weitere Informationen finden Sie unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungseinträgen oder .ini Dateieinträgen.](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



