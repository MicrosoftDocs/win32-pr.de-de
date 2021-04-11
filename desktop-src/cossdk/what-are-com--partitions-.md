---
description: Eine COM+-Partition ist ein logischer Container, der es ermöglicht, Anwendungen unabhängig von anderen Konfigurationen dieser Anwendungen auszuführen.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: Was sind COM+-Partitionen?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104132125"
---
# <a name="what-are-com-partitions"></a>Was sind COM+-Partitionen?

Eine COM+-Partition ist ein logischer Container, der es ermöglicht, Anwendungen unabhängig von anderen Konfigurationen dieser Anwendungen auszuführen. Jede Konfiguration einer Anwendung wird in einer separaten Partition installiert und kann gemäß den spezifischen Anforderungen Ihrer Benutzer separat verwaltet werden.

Während der Aktivierung einer COM+-Komponente bestimmt der Partitions Dienst, welche Konfiguration der Komponente aktiviert werden soll, basierend auf der Identität des Benutzers, der die Komponenten Aktivierung anfordert. Beispielsweise könnte eine einzelne Organisation mit zwei separaten Gruppen, Produktion und Schulung, com+-Partitionen implementieren, damit die beiden Gruppen unterschiedliche Konfigurationen einer COM+-Anwendung auf demselben Computer verwenden können.

**Windows XP:** Die Möglichkeit, com+-Partitionen zu erstellen, zu konfigurieren oder zu delegieren, ist nicht verfügbar. Die globale Partition ist die einzige verfügbare com+-Partition.

**Windows 2000:** Der com+-Partitions Dienst ist in Windows 2000 nicht verfügbar.

## <a name="benefits-of-using-com-partitions"></a>Vorteile der Verwendung von COM+-Partitionen

Die Verwendung von COM+-Partitionen bietet verschiedene Vorteile, einschließlich der folgenden:

-   Organisationen können Ihre Gesamtbetriebskosten (TCO) senken, indem Sie weniger physische Anwendungsserver verwenden, um Benutzer zu unterstützen, die mehrere Anwendungs Konfigurationen benötigen.
-   Der Verwaltungsaufwand wird reduziert. Anstatt mehrere Computer konfigurieren und verwalten zu müssen, müssen Administratoren nur mehrere Partitionen auf demselben Computer konfigurieren und verwalten. Darüber hinaus können Partitionen Programm gesteuert durch Hinzufügen einer neuen com+-Programmierschnittstelle verwaltet werden.
-   Die Sicherheit kann für lokale Benutzer, Domänen Benutzer und Organisationseinheiten (OUs) auf Partitions Basis implementiert und verwaltet werden.
-   Programmierer und Administratoren können die Entwicklungs-und Verwaltungs Tools von Microsoft – wie z. b. die Windows SDK, Active Directory Benutzer und Computer und das Verwaltungs Programmkomponenten Dienste – zum Verwalten von COM+-Partitionen verwenden. Die Partitions Funktion ist vollständig in diese Tools integriert.

## <a name="primary-usage-scenario"></a>Primäres Verwendungs Szenario

Ein Hauptgrund für die Bereitstellung der com+-Partitions Funktion besteht darin, webbasierte Anwendungen zu hosten. Nehmen wir beispielsweise an, ein kleines Softwareunternehmen entwickelt eine COM+-Anwendung für die Verwendung durch Krankenhausmitarbeiter. Die Anwendung, die eine verteilte webbasierte Anwendung ist, ermöglicht es Krankenhäusern, Patientendaten Sätze mit einer SQL Server Datenbank zu speichern und abzurufen.

Angenommen, das Softwareunternehmen hat drei Kunden: Krankenhaus a, Krankenhaus B und Krankenhaus C. Obwohl jeder Kunde die Clientseite der com+-Anwendung lokal auf seinen Desktop Computern ausführt, befindet sich die Serverseite der com+-Anwendung auf dem internen Webserver des Softwareunternehmens und wird von seinen Kunden über das Web aufgerufen.

Da jedes Krankenhaus über einen eigenen Satz an Speicher-und Abruf Anforderungen und seinen eigenen Satz angepasster Patientendaten verfügt, muss das Softwareunternehmen eine Methode bereitstellen, mit der mehrere Konfigurationen des Server Teils der Anwendung gleichzeitig auf dem Webserver ausgeführt werden können. Com+-Partitionen stellen eine Lösung für dieses Problem dar.

Die folgende Abbildung zeigt das Partitions Szenario für die COM+-Anwendung des Softwareunternehmens.

![Diagramm, das ein Partitions Szenario für eine COM+-Anwendung anzeigt, mit einer Client Anwendung zu Serveranwendung für die SQL Server-Datenbank.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen beim Anwendungs Entwurf](application-design-restrictions.md)
</dt> <dt>

[Komponenten und Partitionen in der com+-Warteschlange](com--queued-components-and-partitions.md)
</dt> <dt>

[Partitions Implementierung](partition-implementation.md)
</dt> <dt>

[Registrieren und Aktivieren von Komponenten in Partitionen](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



