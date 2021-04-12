---
title: ADSI-Schnittstellen
description: In diesem Thema werden die für ADSI-Schnittstellen verwendeten Kategorien beschrieben.
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- ADSI-Schnittstellen ADSI
- ADSI ADSI, Referenz, Schnittstellen
- Schnittstellen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2930292defa99301fb74f37c933a9af24b73f1fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387972"
---
# <a name="adsi-interfaces"></a>ADSI-Schnittstellen

Active Directory Service Interfaces (ADSI) unterstützt einen umfangreichen Satz von Schnittstellen, die nach den folgenden Kategorien klassifiziert werden können:

-   [Core](core-interfaces.md). Diese Schnittstellen stellen die grundlegenden Objekt Verwaltungsfunktionen von ADSI-Objekten bereit. Zu den Kernfunktionen gehören das Bereitstellen eines Einstiegs Punkts in einem Verzeichnis Speicher, das Laden von Eigenschaften in den Eigenschaften Cache und das Ausführen von Änderungen an das zugrunde liegende Verzeichnis.
-   [Schema](schema-interfaces.md). Diese Schnittstellen bieten Methoden zum Verwalten und Erweitern des Verzeichnis Schemas.
-   [Eigenschafts Cache](property-cache-interfaces.md). Diese Schnittstellen definieren Methoden zum Bearbeiten von Eigenschaften im Eigenschaften Cache.
-   [Persistentes Objekt](persistent-object-interfaces.md). Diese Schnittstellen bearbeiten persistente Daten im Namespace des zugrunde liegenden Verzeichnis Dienstanbieter. ADSI-Objekte implementieren diese Schnittstellentypen, um den Zugriff auf die persistenten Daten, einschließlich Benutzerkonten, Dateifreigaben, Organisations Hierarchien und Auftrags Auflistungen in einer Druck Warteschlange, bereitzustellen.
-   [Dynamisches Objekt](dynamic-object-interfaces.md). Diese Schnittstellen arbeiten mit dynamischen Daten in einem Verzeichnisdienst. Verzeichnisobjekte, die nicht im zugrunde liegenden Verzeichnisdienst dargestellt werden, implementieren solche Schnittstellen. Beispiele für dynamische Daten sind Befehle, die über ein Netzwerk ausgegeben werden.
-   [Sicherheit:](security-interfaces.md) Mit diesen Schnittstellen kann ein ADSI-Client seine Anmelde Informationen für einen Server einrichten und Sicherheitsfunktionen verwenden, die vom Verzeichnisdienst unterstützt werden, z. b. die Zugriffs Steuerungs Liste oder Sicherheits Beschreibungen.
-   [Nicht Automation](non-automation-interfaces.md). Diese Schnittstellen ermöglichen nicht Automatisierungs Clients (z. b. C/C++-Anwendungen) den Zugriff auf Verzeichnisobjekte durch den vtable-Zugriff auf die Methoden zum Verwalten und Durchsuchen von Verzeichnisdienst Objekten.
-   [Erweiterung](extension-interfaces.md). Mit diesen Schnittstellen können ADSI-Clients die Features vorhandener ADSI-Klassen erweitern, um den Verzeichnisdiensten angepasste Lösungen bereitzustellen.
-   - [Hilfsprogramm](utility-interfaces.md). Diese Schnittstellen stellen erweiterte Hilfsfunktionen zum Verwalten von ADSI-Objekten bereit.
-   [Datentyp](data-type-interfaces.md). Diese Schnittstellen stellen Methoden für den Zugriff auf ADSI-Datentypen bereit.

 

 




