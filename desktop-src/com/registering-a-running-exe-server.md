---
title: Registrieren eines ausführenden exe-Servers
description: Registrieren eines ausführenden exe-Servers
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310832"
---
# <a name="registering-a-running-exe-server"></a>Registrieren eines ausführenden exe-Servers

Wenn ein ausführbarer (exe-) Server gestartet wird, sollte er [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)aufrufen, das die CLSID für den Server in der als Klassen Tabelle bezeichneten Tabelle registriert (eine andere Tabelle als die laufende Objekttabelle). Wenn ein Server in der Klassen Tabelle registriert ist, kann der Dienststeuerungs-Manager (Service Control Manager, SCM) bestimmen, dass es nicht erforderlich ist, die Klasse erneut zu starten, da der Server bereits ausgeführt wird. Nur wenn der Server nicht in der Klassen Tabelle aufgeführt ist, überprüft der SCM die Registrierung auf entsprechende Werte und startet den Server, der der angegebenen CLSID zugeordnet ist.

Sie übergeben [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) die CLSID für die Klasse und einen Zeiger auf die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle. Clients, die anschließend [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) mit dieser CLSID aufrufen, rufen einen Zeiger auf die angeforderte Schnittstelle ab, sofern Sie von der Sicherheit nicht unterbunden wird. (Eine Beschreibung mehrerer Instanzen Erstellungs-und Aktivierungs Funktionen finden Sie unter [Hilfsfunktionen](instance-creation-helper-functions.md) für die Instanzerstellung.)

Der Server für ein Klassenobjekt sollte [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) zum Widerrufen des Klassen Objekts (Entfernen der Registrierung) abrufen, wenn Folgendes zutrifft:

-   Es sind keine Instanzen der Objektdefinition vorhanden.
-   Es sind keine Sperren für das Klassenobjekt vorhanden.
-   Die Anwendung, die Dienste für das Klassenobjekt bereitstellt, befindet sich nicht unter dem Benutzer Steuerelement (für den Benutzer auf der Anzeige nicht sichtbar).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Installieren von als Dienst Anwendung](installing-as-a-service-application.md)
</dt> <dt>

[Registrieren einer Klasse bei der Installation](registering-a-class-at-installation.md)
</dt> <dt>

[Registrieren von Objekten in der rot](registering-objects-in-the-rot.md)
</dt> <dt>

[Selbstregistrierung](self-registration.md)
</dt> </dl>

 

 




