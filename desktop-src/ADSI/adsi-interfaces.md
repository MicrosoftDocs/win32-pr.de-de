---
title: ADSI-Schnittstellen
description: In diesem Thema werden die Kategorien beschrieben, die für ADSI-Schnittstellen verwendet werden.
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- ADSI-Schnittstellen ADSI
- ADSI ADSI , Referenz,Schnittstellen
- AdsI-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75463a2b9ce70013482d2abee4f21ff786e7914cff0fefe691c562c4f39edb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023818"
---
# <a name="adsi-interfaces"></a>ADSI-Schnittstellen

Active Directory Service Interfaces (ADSI) unterstützt einen großen Satz von Schnittstellen, die nach den folgenden Kategorien klassifiziert werden können:

-   [Core](core-interfaces.md). Diese Schnittstellen stellen die grundlegenden Objektverwaltungsfunktionen von ADSI-Objekten bereit. Zu den Kernfunktionen gehören das Bereitstellen eines Einstiegspunkts in einen Verzeichnisspeicher, das Laden von Eigenschaften in den Eigenschaftencache und das Committen von Änderungen am zugrunde liegenden Verzeichnis.
-   [Schema](schema-interfaces.md). Diese Schnittstellen stellen Methoden zum Verwalten und Erweitern des Verzeichnisschemas bereit.
-   [Eigenschaftencache](property-cache-interfaces.md). Diese Schnittstellen definieren Methoden zum Bearbeiten von Eigenschaften im Eigenschaftencache.
-   [Persistentes Objekt](persistent-object-interfaces.md). Diese Schnittstellen bearbeiten persistente Daten im Namespace des zugrunde liegenden Verzeichnisdiensts. ADSI-Objekte implementieren diese Schnittstellentypen, um Zugriff auf ihre persistenten Daten zu ermöglichen, einschließlich Benutzerkonten, Dateifreigaben, Organisationshierarchien und Auftragsauflistungen in einer Druckwarteschlange.
-   [Dynamisches Objekt](dynamic-object-interfaces.md). Diese Schnittstellen funktionieren mit dynamischen Daten in einem Verzeichnisdienst. Verzeichnisobjekte, die nicht im zugrunde liegenden Verzeichnisdienst dargestellt werden, implementieren solche Schnittstellen. Beispiele für dynamische Daten sind Befehle, die über ein Netzwerk ausgegeben werden.
-   [Sicherheit](security-interfaces.md). Diese Schnittstellen ermöglichen es einem ADSI-Client, seine Anmeldeinformationen für einen Server herzustellen und sicherheitsfeatures zu verwenden, die der Verzeichnisdienst unterstützt, z. B. die Zugriffssteuerungsliste oder Sicherheitsbeschreibungen.
-   [Nicht-Automatisierung.](non-automation-interfaces.md) Diese Schnittstellen ermöglichen Nicht-Automation-Clients (z. B. C/C++-Anwendungen) den Zugriff auf Verzeichnisobjekte mit geringem Mehraufwand, indem sie VTable-Zugriff auf Methoden zum Verwalten und Durchsuchen von Verzeichnisdienstobjekten bereitstellen.
-   [Erweiterung](extension-interfaces.md). Mit diesen Schnittstellen können ADSI-Clients die Features vorhandener ADSI-Klassen erweitern, um angepasste Lösungen für Verzeichnisdienste anzubieten.
-   [Hilfsprogramm](utility-interfaces.md). Diese Schnittstellen bieten erweiterte Hilfsfunktionen zum Verwalten von ADSI-Objekten.
-   [Datentyp.](data-type-interfaces.md) Diese Schnittstellen stellen Methoden für den Zugriff auf ADSI-Datentypen bereit.

 

 




