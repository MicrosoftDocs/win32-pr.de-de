---
title: Registrieren von com-Anwendungen
description: Registrieren von com-Anwendungen
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310944"
---
# <a name="registering-com-applications"></a>Registrieren von com-Anwendungen

Die Registrierung ist eine-Systemdatenbank, die Informationen zur Konfiguration von System Hardware und-Software sowie zu den Benutzern des Systems enthält. Alle Windows-basierten Programme können der Registrierung Informationen hinzufügen und Informationen aus der Registrierung lesen. Clients durchsuchen die Registrierung nach interessanten Komponenten, die verwendet werden sollen.

Die Registrierung verwaltet Informationen zu allen COM-Objekten, die im System installiert sind. Jedes Mal, wenn eine Anwendung eine Instanz einer COM-Komponente erstellt, wird die Registrierung so abgefragt, dass entweder die CLSID oder ProgID der Komponente in den Pfadnamen der Server-DLL oder der exe-Datei aufgelöst wird, in der Sie enthalten ist. Nachdem der Server der Komponente ermittelt wurde, lädt Windows entweder den Server in den Prozessbereich der Client Anwendung (Prozess interne Komponenten) oder startet den Server im eigenen Prozessbereich (lokale Server und Remote Server). Der Server erstellt eine Instanz der Komponente und kehrt zum Client einen Verweis auf eine der Schnittstellen der Komponente zurück.

Weitere Informationen zur Windows-Registrierung finden Sie in den folgenden Themen:

-   [Registrierungs Hierarchie](registry-hierarchy.md)
-   [Klassen und Server](classes-and-servers.md)
-   [Klassifizierender Komponenten](classifying-components.md)
-   [Verwenden von OLEVIEW](using-oleview.md)
-   [Registrieren von Komponenten](registering-components.md)
-   [Registrierung wird überprüft](checking-registration.md)
-   [Unbekannte Benutzer Typen](unknown-user-types.md)
-   [COM-Registrierungsschlüssel](com-registry-keys.md)

 

 




