---
description: Beschreibt eine Festplatte, Partitionierung und den Master boot Record.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Datenträgergeräte und Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758454c9fc9e684e918646bf99869c7544b3b02c0201eb2ba507f8ffbdc303d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015373"
---
# <a name="disk-devices-and-partitions"></a>Datenträgergeräte und Partitionen

Eine Festplatte besteht aus einer Reihe von gestapelten Feldern, von denen jede Daten in konzentrierten Kreisen gespeichert oder *verfolgt.* Jede Person verfügt über zwei Kopf, einen auf jeder Seite des 30-Seitigen, der Daten liest oder schreibt, während der Datenträger sich dreht. Eine *Festplatte steuert die* Positionierung, das Lesen und Schreiben der Festplatte. Beachten Sie, dass die Kopf aller Köpfe als Einheit positioniert sind.

Die kleinste adressierbare Einheit einer Spur ist ein *Sektor.* Ein *Zylinder* ist definiert als die Gruppe von Spuren, die an der gleichen Position auf jedem Anderen angezeigt werden. Das folgende Diagramm zeigt beispielsweise eine Festplatte mit vier Datenträgern. Der Zylinder X besteht aus acht Spuren (Spur X von jeder Seite der einzelnen Titel).

![Festplatte, einschließlich Spuren, Sektoren und Scheiben](images/diskdevice.png)

Eine Festplatte kann einen oder mehrere logische Regionen enthalten, die als *Partitionen bezeichnet werden.* Partitionen werden erstellt, wenn der Benutzer eine Festplatte als *Basisdatenträger formatiert.* Windows unterstützt auch *dynamische Datenträger,* die in diesem Thema nicht behandelt werden. Weitere Informationen zu Basisdatenträgern und dynamischen Datenträgern finden Sie unter [Basic und Dynamic Disks](basic-and-dynamic-disks.md).

Die Erstellung mehrerer Partitionen auf einem Datenträger ermöglicht das Aussehen separater Festplatten. Beispielsweise enthält ein System mit einer Festplatte mit einer Partition ein einzelnes Volume, das vom System als Laufwerk C festgelegt wird. Ein System mit einer Festplatte mit zwei Partitionen enthält in der Regel die Laufwerke C und D. Die Verwendung mehrerer Partitionen auf einer Festplatte kann die Verwaltung des Systems vereinfachen, z. B. das Organisieren von Dateien oder die Unterstützung mehrerer Benutzer.

Der erste physische Sektor auf einem Basisdatenträger enthält eine Datenstruktur, die als Master Boot Record (MBR) bekannt ist. Die MBR enthält Folgendes:

-   Ein Startprogramm (bis zu 442 Byte groß)
-   Eine Datenträgersignatur (eine eindeutige 4-Byte-Zahl)
-   Eine Partitionstabelle (bis zu vier Einträge)
-   Ein MbR-Endemarker (immer 0x55AA)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Volumeverwaltung](about-volume-management.md)
</dt> <dt>

[Basisdatenträger und dynamische Datenträger](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



