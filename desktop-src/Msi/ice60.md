---
description: ICE60 überprüft die Dateitabelle einer Windows Installer Datenbank.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349530"
---
# <a name="ice60"></a>ICE60

ICE60 prüft, ob die Dateien in der [Dateitabelle](file-table.md) die folgende Bedingung erfüllen:

-   Wenn es sich bei der Datei nicht um eine Schriftart handelt, die über eine Version verfügt, muss Sie über eine Sprache verfügen.
-   ICE60 prüft, ob in der [Tabelle "msiflehash](msifilehash-table.md)" keine Dateien mit Versions Angabe aufgeführt sind.

Wenn eine Warnung, die von ICE60 gemeldet wird, nicht behoben werden kann, führt dies im Allgemeinen dazu, dass eine Datei bei einer Produkt Reparatur unnötig neu installiert wird. Dies liegt daran, dass die Datei, die bei der Reparatur installiert werden soll, und die vorhandene Datei auf dem Datenträger die gleiche Version (dieselbe Datei), aber unterschiedliche Sprachen aufweisen. In der Dateitabelle wird die Sprache als NULL aufgelistet, aber die Datei selbst hat einen sprach Wert in der Ressource. Basierend auf den [Regeln für die Datei Versions](file-versioning-rules.md)Verwaltung bevorzugt das Installationsprogramm die zu installierende Datei, sodass Sie unnötig neu kopiert wird.

## <a name="result"></a>Ergebnis

ICE60 gibt eine Warnung oder einen Fehler aus, wenn eine Datei in der [Dateitabelle](file-table.md) , die keine Schriftart ist und eine Version aufweist, nicht über eine Sprache verfügt.

ICE60 gibt den folgenden Fehler aus, wenn eine in der Tabelle "msiflehash" aufgeführte Datei mit Versions Angabe versehen ist.

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a>Beispiel

ICE60 meldet den folgenden Fehler und die Warnung für das gezeigte Beispiel. (Datei B ist eine Schriftart, die anderen Dateien nicht.)

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

Die-Flea hat sowohl eine Version als auch eine Sprache. Daher wird keine Warnung oder kein Fehler generiert.

FileB hat eine Version, aber keine Sprache. Es wird jedoch weder eine Warnung noch ein Fehler generiert, da es sich um eine Schriftart handelt.

Filec ist eine begleitende Referenz, daher muss keine Sprache vorhanden sein. Es wird keine Warnung oder kein Fehler generiert.

Das Profil hat keine Version, daher muss es nicht über eine Sprache verfügen. Es wird keine Warnung oder kein Fehler generiert.

"Flee" hat eine Version, aber keine Sprache. Daher wird eine Warnung generiert.

Um diese Warnung zu beheben, fügen Sie eine Sprache zu "flee" hinzu.

Dateien sollten nach Möglichkeit in der Versions Ressource gespeichert werden. Wenn eine Datei sprachneutral ist, verwenden Sie die [LangID](column-data-types.md) 0.

[File Table](file-table.md) (fileB ist eine Schriftart, die anderen Dateien nicht.)



| File  | Version | Sprache |
|-------|---------|----------|
| Mit der | 1.0     | 1033     |
| FileB | 1.0     |          |
| Filec | Mit der   |          |
| Fassung |         |          |
| Mit der | 1.0     |          |



 

[Schriftart Tabelle](font-table.md)



| File  | FontTitle  |
|-------|------------|
| FileB | Schriftart Titel |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



