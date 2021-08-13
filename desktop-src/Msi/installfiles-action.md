---
description: Die Aktion InstallFiles kopiert die in der Tabelle Datei angegebenen Dateien aus dem Quellverzeichnis in das Zielverzeichnis.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: InstallFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df2a62deb253314e84e72cd84e88052f1175db7451807c3f266542e29c10c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629931"
---
# <a name="installfiles-action"></a>InstallFiles-Aktion

Die Aktion InstallFiles kopiert die in der Tabelle Datei angegebenen Dateien aus dem Quellverzeichnis in das Zielverzeichnis.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die InstallFiles-Aktion muss nach der [InstallValidate-Aktion](installvalidate-action.md) und vor dateiabhängigen Aktionen durchgeführt werden.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                      |
|-------|-------------------------------------------------|
| \[1\] | Bezeichner der installierten Datei.                   |
| \[6\] | Größe der installierten Datei in Bytes.                |
| \[9\] | Bezeichner des Verzeichnisses, das die installierte Datei enthält. |



 

## <a name="remarks"></a>Hinweise

Die Aktion InstallFiles wird für Dateien verwendet, die in der [Dateitabelle angegeben sind.](file-table.md) Jede Datei wird basierend auf dem Installationsstatus der zugeordneten Komponente der Datei in der [Component-Tabelle installiert.](component-table.md) Nur die Dateien, deren Komponenten in den **MsiInstallStatelocal-Zustand** aufgelöst werden, sind zum Kopieren berechtigt.

Die InstallFiles-Aktion implementiert die folgenden Spalten der File-Tabelle.

-   Die Spalte FileName gibt den Namen der Zieldatei an.
-   Die Spalte Version gibt die Dateiversion an.
-   Die Spalte Attribute gibt die Datei- und Installationsattribut-Flagbits an.
-   Die Spalte Datei gibt das eindeutige Dateitoken an.
-   Die FileSize -Spalte gibt die unkomprimierte Dateigröße in Bytes an.
-   Die Spalte Sprache gibt den Bezeichner der Dateisprache an.
-   Die Sequenzspalte gibt die Sequenznummer auf dem Medium an.

Die InstallFiles-Aktion implementiert die folgenden Spalten der Component-Tabelle.

-   Die Spalte \_ Verzeichnis gibt einen Verweis auf ein [Verzeichnistabellenelement](directory-table.md) an.
-   Die Spalte Komponente gibt einen eindeutigen Namen für das Komponentenelement an.

Die angegebene Datei wird nur kopiert, wenn eine der folgenden Bedingungen zutrifft:

-   Die Datei ist derzeit nicht auf dem lokalen Computer installiert.
-   Die Datei befindet sich auf dem lokalen Computer, hat jedoch eine niedrigere Versionsnummer als die Datei in der [Dateitabelle](file-table.md).
-   Die Datei befindet sich auf dem lokalen Computer, aber es gibt keine zugeordnete Versionsnummer.

Das Quellverzeichnis für jede zu kopierende Datei wird durch den sourceMode bestimmt, der wiederum vom Wert in der Spalte "Cabinet" der Media-Tabelle abhängt. Eine vollständige Erörterung des Quellmodus finden Sie in der [Media-Tabelle](media-table.md).

Wenn sich das Quellverzeichnis für eine zu kopierende Datei auf Wechselmedien wie z. B. einer Diskette oder CD-ROM befindet, überprüft die InstallFiles-Aktion, ob das richtige Quellmedium eingefügt wird, bevor versucht wird, die Datei zu kopieren. InstallFiles sucht nach Medien desselben Wechseldatenträgertyps mit einer Volumebezeichnung, die mit dem in der Spalte VolumeLabel der Media-Tabelle angegebenen Wert identisch ist. [](v-gly.md) Wenn ein entsprechendes bereitgestelltes Volume gefunden wird, wird der Dateikopiervorgang fortgesetzt. Wenn keine Übereinstimmung gefunden wird, fordert ein Dialogfeld den Benutzer auf, die richtigen Medien einfügungen. In diesem Fall verwendet das Dialogfeld den Mediennamen in der DiskPrompt-Spalte der Media-Tabelle als Teil der Eingabeaufforderung.

Es muss Vorsicht geboten werden, da die Aktion InstallFiles eine ursprüngliche Datei löschen und nicht ersetzen kann. Dies tritt auf, wenn bei der Aktion InstallFiles beim Ersetzen einer älteren Datei ein Fehler auftritt und der Benutzer den Fehler ignoriert. Das Standardverhalten des Installationsprogramms besteht im Löschen einer alten Datei, bevor sichergestellt wird, dass die neue Datei ordnungsgemäß kopiert wird.

Die vom Installationsprogramm verwendeten Regeln für die Dateiversionsversion finden Sie unter [Regeln für die Dateiversionsversion.](file-versioning-rules.md)

 

 



