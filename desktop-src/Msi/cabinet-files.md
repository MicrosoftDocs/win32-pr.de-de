---
description: Eine CAB-Datei ist eine einzelne Datei, in der Regel mit der Erweiterung ". cab", die komprimierte Dateien in einer Datei Bibliothek speichert.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: CAB-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343850"
---
# <a name="cabinet-files"></a>CAB-Dateien

Eine CAB-Datei ist eine einzelne Datei, in der Regel mit der Erweiterung ". cab", die komprimierte Dateien in einer Datei Bibliothek speichert. Das CAB-Format stellt eine effiziente Möglichkeit zum Packen mehrerer Dateien dar, da die Komprimierung über Dateigrenzen hinweg durchgeführt wird, was das Komprimierungs Verhältnis erheblich verbessert.

Entwickler können mithilfe eines Tools zum Erstellen von CAB-Dateien wie Makecab.exe CAB-Dateien für die Verwendung mit Installer-Paketen verwenden. Das Makecab.exe-Hilfsprogramm ist in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)enthalten.

Entwickler können auch ein Tool zum Erstellen von CAB-Dateien wie Cabarc.exe verwenden, um CAB-Dateien für die Verwendung mit Installer-Paketen zu erstellen. Dieses Tool schreibt in die Diamant-CAB-Struktur.

Die Datei Schlüssel der Dateien, die in einer CAB-Datei gespeichert sind, müssen mit den Einträgen in der File-Spalte der [Dateitabelle](file-table.md) identisch sein, und die Sequenz der Dateien in der CAB-Datei muss mit der in der Sequence-Spalte angegebenen Datei Sequenz identisch sein. Weitere Informationen finden Sie unter [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).

Große Dateien können zwischen zwei oder mehr CAB-Dateien aufgeteilt werden. In einer CAB-Datei, die sich auf die nächste CAB-Datei erstreckt, dürfen nicht mehr als 15 Dateien vorhanden sein. Wenn Sie z. b. drei CAB-Dateien haben, kann die erste CAB-Datei 15 Dateien enthalten, die sich in der zweiten CAB-Datei befinden, und die zweite CAB-Datei kann 15 Dateien enthalten, die für die dritte CAB-Datei spannen.

Das Installationsprogramm extrahiert Dateien aus einer CAB-Datei, da Sie von der Installation benötigt werden, und installiert Sie in derselben Reihenfolge, in der Sie in der CAB-Datei gespeichert sind. Die Speicherplatzanforderungen für die Installation einer Datei, die in einer CAB-Datei gespeichert ist, unterscheiden sich nicht von der Installation unkomprimierter Dateien

Eine CAB-Datei kann sich innerhalb oder außerhalb der MSI-Datei befinden. Ab Windows Installer 5,0, die unter Windows 7 oder Windows Server 2008 R2 ausgeführt wird, speichert das Installationsprogramm alle Schränke, die in die MSI-Datei eingebettet sind, bevor das Installationspaket zwischengespeichert wird.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Um Speicherplatz zu sparen, entfernt das Installationsprogramm immer alle Schränke, die in die MSI-Datei eingebettet sind, bevor das Installationspaket auf dem Computer des Benutzers zwischengespeichert wird.

 

 



