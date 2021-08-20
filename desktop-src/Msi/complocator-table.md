---
description: Die CompLocator-Tabelle enthält die Informationen, die zum Suchen einer Datei oder eines Verzeichnisses erforderlich sind, die die Konfigurationsdaten des Installationsprogramms verwendet.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: CompLocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6a51ad618521ff49b2a5b13f76fcfbae4207b5cdf4d77e76d3e128816bbb82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145079"
---
# <a name="complocator-table"></a>CompLocator-Tabelle

Die CompLocator-Tabelle enthält die Informationen, die zum Suchen einer Datei oder eines Verzeichnisses erforderlich sind, die die Konfigurationsdaten des Installationsprogramms verwendet.

Die Tabelle CompLocator enthält die folgenden Informationen.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Signatur\_ | [Identifier](identifier.md) | J   | N        |
| Componentid | [GUID](guid.md)             | N   | N        |
| Typ        | [Integer](integer.md)       | N   | J        |



 

## <a name="column-information"></a>Spalteninformationen

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatur\_
</dt> <dd>

Diese Spalte stellt eine eindeutige Dateisignatur dar und ist auch der externe Schlüssel in der [Signaturtabelle](signature-table.md). Wenn der Schlüssel in der Signaturtabelle nicht vorhanden ist, wird davon ausgegangen, dass ein Verzeichnis vorhanden ist, auf das von der CompLocator-Tabelle verwiesen wird.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>Componentid
</dt> <dd>

Die Komponenten-ID der Komponente, deren Schlüsselpfad für die Suche verwendet werden soll. Dies sollte die GUID einer Komponente sein, die im Feld ComponentId der [Komponententabelle angezeigt wird.](component-table.md) Dies kann die Komponenten-ID einer Komponente sein, die zu einem anderen auf dem Computer installierten Produkt gehört. Es sollte nicht die GUID einer veröffentlichten Komponente sein, die im Feld ComponentId der [PublishComponent-Tabelle angezeigt wird.](publishcomponent-table.md)

Um den Komponenten-ID-GUID-Wert für eine Datei zu finden, die von einem anderen Produkt installiert wurde, wechseln Sie zum Installationspaket des Produkts. Wechseln Sie zur [Dateitabelle,](file-table.md) und suchen Sie die Zeile, die den Dateibezeichner für die Datei enthält. Die Spalte \_ Komponente dieser Zeile enthält den Komponentenbezeichner für die Komponente, die die Datei steuert. Wechseln Sie zur [Tabelle Komponente,](component-table.md) und suchen Sie in der Spalte Komponente nach der Zeile, die diesen Komponentenbezeichner enthält. Die ComponentId -Spalte dieser Zeile enthält die Komponenten-ID-GUID.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Typ
</dt> <dd>

Ein boolescher Wert, der bestimmt, ob der Schlüsselpfad der Komponente ein Dateiname oder ein Verzeichnisspeicherort ist.

In der folgenden Tabelle sind gültige Werte aufgeführt. Wenn nicht vorhanden, wird Type auf 1 (eins) festgelegt.



| Konstante                      | Hexadezimal | Decimal | Beschreibung              |
|-------------------------------|-------------|---------|--------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Der Schlüsselpfad ist ein Verzeichnis. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Der Schlüsselpfad ist ein Dateiname. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Tabelle wird mit der [AppSearch-Tabelle verwendet.](appsearch-table.md)

In der Regel werden die Spalten in dieser Tabelle nicht lokalisiert. Wenn ein Autor beschließt, nach Produkten in mehreren Sprachen zu suchen, kann in der Tabelle für jede Sprache ein separater Eintrag enthalten sein.

Weitere Informationen finden Sie unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungseinträgen oder .ini Dateieinträgen.](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



