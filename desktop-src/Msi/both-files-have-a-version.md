---
description: Wenn beide Dateien über eine Versionsnummer verfügen, verwendet der Windows Installer die im folgenden Flussdiagramm dargestellte Logik, um zu bestimmen, ob alle installierten Dateien ersetzt werden sollen, die zur Komponente gehören.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Beide Dateien verfügen über eine Version.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1338a93b4a45094a9a5951c3c59def15affde96dbbe74f3b134ba9dd7532092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380812"
---
# <a name="both-files-have-a-version"></a>Beide Dateien verfügen über eine Version.

Wenn die Schlüsseldatei einer komponente, die installiert wird (copy-A), den gleichen Namen hat wie eine Datei, die bereits am Zielspeicherort installiert ist (copy-B), vergleicht das Installationsprogramm die Versionsnummer und die Sprache der beiden Dateien.

Wenn beide Dateien über eine Versionsnummer verfügen, verwendet das Installationsprogramm die im folgenden Flussdiagramm dargestellte Logik, um zu bestimmen, ob alle installierten Dateien ersetzt werden sollen, die zur Komponente gehören. Da das Installationsprogramm nur ganze Komponenten installiert, werden alle Dateien der Komponente ersetzt, wenn die installierte Schlüsseldatei ersetzt wird.

Beachten Sie, dass dieses Diagramm die Standardregeln für die [Dateiversionsversionsierung](file-versioning-rules.md)veranschaulicht, die durch Festlegen der [**REINSTALLMODE-Eigenschaft**](reinstallmode.md) überschrieben werden können. Der Standardwert der **REINSTALLMODE-Eigenschaft** ist "omus".

![Standardregeln für die Dateiversionsierung, wenn beide Dateien den gleichen Namen oder die gleiche Versionsnummer aufweisen](images/waiflow1.png)

Das vorherige Diagramm kann auch mit Dateien ohne angegebene Sprache verwendet werden. Wenn copy-A über eine angegebene Sprache und Copy-B über keine angegebene Sprache verfügt, wird copy-B durch copy-A ersetzt. Wenn copy-A und copy-B keine Sprache angegeben haben, wird copy-B nicht ersetzt.

Beispiele für die Standarddateiversionsierung finden Sie unter [Ersetzen vorhandener Dateien.](replacing-existing-files.md)

-   [Keine Datei hat eine Version](neither-file-has-a-version.md)
-   [Keine Datei verfügt über eine Version mit Dateihashüberprüfung](neither-file-has-a-version-with-file-hash-check.md)
-   [Eine Datei verfügt über eine Version.](one-file-has-a-version.md)

 

 



