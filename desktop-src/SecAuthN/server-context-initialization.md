---
description: Wie der Client erhält der Server auch ein Anmelde Informations handle, das auf eine eingehende Authentifizierungsanforderung vom Client reagiert.
ms.assetid: 2a0aeadf-e099-4264-8522-e498f437bf75
title: Initialisierung des Server Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1362c8fd71e079392f10a8e35f76ad511de3c49f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756415"
---
# <a name="server-context-initialization"></a>Initialisierung des Server Kontexts

Wie der Client erhält der Server auch ein [*Anmelde*](../secgloss/c-gly.md) Informations handle, das auf eine eingehende Authentifizierungsanforderung vom Client reagiert. Server Anmelde Informationen werden verwendet, um den Server für den Client in [*Sicherheitsprotokollen*](../secgloss/s-gly.md) zu authentifizieren, die die Server Authentifizierung oder gegenseitige Authentifizierung unterstützen. Der Server erhält ein Handle für die Anmelde Informationen, die durch das Dienst Konto definiert werden, das zum Starten des Servers verwendet wird. Dies erfolgt durch Aufrufen von [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).

Der Server kann sein Anmelde Informations handle abrufen und dann in den Zustand "lauschen" wechseln, oder er kann in einem lausch Status warten, bis eine Verbindungsanforderung eingeht, und dann ein Handle für eingehende Anmelde Informationen abrufen. Weitere Informationen zu Anmelde Informationsfunktionen finden Sie unter [Verwaltung](authentication-functions.md)von Anmelde Informationen.

Wenn der Server eine Verbindungs Anforderungs Nachricht von einem Client empfängt, erstellt er mithilfe von " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)" einen lokalen [*Sicherheitskontext*](../secgloss/s-gly.md) für den Client. Der Server verwendet diesen lokalen Sicherheitskontext, um zukünftige Anforderungen vom gleichen Client auszuführen. Weitere Informationen zu Kontextfunktionen finden Sie unter [Context Management (Kontext Verwaltung](authentication-functions.md)).

Der Server überprüft den Rückgabestatus und den Ausgabepuffer Deskriptor, um sicherzustellen, dass bisher keine Fehler vorliegen, und kann die Verbindungsanforderung ablehnen, wenn Fehler auftreten. Wenn im Ausgabepuffer Informationen vorhanden sind, die von " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)" zurückgegeben werden, wird dieser Puffer in eine Antwortnachricht an den Client integriert.

Jeder Ausgabepuffer von " [**Accept-SecurityContext" (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) muss an den Client zurückgesendet werden. Außerdem ist ein weiterer Nachrichtenaustausch mit dem Client erforderlich, wenn für den Rückgabestatus das Protokoll fortgesetzt werden muss (s muss \_ \_ weiterhin \_ benötigt werden \_ \_ \_ , und der Vorgang wird beendet und \_ fortgesetzt).

Bei zusätzlichen Beinen wartet der Server darauf, dass der Client mit einer anderen Nachricht antwortet. Bei diesem warte Vorgang kann ein Timeout auftreten, um einen Denial-of-Service-Angriff zu vermeiden, bei dem ein Client absichtlich nie antwortet, was dazu führt, dass ein Server Thread und bald alle Serverthreads nicht mehr reagiert.

 

 
