---
title: Registrieren eines ausgeführten EXE-Servers
description: Registrieren eines ausgeführten EXE-Servers
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc4aa984090c35a4b700719d248a75c1a8d917dfcb707f288a6b9985c672742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104875"
---
# <a name="registering-a-running-exe-server"></a>Registrieren eines ausgeführten EXE-Servers

Wenn ein ausführbarer Server (EXE) gestartet wird, sollte er [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)aufrufen, der die CLSID für den Server in der sogenannten Klassentabelle registriert (eine andere Tabelle als die ausgeführte Objekttabelle). Wenn ein Server in der Klassentabelle registriert ist, kann der Dienststeuerungs-Manager (Service Control Manager, SCM) feststellen, dass es nicht erforderlich ist, die Klasse erneut zu starten, da der Server bereits ausgeführt wird. Nur wenn der Server nicht in der Klassentabelle aufgeführt ist, überprüft der SCM die Registrierung auf die entsprechenden Werte und startet den Server, der der angegebenen CLSID zugeordnet ist.

Sie übergeben [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) die CLSID für die Klasse und einen Zeiger auf ihre [**IUnknown-Schnittstelle.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Clients, die [**anschließend CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) mit dieser CLSID aufrufen, rufen einen Zeiger auf ihre angeforderte Schnittstelle ab, solange die Sicherheit dies nicht unterbietet. (Eine Beschreibung mehrerer Funktionen zum Erstellen und Aktivieren von Instanzen finden Sie unter [Hilfsfunktionen](instance-creation-helper-functions.md) für die Instanzerstellung.)

Der Server für ein Klassenobjekt sollte [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) aufrufen, um das Klassenobjekt zu widerrufen (seine Registrierung zu entfernen), wenn folgendes zutrifft:

-   Es sind keine Instanzen der Objektdefinition vorhanden.
-   Es gibt keine Sperren für das Klassenobjekt.
-   Die Anwendung, die Dienste für das Klassenobjekt bereitstellt, wird nicht vom Benutzer gesteuert (für den Benutzer auf der Anzeige nicht sichtbar).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Installieren als Dienstanwendung](installing-as-a-service-application.md)
</dt> <dt>

[Registrieren einer Klasse bei der Installation](registering-a-class-at-installation.md)
</dt> <dt>

[Registrieren von Objekten in rot](registering-objects-in-the-rot.md)
</dt> <dt>

[Selbstregistrierung](self-registration.md)
</dt> </dl>

 

 




