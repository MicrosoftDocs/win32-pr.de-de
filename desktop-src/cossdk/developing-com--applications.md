---
description: Beim Entwickeln von com+-Anwendungen umfassen die Hauptaufgaben das Entwerfen von COM-Komponenten, um Anwendungslogik zu kapseln und diese Komponenten in eine COM+-Anwendung zu integrieren, die COM+-Anwendung zu erstellen und die Anwendung durch Bereitstellung und Wartung zu verwalten.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Entwickeln von com+-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523243"
---
# <a name="developing-com-applications"></a>Entwickeln von com+-Anwendungen

Beim Entwickeln von com+-Anwendungen umfassen die Hauptaufgaben das Entwerfen von COM-Komponenten, um Anwendungslogik zu kapseln und diese Komponenten in eine COM+-Anwendung zu integrieren, die COM+-Anwendung zu erstellen und die Anwendung durch Bereitstellung und Wartung zu verwalten.

## <a name="designing-com-components"></a>Entwerfen von COM-Komponenten

In den folgenden Schritten wird ein allgemeines Verfahren für einen guten Komponenten Entwurf beschrieben:

1.  Definieren Sie die com-Klassen und Implementierungsklassen.
2.  Gruppieren Sie die Klassen in Komponenten.
3.  Wählen Sie den Satz der com+-Dienste für die Komponente aus, auch wenn Sie beim Entwickeln der Komponente nicht alle angegeben haben. Diese Dienste können später mithilfe des Verwaltungs Programms Komponenten Dienste oder des com+-Verwaltungs Objektmodells angegeben werden (Weitere Informationen zum com+-Verwaltungs Objektmodell finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md) ).

## <a name="creating-the-com-application"></a>Erstellen der com+-Anwendung

Nach dem Entwerfen der COM-Komponenten integriert der Entwickler die Komponenten in eine COM+-Anwendung und konfiguriert die Anwendung. Die folgenden Schritte beschreiben den Prozess:

1.  Integrieren Sie die Komponenten in eine COM+-Anwendung. Sie können die Komponenten in eine vorhandene COM+-Anwendung integrieren oder eine neue (leere) Anwendung für die Komponenten erstellen. (Siehe [Erstellen von com+-Anwendungen](creating-com--applications.md).)
2.  Geben Sie den richtigen Satz von Attributen für jede der Klassen an (sofern vorhanden, und, wenn Sie im Entwicklungs Tool nicht angegeben sind). Diese Attribute geben die Komponenten Abhängigkeiten von allen COM+-Diensten, die ihre Implementierung unterstützen könnte (z. b. Transaktionen, in der Warteschlange befindliche Komponenten, Sicherheit, Objekt Pooling und Just-in-Time-Aktivierung), aus.
3.  Einrichten des Sicherheits Frameworks (Rollen und Zuweisung von Rollen für Klassen, Schnittstellen und Methoden).
4.  Konfigurieren Sie Umgebungs spezifische Attribute für Klassen und Anwendungen (z. b. die standardmäßige Objekt Pool Größe). Diese Umgebungs spezifischen Attribute können später vom Systemadministrator festgelegt (oder geändert) werden.
5.  Exportieren Sie die Anwendung für die Verteilung und Bereitstellung.

Ausführlichere Informationen zu den Schritten beim Entwerfen verteilter Anwendungen finden Sie unter [Entwerfen von com+-Anwendungen](designing-com--applications.md).

## <a name="administering-com-applications"></a>Verwalten von com+-Anwendungen

In der Regel stellt ein Entwickler dem Systemadministrator eine teilweise konfigurierte COM+-Anwendung bereit. Der Administrator kann die Anwendung dann für eine oder mehrere bestimmte Umgebungen anpassen (z. b. durch Hinzufügen von Benutzerkonten in Rollen und Servernamen in einem Anwendungs Cluster). Die Aufgaben des Administrators umfassen Folgendes:

-   Die teilweise konfigurierte COM+-Anwendung wird auf einem administrativen Computer installiert.
-   Bereitstellen von Umgebungs spezifischen Attributen, z. b. Rollen Mitgliedern und Größe des Objekt Pools.
-   Erneutes Exportieren der vollständig konfigurierten COM+-Anwendung.
-   Erstellen eines Anwendungs Proxys (wenn ein Remote Zugriff auf die Anwendung möglich ist).

Nachdem eine Anwendung vollständig für eine bestimmte Umgebung konfiguriert wurde, kann Sie vom Administrator auf Test-oder Produktions Computern bereitgestellt werden. Dies umfasst die Installation der vollständig konfigurierten COM+-Anwendung auf einem oder mehreren Computern.

Ausführliche Informationen zu com+-Verwaltungsverfahren finden Sie im Verwaltungs Programmkomponenten Dienste.

 

 



