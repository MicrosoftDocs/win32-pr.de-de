---
description: Die Verwendung von öffentlichen Symbolen für Ihre Ziel- und Upgradeimagebinärdateien kann binäre Patchgrößen um etwa die Hälfte reduzieren.
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: Verwenden von Symbolen zum Reduzieren der Größe von binären Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502c11a1a6b058db8c9f4a7c9bde897034c3b4affa8c02d1b049d754013f4455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804082"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a>Verwenden von Symbolen zum Reduzieren der Größe von binären Patches

Die Verwendung von öffentlichen Symbolen für Ihre Ziel- und Upgradeimagebinärdateien kann binäre Patchgrößen um etwa die Hälfte reduzieren. Die tatsächliche Reduzierung hängt von den verwendeten Symbolen ab. Beachten Sie, dass die Verwendung von Symbolen zu langsameren Patcherstellungszeiten führen kann, da die Verarbeitung der Symboldateien länger dauert.

Um die Größe eines binären Patches mithilfe von Symbolen zu reduzieren, müssen Sie Symbole für die Ziel- und Upgradeimagebinärdateien bereitstellen. Geben Sie die Symbole in der Spalte SymbolPaths der [Tabelle TargetImages](targetimages-table-patchwiz-dll-.md) und in der Spalte SymbolPaths der Tabelle [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) an. Sie müssen Visual C++ verwenden, um Symbole im Dateiformat der Programmdatenbank (PDB) zu generieren. Neuere Versionen von Visual C++ stellen alle erforderlichen Informationen in der PDB-Datei bereit. Ältere Versionen von Visual C++ generieren auch das Debugdateiformat (DBG). In diesem Fall sollte der SymbolsPaths-Wert den Speicherort der PDB- und DBG-Dateien angeben.

Das TargetImage für einen Patch kann z. B. das Installationspaket sein, das mit Windows 2000 ausgeliefert wurde und die Version 1.1.1029.0 von MSI.DLL installiert. UpgradeImage kann das aktualisierte Installationspaket sein, das mit Windows 2000 mit Service Pack 1 (SP1) ausgeliefert wurde und die Version 1.11.1314.0 von MSI.DLL installiert. Anschließend müssten zwei PCP-Dateien (Patch Creation Properties) erstellt werden, eine mit der Spalte SymbolPaths der Tabellen [TargetImages](targetimages-table-patchwiz-dll-.md) und [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) links NULL (leer) und die andere mit der Spalte SymbolPaths der Tabellen TargetImages und UpgradedImages, die mit dem Speicherort der Symbole für die Binärdateien aufgefüllt wurden. In diesem Fall kann die Größe des Patches, der ohne Verwendung von Symbolen generiert wird, ungefähr dreimal so groß sein wie der Patch, der mithilfe von Symbolen generiert wurde.

Das hilfsprogramm Mpatch.exe kann verwendet werden, um die Generierung von binären Patches für eine einzelne Datei zu testen und zu überprüfen, ob die Symbole gültig sind. Das hilfsprogramm Mpatch.exe ist in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)enthalten. Die Ausgabe von Mpatch.exe gibt an, ob die Symbole nicht übereinstimmen.

Geben Sie beispielsweise die folgende Befehlszeile ein, um zu überprüfen, ob die Symbole gültig sind.

**mpatch.exe -NEWSYMPATH:d: \\ update -OLDSYMPATH:d: \\ target d: \\ targetexample.dll \\ d: updateexample.dll \\ \\ example.pat**

Wenn sich die Symbole nicht am richtigen Speicherort befinden, kann die Ausgabe von Mpatch.exe die folgende Warnung enthalten.

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



