---
description: Registrieren und Aktivieren von Komponenten in Partitionen
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registrieren und Aktivieren von Komponenten in Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf17787c953e3fe615432a8100fa71390e8aa3b8c90453a310813207ba5df7fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547062"
---
# <a name="registering-and-activating-components-in-partitions"></a>Registrieren und Aktivieren von Komponenten in Partitionen

Nachdem eine Partition erstellt wurde, registrieren Sie im nächsten Schritt Ihre COM+-Komponenten in dieser Partition. Eine Komponente wird innerhalb einer Partition registriert, wenn eine neue COM+-Anwendung erstellt wird oder wenn eine vorhandene COM+-Anwendung in der Partition installiert wird. Um die Verwaltung der Registrierung zu erleichtern, wenn mehrere Partitionen die gleichen COM+-Komponenten enthalten, ermöglicht der Partitionsdienst einem Administrator das Kopieren von Anwendungen oder Komponenten aus einer Partition in eine andere. Wenn eine COM+-Anwendung oder eine Komponente kopiert wird, werden alle zugeordneten Partitionseigenschaften mit ausnahme der Identität der Anwendung oder eines der Mitglieder einer Rolle kopiert.

Wenn das Clientprogramm die [**CoCreateInstance-**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**CoGetObject-Funktion**](/windows/desktop/api/objbase/nf-objbase-cogetobject) aufruft, um ein Objekt zu instanziieren, führt COM+ wie folgt zwei unterschiedliche Schritte aus:

1.  Sucht die Partition, in der sich die Komponente befindet.
2.  Sucht die richtige Komponente innerhalb dieser Partition.

In den folgenden Themen in diesem Abschnitt werden diese Schritte ausführlich beschrieben:

-   [Suchen von Partitionen während der Aktivierung](locating-partitions-during-activation.md)
-   [Suchen einer Komponente für die Aktivierung](locating-a-component-for-activation.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsentwurfseinschränkungen](application-design-restrictions.md)
</dt> <dt>

[KOMPONENTEN und Partitionen in DER COM+-Warteschlange](com--queued-components-and-partitions.md)
</dt> <dt>

[Partitionsimplementierung](partition-implementation.md)
</dt> <dt>

[Was sind COM+-Partitionen?](what-are-com--partitions-.md)
</dt> </dl>

 

 
