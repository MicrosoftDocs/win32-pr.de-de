---
description: COM+ stellt ein Verwaltungsobjektmodell zur Verfügung, das alle Funktionen des Komponentendienste-Verwaltungstools verfügbar macht, selbst ein grafisches Front-End, das auf den administrativen Objekten geschrieben wird.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatisieren der COM+-Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cb7370c3b1a90324b612108e9ec1ef17c7030d3372d303da74ced95298ab02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029840"
---
# <a name="automating-com-administration"></a>Automatisieren der COM+-Verwaltung

COM+ stellt ein Verwaltungsobjektmodell zur Verfügung, das alle Funktionen des Komponentendienste-Verwaltungstools verfügbar macht, selbst ein grafisches Front-End, das auf den administrativen Objekten geschrieben wird. Sie können diese Objekte, die von der COMAdmin-Bibliothek (Component Services Administration) bereitgestellt werden, verwenden, um alle Aufgaben in der Verwaltung von COM+-Anwendungen und -Diensten zu automatisieren.

Mit den COMAdmin-Objekten können Sie Informationen lesen und schreiben, die im COM+-Katalog gespeichert sind, dem zugrunde liegenden Datenspeicher, der alle COM+-Konfigurationsdaten enthält.

Sie können diese Objekte für folgende Aufgaben verwenden:

-   Erstellen und Konfigurieren von COM+-Anwendungen.
-   Installieren und exportieren Sie vorhandene COM+-Anwendungen.
-   Verwalten installierter COM+-Anwendungen.
-   Verwalten und Konfigurieren von Diensten.
-   Remoteverwaltung von Komponentendiensten auf einem anderen Computer.

Sie können die skriptbaren COMAdmin-Objekte mit einer beliebigen Automation-kompatiblen Sprache verwenden, z. B. Microsoft Visual Basic und Visual Basic Script. Sie können entweder einfache Skripts oder allgemeine Verwaltungstools entwickeln. So können Sie z. B. Folgendes tun:

-   Schreiben Sie Skripts, um routinemäßige verwaltungsaufgaben auszuführen.
-   Schreiben Sie Skripts, um Prozesse bei der Entwicklung von COM+-Anwendungen zu automatisieren.
-   Entwickeln Sie allgemeine Tools für die Verwaltung und Überwachung von Komponentendiensten.
-   Entwickeln Sie ausführbare Setupdateien, um Ihre COM+-Anwendung zu installieren und bereitzustellen.

Die COMAdmin-Bibliothek bietet Abwärtskompatibilität mit der MTS 2.0-Verwaltungsbibliothek. Die meisten vorhandenen MTS 2.0-Verwaltungscodes funktionieren weiterhin, allerdings mit einigen Ausnahmen. (Siehe [MTS-Verwaltungsbibliothek](mts-administration-library.md).)

Um die Verwaltung effektiv zu automatisieren, sollten Sie mit Verwaltungsaufgaben vertraut sein, die mit dem Verwaltungstool für Komponentendienste ausgeführt werden.

Vollständige Beschreibungen der COMAdmin-Objekte und der entsprechenden Schnittstellen finden Sie in der COM+-Referenzdokumentation für die folgenden Klassen und Schnittstellen:

-   [**COMAdminCatalog**](comadmincatalog.md)
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md)
-   [**COMAdminCatalogObject**](comadmincatalogobject.md)
-   [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

Die folgenden Themen in diesem Abschnitt bieten eine Übersicht über die Automatisierung der Verwaltung mithilfe der COMAdmin-Objekte:

-   [Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
-   [Abrufen von Sammlungen im COM+-Katalog](retrieving-collections-on-the-com--catalog.md)
-   [Festlegen von Eigenschaften und Speichern von Änderungen am COM+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [Behandeln von COM+-Verwaltungsfehlern](handling-com--administration-errors.md)
-   [COM+-Verwaltungsvorgänge innerhalb von Transaktionen](com--administration-operations-within-transactions.md)
-   [Einführendes Beispiel mit dem COM+-Verwaltungskatalog](introductory-example-using-the-com--administration-catalog.md)

 

 



