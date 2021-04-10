---
description: Grundlegende Richtlinien zum Entwerfen von com+-Anwendungen
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Grundlegende Richtlinien zum Entwerfen von com+-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127161"
---
# <a name="basic-guidelines-for-designing-com-applications"></a>Grundlegende Richtlinien zum Entwerfen von com+-Anwendungen

Um com+ in vollem Umfang nutzen zu können, gibt es einige grundlegende Richtlinien, die Sie beim Erstellen einer Anwendung verwenden können:

-   **Modellieren Sie Ihren permanenten Zustand als Datenbankschema, indem Sie das gewünschte Daten Bank Tool verwenden.** Fast jede Anwendung muss einen permanenten Zustand aufrechterhalten. Datenbanken stellen die Dienste bereit, die zum Erstellen dauerhafter und skalierbarer Speicher Zustands erforderlich sind. Der erste Schritt beim Erstellen einer COM+-Anwendung besteht daher darin, den permanenten Zustand Ihrer Anwendung als eine Art Datenbankschema zu modellieren. Es spielt keine Rolle, welche Datenbank Sie verwenden; die meisten kommerziellen Datenbanken sind mit com+ kompatibel. Microsoft SQL Server ist ein gutes Beispiel für eine Lösung, die Sie verwenden können.

-   **Modellieren Sie die Logik der com+-Anwendung als Satz von COM-Schnittstellen.** Wenn Sie über ein Schema verfügen, das die Zustandsinformationen der Anwendung darstellt, modellieren Sie die Austausch Vorgänge in der Anwendung als COM-Schnittstellen. Diese Schnittstellen modellieren das Verhalten der Anwendung. Dies ist auch die Entwicklungsphase, wenn Sie bestimmen möchten, welche com+-Dienste für Ihre Anwendung am besten geeignet sind.

-   **Buildkomponentendlls, die Komponenten enthalten, die das physische Datenschema verwenden, und eine logische Ansicht der Daten für andere Komponenten (das erste Element in dieser Liste) verfügbar machen, sowie Komponenten, die in Bezug auf das logische Datenmodell (das zweite Element in dieser Liste) implementiert werden.** Sobald Sie die Struktur der Logik und die Zustandsinformationen haben, können Sie mit dem Schreiben von Code beginnen und nun dll-basierte com-Komponenten schreiben, die die Schnittstellen im Hinblick auf das definierte Schema implementieren. Ihre Komponenten fungieren einfach als Manipulatoren zum Arbeiten mit ihren Datenbankinformationen, und mit ihren Komponenten-DLLs können Sie eine COM+-Anwendung erstellen, die funktioniert und erfolgreich skaliert werden kann.

-   **Stellen Sie die Komponenten in der com+-Umgebung mithilfe der com+-Dienste bereit, die Sie ausgewählt haben.** Nachdem Sie die Anwendung erstellt haben, können Sie die Anwendung in einem Netzwerk oder einem Server Cluster bereitstellen. Sie können jetzt auf der Grundlage der verfügbaren ressourcenentscheidungen treffen, und Sie können jede Komponente für maximale Leistung anpassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Entwurfs Annahmen und-Prinzipien](com--design-assumptions-and-principles.md)
</dt> <dt>

[Entwerfen der com+-Anwendung mithilfe von UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Allgemeine Entwurfs Tipps für die Verwendung von com+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimieren von Interaktionen mit der com+-Geschäftslogik Ebene](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



