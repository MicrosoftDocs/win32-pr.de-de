---
description: Bei der Installation auf einem Anwendungsserver erstellt com+ automatisch eine Partition, die als globale Partition bezeichnet wird.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Partitions Implementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343998"
---
# <a name="partition-implementation"></a>Partitions Implementierung

Bei der Installation auf einem Anwendungsserver erstellt com+ automatisch eine Partition, die als *globale Partition* bezeichnet wird. Die globale Partition enthält einen Standardsatz von com+-Anwendungen. Com+-Anwendungen, die in der globalen Partition installiert werden, sind automatisch für alle Benutzer auf dem Server verfügbar. Wenn Sie andere com+-Anwendungen haben, die Sie allen Benutzern auf dem Server zur Verfügung stellen möchten, können Sie Sie der globalen Partition hinzufügen.

Neben der globalen Partition können Sie auch andere Partitionen für Benutzer auf diesem Server oder für Benutzer in der gesamten Domäne erstellen. Wenn Sie zusätzliche Partitionen erstellen und mehrere Konfigurationen einer COM+-Anwendung installieren, können die Benutzer diese Anwendungs Konfigurationen gleichzeitig auf demselben Computer ausführen. Außerdem können Sie den Benutzer Zugriff auf diese Anwendungen steuern, indem Sie com+-Anwendungen in einer anderen Partition als der globalen Partition installieren.

**Windows XP:** Die Möglichkeit, com+-Partitionen zu erstellen, zu konfigurieren oder zu delegieren, ist nicht verfügbar. Die globale Partition ist die einzige verfügbare com+-Partition.

Weitere Informationen zu lokalen Partitionen und Partitionen, die in Active Directory definiert sind, finden Sie in den folgenden Themen:

-   [Lokale Partitionen](local-partitions.md)
-   [Partitionen und Active Directory](partitions-and-active-directory.md)
-   [Standard Partitionen](default-partitions.md)
-   [Die globale Partition](the-global-partition.md)
-   [Partitions Eigenschaften](partition-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen beim Anwendungs Entwurf](application-design-restrictions.md)
</dt> <dt>

[Komponenten und Partitionen in der com+-Warteschlange](com--queued-components-and-partitions.md)
</dt> <dt>

[Registrieren und Aktivieren von Komponenten in Partitionen](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Was sind COM+-Partitionen?](what-are-com--partitions-.md)
</dt> </dl>

 

 



