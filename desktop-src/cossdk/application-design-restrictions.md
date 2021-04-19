---
description: Einige Anwendungen sind so konzipiert, dass mehrere Instanzen der Anwendung auf einem Computer installiert werden.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Einschränkungen beim Anwendungs Entwurf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344954"
---
# <a name="application-design-restrictions"></a>Einschränkungen beim Anwendungs Entwurf

Einige Anwendungen sind so konzipiert, dass mehrere Instanzen der Anwendung auf einem Computer installiert werden. Mit einer solchen Einschränkung kann eine Anwendung die Partitions Funktion nicht verwenden. Die folgenden Anwendungs Entwurfs Features müssen möglicherweise geändert werden, bevor Partitionen für diese Anwendung verwendet werden können.

## <a name="tables-and-arrays"></a>Tabellen und Arrays

Einige Anwendungen erstellen Datenbanktabellen, in-Memory-Tabellen oder Arrays, die eine CLSID als eindeutigen Registrierungsschlüssel verwenden. Auf einem Computer ohne Partitionen lautet dieser Registrierungsschlüssel in der Regel Computer/CLSID (eine CLSID pro Computer).

Umgekehrt ist dieser Registrierungsschlüssel auf einem Computer mit Partitionen der Computer/Partitions-ID/Anwendungs-ID/CLSID (mehrere Instanzen einer CLSID pro Computer). Da mit der Partitions Funktion mehrere Instanzen einer CLSID auf einem Computer vorhanden sein können, können Anwendungen, die Entwurfs Elemente enthalten, die eine eindeutige CLSID pro Computer erfordern, beeinträchtigt werden.

## <a name="global-resources"></a>Globale Ressourcen

Einige Anwendungen verwenden globale Ressourcen wie freigegebenen Arbeitsspeicher, Datendateien und Registrierungseinträge. Dies kann zu Problemen führen, wenn mehrere Instanzen einer solchen Anwendung gleichzeitig ausgeführt werden.

Wenn eine Komponente z. b. gemeinsam genutzten Speicher für die Interaktion mit anderen Komponenten verwendet, muss die Komponente so geändert werden, dass jede Instanz der Komponente ihren eigenen gemeinsam genutzten Speicher zuordnet.

## <a name="type-libraries"></a>Typbibliotheken

Typbibliotheken stellen Informationen über die Schnittstellen und Methoden einer Komponente bereit. Diese Informationen werden für verschiedene Zwecke verwendet, einschließlich der folgenden:

-   Marshalling von Daten zwischen Komponenten, wenn Funktionsaufrufe durchgeführt werden
-   Unterstützung der COM+-Komponenten in der Warteschlange und der com+-Ereignis Dienste
-   Bereitstellen der richtigen Informationen in einem Microsoft Visual Basic-Editor

Verweise auf eine Typbibliothek werden in der Registrierung eines Computers installiert. Beim Entwickeln von Anwendungen, die in Partitionen aufgerufen werden, ist es wichtig, dass die aktuelle Version einer Typbibliothek in der Registrierung installiert ist. Dadurch wird sichergestellt, dass der verwendete Visual Basic-Editor genaue Informationen zu den Methoden erhält, die für diese Komponente verfügbar sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponenten und Partitionen in der com+-Warteschlange](com--queued-components-and-partitions.md)
</dt> <dt>

[Partitions Implementierung](partition-implementation.md)
</dt> <dt>

[Registrieren und Aktivieren von Komponenten in Partitionen](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Was sind COM+-Partitionen?](what-are-com--partitions-.md)
</dt> </dl>

 

 



