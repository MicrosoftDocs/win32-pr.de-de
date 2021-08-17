---
description: Ein Schränk ist eine einzelne Datei, in der Regel mit einer .cab Erweiterung, in der komprimierte Dateien in einer Dateibibliothek gespeichert werden.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: Cab-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2331b60c42bf975856987d1e13d67c95bc01fa685f99f49543650c48347cac49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380719"
---
# <a name="cabinet-files"></a>Cab-Dateien

Ein Schränk ist eine einzelne Datei, in der Regel mit einer .cab Erweiterung, in der komprimierte Dateien in einer Dateibibliothek gespeichert werden. Das Schränkformat ist eine effiziente Möglichkeit zum Packen mehrerer Dateien, da die Komprimierung über Dateigrenzen hinweg durchgeführt wird, wodurch das Komprimierungsverhältnis erheblich verbessert wird.

Entwickler können ein Tool zum Erstellen von Cab-Dateien wie Makecab.exe verwenden, um Cab-Dateien für die Verwendung mit Installationspaketen zu erstellen. Das hilfsprogramm Makecab.exe ist in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)enthalten.

Entwickler können auch ein Tool zum Erstellen von Cab-Dateien wie Cabarc.exe verwenden, um Cab-Dateien für die Verwendung mit Installationspaketen zu erstellen. Dieses Tool schreibt in die Diamond-Gehäusestruktur.

Die Dateischlüssel der Dateien, die in einer Cab-Datei gespeichert sind, müssen mit den Einträgen in der Spalte Datei der [Dateitabelle](file-table.md) übereinstimmen, und die Sequenz der Dateien im Cab muss mit der in der Spalte Sequenz angegebenen Dateisequenz übereinstimmen. Weitere Informationen finden Sie unter [Verwenden von Schränken und komprimierten Quellen.](using-cabinets-and-compressed-sources.md)

Große Dateien können auf zwei oder mehr Cab-Dateien aufgeteilt werden. Es dürfen nicht mehr als 15 Dateien in einer Schränkdatei vorhanden sein, die sich auf die nächste Cab-Datei erstreckt. Wenn Sie z. B. über drei Cab-Dateien verfügen, kann das erste Schränke 15 Dateien enthalten, die sich auf die zweite Cab-Datei erstrecken, und die zweite Cab-Datei kann 15 Dateien enthalten, die sich auf die dritte Cab-Datei erstrecken.

Das Installationsprogramm extrahiert Dateien aus einem Schränk, da sie von der Installation benötigt werden, und installiert sie in der gleichen Reihenfolge, in der sie in der Cab-Datei gespeichert sind. Die Speicherplatzanforderungen für die Installation einer in einem Schränk gespeicherten Datei unterscheiden sich nicht von der Installation einer nicht komprimierten Datei.

Eine Cab-Datei kann sich innerhalb oder außerhalb der .msi befinden. Ab Windows Installer 5.0, der auf Windows 7 oder Windows Server 2008 R2 ausgeführt wird, speichert das Installationsprogramm alle Schränke, die in die .msi Datei eingebettet sind, bevor das Installationspaket zwischengespeichert wird.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Um Speicherplatz zu sparen, entfernt das Installationsprogramm immer alle Schränke, die in die .msi-Datei eingebettet sind, bevor das Installationspaket auf dem Computer des Benutzers zwischengespeichert wird.

 

 



