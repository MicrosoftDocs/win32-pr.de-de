---
description: Beschreibt eine Festplatte, Partitionierung und den Master Boot Record.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Datenträger Geräte und Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553702"
---
# <a name="disk-devices-and-partitions"></a>Datenträger Geräte und Partitionen

Eine Festplatte besteht aus einem Satz von gestapelten platzern, von denen jede Daten in konzentrischen Kreisen oder nach *verfolgt*. Jede Platte verfügt über zwei Köpfe, eine auf jeder Seite der Platte, die Daten während des Datenträgers liest oder schreibt. Ein *Festplattenlaufwerk* steuert die Positionierung, das Lesen und Schreiben der Festplatte. Beachten Sie, dass die Köpfe aller Scheiben als Einheit positioniert werden.

Die kleinste adressierbare Einheit einer Spur ist ein *Sektor*. Ein *Zylinder* ist als Satz von Spuren definiert, die an derselben Position auf jeder Platte angezeigt werden. Im folgenden Diagramm wird z. b. eine Festplatte mit vier platzern angezeigt. Zylinder x besteht aus acht Spuren (Nachverfolgung x von jeder Seite jeder Platte).

![Festplatte, einschließlich Spuren, Sektoren und platzern](images/diskdevice.png)

Eine Festplatte kann eine oder mehrere logische Regionen enthalten, die als *Partitionen* bezeichnet werden. Partitionen werden erstellt, wenn der Benutzer eine Festplatte als *Basis* Datenträger formatiert. Windows unterstützt auch *dynamische* Datenträger, die in diesem Thema nicht erläutert werden. Weitere Informationen zu Basis Datenträgern und dynamischen Datenträgern finden Sie unter [Basic und Dynamic Disks](basic-and-dynamic-disks.md).

Die Erstellung mehrerer Partitionen auf einem Datenträger ermöglicht das Aussehen von separaten Festplatten. Beispielsweise enthält ein System mit einer Festplatte, die über eine Partition verfügt, ein einzelnes Volume, das vom System als Laufwerk C festgelegt wird. Ein System mit einer Festplatte mit zwei Partitionen enthält normalerweise die Laufwerke C und D. Wenn mehrere Partitionen auf einer Festplatte vorhanden sind, kann es einfacher sein, das System zu verwalten, z. b. zum Organisieren von Dateien oder zur Unterstützung mehrerer Benutzer.

Der erste physische Sektor auf einem Basis Datenträger enthält eine Datenstruktur, die als Master Boot Record (MBR) bezeichnet wird. Der MBR enthält Folgendes:

-   Ein Start Programm (bis zu 442 Bytes groß)
-   Eine Datenträger Signatur (eine eindeutige 4-Byte-Zahl)
-   Eine Partitionstabelle (bis zu vier Einträge)
-   Ein End-of-MBR-Marker (immer 0x55aa)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Volumeverwaltung](about-volume-management.md)
</dt> <dt>

[Basis-und dynamische Datenträger](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



