---
description: Wenn keine datei über eine Versionsnummer verfügt, verwendet der Windows Installer die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die zur Komponente gehören, ersetzt werden.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Keine der Dateien verfügt über eine Version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68a6d74a26a810f2ddb33e1c13b2ed7b372a75d5b262a8b6d8d7ecaca1c99f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065934"
---
# <a name="neither-file-has-a-version"></a>Keine der Dateien verfügt über eine Version

Wenn die Schlüsseldatei einer komponente, die installiert wird (copy-A), den gleichen Namen hat wie eine Datei, die bereits am Zielspeicherort installiert ist (copy-B), vergleicht das Installationsprogramm Versionsnummer, Datum und Sprache der beiden Dateien.

Wenn keine datei über eine Versionsnummer verfügt, verwendet das Installationsprogramm die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die zur Komponente gehören, ersetzt werden. Da das Installationsprogramm nur ganze Komponenten installiert, werden alle Komponentendateien ersetzt, wenn die installierte Schlüsseldatei ersetzt wird.

Beachten Sie, dass dieses Diagramm die Standardregeln für die [Dateiversionsversion](file-versioning-rules.md)veranschaulicht, die durch Festlegen der [**REINSTALLMODE-Eigenschaft überschrieben werden**](reinstallmode.md) können. Der Standardwert der **REINSTALLMODE-Eigenschaft** ist "omus".

![Standardregeln für die Dateiversionsversion, wenn keine Datei über eine Versionsnummer verfügt](images/waiflow2.png)

Weitere Informationen finden Sie in den Beispielen für die Standarddateiversionsvererbung unter [Ersetzen vorhandener Dateien.](replacing-existing-files.md)

-   [Beide Dateien verfügen über eine Version](both-files-have-a-version.md)
-   [Keine der Dateien verfügt über eine Version mit Dateihashüberprüfung](neither-file-has-a-version-with-file-hash-check.md)
-   [Eine Datei verfügt über eine Version](one-file-has-a-version.md)

 

 



