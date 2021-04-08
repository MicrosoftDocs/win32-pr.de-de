---
description: Wenn beide Dateien eine Versionsnummer aufweisen, verwendet die Windows Installer die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die der Komponente angehören, ersetzt werden sollen.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Beide Dateien haben eine Version.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864428"
---
# <a name="both-files-have-a-version"></a>Beide Dateien haben eine Version.

Wenn die Schlüsseldatei einer Komponente, die installiert wird (Copy-a) denselben Namen wie eine Datei hat, die bereits am Ziel Speicherort (Copy-B) installiert ist, vergleicht das Installationsprogramm die Versionsnummer und die Sprache der beiden Dateien.

Wenn beide Dateien eine Versionsnummer aufweisen, verwendet das Installationsprogramm die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die der Komponente angehören, ersetzt werden sollen. Da beim Installer nur die gesamten Komponenten installiert werden, werden alle Dateien der Komponente ersetzt, wenn die installierte Schlüsseldatei ersetzt wird.

Beachten Sie, dass dieses Diagramm die Standardregeln für die [Datei Versions](file-versioning-rules.md)Verwaltung veranschaulicht, die durch Festlegen der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft überschrieben werden können. Der Standardwert der Eigenschaft **REINSTALLMODE** ist "omus".

![Standardregeln für die Datei Versionsverwaltung, wenn beide Dateien denselben Namen oder dieselbe Versionsnummer aufweisen](images/waiflow1.png)

Das vorherige Diagramm kann auch mit Dateien verwendet werden, für die keine Sprache angegeben wurde. Wenn Copy-A eine angegebene Sprache hat und für Copy-b keine Sprache angegeben ist, wird Copy-b durch Copy-a ersetzt. Wenn für Copy-A und copy-b keine Sprache angegeben ist, wird Copy-b nicht ersetzt.

Weitere Informationen finden Sie unter Beispiele für die Standarddatei Versionsverwaltung beim [Ersetzen vorhandener Dateien](replacing-existing-files.md).

-   [Keine der Dateien hat eine Version.](neither-file-has-a-version.md)
-   [Keine der Dateien weist eine Version mit Datei Hash Überprüfung auf.](neither-file-has-a-version-with-file-hash-check.md)
-   [Eine Datei hat eine Version.](one-file-has-a-version.md)

 

 



