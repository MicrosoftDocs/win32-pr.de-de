---
description: Um den Domänen Controller-Datenverkehr zu reduzieren und die Leistung zu verbessern, werden von der Clientseite Microsoft Digest Informationen zwischengespeichert, die nach erfolgreicher Authentifizierung mit einem Server
ms.assetid: cd928266-889a-494c-a94b-4ea7b1dcc241
title: Beibehalten des Sicherheits Kontexts zwischen Verbindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb450dde789f17f46397cb56fe74b94adcf8ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347148"
---
# <a name="maintaining-the-security-context-between-connections"></a>Beibehalten des Sicherheits Kontexts zwischen Verbindungen

Um den Domänen Controller-Datenverkehr zu reduzieren und die Leistung zu verbessern, werden von der Clientseite Microsoft Digest Informationen zwischengespeichert, die nach erfolgreicher Authentifizierung mit einem Server Client Anwendungen müssen das Handle nur für den [*Sicherheitskontext*](../secgloss/s-gly.md) Zwischenspeichern, der eingerichtet wurde. In der folgenden Tabelle werden die vom Sicherheitspaket zwischengespeicherten Informationen beschrieben.



| Information                                                       | BESCHREIBUNG                                                                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Servername                                                       | Der Server, der erfolgreich einen Sicherheitskontext für den Benutzer erstellt hat.                                                                           |
| Bereich/Domäne                                                      | Der Domänen Name, der bei erfolgreicher Authentifizierung verwendet wird.                                                                                              |
| [*Nonce*](../secgloss/n-gly.md) | Ein Server Nonce, der der erfolgreichen Authentifizierung zugeordnet ist.                                                                               |
| Nonce-Anzahl                                                       | Gibt an, wie oft der Client die Nonce in Anforderungen an den Server eingefügt hat. Diese wird für die Wiedergabe Erkennung verwendet.                                 |
| Nicht transparenter Wert                                                      | Der Wert, der nach erfolgreicher Authentifizierung für die opop-Direktive zurückgegeben wurde. Dieser Wert enthält einen Verweis auf den Sicherheitskontext des Benutzers. |



 

Wenn ein Client eine Nachricht an einen Server sendet, muss der Server bestimmen, ob der Client über einen vorhandenen Sicherheitskontext verfügt. Zu diesem Zweck übergibt der Server jede Client Anforderung an die Funktion " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) ". Diese Funktion extrahiert den Wert der opaken Direktive aus der Anforderung, falls vorhanden, und verwendet Sie, um den Sicherheitskontext des Clients zu suchen. Wenn der Sicherheitskontext gefunden wird, wird das Handle des Kontexts an den Server zurückgegeben. Weitere Informationen finden Sie unter [Authentifizieren von nachfolgenden Anforderungen](authenticating-subsequent-requests-using-microsoft-digest.md).

Um Spoofing-und Replay-Angriffe zu erkennen, ruft der Client die [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -Funktion auf, die einen Sicherheitskontext verwendet, um eine Nachricht zu signieren. Wenn Nachrichten mithilfe der **makesignature** -Funktion geschützt werden, verwendet der Server die [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) -Funktion mit dem zwischengespeicherten Kontext zum Überprüfen des Ursprungs und der [*Integrität*](../secgloss/i-gly.md)der Nachricht. Weitere Informationen finden Sie unter [Schützen von Nachrichten](protecting-messages-using-microsoft-digest.md).

 

 
