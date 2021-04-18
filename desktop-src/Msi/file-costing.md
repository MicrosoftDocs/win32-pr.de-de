---
description: Kosten ist der Prozess, bei dem die Gesamtspeicher Platzanforderungen für eine-Installation ermittelt werden.
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: Datei Kosten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a4e6221775c2b9ecc429bd32f136e519a2b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345829"
---
# <a name="file-costing"></a>Datei Kosten

Kosten ist der Prozess, bei dem die Gesamtspeicher Platzanforderungen für eine-Installation ermittelt werden. Zu den im Datei Kosten Prozess berechneten Elementen zählt der Speicherplatz, in dem Dateien installiert oder entfernt werden, sowie die Menge des Speicherplatzes, der von Registrierungs Einträgen, Verknüpfungen und anderen sonstigen Dateien belegt wird. Vorhandene Dateien, die überschrieben werden sollen, werden auch in den Datenträger Kosten berechnet.

Die Gesamtkosten werden pro[Komponente](components-and-features.md) gesammelt und bestehen aus drei separaten Teilen: lokale Kosten, Quell Kosten und Entfernungs Kosten. Diese Teile entsprechen den Datenträger Kosten, die anfallen, wenn die Komponente lokal installiert, auf dem Quell Medium installiert oder entfernt wird.

Alle Berechnungen, die die Kosten für die Installation von Dateien betreffen, hängen von dem Datenträgervolume ab, auf dem die Datei installiert oder entfernt werden soll. Jedes Mal, wenn sich das Verzeichnis ändert, das einer Komponente zugeordnet ist, müssen die Kosten der von dieser Komponente kontrollierten Installationsdateien neu berechnet werden. Da z. b. eine Verzeichnis Änderung auch eine volumeänderung impliziert, müssen die Cluster Dateigrößen neu berechnet werden. Außerdem muss das neue Verzeichnis geprüft werden, um zu bestimmen, ob vorhandene Dateien, die möglicherweise überschrieben werden, berücksichtigt werden müssen.

Nachdem die [costinitialize](costinitialize-action.md) -Aktion aufgerufen wurde, muss die [filecost](filecost-action.md) -Aktion aufgerufen werden. Mit der Aktion "costinitialize" werden die internen Routinen des Installers initialisiert, mit denen die mit den Standard Installations Aktionen verbundenen Datenträger Kosten dynamisch berechnet werden. An dieser Stelle werden keine weiteren dynamischen Kostenberechnungen durchgeführt.

Als nächstes muss die Aktion " [costfinalize](costfinalize-action.md) " aufgerufen werden. Mit dieser Aktion werden alle Kostenberechnungen abgeschlossen, und die Kostendaten werden über die [Komponenten](component-table.md) Tabelle zur Verfügung gestellt.

Nachdem die [costfinalize](costfinalize-action.md) -Aktion die Ausführung abgeschlossen hat, ist die [Komponenten](component-table.md) Tabelle vollständig initialisiert, und eine Benutzeroberflächen-Dialogfeld Sequenz mit einem [SelectionTree](selectiontree-control.md) -Steuerelement kann bei Bedarf initiiert werden. Die Dialogfelder für die Benutzeroberfläche können die Option zum Ändern des Auswahl Zustands oder des Zielverzeichnisses für beliebige Features in der Featuretabelle in den [Benutzer enthalten.](feature-table.md) Der Prozess ist ähnlich, wenn der Auswahl Zustand einer Komponente geändert wird. in diesem Fall werden jedoch nur die dynamischen Kosten der geänderten Komponente neu berechnet.

Nachdem der Benutzer die Auswahl der Features in der Benutzeroberfläche abgeschlossen hat, sollte die [InstallValidate](installvalidate-action.md) -Aktion aufgerufen werden. Mit dieser Aktion wird überprüft, ob alle Volumes, denen die Kosten zugewiesen wurden, über ausreichend Speicherplatz für die Installation verfügen.

 

 



