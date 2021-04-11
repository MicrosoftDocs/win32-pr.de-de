---
description: Com+ bietet ein Verwaltungs Objektmodell, das die gesamte Funktionalität des Verwaltungs Programms Komponenten Dienste verfügbar macht, selbst ein grafisches Front-End, das auf den administrativen Objekten verfasst ist.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatisieren der com+-Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127164"
---
# <a name="automating-com-administration"></a>Automatisieren der com+-Verwaltung

Com+ bietet ein Verwaltungs Objektmodell, das die gesamte Funktionalität des Verwaltungs Programms Komponenten Dienste verfügbar macht, selbst ein grafisches Front-End, das auf den administrativen Objekten verfasst ist. Mithilfe dieser Objekte, die von der Bibliothek für die Verwaltung von Komponenten Diensten (COMAdmin) bereitgestellt werden, können Sie alle Aufgaben in der Verwaltung von com+-Anwendungen und-Diensten automatisieren.

Mit den COMAdmin-Objekten können Sie Informationen lesen und schreiben, die im com+-Katalog gespeichert sind, dem zugrunde liegenden Datenspeicher, der alle com+-Konfigurationsdaten enthält.

Mit diesen Objekten können Sie folgende Aufgaben ausführen:

-   Erstellen und konfigurieren Sie com+-Anwendungen.
-   Installieren und exportieren Sie vorhandene COM+-Anwendungen.
-   Installierte COM+-Anwendungen verwalten.
-   Verwalten und Konfigurieren von Diensten.
-   Remote Verwaltung von Komponenten Diensten auf einem anderen Computer.

Sie können die Skript fähigen COMAdmin-Objekte mit einer beliebigen Automatisierungs kompatiblen Sprache verwenden, wie z. b. Microsoft Visual Basic und Visual Basic Skripts. Sie können entweder Lightweight-Skripts oder allgemeine Verwaltungs Tools entwickeln. So können Sie z. B. Folgendes tun:

-   Schreiben Sie Skripts, um routinemäßige administrative Aufgaben auszuführen.
-   Schreiben Sie Skripts, um Prozesse bei der Entwicklung von com+-Anwendungen zu automatisieren.
-   Entwickeln Sie allgemeine Tools zum Verwalten und Überwachen von Komponenten Diensten.
-   Entwickeln Sie ausführbare Setup Dateien zum Installieren und Bereitstellen der com+-Anwendung.

Die COMAdmin-Bibliothek bietet Abwärtskompatibilität mit der MTS 2,0-Verwaltungs Bibliothek. Der größte vorhandene MTS 2,0-Verwaltungs Code funktioniert trotz einiger Ausnahmen weiterhin. (Siehe die [MTS-Verwaltungs Bibliothek](mts-administration-library.md).)

Um die Verwaltung effektiv zu automatisieren, sollten Sie mit den Verwaltungsaufgaben vertraut sein, die mit dem Verwaltungs Programmkomponenten Dienste ausgeführt werden.

Vollständige Beschreibungen der COMAdmin-Objekte und der entsprechenden Schnittstellen finden Sie in der com+-Referenz Dokumentation für die folgenden Klassen und Schnittstellen:

-   [**Comadmincatalog**](comadmincatalog.md)
-   [**Comadmincatalogcollection**](comadmincatalogcollection.md)
-   [**COMAdminCatalogObject**](comadmincatalogobject.md)
-   [**Icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [**Icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [**Icatalogobject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

Die folgenden Themen in diesem Abschnitt bieten eine Übersicht über die Automatisierung der Verwaltung mithilfe der COMAdmin-Objekte:

-   [Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
-   [Abrufen von Auflistungen im com+-Katalog](retrieving-collections-on-the-com--catalog.md)
-   [Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [Behandeln von com+-Verwaltungsfehlern](handling-com--administration-errors.md)
-   [Com+-Verwaltungsvorgänge in Transaktionen](com--administration-operations-within-transactions.md)
-   [Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog](introductory-example-using-the-com--administration-catalog.md)

 

 



