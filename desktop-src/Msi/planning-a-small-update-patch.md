---
description: Die Konzert Funktions Datei des ursprünglichen Produkts, MNP2000, enthält einen Fehler in der Concert.txt-Datei.
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: Planen eines kleinen Update Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15f3667c6a18ab7a71e86997091bd76d4b15577
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869632"
---
# <a name="planning-a-small-update-patch"></a>Planen eines kleinen Update Patches

Die Konzert Funktions Datei des ursprünglichen Produkts, MNP2000, enthält einen Fehler in der Concert.txt-Datei. Da Windows Installer für die Installation und Einrichtung der Anwendung verwendet wurde, können kleinere Korrekturen an der Anwendung verarbeitet werden, indem ein kleines Update Patchpaket installiert wird. Bei einem [kleinen Update](small-updates.md) werden mindestens eine Anwendungsdatei geändert, die zu gering ist, um den Produktcode zu ändern. Im folgenden Beispiel wird gezeigt, wie ein Windows Installer Patch-Paket erstellt wird, das das kleine Update anwenden und eine schnelle Korrektur für das MNP2000-Produkt bereitstellen kann.

Um das kleine Update zu erstellen, rufen Sie zunächst ein vollständig unkomprimiertes Image des MNP2000-Produkts ab, das den Fehler in Concert.txt enthält. Das Image muss MNP2000.msi und alle Quelldateien enthalten, die unter [Planen der Installation](planning-the-installation.md)beschrieben werden. In der folgenden Erörterung wird dies als Zielbild bezeichnet. Das Zielbild muss vollständig unkomprimiert sein, da der patcherstellungs Prozess keine binären Patches für Dateien generieren kann, die in den Schränken komprimiert sind. Platzieren Sie die MSI-Datei und alle Quelldateien des zielbilds in einem Ordner mit dem Namen Target.

Rufen Sie als nächstes ein vollständig unkomprimiertes Image des MNP2000-Produkts mit einer Concert.txt Datei ab, die korrigiert ist. Dies wird in der folgenden Erörterung als aktualisiertes Image bezeichnet. Verwenden Sie zum Aktualisieren der MSI-Datei ein Tool zum Bearbeiten von Installations Datenbanken, z. b. Orca. Wenn beispielsweise die Größe des korrigierten Concert.txt kleiner als der ursprüngliche ist, stellen Sie sicher, dass Sie die neue Größe im Feld Filesize der Dateitabelle des aktualisierten Images eingeben. Beachten Sie, dass Sie, da das Paket geändert wurde, einen neuen Paketcode in der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " zuweisen müssen. Platzieren Sie die MSI-Datei und alle Quelldateien des aktualisierten Images in einem Ordner mit dem Namen "aktualisiert".

Bei diesem Beispiel wird davon ausgegangen, dass sich die Größe der Concert.txt Datei ändert. Dies bedeutet, dass die Filesize-Felder in den Datei Tabellen der Zieldatenbank und der aktualisierten Datenbank unterschiedliche Daten enthalten.

In der folgenden [Dateitabelle](file-table.md) ist der Datensatz aus dem Zielimage angegeben.



| File        | Komponente\_ | FileName    | FileSize | Version | Sprache | Attribute | Sequenz |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Konzert     | Concert.txt | 1000     |         |          | 0          | 1        |



 

Die folgende Dateitabelle identifiziert den Datensatz aus dem aktualisierten Image.



| File        | Komponente\_ | FileName    | FileSize | Version | Sprache | Attribute | Sequenz |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Konzert     | Concert.txt | 900      |         |          | 0          | 1        |



 

> [!Note]
> Die Datei muss den gleichen Schlüssel in den [Datei Tabellen](file-table.md) sowohl für das Ziel Image als auch für das aktualisierte Image aufweisen. Die Zeichen folgen Werte in der Datei Spalte beider Tabellen müssen identisch sein. Groß-und Kleinbuchstaben müssen ebenfalls identisch sein.
> 
> Befolgen Sie die unter [Erstellen eines Patchpakets](creating-a-patch-package.md)beschriebenen Richtlinien. Erstellen Sie kein Paket mit [Datei Tabellen](file-table.md) Schlüsseln, die sich nur in der Groß-/Kleinschreibung unterscheiden, da [Msimsp.exe](msimsp-exe.md) und [Patchwiz.dll](patchwiz-dll.md) Makecab.exe anrufen, bei dem die Groß-und Kleinschreibung nicht beachtet wird.

[Fortsetzen](creating-a-patch-creation-properties-file.md)

 

 



