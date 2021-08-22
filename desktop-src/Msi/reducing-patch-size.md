---
description: Ab Version Windows Installer 3.0 können Patchautoren die vom Installationsprogramm zwischengespeicherte Produktbaseline verwenden, um Anwendungen mit kleineren Deltapatches einfacher zu bedienen.
ms.assetid: ab5b193d-79ce-4ed4-af53-89a4197197c1
title: Reduzieren der Patchgröße
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9024307ecb0971b02c93036dd0de2aefbe797dcf5645f0f07045c4df8956a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534080"
---
# <a name="reducing-patch-size"></a>Reduzieren der Patchgröße

Ab Version Windows Installer 3.0 können Patchautoren die vom Installationsprogramm zwischengespeicherte Produktbaseline verwenden, um Anwendungen mit kleineren Deltapatches einfacher zu bedienen. In vielen Fällen kann ein [*Deltapatch,*](d-gly.md) der Wartungsinformationen an eine Anwendung liefert, erheblich kleiner sein als ein Vollständigdateipatch oder -installationspaket, das die gleichen Informationen liefert.

**Windows Installer 2.0:** Nicht unterstützt. Ab Windows Installer 3.0 speichert das Installationsprogramm selektiv Baselineinformationen zu Dateien, wenn sie aktualisiert werden.

Windows Das Installationsprogramm bietet drei Methoden zum Aktualisieren und Warten von Anwendungen: [kleine](small-updates.md)Updates, [kleinere Upgrades](minor-upgrades.md)und [größere Upgrades.](major-upgrades.md) Ein kleines Update wird auch als Quick Fix Engineering Update (QFE) bezeichnet, und ein kleineres Upgrade wird auch als Service Pack-Update (SP) bezeichnet. Bei einem typischen größeren Upgrade wird eine vorherige Anwendung entfernt und eine neue Anwendung installiert. Windows Das Installationsprogramm kann Wartungsinformationen [](installation-package.md) als Installationspaket (.msi Datei) oder als Patchpaket (MSP-Datei) an Anwendungen liefern. [](patch-packages.md)

Ein Windows Installer-Patchpaket, das Wartungsinformationen für ein kleines Update oder kleineres Upgrade liefert, ist im Allgemeinen viel kleiner als das entsprechende Installationspaket, das die gleichen Wartungsinformationen liefert. Es wird empfohlen, Patchpakete für die Verteilung kleiner und kleiner Upgrades zu verwenden. Es wird empfohlen, ein Installationspaket für die Verteilung eines größeren Upgrades zu verwenden.

Windows Installerpatches (MSP-Dateien) können entweder aus vollständigen Dateien oder aus Dateiunterschieden (auch als Dateideltadateien bezeichnet) generiert werden. Ein Windows Installer-Patch, der aus Dateideltata generiert wurde, kann viel kleiner als der entsprechende vollständige Dateipatch sein. Alle Versionen des Windows Installers können sowohl Vollständige Dateipatches als auch Deltapatches verwenden.

Ab version Windows Installer 3.0 speichert das Installationsprogramm selektiv Baselineinformationen zu Dateien, wenn sie aktualisiert werden. Informationen zur ursprünglichen Basisanwendung (RTM-Version) und zum letzten kleineren Upgrade (Service Pack) werden an einem privaten Speicherort gespeichert, wenn die Anwendung installiert wird oder ein kleineres Upgrade empfängt.

Das Installationsprogramm führt folgende Schritte aus, um die Größe des Baselinecaches zu minimieren:

-   Für jede Anwendung werden nicht mehr als zwei Baselines verwaltet: eine Baseline der Datei wie ursprünglich freigegeben (RTM) und eine Baseline der Datei beim letzten kleineren Upgrade (Service Pack).
-   Eine Datei wird dem Cache erst hinzugefügt, wenn sie gepatcht wurde. Der Baselinecache ist "copy-on-write".
-   Wenn die Anwendung noch nie aktualisiert wurde, befinden sich keine Dateien im Baselinecache.
-   Wenn die letzte Wartung der Anwendung ein kleineres Upgrade (Service Pack) war, befindet sich die Anwendung auf einer Baselineebene, und es können mindestens zwei Kopien einer Datei auf dem Computer vorhanden sein. Eine Kopie der Datei befindet sich im Zielverzeichnis der Installation. Die andere Kopie kann im RTM-Baselinecache vorhanden sein.
-   Wenn die letzte Wartung der Anwendung ein kleines Update (QFE) war, befindet sich die Anwendung nicht auf einer Baselineebene, und es können mindestens drei Kopien einer Datei auf dem Computer vorhanden sein. Die erste Kopie der Datei befindet sich im Zielverzeichnis der Installation. Die zweite Kopie der Datei befindet sich im RTM-Baselinecache. Die letzte Kopie der Datei befindet sich im letzten Baselinecache.
-   Der Baselinecache der Anwendung wird entfernt, wenn das Produkt deinstalliert wird.

Ab version Windows Installer 3.0 kann das Installationsprogramm den Baselinecache verwenden, wenn Patches auf die Anwendung angewendet werden. Die Baselineinformationen können verwendet werden, um einen Deltapatch anzuwenden oder eine Datei während einer Patchdeinstallation auf eine frühere Version zurück zu stellen. Dadurch können Patchautoren von kleineren Deltapatches profitieren. Wenn das Installationsprogramm ermittelt, dass der Deltapatch nicht auf die Zieldatei angewendet werden kann, kann das Installationsprogramm versuchen, eine im Baselinecache gespeicherte Datei als Ausgangspunkt zu verwenden. Das Installationsprogramm greift nur auf das Anfordern der ursprünglichen Installationsquelle zurück, nachdem alle Möglichkeiten im Cache versucht wurden.

Die Einhaltung der folgenden Richtlinien kann Patchautoren dabei unterstützen, patches Windows Installer Version 3.0 und den Baselinecache zu verwenden, um kleinere Deltapatches zu erstellen:

-   Erstellen Sie Patches, die die [MsiPatchSequence-Tabelle enthalten.](msipatchsequence-table.md) Diese Tabelle ist für die Verwendung des Baselinecaches erforderlich und ab Windows Installer-Version 3.0 verfügbar.
-   Legen Sie keine Richtlinie fest, die das Zwischenspeichern von Baselines verhindert. Der Wert der [MaxPatchCacheSize-Richtlinie](maxpatchcachesize.md) gibt den maximalen Prozentsatz des Speicherplatzes an, der verwendet werden kann. Wenn die MaxPatchCacheSize-Richtlinie auf 0 festgelegt ist, werden keine zusätzlichen Dateien im Baselinecache gespeichert. Wenn die Richtlinie nicht festgelegt ist, ist die Standardeinstellung, dass maximal 10 % des Speicherplatzes auf dem Datenträger verwendet werden können. Wenn die Gesamtgröße des Caches den maximalen Prozentsatz des Speicherplatzes erreicht, werden keine zusätzlichen Dateien gespeichert. Die Richtlinie wirkt sich nicht auf Dateien aus, die bereits gespeichert wurden. Auch wenn das Zwischenspeichern deaktiviert ist, kann das Installationsprogramm vorhandene Produktbaselinecaches verwenden.
-   Wenn der erste angewendete Patch die [MsiPatchSequence-Tabelle enthält,](msipatchsequence-table.md)wird die Zwischenspeicherung für die Anwendung aktiviert.
-   Wenn ein Patch in der Wartungstransaktion die MsiPatchSequence-Tabelle nicht enthält, wird die Zwischenspeicherung für die Anwendung nur aktiviert, wenn ein kleiner Upgradepatch (Service Pack), der die [MsiPatchSequence-Tabelle](msipatchsequence-table.md)enthält, erfolgreich auf das Produkt angewendet wird.
-   Generieren Sie das Patchpaket mithilfe von Tools zur Patcherstellung wie [Msimsp.exe](msimsp-exe.md) und [PATCHWIZ.DLL](patchwiz-dll.md).
-   Zielpatches sind immer für die RTM-Version der Anwendung oder eine kleinere Upgradeversion (Service Pack) der Anwendung. Die ziele, die in der [TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md) der PcP-Datei (Patch Creation Properties) angegeben sind, sollten Produktprüfpunkte sein, die durch die ersten drei Felder der [**ProductVersion-Eigenschaft definiert**](productversion.md) werden.
-   Stellen Sie Patches niemals auf kleine Updateabbilder als Ziel. Die Ziele zum Erstellen des Patches sollten keine vorherigen Images für kleine Aktualisierungsupgrades enthalten.

 

 



