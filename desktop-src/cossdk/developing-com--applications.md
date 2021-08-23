---
description: Bei der Entwicklung von COM+-Anwendungen umfassen die Hauptaufgaben das Entwerfen von COM-Komponenten zum Kapseln der Anwendungslogik und die Integration dieser Komponenten in eine COM+-Anwendung, das Erstellen der COM+-Anwendung und das Verwalten der Anwendung durch Bereitstellung und Wartung.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Entwickeln von COM+-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54526cc0fd900dbf92f8a69986b9aafc8e41a59f3964eafa2317b196ffbf6f0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047484"
---
# <a name="developing-com-applications"></a>Entwickeln von COM+-Anwendungen

Bei der Entwicklung von COM+-Anwendungen umfassen die Hauptaufgaben das Entwerfen von COM-Komponenten zum Kapseln der Anwendungslogik und die Integration dieser Komponenten in eine COM+-Anwendung, das Erstellen der COM+-Anwendung und das Verwalten der Anwendung durch Bereitstellung und Wartung.

## <a name="designing-com-components"></a>Entwerfen von COM-Komponenten

In den folgenden Schritten wird ein allgemeines Verfahren für einen guten Komponentenentwurf beschrieben:

1.  Definieren Sie die COM-Klassen und Implementierungsklassen.
2.  Gruppen Sie die Klassen in Komponenten.
3.  Wählen Sie den Satz von COM+-Diensten für Ihre Komponente aus, auch wenn Sie bei der Entwicklung der Komponente nicht alle angeben. Diese Dienste können später mit dem Component Services-Verwaltungstool oder dem COM+-Verwaltungsobjektmodell angegeben werden (weitere Informationen zum COM+-Verwaltungsobjektmodell finden Sie unter [Automatisieren](automating-com--administration.md) der COM+-Verwaltung.)

## <a name="creating-the-com-application"></a>Erstellen der COM+-Anwendung

Nach dem Entwerfen der COM-Komponenten integriert der Entwickler die Komponenten in eine COM+-Anwendung und konfiguriert die Anwendung. Die folgenden Schritte beschreiben den Prozess:

1.  Integrieren Sie die Komponenten in eine COM+-Anwendung. Sie können die Komponenten in eine vorhandene COM+-Anwendung integrieren oder eine neue (leere) Anwendung für die Komponenten erstellen. (Weitere Informationen [finden Sie unter Erstellen von COM+-Anwendungen.)](creating-com--applications.md)
2.  Geben Sie den richtigen Satz von Attributen für jede der Klassen an (falls zutreffend, und wenn sie nicht im Entwicklungstool angegeben ist). Diese Attribute ausdrücken die Komponentenabhängigkeiten von allen COM+-Diensten, von deren Implementierung abhängig sein kann (z. B. Transaktionen, Komponenten in der Warteschlange, Sicherheit, Objektpooling und Just-in-Time-Aktivierung).
3.  Richten Sie das Sicherheitsframework ein (Rollen und Zuweisung von Rollen zu Klassen, Schnittstellen und Methoden).
4.  Konfigurieren Sie umgebungsspezifische Attribute für Klassen und Anwendungen (z. B. die Standardgröße des Objektpools). Diese umgebungsspezifischen Attribute können später vom Systemadministrator festgelegt (oder geändert) werden.
5.  Exportieren Sie die Anwendung für die Neuverteilung und Bereitstellung.

Ausführlichere Informationen zu den Schritten beim Entwerfen verteilter Anwendungen finden Sie unter [Entwerfen von COM+-Anwendungen.](designing-com--applications.md)

## <a name="administering-com-applications"></a>Verwalten von COM+-Anwendungen

In der Regel übermittelt ein Entwickler eine teilweise konfigurierte COM+-Anwendung an den Systemadministrator. Der Administrator kann die Anwendung dann für eine oder mehrere bestimmte Umgebungen anpassen (z. B. durch Hinzufügen von Benutzerkonten in Rollen und Servernamen in einem Anwendungscluster). Die Aufgaben des Administrators umfassen Folgendes:

-   Installieren der teilweise konfigurierten COM+-Anwendung auf einem Administratorcomputer.
-   Bereitstellen von umgebungsspezifischen Attributen, z. B. Rollenmitglieder und Objektpoolgröße.
-   Erneutes Exportieren der vollständig konfigurierten COM+-Anwendung.
-   Erstellen eines Anwendungsproxys (wenn remote auf die Anwendung zugegriffen werden soll).

Nachdem eine Anwendung vollständig für eine bestimmte Umgebung konfiguriert wurde, kann sie vom Administrator auf Test- oder Produktionscomputern bereitgestellt werden. Dies umfasst die Installation der vollständig konfigurierten COM+-Anwendung auf mindestens einem Computer.

Ausführliche Informationen zu COM+-Verwaltungsverfahren finden Sie unter Component Services-Verwaltungstool.

 

 



