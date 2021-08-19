---
description: JugendschutzTop-Level Benutzeroberfläche
ms.assetid: c6dfd3bc-191f-42d1-b9de-cc85a2da0a99
title: JugendschutzTop-Level Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c989a1c4aed25a15fe0942bb5f1f540246a40d349e452ce4efe518454d523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869176"
---
# <a name="parental-controls-top-level-user-interface"></a>JugendschutzTop-Level Benutzeroberfläche

Die starke Verknüpfung zwischen Family Safety- und Windows-Benutzerkonten hat eine kombinierte Kategorie als Benutzerkonten und **Family Safety** in Systemsteuerung für verbraucherorientierte SKUs von Windows Vista gesteuert.

> [!Note]  
> Die Kategorie wird als Benutzerkonten **angezeigt,** wenn ein Computer mit Domänenverkninungsfunktion verbunden ist.

 

Wenn für den kontrollierten Benutzer noch kein Standardbenutzerkonto eingerichtet wurde, bietet ein Link in Systemsteuerung einen einfachen Workflow zum Hinzufügen eines neuen kontos mit Jugendschutz.

Nachdem ein Konto erstellt wurde, stellt die Systemsteuerung die benutzerorientierten Funktionen der obersten Ebene für den kontrollierten Benutzer zur Verfügung. Elemente:

-   Allgemeine Einschränkungen der Jugendschutz für Optionsfelder oder deaktivierte Optionsfelder.
-   Unabhängige Aktivitätsberichterstattung Ein- oder Ausschaltflächen des Steuerelements.
-   Ein Einstellungen abschnitt mit dem von Microsoft implementierten Link Webeinschränkungen, der bedingt angezeigt wird, und verfügbaren offline von Microsoft implementierten Einschränkungstypen.
-   Der Bereich Weitere Einstellungen, der angezeigt wird, Benutzeroberfläche Erweiterungen von Microsoft oder Drittanbietern registriert werden.
-   Ein Zusammenfassungsstatusbereich mit dem Benutzernamen und der Kachel, dem Link Aktivitätsberichte anzeigen und dem Status der Einstellungen für die Jugendschutzkontrollen. Wenn diese Einstellung aktiv ist, enthält die Anzeige die Einstellungsebene Webinhaltsfilter (wenn der Microsoft-Filter aktiv ist) oder den Filternamen, wenn er von einer Drittanbietererweiterung überschrieben wird, sowie den Status der Offlineeinstellungen für den Benutzer.

Das optionsfeld Aktivieren der übergeordneten Steuerelemente ist anfänglich auf den Aus-Zustand festgelegt. Wenn sie von einem Administrator aktiviert wird, Aktivitätsberichterstattung standardmäßig auch aktiviert, kann jedoch unabhängig deaktiviert werden. Wie bei fast allen Einstellungen in Der Jugendschutz kann die Konfiguration programmgesteuert über die verfügbaren APIs erfolgen.

 

 



