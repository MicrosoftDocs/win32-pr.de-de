---
description: Ab Windows Installer Version 3,0 können patchautoren die vom Installer zwischengespeicherte Produktbasis Linie verwenden, um Anwendungen mit kleineren Delta Patches leichter zu bedienen.
ms.assetid: ab5b193d-79ce-4ed4-af53-89a4197197c1
title: Verringern der Patchgröße
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa365e831ab8685073347dc254bac58269135f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358875"
---
# <a name="reducing-patch-size"></a>Verringern der Patchgröße

Ab Windows Installer Version 3,0 können patchautoren die vom Installer zwischengespeicherte Produktbasis Linie verwenden, um Anwendungen mit kleineren Delta Patches leichter zu bedienen. In vielen Fällen kann ein [*Delta-Patch*](d-gly.md) , der Wartungsinformationen für eine Anwendung bereitstellt, erheblich kleiner sein als ein Patch-oder Installationspaket mit einer vollständigen Datei, das dieselben Informationen liefert.

**Windows Installer 2,0:** Nicht unterstützt. Ab Windows Installer 3,0 speichert das Installationsprogramm selektiv grundlegende Informationen zu Dateien, wenn diese aktualisiert werden.

Windows Installer bietet drei Methoden zum Aktualisieren und warten von Anwendungen: [kleine Updates](small-updates.md), [kleinere Upgrades](minor-upgrades.md)und [größere Upgrades](major-upgrades.md). Ein kleines Update wird auch als QFE-Update (Quick Fix Engineering) bezeichnet, und ein kleineres Upgrade wird auch als Service Pack Update (SP) bezeichnet. Bei einem typischen Haupt Upgrade wird eine vorherige Anwendung entfernt und eine neue Anwendung installiert. Windows Installer können Wartungsinformationen an Anwendungen als [Installationspaket](installation-package.md) (MSI-Datei) oder als [Patchpaket](patch-packages.md) (MSP-Datei) bereitstellen.

Ein Windows Installer Patch-Paket, das Wartungsinformationen für ein kleines Update oder ein geringfügige Upgrade bereitstellt, ist in der Regel viel kleiner als das entsprechende Installationspaket, das die gleichen Wartungsinformationen liefert. Es wird empfohlen, Patch-Pakete für die Verteilung von kleinen und kleinen Upgrades zu verwenden. Es wird empfohlen, ein Installationspaket für die Verteilung eines größeren Upgrades zu verwenden.

Windows Installer Patches (MSP-Dateien) können entweder aus vollständigen Dateien oder aus Datei unterschieden (auch als "Datei Delta" bezeichnet) generiert werden. Ein aus Datei-Delta generierter Windows Installer Patch kann viel kleiner als der entsprechende Patch für die vollständige Datei sein. Alle Versionen der Windows Installer können sowohl volldateipatches als auch Delta Patches verwenden.

Ab Windows Installer Version 3,0 speichert das Installationsprogramm selektiv grundlegende Informationen zu Dateien, wenn diese aktualisiert werden. Informationen zur ursprünglichen Basisanwendung (RTM-Version) und zum neuesten neben Upgrade (Service Pack) werden an einem privaten Speicherort gespeichert, wenn die Anwendung installiert wird, oder es wird ein geringfügiges Upgrade empfangen.

Der Installer führt Folgendes aus, um die Größe des baselinecaches zu minimieren:

-   Es werden nicht mehr als zwei Basis Linien für jede Anwendung verwaltet: eine Baseline der Datei, die ursprünglich freigegeben wurde (RTM), und eine Baseline der Datei am letzten kleinen Upgrade (Service Pack.)
-   Eine Datei wird nicht zum Cache hinzugefügt, bis Sie gepatcht wird. Der baselinecache ist Copy-on-Write.
-   Wenn die Anwendung noch nicht aktualisiert wurde, befinden sich keine Dateien im Baseline-Cache.
-   Wenn die letzte Wartung der Anwendung ein kleineres Upgrade war (Service Pack), hat die Anwendung eine Baselineversion, und höchstens zwei Kopien einer Datei können auf dem Computer vorhanden sein. Eine Kopie der Datei befindet sich im Zielverzeichnis der-Installation. Die andere Kopie kann im RTM-baselinecache gespeichert werden.
-   Wenn die letzte Wartung der Anwendung ein kleines Update (QFE) war, liegt die Anwendung nicht auf einer Baselineversion, und höchstens drei Kopien einer Datei können auf dem Computer vorhanden sein. Die erste Kopie der Datei befindet sich im Zielverzeichnis der-Installation. Die zweite Kopie der Datei befindet sich im RTM-baselinecache. Die letzte Kopie der Datei befindet sich im aktuellen baselinecache.
-   Der baselinecache der Anwendung wird entfernt, wenn das Produkt deinstalliert wird.

Ab Windows Installer Version 3,0 kann das Installationsprogramm den baselinecache verwenden, wenn Patches auf die Anwendung angewendet werden. Die grundlegenden Informationen können verwendet werden, um einen Delta Patch anzuwenden oder eine Datei auf eine frühere Version während der Deinstallation eines Patches zurückzusetzen. Dadurch können patchautoren von kleineren Delta Patches profitieren. Wenn das Installationsprogramm feststellt, dass der Delta Patch nicht auf die Zieldatei angewendet werden kann, kann das Installationsprogramm versuchen, eine Datei zu verwenden, die im Baseline-Cache als Ausgangspunkt gespeichert ist. Das Installationsprogramm greift nur auf die Anforderung der ursprünglichen Installationsquelle zu, nachdem alle Möglichkeiten im Cache ausprobiert wurden.

Wenn Sie sich an die folgenden Richtlinien halten, können patchautoren mithilfe von Windows Installer-Patches der Version 3,0 und dem baselinecache kleinere Delta Patches erstellen:

-   Erstellen Sie Patches, die die [msipatchsequence-Tabelle](msipatchsequence-table.md)einschließen. Diese Tabelle ist erforderlich, um den baselinecache zu verwenden, und ist ab Windows Installer Version 3,0 verfügbar.
-   Legen Sie keine Richtlinie fest, die das Zwischenspeichern der Grundwerte Der Wert der [maxpatchcachesize](maxpatchcachesize.md) -Richtlinie gibt den maximalen Prozentsatz des Speicherplatzes an, der verwendet werden kann. Wenn die maxpatchcachesize-Richtlinie auf 0 festgelegt ist, werden keine zusätzlichen Dateien im baselinecache gespeichert. Wenn die Richtlinie nicht festgelegt ist, ist der Standardwert, dass maximal 10% des Speicherplatzes verwendet werden können. Wenn die Gesamtgröße des Caches den maximalen Prozentsatz des Speicherplatzes erreicht, werden keine zusätzlichen Dateien gespeichert. Die Richtlinie wirkt sich nicht auf Dateien aus, die bereits gespeichert wurden. Auch wenn das Caching deaktiviert ist, kann das Installationsprogramm vorhandene produktbaselinecaches verwenden.
-   Wenn der erste angewendete Patch die [msipatchsequence-Tabelle](msipatchsequence-table.md)umfasst, wird die Zwischenspeicherung für die Anwendung aktiviert.
-   Wenn ein Patch in der Wartungs Transaktion nicht die [msipatchsequence-Tabelle](msipatchsequence-table.md)enthält, wird die Zwischenspeicherung nur für die Anwendung aktiviert, wenn ein kleines Upgradepatch (Service Pack), das die msipatchsequence-Tabelle enthält, erfolgreich auf das Produkt angewendet wurde.
-   Generieren Sie das Patchpaket mithilfe von Tools für die Patcherstellung wie [Msimsp.exe](msimsp-exe.md) und [PATCHWIZ.DLL](patchwiz-dll.md).
-   Richten Sie für die RTM-Version der Anwendung oder für eine geringfügige Upgradeversion (Service Pack) der Anwendung immer eine Zieldatei ein. Die Ziele, die in der [Tabelle TargetImages](targetimages-table-patchwiz-dll-.md) der patcherstellungs-Eigenschaften Datei (PCP) angegeben sind, sollten produktprüf Punkte sein, die durch die ersten drei Felder der [**ProductVersion**](productversion.md) -Eigenschaft definiert werden.
-   Patches bei kleinen Update Images niemals als Ziel. Die Ziele zum Entwickeln des Patches sollten keine früheren Images für die Aktualisierung von kleinen Updates enthalten.

 

 



