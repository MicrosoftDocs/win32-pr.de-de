---
description: Eine COM+-Anwendung ist die primäre Verwaltungs-und Sicherheitseinheit für Komponenten Dienste und besteht aus einer Gruppe von COM-Komponenten, die im allgemeinen verwandte Funktionen ausführen.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Übersicht über die COM+-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "106349753"
---
# <a name="com-application-overview"></a>Übersicht über die COM+-Anwendung

Eine COM+-Anwendung ist die primäre Verwaltungs-und Sicherheitseinheit für Komponenten Dienste und besteht aus einer Gruppe von COM-Komponenten, die im allgemeinen verwandte Funktionen ausführen. Diese Komponenten bestehen weiter aus Schnittstellen und Methoden, wie in der folgenden Abbildung dargestellt.

![Diagramm, das Schnittstellen und Methoden innerhalb von Feldern anzeigt, in der Reihenfolge der Methode innerhalb der Komponente innerhalb der com+-Anwendung.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

Mit dem Verwaltungs Programmkomponenten Dienste können Sie neue COM+-Anwendungen erstellen, Anwendungen Komponenten hinzufügen und die Attribute für eine Anwendung und deren Komponenten festlegen.

Indem Sie logische Gruppen von COM-Komponenten als com+-Anwendungen erstellen, können Sie die folgenden Vorteile von com+ nutzen:

-   Einen Bereitstellungs Bereich für COM-Komponenten.
-   Einen allgemeinen Konfigurationsbereich für COM-Komponenten, einschließlich Sicherheitsgrenzen und Warteschlangen.
-   Speicherung von Komponenten Attributen, die nicht vom Komponenten Entwickler bereitgestellt werden (z. b. Transaktionen und Synchronisierung).
-   Komponenten-DLLs (Dynamic-Link Libraries), die bei Bedarf in Prozesse (DLLHost.exe) geladen werden.
-   Verwaltete Server Prozesse zum Hosten von-Komponenten.
-   Erstellung und Verwaltung von Threads, die von-Komponenten verwendet werden.
-   Zugriff auf das Kontext Objekt für Ressourcen Spender, sodass die zugeordneten Ressourcen automatisch dem Kontext zugeordnet werden können. (Weitere Informationen zu COM-Komponenten und Kontexten finden Sie unter [com+-Kontexte](com--contexts.md).)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von com+-Anwendungen](developing-com--applications.md)
</dt> <dt>

[Teile einer COM+-Anwendung](parts-of-a-com--application.md)
</dt> <dt>

[Typen von com+-Anwendungen](types-of-com--applications.md)
</dt> </dl>

 

 



