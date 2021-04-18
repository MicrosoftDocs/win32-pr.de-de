---
description: Wenn Sie öffentliche Symbole für die Ziel-und upgradeabbild-Binärdateien verwenden, können binäre patchgrößen um ungefähr eine Hälfte reduziert werden.
ms.assetid: 83351a1b-ba70-4f0b-bacf-71ad7993a5aa
title: Verwenden von Symbolen zum Verringern der Binär Patchgröße
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5ccf33dbf3ffefbee909d99bd0204ea2f49aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357375"
---
# <a name="using-symbols-to-reduce-binary-patch-size"></a>Verwenden von Symbolen zum Verringern der Binär Patchgröße

Wenn Sie öffentliche Symbole für die Ziel-und upgradeabbild-Binärdateien verwenden, können binäre patchgrößen um ungefähr eine Hälfte reduziert werden. Die tatsächliche Reduzierung hängt von den verwendeten Symbolen ab. Beachten Sie, dass das Verwenden von Symbolen zu langsameren patcherstellungs Zeiten führen kann, da die Verarbeitung der Symbol Dateien länger dauert.

Um die Größe eines binären Patches mithilfe von Symbolen zu verringern, müssen Sie Symbole sowohl für die Ziel-als auch für die upgradeabbild-Binärdateien angeben. Geben Sie die Symbole in der SymbolPath-Spalte der [TargetImages](targetimages-table-patchwiz-dll-.md) -Tabelle und in der SymbolPath-Spalte der [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) -Tabelle an. Sie müssen Visual C++ verwenden, um Symbole im Dateiformat der Programmdatenbank (PDB) zu generieren. Neuere Versionen von Visual C++ enthalten alle erforderlichen Informationen in der PDB-Datei. Ältere Versionen von Visual C++ generieren auch das Debug-Dateiformat (dbg). In diesem Fall sollte der symbolspaths-Wert den Speicherort der PDB-und dbg-Dateien angeben.

Beispielsweise kann das targetimage für einen Patch das Installationspaket sein, das in Windows 2000 enthalten ist, und das die 1.1.1029.0-Version von MSI.DLL installiert. Upgradedimage könnte das aktualisierte Installationspaket sein, das in Windows 2000 mit Service Pack 1 (SP1) enthalten ist und die 1.11.1314.0-Version von MSI.DLL installiert. Es müssen zwei patcherstellungs-Eigenschaften (PCP) erstellt werden, von denen eine mit der SymbolPath-Spalte der [TargetImages](targetimages-table-patchwiz-dll-.md) -Tabelle und der [UpgradedImages](upgradedimages-table-patchwiz-dll-.md) -Tabelle NULL (leer) und die andere mit der SymbolPath-Spalte der TargetImages-Tabelle und der UpgradedImages-Tabelle mit dem Speicherort der Symbole für die Binärdateien aufgefüllt wird. In diesem Fall kann die Größe des Patches, die ohne Verwendung von Symbolen generiert wurde, ungefähr dreimal so groß wie die Größe des Patches sein, die mithilfe von Symbolen generiert wurde.

Mit dem Mpatch.exe-Hilfsprogramm können Sie die Generierung von binären Patches für eine einzelne Datei testen und überprüfen, ob die Symbole gültig sind. Das Mpatch.exe-Hilfsprogramm ist in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)enthalten. Die Ausgabe Mpatch.exe gibt an, ob die Symbole nicht stimmen.

Geben Sie z. b. die folgende Befehlszeile ein, um zu überprüfen, ob die Symbole gültig sind.

**mpatch.exe-newsymsympath: d: \\ Update-oldsympath: d: \\ target d: \\ Target \\example.dll d: \\ Update \\example.dll example. Pat**

Wenn sich die Symbole nicht am richtigen Speicherort befinden, kann die Ausgabe von Mpatch.exe folgende Warnung enthalten.

``` syntax
WARNING: no debug symbols for d:\update\example.dll
```

 

 



