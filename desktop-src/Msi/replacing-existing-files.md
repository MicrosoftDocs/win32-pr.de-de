---
description: Da unnötige Datei Kopien eine Installation verlangsamt, bestimmt der Windows Installer, ob die Schlüsseldatei der Komponente bereits installiert ist, bevor versucht wird, die Dateien einer beliebigen Komponente zu installieren.
ms.assetid: 8be734c7-4f16-4f54-93db-bb8efb1ea6da
title: Ersetzen vorhandener Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0b3908749e5496e4be9bf0ff68c7038a9ea6573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866072"
---
# <a name="replacing-existing-files"></a>Ersetzen vorhandener Dateien

Da unnötige Datei Kopien eine Installation verlangsamt, bestimmt der Windows Installer, ob die Schlüsseldatei der Komponente bereits installiert ist, bevor versucht wird, die Dateien einer beliebigen Komponente zu installieren. Wenn das Installationsprogramm eine Datei mit dem gleichen Namen wie die Schlüsseldatei der Komponente findet, die am Ziel Speicherort installiert ist, vergleicht Sie die Version, das Datum und die Sprache der beiden Schlüsseldateien und verwendet Datei Versions Regeln, um zu bestimmen, ob die vom Paket bereitgestellte Komponente installiert werden soll. Wenn das Installationsprogramm feststellt, dass es die Komponentenbasis auf der Schlüsseldatei ersetzen muss, verwendet es die Datei Versions Regeln für jede installierte Datei, um zu bestimmen, ob die Datei ersetzt werden soll.

Beachten Sie Folgendes: Wenn Sie ein Installationspaket mit Dateien mit Versions Angabe erstellen, muss die Versions Zeichenfolge in der Spalte Version der [Dateitabelle](file-table.md) immer mit der Version der im Paket enthaltenen Datei identisch sein.

Die Standardregeln für die Datei Versionsverwaltung können mithilfe der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft überschrieben oder geändert werden. Beim Installieren, erneuten Installieren oder Reparieren einer Datei verwendet das Installationsprogramm die von der Eigenschaft **REINSTALLMODE** angegebenen Regeln zur Datei Versionsverwaltung. Das folgende Beispiel zeigt, wie das Installationsprogramm die Standardregeln für die [Datei Versions](file-versioning-rules.md)Verwaltung anwendet. Der Standardwert der Eigenschaft **REINSTALLMODE** ist "omus".

Die folgenden Komponenten Schlüsseldateien werden auf dem System installiert, bevor die Komponente neu installiert wird.



| File                                    | Version  | Erstellungsdatum | Änderungsdatum | Sprache    |
|-----------------------------------------|----------|-------------|---------------|-------------|
| Mit der                                   | 1.0.0000 | 1/1/99      | 1/1/99        | DE         |
| FileB                                   | 2.0.0000 | 1/1/99      | 1/1/99        | DE         |
| Filec                                   | 1.0.0000 | 1/1/99      | 1/1/99        | DE         |
| Fassung                                   | 1.0.0000 | 1/1/99      | 1/2/99        | DE         |
| Mit der                                   | none     | 1/1/99      | 1/1/99        | none        |
| FILEF (geändert > erstellt)<br/> | none     | 1/1/99      | 1/2/99        | none        |
| Mit der                                   | 1.0.0000 | 1/1/99      | 1/1/99        | DE         |
| Fileh                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| Mit der                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN     |
| Filej                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, GER, ItN |



 

Die folgenden Komponenten Schlüsseldateien sind im Installer-Paket enthalten.



| File                               | Version  | Erstellungsdatum | Änderungsdatum | Sprache    |
|------------------------------------|----------|-------------|---------------|-------------|
| "Flea" (markiert)<br/>     | 1.0.0000 | 1/1/99      | 1/1/99        | DE         |
| FileB (frühere Version)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | DE         |
| Filec (spätere Version)<br/>   | 2.0.0000 | 1/1/99      | 1/1/99        | DE         |
| Abgelegt (spätere Version)<br/>   | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| "Fi" (markiert)<br/>     | none     | 1/1/99      | 1/1/99        | none        |
| FILEF (neue Datei)<br/>        | none     | 1/3/99      | 1/3/99        | none        |
| (Neue Sprache)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| Fileh (neue Sprache)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | ItN, eng, GER |
| Weitere Sprachen (weitere Sprachen)<br/>  | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| Filej (weniger Sprachen)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | Fisch         |



 

Die folgenden Komponenten Schlüsseldateien bleiben nach der erneuten Installation der Komponente im System erhalten. Der Status der Schlüsseldatei bestimmt den Status aller anderen Dateien in der Komponente.



| File                | Version  | Erstellungsdatum | Änderungsdatum | Sprache    |
|---------------------|----------|-------------|---------------|-------------|
| "Flea" (Original)    | 1.0.0000 | 1/1/99      | 1/1/99        | DE         |
| FileB (Original)    | 2.0.0000 | 1/1/99      | 1/1/99        | DE         |
| Filec (Ersetzung) | 2.0.0000 | 1/1/99      | 1/1/99        | DE         |
| Abgelegt (Ersetzung) | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| "Fi" (Ersetzung) | none     | 1/1/99      | 1/1/99        | none        |
| FILEF (Original)    | none     | 1/1/99      | 1/2/99        | none        |
| (Ersetzung) | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| Fileh (Ersetzung) | 1.0.0000 | 1/1/99      | 1/1/99        | ItN, eng, GER |
| (Ersetzung) | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| Filej (Original)    | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, GER, ItN |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CRC-Überprüfung während einer Installation](crc-checking-during-an-installation.md)
</dt> </dl>

 

 




