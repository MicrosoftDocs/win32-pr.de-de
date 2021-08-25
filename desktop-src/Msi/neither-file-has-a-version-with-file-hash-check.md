---
description: Dateihashing ist mit dem Windows verfügbar. Weitere Informationen finden Sie unter MsiGetFileHash und die Tabelle MsiFileHash. Die MsiFileHash-Tabelle kann nur mit Nichtversionsdateien verwendet werden.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Keine der Dateien verfügt über eine Version mit Dateihashüberprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb874cdc29c56f34be2d4ec8604c2436892744e44581258ec237f515600f9024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869195"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a>Keine der Dateien verfügt über eine Version mit Dateihashüberprüfung

Dateihashing ist mit dem Windows verfügbar. Weitere Informationen finden Sie unter [**MsiGetFileHash und**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) in der [MsiFileHash-Tabelle.](msifilehash-table.md) Die MsiFileHash-Tabelle kann nur mit Nichtversionsdateien verwendet werden.

Wenn die Schlüsseldatei einer komponente, die installiert wird (copy-A), den gleichen Namen hat wie eine Datei, die bereits am Zielspeicherort installiert ist (copy-B), vergleicht das Installationsprogramm Versionsnummer, Datum und Sprache der beiden Dateien.

Wenn keine datei über eine Versionsnummer verfügt, verwendet das Installationsprogramm die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die zur Komponente gehören, ersetzt werden. Da das Installationsprogramm nur ganze Komponenten installiert, werden alle Komponentendateien ersetzt, wenn die installierte Schlüsseldatei ersetzt wird.

Beachten Sie, dass dieses Diagramm die Standardregeln für die [Dateiversionsversion](file-versioning-rules.md)veranschaulicht, die durch Festlegen der [**REINSTALLMODE-Eigenschaft überschrieben werden**](reinstallmode.md) können. Der Standardwert der **REINSTALLMODE-Eigenschaft** ist "omus".

![Standardregeln für die Dateiversionsversion beim Überschreiben durch die Eigenschafteneinstellung "reinstallmode"](images/waiflow2b.png)

Weitere Informationen finden Sie in den Beispielen für die Standarddateiversionsvererbung unter [Ersetzen vorhandener Dateien.](replacing-existing-files.md)

-   [Beide Dateien verfügen über eine Version](both-files-have-a-version.md)
-   [Keine der Dateien verfügt über eine Version](neither-file-has-a-version.md)
-   [Eine Datei verfügt über eine Version](one-file-has-a-version.md)

 

 



