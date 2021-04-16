---
description: Die complocator-Tabelle enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis zu finden, das die installerkonfigurationsdaten verwendet.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Complocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530239"
---
# <a name="complocator-table"></a>Complocator-Tabelle

Die complocator-Tabelle enthält die Informationen, die erforderlich sind, um eine Datei oder ein Verzeichnis zu finden, das die installerkonfigurationsdaten verwendet.

Die complocator-Tabelle enthält die folgenden Informationen.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Signatur\_ | [Bezeichner](identifier.md) | J   | N        |
| ComponentID | [GUID](guid.md)             | N   | N        |
| type        | [Integer](integer.md)       | N   | J        |



 

## <a name="column-information"></a>Spalten Informationen

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_
</dt> <dd>

Diese Spalte stellt eine eindeutige Datei Signatur dar und ist auch der externe Schlüssel in der [Signatur Tabelle](signature-table.md). Wenn der Schlüssel in der Signatur Tabelle nicht vorhanden ist, wird davon ausgegangen, dass es sich bei der Suche um das vorhanden sein eines Verzeichnisses handelt, auf das von der complocator-Tabelle verwiesen wird.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentID
</dt> <dd>

Die Komponenten-ID der Komponente, deren Schlüssel Pfad für die Suche verwendet werden soll. Dies sollte die GUID einer Komponente sein, die im Feld "ComponentId" der [Komponenten Tabelle](component-table.md)angezeigt wird. Dies kann die Komponenten-ID einer Komponente sein, die zu einem anderen Produkt gehört, das auf dem Computer installiert ist. Dies sollte nicht der GUID einer veröffentlichten Komponente sein, die im Feld "ComponentId" der [Tabelle "PublishComponent](publishcomponent-table.md)" angezeigt wird.

Wechseln Sie zum Installationspaket des Produkts, um den GUID-Wert der Komponenten-ID für eine Datei zu ermitteln, die von einem anderen Produkt installiert wurde. Wechseln Sie zur [Dateitabelle](file-table.md) , und suchen Sie die Zeile, die den Datei Bezeichner für die Datei enthält. Die Komponenten \_ Spalte dieser Zeile enthält den Komponenten Bezeichner für die Komponente, mit der die Datei gesteuert wird. Wechseln Sie zur [Komponenten Tabelle](component-table.md) , und suchen Sie die Zeile, die diesen Komponenten Bezeichner enthält, in der Spalte Komponente. Die Spalte ComponentID dieser Zeile enthält die Komponenten-ID-GUID.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte
</dt> <dd>

Ein boolescher Wert, der bestimmt, ob der Schlüssel Pfad der Komponente ein Dateiname oder ein Verzeichnis Speicherort ist.

In der folgenden Tabelle sind gültige Werte aufgeführt. Wenn nicht vorhanden, wird Type auf 1 (eins) festgelegt.



| Konstante                      | Hexadezimal | Decimal | BESCHREIBUNG              |
|-------------------------------|-------------|---------|--------------------------|
| **msidbloprojekttypedirectory** | 0x000       | 0       | Der Schlüssel Pfad ist ein Verzeichnis. |
| **msidblo-typefilename**  | 0x001       | 1       | Der Schlüssel Pfad ist ein Dateiname. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird mit der [AppSearch-Tabelle](appsearch-table.md)verwendet.

In der Regel werden die Spalten in dieser Tabelle nicht lokalisiert. Wenn ein Autor eine Suche nach Produkten in mehreren Sprachen beschließt, kann in der Tabelle für jede Sprache ein separater Eintrag enthalten sein.

Weitere Informationen finden Sie unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



