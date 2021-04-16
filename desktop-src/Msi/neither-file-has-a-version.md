---
description: Wenn keine der Dateien über eine Versionsnummer verfügt, wird in der Windows Installer die im folgenden Flussdiagramm veranschaulichte Logik verwendet, um zu bestimmen, ob alle installierten Dateien, die der Komponente angehören, ersetzt werden sollen.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Keine der Dateien hat eine Version.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5360bb7b6b4deda54156006073f353ab65ab2b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553661"
---
# <a name="neither-file-has-a-version"></a>Keine der Dateien hat eine Version.

Wenn die Schlüsseldatei einer installierten Komponente (Copy-a) denselben Namen wie eine Datei hat, die bereits am Ziel Speicherort (Copy-B) installiert ist, vergleicht das Installationsprogramm die Versionsnummer, das Datum und die Sprache der beiden Dateien.

Wenn keine der Dateien über eine Versionsnummer verfügt, verwendet das Installationsprogramm die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die der Komponente angehören, ersetzt werden sollen. Da beim Installer nur die gesamten Komponenten installiert werden, werden alle Dateien der Komponente ersetzt, wenn die installierte Schlüsseldatei ersetzt wird.

Beachten Sie, dass dieses Diagramm die Standardregeln für die [Datei Versions](file-versioning-rules.md)Verwaltung veranschaulicht, die durch Festlegen der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft überschrieben werden können. Der Standardwert der Eigenschaft **REINSTALLMODE** ist "omus".

![Standardregeln für die Datei Versionsverwaltung, wenn keine der Dateien eine Versionsnummer aufweist](images/waiflow2.png)

Weitere Informationen finden Sie in den Beispielen für die Standarddatei Versionsverwaltung beim [Ersetzen vorhandener Dateien](replacing-existing-files.md).

-   [Beide Dateien haben eine Version.](both-files-have-a-version.md)
-   [Keine der Dateien weist eine Version mit Datei Hash Überprüfung auf.](neither-file-has-a-version-with-file-hash-check.md)
-   [Eine Datei hat eine Version.](one-file-has-a-version.md)

 

 



