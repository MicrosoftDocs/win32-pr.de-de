---
description: Um den Datenverkehr des Domänencontrollers zu reduzieren und die Leistung zu verbessern, speichert die clientseitige Microsoft Digest informationen zwischen, die nach erfolgreicher Authentifizierung bei einem Server empfangen wurden.
ms.assetid: cd928266-889a-494c-a94b-4ea7b1dcc241
title: Verwalten des Sicherheitskontexts zwischen Verbindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d36b28d1db96efd6c41b3532b8021db7e6f8cf206e0df0bedf62b5775d2ba7de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787047"
---
# <a name="maintaining-the-security-context-between-connections"></a>Verwalten des Sicherheitskontexts zwischen Verbindungen

Um den Datenverkehr des Domänencontrollers zu reduzieren und die Leistung zu verbessern, speichert die clientseitige Microsoft Digest informationen zwischen, die nach erfolgreicher Authentifizierung bei einem Server empfangen wurden. Clientanwendungen müssen das Handle nur im [*eingerichteten*](../secgloss/s-gly.md) Sicherheitskontext zwischenspeichern. In der folgenden Tabelle werden die vom Sicherheitspaket zwischengespeicherten Informationen beschrieben.



| Information                                                       | BESCHREIBUNG                                                                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Servername                                                       | Der Server, der erfolgreich einen Sicherheitskontext für den Benutzer erstellt hat.                                                                           |
| Bereich/Domäne                                                      | Der Domänenname, der bei der erfolgreichen Authentifizierung verwendet wird.                                                                                              |
| [*Nonce*](../secgloss/n-gly.md) | Eine Server-Nonce, die der erfolgreichen Authentifizierung zugeordnet ist.                                                                               |
| Nonce-Anzahl                                                       | Gibt an, wie oft der Client die Nonce in Anforderungen an den Server eingeschlossen hat. Dies wird für die Wiedergabeerkennung verwendet.                                 |
| Nicht transparenter Wert                                                      | Der Wert, der nach einer erfolgreichen Authentifizierung für die nicht transparente -Direktive zurückgegeben wird. Dieser Wert enthält einen Verweis auf den Sicherheitskontext des Benutzers. |



 

Wenn ein Client eine Nachricht an einen Server sendet, muss der Server bestimmen, ob der Client über einen vorhandenen Sicherheitskontext verfügt. Hierzu übergibt der Server jede Clientanforderung an die [**AcceptSecurityContext(General)-Funktion.**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Diese Funktion extrahiert den Wert der nicht transparenten Direktive aus der Anforderung (sofern vorhanden) und verwendet ihn, um den Sicherheitskontext des Clients zu suchen. Wenn der Sicherheitskontext gefunden wird, wird das Handle des Kontexts an den Server zurückgegeben. Weitere Informationen finden Sie unter [Authentifizieren nachfolgender Anforderungen.](authenticating-subsequent-requests-using-microsoft-digest.md)

Zur Erkennung von Spoofing- und Replayangriffen ruft der Client die [**MakeSignature-Funktion**](/windows/desktop/api/Sspi/nf-sspi-makesignature) auf, die einen Sicherheitskontext zum Signieren einer Nachricht verwendet. Wenn Nachrichten mit der **MakeSignature-Funktion** geschützt werden, verwendet der Server die [**VerifySignature-Funktion**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) mit dem zwischengespeicherten Kontext, um den Ursprung und die Integrität der Nachricht [*zu überprüfen.*](../secgloss/i-gly.md) Weitere Informationen finden Sie unter [Schützen von Nachrichten.](protecting-messages-using-microsoft-digest.md)

 

 
