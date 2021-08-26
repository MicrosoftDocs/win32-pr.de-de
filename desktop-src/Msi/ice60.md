---
description: ICE60 überprüft die Dateitabelle einer Windows Installer-Datenbank.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce8d2cbf9136ea6195a138c586d4408dc0d2e5ff411b52fd73fec8a569c5d186
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044030"
---
# <a name="ice60"></a>ICE60

ICE60 überprüft, ob dateien in der [Dateitabelle](file-table.md) die folgende Bedingung erfüllen:

-   Wenn die Datei keine Schriftart ist und über eine Version verfügt, muss sie über eine Sprache verfügen.
-   ICE60 überprüft, ob keine Dateien mit Versionsversion in der [MsiFileHash-Tabelle](msifilehash-table.md)aufgeführt sind.

Wenn eine von ICE60 gemeldete Warnung nicht behoben wird, führt dies in der Regel dazu, dass eine Datei unnötigerweise neu installiert wird, wenn eine Produktreparatur abgeschlossen ist. Dies liegt daran, dass die Datei, die in der Reparatur installiert werden soll, und die vorhandene Datei auf dem Datenträger die gleiche Version (sie sind die gleiche Datei), aber unterschiedliche Sprachen aufweisen. Die Dateitabelle listet die Sprache als NULL auf, aber die Datei selbst weist einen Sprachwert in der Ressource auf. Basierend auf den Regeln für die [Dateiversionsierung](file-versioning-rules.md)bevorzugt das Installationsprogramm die Installation der Datei, sodass sie unnötigerweise erneut kopiert wird.

## <a name="result"></a>Ergebnis

ICE60 gibt eine Warnung oder einen Fehler aus, wenn eine Datei in der [Dateitabelle,](file-table.md) die keine Schriftart ist und eine Version aufweist, keine Sprache aufweist.

ICE60 gibt den folgenden Fehler aus, wenn eine in der MsiFileHash-Tabelle aufgeführte Datei versioniert ist.

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a>Beispiel

ICE60 meldet den folgenden Fehler und die folgende Warnung für das gezeigte Beispiel. (Datei B ist eine Schriftart, die anderen Dateien nicht.)

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

FileA verfügt sowohl über eine Version als auch über eine Sprache. daher wird keine Warnung oder kein Fehler generiert.

FileB verfügt über eine Version, aber keine Sprache. Es wird jedoch keine Warnung oder kein Fehler generiert, da es sich um eine Schriftart handelt.

FileC ist ein begleiter Verweis, sodass er keine Sprache aufweisen muss. Es wird keine Warnung oder kein Fehler generiert.

FileD verfügt über keine Version, sodass keine Sprache benötigt wird. Es wird keine Warnung oder kein Fehler generiert.

FileE verfügt über eine Version, aber keine Sprache. Daher wird eine Warnung generiert.

Um diese Warnung zu beheben, fügen Sie FileE eine Sprache hinzu.

Dateien sollten nach Möglichkeit sprachwerte in der Versionsressource gespeichert haben. Wenn eine Datei sprachneutral ist, verwenden Sie [langid](column-data-types.md) 0.

[Dateitabelle](file-table.md) (FileB ist eine Schriftart, die anderen Dateien nicht.)



| Datei  | Version | Sprache |
|-------|---------|----------|
| Filea | 1.0     | 1033     |
| Fileb | 1.0     |          |
| FileC | Filea   |          |
| Abgelegt |         |          |
| FileE | 1.0     |          |



 

[Schriftarttabelle](font-table.md)



| Datei  | FontTitle  |
|-------|------------|
| Fileb | Schriftarttitel |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



