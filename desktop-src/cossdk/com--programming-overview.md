---
description: COM+ bietet eine Unternehmensentwicklungsumgebung, die auf dem Microsoft Component Object Model (COM) basiert, um komponentenbasierte, verteilte Anwendungen zu erstellen.
ms.assetid: 141982d4-1e6c-4f01-8b0e-8b94f20dd82c
title: Übersicht über die COM+-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421fd6a52eade351eaab09ececff8fc63cc687002dede350ab9f06fa0b2c20e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096890"
---
# <a name="com-programming-overview"></a>Übersicht über die COM+-Programmierung

COM+ bietet eine Unternehmensentwicklungsumgebung, die auf dem Microsoft Component Object Model (COM) basiert, um komponentenbasierte, verteilte Anwendungen zu erstellen. Außerdem erhalten Sie die Tools zum Erstellen transaktionaler Anwendungen mit mehreren Ebenen. COM+ kombiniert Erweiterungen der herkömmlichen COM-basierten Entwicklung mit vielen nützlichen Programmier- und Verwaltungsdiensten. Eine [vollständige Liste dieser Dienste](com--services.md) finden Sie unter COM+-Dienste.

Die COM-Erweiterungen umfassen Verbesserungen bei Threading und Sicherheit sowie die Einführung von Synchronisierungsdiensten. Die Dienste umfassen das Verwaltungstool Komponentendienste.

Für Diejenigen, die mit der COM-Programmierung vertraut sind, sind die COM+-Verbesserungen von Bedeutung, einschließlich der folgenden:

-   COM+ implementiert ein Threadingmodell namens neutrales Apartmentthreading, das es einer Komponente ermöglicht, serialisierten Zugriff sowie die Möglichkeit zur Ausführung in jedem Thread zu erhalten.
-   COM+ unterstützt Komponenten mit einer [](com--contexts.md)speziellen Umgebung, die als Kontext bezeichnet wird und einen erweiterbaren Satz von Eigenschaften bietet, die die Ausführungsumgebung für die Komponente definieren.
-   COM+ bietet rollenbasierte Sicherheit, asynchrone Objektausführung und einen integrierten Moniker, der einen Verweis auf eine Objektinstanz darstellt, die auf einem Out-of-Process-Server ausgeführt wird.

## <a name="application-and-component-administration"></a>Anwendungs- und Komponentenverwaltung

In COM+ speichert eine Registrierungsdatenbank mit dem Namen RegDB die Metadaten, die Komponenten beschreiben. Diese Datenbank ist stark für den Informationstyp optimiert, den COM+ für die Aktivierung von Komponenten benötigt, und wird anstelle der Systemregistrierung verwendet. Darüber hinaus macht COM+ den *COM+-Katalog verfügbar,* der auf Informationen in der RegDB zutritt. Der COM+-Katalog ist ein Systemdatenspeicher, der Konfigurationsinformationen für COM+-Anwendungen auf einem bestimmten Servercomputer enthält.

Schließlich bietet das Component Services-Verwaltungstool eine vollständig skriptfähige Benutzeroberfläche für Entwickler und Administratoren zum Verwalten von Komponenten sowie zum Bereitstellen clientseitiger und serverseitiger Anwendungen mit mehreren Tieringen. Weitere Informationen finden Sie unter [Bereitstellen von COM+-Anwendungen.](deploying-com--applications.md)

## <a name="automatic-transactions"></a>Automatische Transaktionen

COM+ unterstützt die semantische Komponente von Microsoft Transaction Server [](enabling-auto-done-for-a-method.md) (MTS) 2.0 und fügt die Funktion "Automatisch erledigt" hinzu, die Sie mit dem Verwaltungstool für Komponentendienste festlegen können. Mit diesem Feature kann das System eine Transaktion automatisch abbrechen, wenn eine Ausnahme ausgelöst wird, oder andernorts einen Commit. Weitere Informationen finden Sie unter [COM+-Transaktionen](com--transactions.md)und [COM+ Just-in-Time-Aktivierung.](com--just-in-time-activation.md)

 

 



