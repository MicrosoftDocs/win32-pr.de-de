---
description: File hashingist mit Windows Installer verfügbar. Weitere Informationen finden Sie unter msigetflehash und in der Tabelle msigetfash. Die msiflehash-Tabelle kann nur mit Dateien ohne Versions Angabe verwendet werden.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Keine der Dateien weist eine Version mit Datei Hash Überprüfung auf.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528172"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a>Keine der Dateien weist eine Version mit Datei Hash Überprüfung auf.

File hashingist mit Windows Installer verfügbar. Weitere Informationen finden Sie unter [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) und in der [Tabelle msigetfash](msifilehash-table.md). Die msiflehash-Tabelle kann nur mit Dateien ohne Versions Angabe verwendet werden.

Wenn die Schlüsseldatei einer installierten Komponente (Copy-a) denselben Namen wie eine Datei hat, die bereits am Ziel Speicherort (Copy-B) installiert ist, vergleicht das Installationsprogramm die Versionsnummer, das Datum und die Sprache der beiden Dateien.

Wenn keine der Dateien über eine Versionsnummer verfügt, verwendet das Installationsprogramm die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die der Komponente angehören, ersetzt werden sollen. Da beim Installer nur die gesamten Komponenten installiert werden, werden alle Dateien der Komponente ersetzt, wenn die installierte Schlüsseldatei ersetzt wird.

Beachten Sie, dass dieses Diagramm die Standardregeln für die [Datei Versions](file-versioning-rules.md)Verwaltung veranschaulicht, die durch Festlegen der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft überschrieben werden können. Der Standardwert der Eigenschaft **REINSTALLMODE** ist "omus".

![Standardregeln für die Datei Versionsverwaltung, wenn Sie durch die rein Stall Mode-Eigenschaften Einstellung überschrieben werden](images/waiflow2b.png)

Weitere Informationen finden Sie in den Beispielen für die Standarddatei Versionsverwaltung beim [Ersetzen vorhandener Dateien](replacing-existing-files.md).

-   [Beide Dateien haben eine Version.](both-files-have-a-version.md)
-   [Keine der Dateien hat eine Version.](neither-file-has-a-version.md)
-   [Eine Datei hat eine Version.](one-file-has-a-version.md)

 

 



