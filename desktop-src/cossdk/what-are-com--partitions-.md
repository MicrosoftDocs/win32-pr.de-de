---
description: Eine COM+-Partition ist ein logischer Container, mit dem Anwendungen unabhängig von anderen Konfigurationen dieser Anwendungen ausgeführt werden können.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: Was sind COM+-Partitionen?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc678089948770181d98af065afa414741055062ed2e942215de5d7cb8bc7b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070264"
---
# <a name="what-are-com-partitions"></a>Was sind COM+-Partitionen?

Eine COM+-Partition ist ein logischer Container, mit dem Anwendungen unabhängig von anderen Konfigurationen dieser Anwendungen ausgeführt werden können. Jede Konfiguration einer Anwendung wird in einer separaten Partition installiert und kann gemäß den spezifischen Anforderungen ihrer Benutzer separat verwaltet werden.

Während der Aktivierung einer COM+-Komponente bestimmt der Partitionsdienst basierend auf der Identität des Benutzers, der die Komponentenaktivierung anfordert, welche Konfiguration der Komponente aktiviert werden soll. Beispielsweise könnte eine einzelne Organisation, die über zwei separate Gruppen (Produktion und Training) verfügt, COM+-Partitionen implementieren, um es den beiden Gruppen zu ermöglichen, unterschiedliche Konfigurationen einer COM+-Anwendung auf demselben Computer zu verwenden.

**Windows XP:** Com+-Partitionen können nicht erstellt, konfiguriert oder delegiert werden. Die globale Partition ist die einzige verfügbare COM+-Partition.

**Windows 2000:** Der COM+-Partitionsdienst ist in Windows 2000 nicht verfügbar.

## <a name="benefits-of-using-com-partitions"></a>Vorteile der Verwendung von COM+-Partitionen

Die Verwendung von COM+-Partitionen bietet mehrere Vorteile, einschließlich der folgenden:

-   Organisationen können ihre Gesamtbetriebskosten senken, indem sie weniger physische Anwendungsserver verwenden, um Benutzer zu unterstützen, die mehrere Anwendungskonfigurationen benötigen.
-   Der Verwaltungsaufwand wird reduziert. Anstatt mehrere Computer konfigurieren und verwalten zu müssen, müssen Administratoren nur mehrere Partitionen auf demselben Computer konfigurieren und verwalten. Darüber hinaus können Partitionen durch hinzufügen einer neuen COM+-Programmierschnittstelle programmgesteuert verwaltet werden.
-   Die Sicherheit kann partitionsweise für lokale Benutzer, Domänenbenutzer und Organisationseinheiten (OUs) implementiert und verwaltet werden.
-   Programmierer und Administratoren können die Entwicklungs- und Verwaltungstools von Microsoft , z. B. das Windows SDK, Active Directory-Benutzer und -Computer und Das Component Services-Verwaltungstool, verwenden, um COM+-Partitionen zu verwalten. Das Partitionsfeature ist vollständig in diese Tools integriert.

## <a name="primary-usage-scenario"></a>Primäres Verwendungsszenario

Ein Hauptgrund für Kunden, das Feature COM+-Partitionen bereitzustellen, ist das Hosten webbasierter Anwendungen. Angenommen, ein kleines Softwareunternehmen entwickelt eine COM+-Anwendung für die Verwendung durch Krankenhausmitarbeiter. Die Anwendung, bei der es sich um eine verteilte webbasierte Anwendung handelt, bietet Patienten eine Möglichkeit, Patientenakten mithilfe einer SQL Server-Datenbank zu speichern und abzurufen.

Angenommen, das Softwareunternehmen hat drei Kunden: Krankenhaus A, Krankenhaus B und Krankenhaus C. Während jeder Kunde die Clientseite der COM+-Anwendung lokal auf seinen Desktopcomputern ausführt, befindet sich die Serverseite der COM+-Anwendung auf dem firmeninternen Webserver des Softwareunternehmens und wird von seinen Kunden über das Web aufgerufen.

Da jedes Krankenhaus über eigene Speicher- und Abrufanforderungen und einen eigenen Satz angepasster Patientendaten verfügt, muss das Softwareunternehmen eine Möglichkeit bieten, mehrere Konfigurationen des Serverteils der Anwendung gleichzeitig auf dem Webserver auszuführen. COM+-Partitionen bieten eine Lösung für dieses Problem.

Die folgende Abbildung zeigt das Partitionsszenario für die COM+-Anwendung des Softwareunternehmens.

![Diagramm, das ein Partitionsszenario für eine COM+-Anwendung mit einer Clientanwendung zum Server der SQL Serverdatenbank zeigt.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen beim Anwendungsentwurf](application-design-restrictions.md)
</dt> <dt>

[COM+-Komponenten und -Partitionen in der Warteschlange](com--queued-components-and-partitions.md)
</dt> <dt>

[Partitionsimplementierung](partition-implementation.md)
</dt> <dt>

[Registrieren und Aktivieren von Komponenten in Partitionen](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



