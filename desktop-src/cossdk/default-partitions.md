---
description: Standard Partitionen
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Standard Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214286"
---
# <a name="default-partitions"></a>Standard Partitionen

Wenn einem Benutzer eine Standard Partition zugewiesen wird, versucht com+ zunächst, Komponenten in dieser Partition zu aktivieren. Wenn die Aktivierung fehlschlägt, durchsucht com+ die globale Partition nach der zu aktivierbaren Komponente. Eine Ausnahme zu diesem Vorgang tritt auf, wenn die COM+-Komponente einen partitionmoniker enthält, der explizit die Partition angibt, in der sich die Komponente befindet. In diesem Fall hat der partitionsmoniker Vorrang vor jeder standardmäßigen Partitions Konfiguration.

Wenn Sie lokale Partitionen verwenden, wird die Standard Partition Benutzern mithilfe des Ordners " **com+-Partitions Benutzer** " im Verwaltungs Programm "Komponenten Dienste" auf dem Anwendungsserver zugewiesen. Bei der Verwendung von Partitions Sätzen im Active Directory wird die Standard Partition des Benutzers durch den Partitions Satz des Benutzers bestimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lokale Partitionen](local-partitions.md)
</dt> <dt>

[Partitions Eigenschaften](partition-properties.md)
</dt> <dt>

[Partitionen und Active Directory](partitions-and-active-directory.md)
</dt> <dt>

[Die globale Partition](the-global-partition.md)
</dt> </dl>

 

 



