---
description: Kosten sind der Prozess, bei dem der gesamte Speicherplatzbedarf für eine Installation bestimmt wird.
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: Dateikosten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad2dc3ad9da4fab21345e74f3f9db99992445d7cf1e2266806bda55cd6ca638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529580"
---
# <a name="file-costing"></a>Dateikosten

Kosten sind der Prozess, bei dem der gesamte Speicherplatzbedarf für eine Installation bestimmt wird. Die im Dateikostenprozess berechneten Elemente umfassen den Speicherplatz, in dem Dateien installiert oder entfernt werden, sowie den Speicherplatz, der von Registrierungseinträgen, Verknüpfungen und anderen dateien belegt wird. Vorhandene Dateien, die überschrieben werden sollen, werden ebenfalls in den Gesamtkosten des Datenträgers berechnet.

Die Gesamtkosten werden auf[Komponentenbasis](components-and-features.md) akkumuliert und bestehen aus drei separaten Teilen: lokale Kosten, Quellkosten und Entfernungskosten. Diese Teile entsprechen den Datenträgerkosten, die anfallen, wenn die Komponente lokal installiert, für die Ausführung auf dem Quellmedium installiert oder entfernt wird.

Alle Berechnungen im Zusammenhang mit den Kosten für die Installation von Dateien hängen vom Datenträgervolume ab, auf dem die Datei installiert oder entfernt werden soll. Bei jeder Änderung des einer Komponente zugeordneten Verzeichnisses müssen die Kosten für die von dieser Komponente gesteuerten Installationsdateien neu berechnet werden. Da eine Verzeichnisänderung beispielsweise auch eine Volumeänderung implizieren kann, müssen die Größen der gruppierten Dateien neu berechnet werden. Darüber hinaus muss das neue Verzeichnis überprüft werden, um festzustellen, ob vorhandene Dateien, die überschrieben werden können, berücksichtigt werden müssen.

Nachdem die [CostInitialize-Aktion](costinitialize-action.md) aufgerufen wurde, muss die [FileCost-Aktion](filecost-action.md) aufgerufen werden. Die CostInitialize-Aktion initialisiert die internen Routinen des Installationsprogramms, die die Datenträgerkosten für die Standardinstallationsaktionen dynamisch berechnen. An diesem Punkt werden keine anderen dynamischen Kostenberechnungen durchgeführt.

Als Nächstes muss die [CostFinalize-Aktion](costfinalize-action.md) aufgerufen werden. Mit dieser Aktion werden alle Kostenberechnungen abgeschlossen, und die Kostendaten werden über die [Tabelle Komponente](component-table.md) verfügbar.

Nachdem die [CostFinalize-Aktion](costfinalize-action.md) die Ausführung abgeschlossen hat, wird die [Tabelle Komponente](component-table.md) vollständig initialisiert, und bei Bedarf kann eine Dialogfeldsequenz der Benutzeroberfläche mit einem [SelectionTree-Steuerelement](selectiontree-control.md) initiiert werden. Die Dialogfelder der Benutzeroberfläche bieten möglicherweise die Möglichkeit, den Auswahlzustand oder das Zielverzeichnis eines Features in der [Featuretabelle](feature-table.md) für den Benutzer zu ändern. Der Prozess ist ähnlich, wenn sich der Auswahlzustand einer Komponente ändert. in diesem Fall werden jedoch nur die dynamischen Kosten der geänderten Komponente neu berechnet.

Nachdem der Benutzer die Auswahl von Features auf der Benutzeroberfläche abgeschlossen hat, sollte die Aktion [InstallValidate](installvalidate-action.md) aufgerufen werden. Mit dieser Aktion wird überprüft, ob alle Volumes, denen Kosten zugeordnet wurden, über ausreichend Speicherplatz für die Installation verfügen.

 

 



