---
description: Anmeldeinformationen Verwaltungs-API
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: Anmeldeinformationen Verwaltungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a290cf9d7e5a2d527368c2fd7350fa1bb9549af862c7da7c3845ceae9efc8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008838"
---
# <a name="credential-management-api"></a>Anmeldeinformationen Verwaltungs-API

Die Verwaltungsfunktionen für Anmeldeinformationen bilden den Satz von Funktionen, die ein Anmeldeinformations-Manager implementieren muss. Diese lauten wie folgt:

-   [**NPLogonNotify,**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)eine Ereignishandlerfunktion, die vom MPR aufgerufen wird, wenn sich ein Benutzer anmeldet.
-   [**NPPasswordChangeNotify,**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)eine Ereignishandlerfunktion, die vom MPR aufgerufen wird, wenn ein Kontokennwort geändert wird.

Die Verwaltungsfunktionen für Anmeldeinformationen werden immer im Systemkontext (LocalSystem) und nicht im Benutzerkontext aufgerufen.

Weitere Informationen zum Erstellen und Registrieren einer Anwendung für den Anmeldeinformations-Manager finden Sie unter [Implementieren](implementing-a-credential-manager.md) eines Anmeldeinformationsverwaltung und Registrieren von Netzwerkanbietern und [Anmeldeinformations-Managern.](registering-network-providers-and-credential-managers.md)

 

 



