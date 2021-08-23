---
description: Die Concert-Featuredatei des ursprünglichen Produkts, MNP2000, enthält einen Fehler in der Concert.txt Datei.
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: Planen eines kleinen Updatepatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aed6c947ee278e7c4856281790a9c392af38734c475e3d40561d72d805f6011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519540"
---
# <a name="planning-a-small-update-patch"></a>Planen eines kleinen Updatepatches

Die Concert-Featuredatei des ursprünglichen Produkts, MNP2000, enthält einen Fehler in der Concert.txt Datei. Da Windows Installer für die Installation und Einrichtung der Anwendung verwendet wurde, können kleinere Korrekturen an der Anwendung durch die Installation eines kleinen Updatepatchpakets behandelt werden. Bei [einem kleinen Update](small-updates.md) werden Änderungen an mindestens einer Anwendungsdateien vorgenommen, die zu klein sind, um den Produktcode zu ändern. Im folgenden Beispiel wird gezeigt, wie Sie ein Windows Installer-Patchpaket erstellen, das das kleine Update anwenden und eine schnelle Korrektur für das MNP2000-Produkt bereitstellen kann.

Um das kleine Update zu erstellen, erhalten Sie zunächst ein vollständig unkomprimiertes Image des MNP2000-Produkts, das den Fehler in Concert.txt. Das Image muss MNP2000.msi und alle Quelldateien enthalten, die unter [Planning the Installation (Planen der Installation) beschrieben werden.](planning-the-installation.md) In der folgenden Diskussion wird dies als Zielimage bezeichnet. Das Zielimage muss vollständig dekomprimiert sein, da der Patcherstellungsprozess keine binären Patches für Dateien generieren kann, die in Schränken komprimiert sind. Speichern Sie .msi-Datei und alle Quelldateien des Zielimages in einem Ordner namens Target.

Als Nächstes erhalten Sie ein vollständig unkomprimiertes Image des Produkts MNP2000 mit einer Concert.txt datei, die korrigiert ist. Dies wird in der folgenden Diskussion als Aktualisiertes Image bezeichnet. Verwenden Sie ein Bearbeitungstool für die Installationsdatenbank, z. B. Orca, um die .msi aktualisieren. Wenn z. B. die größe der korrigierten Concert.txt kleiner als die ursprüngliche ist, stellen Sie sicher, dass Sie die neue Größe in das Feld FileSize der Tabelle Datei des aktualisierten Images eingeben. Beachten Sie, dass Sie, da das Paket geändert wurde, einen neuen Paketcode in der [**Eigenschaft Zusammenfassung der Revisionsnummer zuweisen**](revision-number-summary.md) müssen. Speichern Sie .msi-Datei und alle Quelldateien des Aktualisierten Images in einem Ordner mit dem Namen Upgraded.

Gehen Sie für dieses Beispiel davon aus, dass sich die Größe der Concert.txt ändert. Dies bedeutet, dass FileSize-Felder in den Dateitabellen der Ziel- und Der aktualisierten Datenbank unterschiedliche Daten enthalten.

Die folgende [Dateitabelle](file-table.md) identifiziert den Datensatz aus dem Zielimage.



| Datei        | Komponente\_ | FileName    | FileSize | Version | Sprache | Attribute | Sequenz |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Konzert     | Concert.txt | 1000     |         |          | 0          | 1        |



 

Die folgende Dateitabelle identifiziert den Datensatz aus dem aktualisierten Image.



| Datei        | Komponente\_ | FileName    | FileSize | Version | Sprache | Attribute | Sequenz |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Konzert     | Concert.txt | 900      |         |          | 0          | 1        |



 

> [!Note]
> Die Datei muss in den [](file-table.md) Dateitabellen des Zielimages und des aktualisierten Images denselben Schlüssel enthalten. Die Zeichenfolgenwerte in der File -Spalte beider Tabellen müssen identisch sein. Groß- und Kleinbuchstaben müssen ebenfalls identisch sein.
> 
> Befolgen Sie die Unter [Erstellen eines Patchpakets beschriebenen Richtlinien.](creating-a-patch-package.md) Erstellen Sie kein [](file-table.md) Paket mit Dateitabellenschlüsseln, die sich nur nach Groß-/Kleinschreibung unterscheiden, da [Msimsp.exe](msimsp-exe.md) und [Patchwiz.dll](patchwiz-dll.md) Makecab.exe aufrufen. Dabei wird die Groß-/Kleinschreibung nicht beachtet, und die Patchgenerierung schlägt fehl.

[Fortsetzen](creating-a-patch-creation-properties-file.md)

 

 



