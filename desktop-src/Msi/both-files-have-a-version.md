---
description: Wenn beide Dateien eine Versionsnummer haben, verwendet der Windows Installer die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die zur Komponente gehören, ersetzt werden.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Beide Dateien verfügen über eine Version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1338a93b4a45094a9a5951c3c59def15affde96dbbe74f3b134ba9dd7532092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380812"
---
# <a name="both-files-have-a-version"></a>Beide Dateien verfügen über eine Version

Wenn die Schlüsseldatei einer komponente, die installiert wird (copy-A), den gleichen Namen hat wie eine Datei, die bereits am Zielspeicherort installiert ist (copy-B), vergleicht das Installationsprogramm die Versionsnummer und Sprache der beiden Dateien.

Wenn beide Dateien eine Versionsnummer haben, verwendet das Installationsprogramm die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die zur Komponente gehören, ersetzt werden. Da das Installationsprogramm nur ganze Komponenten installiert, werden alle Komponentendateien ersetzt, wenn die installierte Schlüsseldatei ersetzt wird.

Beachten Sie, dass dieses Diagramm die Standardregeln für die [Dateiversionsversion](file-versioning-rules.md)veranschaulicht, die durch Festlegen der [**REINSTALLMODE-Eigenschaft überschrieben werden**](reinstallmode.md) können. Der Standardwert der **REINSTALLMODE-Eigenschaft** ist "omus".

![Standardregeln für die Dateiversionsversion, wenn beide Dateien denselben Namen oder dieselbe Versionsnummer haben](images/waiflow1.png)

Das vorherige Diagramm kann auch mit Dateien ohne angegebene Sprache verwendet werden. Wenn copy-A über eine angegebene Sprache verfügt und copy-B keine angegebene Sprache hat, wird copy-B durch copy-A ersetzt. Wenn für copy-A und copy-B keine Sprache angegeben ist, wird copy-B nicht ersetzt.

Beispiele für die Standarddateiversionsierung finden Sie unter [Ersetzen vorhandener Dateien.](replacing-existing-files.md)

-   [Keine der Dateien verfügt über eine Version](neither-file-has-a-version.md)
-   [Keine der Dateien verfügt über eine Version mit Dateihashüberprüfung](neither-file-has-a-version-with-file-hash-check.md)
-   [Eine Datei verfügt über eine Version](one-file-has-a-version.md)

 

 



