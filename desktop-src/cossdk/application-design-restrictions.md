---
description: Einige Anwendungen sind so konzipiert, dass verhindert wird, dass mehrere Instanzen der Anwendung auf einem Computer installiert werden.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Einschränkungen beim Anwendungsentwurf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b98e7b7d8dddf1cd74224573d355e1f42d75c8ae6122d20977bbc1b38ffb99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917544"
---
# <a name="application-design-restrictions"></a>Einschränkungen beim Anwendungsentwurf

Einige Anwendungen sind so konzipiert, dass verhindert wird, dass mehrere Instanzen der Anwendung auf einem Computer installiert werden. Mit einer solchen Einschränkung kann eine Anwendung das Partitionsfeature nicht nutzen. Die folgenden Anwendungsentwurfsfunktionen müssen möglicherweise geändert werden, bevor Partitionen für diese Anwendung verwendet werden können.

## <a name="tables-and-arrays"></a>Tabellen und Arrays

Einige Anwendungen erstellen Datenbanktabellen, In-Memory-Tabellen oder Arrays, die eine CLSID als eindeutigen Registrierungsschlüssel verwenden. Auf einem Computer ohne Partitionen ist dieser Registrierungsschlüssel in der Regel Computer-/CLSID (eine CLSID pro Computer).

Umgekehrt lautet dieser Registrierungsschlüssel auf einem Computer mit Partitionen Computer-/Partitions-ID/Anwendungs-ID/CLSID (mehrere Instanzen einer CLSID pro Computer). Da das Partitionsfeature mehrere Instanzen einer CLSID auf einem Computer zulässt, können Anwendungen, die Entwurfselemente enthalten, die eine eindeutige CLSID pro Computer erfordern, beeinträchtigt werden.

## <a name="global-resources"></a>Globale Ressourcen

Einige Anwendungen verwenden globale Ressourcen wie freigegebenen Arbeitsspeicher, Datendateien und Registrierungseinträge. Dies kann zu Problemen führen, wenn mehrere Instanzen einer solchen Anwendung gleichzeitig ausgeführt werden.

Wenn eine Komponente beispielsweise freigegebenen Arbeitsspeicher für die Interaktion mit anderen Komponenten verwendet, muss die Komponente so geändert werden, dass jede Instanz der Komponente ihren eigenen freigegebenen Arbeitsspeicher zuweist.

## <a name="type-libraries"></a>Typbibliotheken

Typbibliotheken stellen Informationen zu den Schnittstellen und Methoden einer Komponente bereit. Diese Informationen werden für verschiedene Zwecke verwendet, einschließlich der folgenden:

-   Marshallen von Daten zwischen Komponenten, wenn Funktionsaufrufe erfolgen
-   Unterstützung der COM+-Komponenten in der Warteschlange und der COM+-Ereignisdienste
-   Bereitstellen der richtigen Informationen in einem Microsoft Visual Basic-Editor

Verweise auf eine Typbibliothek werden in der Registrierung eines Computers installiert. Beim Entwickeln von Anwendungen, die innerhalb von Partitionen aufgerufen werden, ist es wichtig, dass die neueste Version einer Typbibliothek in der Registrierung installiert ist. Dadurch wird sichergestellt, dass der verwendete Visual Basic-Editor genaue Informationen zu den methoden erhält, die für diese Komponente verfügbar sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Komponenten und -Partitionen in der Warteschlange](com--queued-components-and-partitions.md)
</dt> <dt>

[Partitionsimplementierung](partition-implementation.md)
</dt> <dt>

[Registrieren und Aktivieren von Komponenten in Partitionen](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Was sind COM+-Partitionen?](what-are-com--partitions-.md)
</dt> </dl>

 

 



