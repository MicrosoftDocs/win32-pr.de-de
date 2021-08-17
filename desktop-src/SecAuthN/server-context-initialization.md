---
description: Wie der Client erhält auch der Server ein Anmeldeinformationenhand handle, um auf eine eingehende Authentifizierungsanforderung vom Client reagieren zu können.
ms.assetid: 2a0aeadf-e099-4264-8522-e498f437bf75
title: Initialisierung des Serverkontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d4a81c8033dc6b5dda8baca9ee7dfcc87d2b14c1cd139ff4a7f8eda99603f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918329"
---
# <a name="server-context-initialization"></a>Initialisierung des Serverkontexts

Wie der Client erhält auch [](../secgloss/c-gly.md) der Server ein Anmeldeinformationenhand handle, um auf eine eingehende Authentifizierungsanforderung vom Client reagieren zu können. Serveranmeldeinformationen werden verwendet, um den Server beim Client in Sicherheitsprotokollen [*zu*](../secgloss/s-gly.md) authentifizieren, die die Serverauthentifizierung oder gegenseitige Authentifizierung unterstützen. Der Server erhält ein Handle für seine Anmeldeinformationen, die durch das Dienstkonto definiert sind, das zum Starten des Servers verwendet wird. Rufen Sie dazu [**AcquireCredentialsHandle auf.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)

Der Server kann sein Anmeldeinformationenhand handle erhalten und dann in einen Lauschenzustand wechseln, oder er kann in einem Lauschenzustand warten, bis eine Verbindungsanforderung eintrifft, und dann ein Handle für eingehende Anmeldeinformationen erhalten. Weitere Informationen zu Anmeldeinformationsfunktionen finden Sie unter [Credential Management](authentication-functions.md).

Wenn der Server eine Verbindungsanforderungsnachricht von einem [](../secgloss/s-gly.md) Client empfängt, erstellt er mit [**AcceptSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)einen lokalen Sicherheitskontext für den Client. Der Server verwendet diesen lokalen Sicherheitskontext, um zukünftige Anforderungen durch denselben Client zu senden. Weitere Informationen zu Kontextfunktionen finden Sie unter [Kontextverwaltung.](authentication-functions.md)

Der Server überprüft den Rückgabestatus und den Ausgabepufferdeskriptor, um sicherzustellen, dass bisher keine Fehler aufgetreten sind, und kann die Verbindungsanforderung ablehnen, wenn Fehler auftreten. Wenn informationen im Ausgabepuffer enthalten sind, der von [**AcceptSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)zurückgegeben wird, wird dieser Puffer in einer Antwortnachricht an den Client gebündelt.

Jeder Ausgabepuffer von [**AcceptSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) muss zurück an den Client gesendet werden. Wenn für den Rückgabestatus das Fortsetzen des Protokolls erforderlich ist (SEC I CONTINUE NEEDED oder SEC I COMPLETE AND CONTINUE), ist ein weiterer Nachrichtenaustausch \_ \_ mit dem Client \_ \_ \_ \_ \_ erforderlich.

Für weitere Beide wartet der Server darauf, dass der Client mit einer anderen Nachricht antwortet. Für diese Wartezeit kann ein Time out durchgeführt werden, um einen Denial-of-Service-Angriff zu vermeiden, bei dem ein Client nicht mehr gezielt reagiert. Dies führt dazu, dass ein Serverthread und bald alle Serverthreads nicht mehr reagieren.

 

 
