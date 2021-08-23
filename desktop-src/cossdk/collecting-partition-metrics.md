---
description: Sammeln von Partitionsmetriken
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Sammeln von Partitionsmetriken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8168972a0bac0b4eb79c5adde3530d1a0673469adff6b66b4c1b31cc6446bca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047687"
---
# <a name="collecting-partition-metrics"></a>Sammeln von Partitionsmetriken

In einigen Fällen möchte eine Organisation möglicherweise Informationen zur VERWENDUNG VON COM+-Anwendungen für die Überwachung, Kapazitätsplanung und Ressourcenbuchhaltung sammeln.

Beispielsweise kann ein Anwendungsdienstanbieter (Application Service Provider, ASP) einen Kunden für seine Ressourcennutzung in Rechnung stellen. Hierzu können Sie mit COM+ Ereignis- und Metrikinformationen pro Partition erfassen.

Sie können diese Informationen für eine bestimmte Partition sammeln, indem Sie für jede COM+-Instrumentierungsschnittstelle den Partitions-ID-Member innerhalb der Standardereignisstruktur angeben. Die Ereignisstruktur ist der erste Wert einer COM+-Instrumentierungsschnittstelle. Weitere Informationen finden Sie unter [COM+-Instrumentierungsschnittstellen.](com--instrumentation-interfaces.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren des Partitionscaches](configuring-the-partition-cache.md)
</dt> <dt>

[Gruppieren von Anwendungen in Partitionen](grouping-applications-into-partitions.md)
</dt> <dt>

[Verwalten lokaler Partitionen](managing-local-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



