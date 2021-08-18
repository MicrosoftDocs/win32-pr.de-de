---
title: Registrieren von COM-Anwendungen
description: Registrieren von COM-Anwendungen
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63caaba090c38e5917e6c85884fdf5a76e2353f6a57527ad5870d0fbd984b173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129982"
---
# <a name="registering-com-applications"></a>Registrieren von COM-Anwendungen

Die Registrierung ist eine Systemdatenbank, die Informationen über die Konfiguration von Systemhardware und -software sowie über Benutzer des Systems enthält. Jedes Windows-basierte Programm kann der Registrierung Informationen hinzufügen und Informationen aus der Registrierung zurücklesen. Clients durchsuchen die Registrierung nach interessanten Komponenten, die verwendet werden können.

Die Registrierung verwaltet Informationen zu allen COM-Objekten, die im System installiert sind. Jedes Mal, wenn eine Anwendung eine Instanz einer COM-Komponente erstellt, wird die Registrierung zum Auflösen der CLSID oder ProgID der Komponente in den Pfadnamen der Server-DLL oder EXE-Datei, die sie enthält, konsultieren. Nachdem der Server der Komponente bestimmt wurde, lädt Windows den Server entweder in den Prozessbereich der Clientanwendung (Prozesskomponenten) oder startet den Server in seinem eigenen Prozessbereich (lokale server und Remoteserver). Der Server erstellt eine Instanz der Komponente und gibt einen Verweis auf eine der Schnittstellen der Komponente an den Client zurück.

Weitere Informationen zur registrierung Windows finden Sie in den folgenden Themen:

-   [Registrierungshierarchie](registry-hierarchy.md)
-   [Klassen und Server](classes-and-servers.md)
-   [Klassifizieren von Komponenten](classifying-components.md)
-   [Verwenden von OleView](using-oleview.md)
-   [Registrieren von Komponenten](registering-components.md)
-   [Überprüfen der Registrierung](checking-registration.md)
-   [Unbekannte Benutzertypen](unknown-user-types.md)
-   [COM-Registrierungsschlüssel](com-registry-keys.md)

 

 




