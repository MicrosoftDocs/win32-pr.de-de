---
description: Das verteilte Microsoft-Programmiermodell besteht aus verschiedenen Technologien wie MSMQ, IIS, DCOM und com+. Alle diese Dienste wurden für die Verwendung durch verteilte Anwendungen konzipiert.
ms.assetid: c72bbd47-0219-40ba-a7d5-2a6b725972d0
title: Com+-Entwurfs Annahmen und-Prinzipien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7dea86c404896a3d6095d39ebd6031767f6ccdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344629"
---
# <a name="com-design-assumptions-and-principles"></a>Com+-Entwurfs Annahmen und-Prinzipien

Das verteilte Microsoft-Programmiermodell besteht aus verschiedenen Technologien wie MSMQ, IIS, DCOM und com+. Alle diese Dienste wurden für die Verwendung durch verteilte Anwendungen konzipiert.

Com+ wurde entwickelt, um die Erstellung verteilter Anwendungen zu vereinfachen. Die Gesamtarchitektur basiert auf einer Reihe von Annahmen und Prinzipien.

## <a name="assumptions"></a>Annahmen

Die Annahmen lauten wie folgt:

-   **Die COM+-Anwendung unterstützt mehrere Benutzer auf mehreren Servern.** Anders ausgedrückt: Sie entwickeln eine verteilte Anwendung, und diese mehrere Benutzer befinden sich auf unterschiedlichen Host Computern, auf denen der Code ausgeführt wird. Benutzer greifen über das Internet oder über ein privates Netzwerk auf den Code zu. Die Benutzeroberfläche wird über den Browser oder vielleicht eine benutzerdefinierte Anwendung angezeigt, z. b. eine Formular basierte Anwendung, die mit Microsoft Visual Basic oder MFC geschrieben wurde. Diese Benutzeroberfläche befindet sich auf dem Client Computer.
-   **Die COM+-Anwendung kann skalierbar gemacht werden und bietet eine höhere Verfügbarkeit und Zuverlässigkeit, indem die Anwendung auf mehreren Server Computern bereitgestellt wird.** Auf diese Weise können Sie die Arbeitsauslastung der Anwendung ausgleichen und Fehlertoleranz mithilfe von Windows-Clustering bereitstellen.
-   **Wenn ein Fehler auftritt, wird der Zustand der persistenten Daten, die in einer Datenbank gespeichert sind, in einer COM+-Anwendung beibehalten, wenn Sie Transaktionen verwenden.** Der Anwendungs Status muss Fehler überstehen, die auftreten können, wie z. b. Anwendungsfehler, Systemabstürze oder Netzwerkfehler.

## <a name="principles"></a>Prinzipien

Zusätzlich zu diesen drei Annahmen ist das COM+-Programmiermodell mit den folgenden Prinzipien zu tun:

-   **Die Anwendungslogik befindet sich auf Server Computern, nicht auf Client Computern.** Hierfür gibt es drei Hauptgründe:
    -   Der Client Computer verfügt möglicherweise nicht über die Verarbeitungsleistung oder die Features, die zum Ausführen der Anwendungslogik erforderlich sind. Außerdem wird die Bereitstellung vereinfacht, wenn die Anwendungslogik auf dem Server beibehalten wird.
    -   Die Server Computer sind häufig näher an den Daten. diese Daten befinden sich meistens in einer Datenbank. Da Ihre Anwendung auf Datenbanken zugreift, sollten Sie sehr empfindlich auf die Kosten der Datenbankverbindungen achten. Wenn Sie den größten Teil der Logik auf den Server Computern platzieren, können Sie Datenbankverbindungen freigeben und eine deutliche Leistungsverbesserung erzielen. Es gibt auch noch weitere Ressourcen auf den Server Computern, die ebenfalls gemeinsam genutzt werden können. Dies ist ein Leistungsvorteil.
    -   Wenn sich die Anwendungslogik auf Server Computern befindet, wird die Kontrolle über den Sicherheitskontext mit der Anwendung behalten. Sie haben eine bessere Kontrolle über die Sicherheit, wenn Sie diese Sicherheit auf Anwendungskomponenten aufrechterhalten, die auf Server Computern ausgeführt werden, und nicht auf Client Computern.
-   **Transaktionen sind der Kern.** In der Entwurfs Sprache durchsuchen Transaktionen das COM+-Programmiermodell so, dass es sehr wichtig ist, Sie zu verstehen. Obwohl Sie viele der com+-Dienste nutzen können, ohne Transaktionen zu verwenden, können Sie die für Sie verfügbaren com+-Dienste nicht in vollem Umfang nutzen, wenn Sie sich dafür entscheiden, Sie nicht zu verwenden. Zu den wichtigsten Vorteilen der Verwendung von Transaktionen zählen die folgenden:
    -   Transaktionen stellen eine sinnvolle Lösung für das Problem der Parallelitäts Verwaltung dar. Außerdem tragen Transaktionen zum Schutz vor Abstürzen bei und haben ein gutes Fehler Wiederherstellungs Modell. Außerdem werden Transaktionen als hervorragend für die Verwaltung von Aufgaben auf mehreren Systemen erwiesen.
    -   Sie können eine transaktionsbasierte com+-Anwendung so entwerfen, dass Sie mit einem Ressourcen-Manager und einer-Datenbank arbeitet, wodurch die meisten Zustandsinformationen geschützt werden. Wenn Sie den Zustand innerhalb einer Datenbank oder in einem anderen von einem Ressourcen-Manager verwalteten Speicher belassen, müssen Sie nicht in den eigentlichen Objekten, die von der Anwendung erstellt werden, viel Status behalten. Dies ist zwar eine Abkehr von einem reinen objektorientierten Modell, aber es eignet sich gut für die Erstellung verteilter Anwendungen mit Fehlerwiederherstellung.
-   **Die Anwendungs Funktionalität wird als COM-Objekte erstellt und umwickelt die Protokolle, die für die Kommunikation mit anderen Systemen oder Technologien verwendet werden.** Da Sie wahrscheinlich Komponenten entwickeln, die mehrere Technologien oder Legacy Systeme zusammenstellen, planen Sie die Verwendung einer Vielzahl von Kommunikationsprotokollen. Verwenden Sie http für die Kommunikation zwischen Client und Server oder die Kommunikation zwischen Anwendungen über das Internet. Verwenden Sie DCOM für die Kommunikation zwischen Anwendungen und Anwendungen auf dem Server.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Richtlinien zum Entwerfen von com+-Anwendungen](basic-guidelines-for-designing-com--applications.md)
</dt> <dt>

[Entwerfen der com+-Anwendung mithilfe von UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Allgemeine Entwurfs Tipps für die Verwendung von com+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimieren von Interaktionen mit der com+-Geschäftslogik Ebene](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



