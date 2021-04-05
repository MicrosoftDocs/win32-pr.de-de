---
description: Credential Management-API
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: Credential Management-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757290"
---
# <a name="credential-management-api"></a>Credential Management-API

Die Funktionen zur Verwaltung von Anmelde Informationen bilden die Funktionen, die von einem Anmelde Informationen-Manager implementiert werden müssen. Diese lauten wie folgt:

-   [**Nplogonnotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), eine Ereignishandlerfunktion, die von der MPR aufgerufen wird, wenn sich ein Benutzer anmeldet.
-   [**Nppasswordchangenotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), eine Ereignishandlerfunktion, die von MPR aufgerufen wird, wenn ein Konto Kennwort geändert wird.

Die Funktionen für die Verwaltung von Anmelde Informationen werden immer im Systemkontext ("LocalSystem") statt im Benutzer Kontext aufgerufen.

Weitere Informationen zum Erstellen und Registrieren einer Anwendung für die Anmelde Informationsverwaltung finden Sie unter [Implementieren einer](implementing-a-credential-manager.md) Anmelde Informationsverwaltung und [Registrieren von Netzwerkanbietern und Anmelde Informations Managern](registering-network-providers-and-credential-managers.md).

 

 



