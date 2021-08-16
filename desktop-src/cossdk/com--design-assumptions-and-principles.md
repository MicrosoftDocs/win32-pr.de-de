---
description: Das verteilte Programmiermodell von Microsoft besteht aus mehreren Technologien, einschließlich MSMQ, IIS, DCOM und COM+. Alle diese Dienste wurden für die Verwendung durch verteilte Anwendungen entwickelt.
ms.assetid: c72bbd47-0219-40ba-a7d5-2a6b725972d0
title: COM+-Entwurfsannahmen und -prinzipien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b87c5ae631cd5517b215efae3a09968649cd49ea94fe33b33d9b826082e911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549395"
---
# <a name="com-design-assumptions-and-principles"></a>COM+-Entwurfsannahmen und -prinzipien

Das verteilte Programmiermodell von Microsoft besteht aus mehreren Technologien, einschließlich MSMQ, IIS, DCOM und COM+. Alle diese Dienste wurden für die Verwendung durch verteilte Anwendungen entwickelt.

COM+ wurde entwickelt, um die Erstellung verteilter Anwendungen zu vereinfachen. Die Gesamtarchitektur basiert auf einer Reihe von Annahmen und Prinzipien.

## <a name="assumptions"></a>Annahmen

Die Annahmen lauten wie folgt:

-   **Die COM+-Anwendung unterstützt mehrere Benutzer auf mehreren Servern.** Anders ausgedrückt: Sie erstellen eine verteilte Anwendung, und diese benutzer werden sich auf verschiedenen Hostcomputern befinden, auf denen der Code ausgeführt wird. Benutzer greifen über das Internet oder über ein privates Netzwerk auf den Code zu. Die Benutzeroberfläche wird über den Browser oder vielleicht eine benutzerdefinierte Anwendung dargestellt, z. B. eine formularbasierte Anwendung, die mit Microsoft Visual Basic MFC geschrieben wurde. Diese Benutzeroberfläche wird sich auf dem Clientcomputer befinden.
-   **Die COM+-Anwendung kann skalierbar gemacht werden und eine höhere Verfügbarkeit und Zuverlässigkeit bieten, indem die Anwendung auf mehreren Servercomputern bereitgestellt wird.** Dadurch können Sie die Workload der Anwendung ausgleichen und fehlertoleranz bereitstellen, indem Windows Clustering verwenden.
-   **Wenn ein Fehler auftritt, wird der Status der in einer Datenbank gespeicherten persistenten Daten aus einer COM+-Anwendung beibehalten, wenn Sie Transaktionen verwenden.** Der Anwendungszustand muss das Auftreten von Ausfällen überstehen, z. B. Anwendungsfehler, Systemabstürze oder Netzwerkfehler.

## <a name="principles"></a>Prinzipien

Zusätzlich zu diesen drei Annahmen gelten die folgenden Prinzipien für das COM+-Programmiermodell:

-   **Die Anwendungslogik befindet sich auf Servercomputern, nicht auf Clientcomputern.** Hierfür gibt es drei Hauptgründe:
    -   Der Clientcomputer verfügt möglicherweise nicht über die Verarbeitungsleistung oder die Funktionen, die zum Ausführen der Anwendungslogik erforderlich sind. Darüber hinaus vereinfacht die Beibehaltung der Anwendungslogik auf dem Server die Bereitstellung.
    -   Die Servercomputer sind häufig näher an den Daten, und diese Daten befinden sich am häufigsten in einer Datenbank. Da Ihre Anwendung auf Datenbanken zutritt, möchten Sie sehr empfindlich auf die Kosten von Datenbankverbindungen reagieren. Wenn Sie den Großteil der Logik auf den Servercomputern speichern, können Sie Datenbankverbindungen freigeben und eine erhebliche Leistungsverbesserung erzielen. Es gibt weitere Ressourcen auf den Servercomputern, die auch gemeinsam genutzt werden können, wiederum mit einem Leistungsvorteil.
    -   Die Anwendungslogik auf Servercomputern behält die Kontrolle über den Sicherheitskontext mit der Anwendung. Sie haben mehr Kontrolle über die Sicherheit, wenn Sie diese Sicherheit auf Anwendungskomponenten behalten, die auf Servercomputern und nicht auf Clientcomputern ausgeführt werden.
-   **Transaktionen sind der Kern.** Transaktionen durchdringen das COM+-Programmiermodell so stark, dass Es für Sie sehr wichtig ist, sie zu verstehen. Sie können zwar viele der Com+-Dienste nutzen, ohne Transaktionen zu verwenden, aber wenn Sie sich dafür entscheiden, sie nicht zu verwenden, können Sie die com+-Dienste, die Ihnen zur Verfügung stehen, nicht vollständig nutzen. Zu den wichtigen Vorteilen der Verwendung von Transaktionen gehören die folgenden:
    -   Transaktionen sind eine sinnvolle Lösung für das Problem der Parallelitätsverwaltung. Darüber hinaus tragen Transaktionen zum Schutz vor Abstürzen bei und verfügen über ein gutes Fehlerwiederherstellungsmodell. Darüber hinaus sind Transaktionen eine hervorragende Möglichkeit, Aufgaben über mehrere Systeme hinweg zu verwalten.
    -   Sie können eine transaktionsbasierte COM+-Anwendung so entwerfen, dass sie mit einem Ressourcen-Manager und einer Datenbank zusammenarbeiten kann, wodurch die meisten Zustandsinformationen geschützt werden. Wenn Sie den Zustand in einer Datenbank oder einem anderen Speicher, der von einem Ressourcen-Manager verwaltet wird, speichern, müssen Sie nicht viel Zustand in den tatsächlichen Objekten behalten, die Ihre Anwendung erstellt. Obwohl dies ein Abkehr von einem rein objektorientierten Modell ist, funktioniert es gut zum Erstellen verteilter Anwendungen mit Fehlerwiederherstellung.
-   **Anwendungsfunktionen werden als COM-Objekte erstellt und umschließen die Protokolle, die für die Kommunikation mit anderen Systemen oder Technologien verwendet werden.** Da Sie wahrscheinlich Komponenten erstellen, die mehrere Technologien oder Legacysysteme zusammenbringen werden, planen Sie die Verwendung einer Vielzahl von Kommunikationsprotokollen. Verwenden Sie HTTP für die Client-/Serverkommunikation oder die Kommunikation zwischen Anwendungen über das Internet. Verwenden Sie DCOM für die Kommunikation zwischen Anwendungen oder Komponenten auf dem Server.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Richtlinien für das Entwerfen von COM+-Anwendungen](basic-guidelines-for-designing-com--applications.md)
</dt> <dt>

[Entwerfen der COM+-Anwendung mit UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Allgemeine Entwurfs Tipps für die Verwendung von COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimieren von Interaktionen mit der COM+-Geschäftslogikebene](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Andere Microsoft-Tools zum Erstellen verteilter Anwendungen](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



