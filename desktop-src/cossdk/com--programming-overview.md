---
description: Com+ bietet eine Unternehmens Entwicklungsumgebung, die auf dem Microsoft-Component Object Model (com) basiert, um komponentenbasierte, verteilte Anwendungen zu erstellen.
ms.assetid: 141982d4-1e6c-4f01-8b0e-8b94f20dd82c
title: Übersicht über die COM+-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c225b5ebb6f04f74d6071dc0305d219993fa606e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748073"
---
# <a name="com-programming-overview"></a>Übersicht über die COM+-Programmierung

Com+ bietet eine Unternehmens Entwicklungsumgebung, die auf dem Microsoft-Component Object Model (com) basiert, um komponentenbasierte, verteilte Anwendungen zu erstellen. Außerdem stehen Ihnen die Tools zum Erstellen von transaktionalen Anwendungen mit mehreren Ebenen zur Verfügung. Com+ kombiniert Erweiterungen der herkömmlichen COM-basierten Entwicklung mit vielen nützlichen Programmierungs-und Verwaltungsdiensten. Eine umfassende Liste dieser Dienste finden Sie unter [com+-Dienste](com--services.md) .

Zu den com-Erweiterungen gehören Verbesserungen beim Threading und der Sicherheit sowie die Einführung der Synchronisierungs Dienste. Die Dienste umfassen das Verwaltungs Programmkomponenten Dienste.

Für diejenigen, die mit der com-Programmierung vertraut sind, sind die com+-Verbesserungen wichtig, darunter:

-   Com+ implementiert ein Threading Modell mit dem Namen "neutral Apartment Threading", das es einer Komponente ermöglicht, serialisierten Zugriff zusammen mit der Möglichkeit zu haben, in einem beliebigen Thread auszuführen.
-   Com+ unterstützt Komponenten mit einer speziellen Umgebung, die als [Kontext](com--contexts.md)bezeichnet wird und eine erweiterbare Gruppe von Eigenschaften bereitstellt, die die Ausführungsumgebung für die Komponente definieren.
-   Com+ bietet rollenbasierte Sicherheit, asynchrone Objekt Ausführung und einen integrierten Moniker, der einen Verweis auf eine Objektinstanz darstellt, die auf einem Out-of-Process-Server ausgeführt wird.

## <a name="application-and-component-administration"></a>Anwendungs-und Komponenten Verwaltung

In com+ speichert eine Registrierungsdatenbank mit dem Namen RegDB die Metadaten, die Komponenten beschreiben. Diese Datenbank ist für die Art der Informationen, die com+ zur Aktivierung von Komponenten benötigt, stark optimiert und wird anstelle der Systemregistrierung verwendet. Außerdem macht com+ den *com+-Katalog* verfügbar, der auf Informationen in der RegDB zugreift. Der com+-Katalog ist ein Systemdaten Speicher, der Konfigurationsinformationen für COM+-Anwendungen auf einem bestimmten Server Computer enthält.

Zum Schluss stellt das Verwaltungs Programmkomponenten Dienste eine vollständig Skript fähige Benutzeroberfläche für Entwickler und Administratoren zur Verwaltung von Komponenten sowie zum Bereitstellen von Client seitigen und serverseitigen Anwendungen mit mehreren Ebenen bereit. Weitere Informationen finden Sie unter Bereitstellen von [com+-Anwendungen](deploying-com--applications.md).

## <a name="automatic-transactions"></a>Automatische Transaktionen

Com+ unterstützt alle Microsoft Transaction Server (MTS) 2,0-Semantik und fügt die Funktion für [Automatische](enabling-auto-done-for-a-method.md) Ausführung hinzu, die Sie mit dem Verwaltungs Programmkomponenten Dienste festlegen können. Diese Funktion ermöglicht es dem System, eine Transaktion automatisch abzubrechen, wenn eine Ausnahme ausgelöst wird, oder ein Commit durch den Commit erfolgt. Weitere Informationen finden Sie unter [com+-Transaktionen](com--transactions.md)und [com+-Just-in-Time-Aktivierung](com--just-in-time-activation.md).

 

 



