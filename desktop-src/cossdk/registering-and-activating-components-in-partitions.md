---
description: Registrieren und Aktivieren von Komponenten in Partitionen
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registrieren und Aktivieren von Komponenten in Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523531"
---
# <a name="registering-and-activating-components-in-partitions"></a>Registrieren und Aktivieren von Komponenten in Partitionen

Nachdem eine Partition erstellt wurde, ist der nächste Schritt das Registrieren der COM+-Komponenten innerhalb dieser Partition. Eine Komponente wird in einer Partition registriert, wenn eine neue COM+-Anwendung erstellt wird oder wenn eine vorhandene COM+-Anwendung in der Partition installiert wird. Um die Verwaltung der Registrierung zu vereinfachen, wenn mehrere Partitionen die gleichen com+-Komponenten enthalten, ermöglicht der Partitions Dienst einem Administrator, Anwendungen oder Komponenten aus einer Partition in eine andere zu kopieren. Wenn eine COM+-Anwendung oder eine Komponente kopiert wird, werden alle zugeordneten Partitions Eigenschaften mit dem Element kopiert, mit Ausnahme der Identität der Anwendung oder der Mitglieder einer Rolle.

Wenn das Client Programm die Funktion [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) aufruft, um ein Objekt zu instanziieren, führt com+ wie folgt zwei unterschiedliche Schritte aus:

1.  Lokalisiert die Partition, in der sich die Komponente befindet.
2.  Gibt die richtige Komponente innerhalb dieser Partition an.

In den folgenden Themen dieses Abschnitts werden diese Schritte ausführlich beschrieben:

-   [Suchen von Partitionen während der Aktivierung](locating-partitions-during-activation.md)
-   [Suchen einer Komponente zur Aktivierung](locating-a-component-for-activation.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen beim Anwendungs Entwurf](application-design-restrictions.md)
</dt> <dt>

[Komponenten und Partitionen in der com+-Warteschlange](com--queued-components-and-partitions.md)
</dt> <dt>

[Partitions Implementierung](partition-implementation.md)
</dt> <dt>

[Was sind COM+-Partitionen?](what-are-com--partitions-.md)
</dt> </dl>

 

 
