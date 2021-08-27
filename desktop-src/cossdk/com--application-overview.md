---
description: Eine COM+-Anwendung ist die primäre Verwaltungs- und Sicherheitseinheit für Komponentendienste und besteht aus einer Gruppe von COM-Komponenten, die im Allgemeinen verwandte Funktionen ausführen.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Übersicht über COM+-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c964d760b5ba0ef260bc9dcb0658b564a4b211075692ce6301a0445eee0eb7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991875"
---
# <a name="com-application-overview"></a>Übersicht über COM+-Anwendungen

Eine COM+-Anwendung ist die primäre Verwaltungs- und Sicherheitseinheit für Komponentendienste und besteht aus einer Gruppe von COM-Komponenten, die im Allgemeinen verwandte Funktionen ausführen. Diese Komponenten bestehen weiter aus Schnittstellen und Methoden, wie in der folgenden Abbildung dargestellt.

![Diagramm, das Schnittstellen und Methoden in Feldern in der Reihenfolge methode innerhalb der Schnittstelle innerhalb der Komponente in COM+-Anwendung zeigt.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

Sie können das Verwaltungstool komponentendienste verwenden, um neue COM+-Anwendungen zu erstellen, Anwendungen Komponenten hinzuzufügen und die Attribute für eine Anwendung und deren Komponenten festlegen.

Indem Sie logische Gruppen von COM-Komponenten als COM+-Anwendungen erstellen, können Sie die folgenden Vorteile von COM+ nutzen:

-   Ein Bereitstellungsbereich für COM-Komponenten.
-   Ein gemeinsamer Konfigurationsumfang für COM-Komponenten, einschließlich Sicherheitsgrenzen und Warteschlangen.
-   Storage Komponentenattribute, die nicht vom Komponentenentwickler bereitgestellt werden (z. B. Transaktionen und Synchronisierung).
-   Komponenten-DLLs (Dynamic Link Libraries), die bei Bedarf in Prozesse (DLLHost.exe) geladen werden.
-   Verwaltete Serverprozesse zum Hosten von Komponenten.
-   Erstellung und Verwaltung von Threads, die von Komponenten verwendet werden.
-   Zugriff auf das Kontextobjekt für Ressourcenspender, sodass erworbene Ressourcen automatisch dem Kontext zugeordnet werden können. (Weitere Informationen zu COM-Komponenten und -Kontexten finden Sie unter [COM+-Kontexte.)](com--contexts.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von COM+-Anwendungen](developing-com--applications.md)
</dt> <dt>

[Teile einer COM+-Anwendung](parts-of-a-com--application.md)
</dt> <dt>

[Typen von COM+-Anwendungen](types-of-com--applications.md)
</dt> </dl>

 

 



