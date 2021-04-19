---
description: Die Tabelle "inilocator" enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis mithilfe einer INI-Datei zu suchen oder nach einem bestimmten INI-Eintrag zu suchen. Die INI-Datei muss im Microsoft Windows-Standardverzeichnis vorhanden sein.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Inilocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358840"
---
# <a name="inilocator-table"></a>Inilocator-Tabelle

Die Tabelle "inilocator" enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis mithilfe einer INI-Datei zu suchen oder nach einem bestimmten INI-Eintrag zu suchen. Die INI-Datei muss im Microsoft Windows-Standardverzeichnis vorhanden sein.

Die inilocator-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Signatur\_ | [Bezeichner](identifier.md) | J   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| `Section`     | [Text](text.md)             | N   | N        |
| Schlüssel         | [Text](text.md)             | N   | N        |
| Feld       | [Integer](integer.md)       | N   | J        |
| Typ        | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_
</dt> <dd>

Ein externer Schlüssel in die erste Spalte der [Signatur Tabelle](signature-table.md). Die Signatur \_ stellt eine eindeutige Signatur dar und ist auch der externe Schlüssel in Spalte 1 der Signatur Tabelle. Wenn diese Signatur in der Signatur Tabelle vorhanden ist, wird die Suche nach einer Datei durchsucht. Wenn dieser Schlüssel in der Signatur Tabelle nicht vorhanden ist und der Wert der Type-Spalte **msidblocatortyperawvalue** ist, wird die Suche nach dem von der Tabelle inilocator angegebenen INI-Eintrag durchsucht. Andernfalls ist die Suche nach einem Verzeichnis, das von der Tabelle "inilocator" angegeben wird.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Einfügen
</dt> <dd>

Der Name der INI-Datei.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Sektions
</dt> <dd>

Der Abschnitts Name innerhalb der INI-Datei.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen
</dt> <dd>

Der Schlüsselwert innerhalb des Abschnitts.

</dd> <dt>

<span id="Field"></span><span id="field"></span><span id="FIELD"></span>Flächen
</dt> <dd>

Das Feld in der. ini-Zeile. Wenn Field NULL oder 0 ist, wird die gesamte Zeile gelesen. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte
</dt> <dd>

Ein Wert, der bestimmt, ob der INI-Wert ein Datei Speicherort, ein Verzeichnis Speicherort oder ein RAW. ini-Wert ist.

In der folgenden Tabelle sind gültige Werte aufgeführt. Wenn nicht vorhanden, wird Type auf 1 festgelegt.



| Konstante                      | Hexadezimal | Decimal | BESCHREIBUNG           |
|-------------------------------|-------------|---------|-----------------------|
| **msidbloprojekttypedirectory** | 0x000       | 0       | Ein Verzeichnis Speicherort. |
| **msidblo-typefilename**  | 0x001       | 1       | Ein Datei Speicherort.      |
| **msidbloserortyperawvalue**  | 0x002       | 2       | Ein "RAW. ini"-Wert.     |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.

Die Spalten dieser Tabelle sind im Allgemeinen nicht lokalisiert. Wenn ein Autor eine Suche nach Produkten in mehreren Sprachen beschließt, kann in der Tabelle für jede Sprache ein separater Eintrag enthalten sein.

Der zugeordnete lokalisierte Text für die Statusanzeige oder Protokollierung wird in der [Tabelle "aktiontext](actiontext-table.md)" angegeben.

Weitere Informationen finden Sie [untersuchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



