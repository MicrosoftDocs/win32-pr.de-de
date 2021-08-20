---
description: Bei der Installation auf einem Anwendungsserver erstellt COM+ automatisch eine Partition, die als globale Partition bezeichnet wird.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Partitionsimplementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3014aac80e853ca387538faf034eeadae91dd70cf36931de34638cbcbec7b02f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047348"
---
# <a name="partition-implementation"></a>Partitionsimplementierung

Bei der Installation auf einem Anwendungsserver erstellt COM+ automatisch eine Partition, die als *globale Partition* bezeichnet wird. Die globale Partition enthält einen Standardsatz von COM+-Anwendungen. COM+-Anwendungen, die in der globalen Partition installiert sind, sind automatisch für alle Benutzer auf dem Server verfügbar. Wenn Sie über andere COM+-Anwendungen verfügen, die Sie allen Benutzern auf dem Server zur Verfügung stellen möchten, können Sie sie der globalen Partition hinzufügen.

Zusätzlich zur globalen Partition können Sie andere Partitionen nur für Benutzer auf diesem Server oder für Benutzer in der gesamten Domäne erstellen. Durch das Erstellen zusätzlicher Partitionen und das Installieren mehrerer Konfigurationen einer COM+-Anwendung können Ihre Benutzer diese Anwendungskonfigurationen gleichzeitig auf demselben Computer ausführen. Außerdem können Sie den Benutzerzugriff auf diese Anwendungen steuern, indem Sie COM+-Anwendungen in einer anderen Partition als der globalen Partition installieren.

**Windows XP:** Com+-Partitionen können nicht erstellt, konfiguriert oder delegiert werden. Die globale Partition ist die einzige verfügbare COM+-Partition.

Weitere Informationen zu lokalen Partitionen und Partitionen, die in Active Directory definiert sind, finden Sie in den folgenden Themen:

-   [Lokale Partitionen](local-partitions.md)
-   [Partitionen und Active Directory](partitions-and-active-directory.md)
-   [Standardpartitionen](default-partitions.md)
-   [Die globale Partition](the-global-partition.md)
-   [Partitionseigenschaften](partition-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen beim Anwendungsentwurf](application-design-restrictions.md)
</dt> <dt>

[COM+-Komponenten und -Partitionen in der Warteschlange](com--queued-components-and-partitions.md)
</dt> <dt>

[Registrieren und Aktivieren von Komponenten in Partitionen](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Was sind COM+-Partitionen?](what-are-com--partitions-.md)
</dt> </dl>

 

 



