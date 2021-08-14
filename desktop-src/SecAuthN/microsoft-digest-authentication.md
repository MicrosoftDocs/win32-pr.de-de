---
description: Microsoft Digest führt eine anfängliche Authentifizierung aus, wenn der Server die erste Antwort auf die Herausforderung von einem Client empfängt.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Microsoft Digest Authentication (Microsoft Digest-Authentifizierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135e5374515acb0604ee14a6770b9523e9bf31fd0e2d6c946fec26d2ad789c2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921829"
---
# <a name="microsoft-digest-authentication"></a>Microsoft Digest Authentication (Microsoft Digest-Authentifizierung)

Microsoft Digest führt eine anfängliche Authentifizierung aus, wenn der Server die erste Antwort auf die Herausforderung von einem Client empfängt. Der Server überprüft, ob der Client nicht authentifiziert wurde, und führt dann die erste Authentifizierung durch Zugriff auf die Dienste eines Domänencontrollers aus. Eine ausführliche Beschreibung dieses Verfahrens finden Sie unter [Initial Authentication Using Microsoft Digest](initial-authentication-using-microsoft-digest.md).

Wenn die erste Authentifizierung erfolgreich ist, erhält der Server einen [*Digestsitzungsschlüssel.*](../secgloss/s-gly.md) Der Server speichert diesen Schlüssel zwischen und verwendet ihn, um nachfolgende Anforderungen für Ressourcen vom Client zu authentifizieren. Bei dieser Authentifizierung handelt es sich um eine lokale Authentifizierung, d. b. sie erfordert keinen Zugriff auf einen Domänencontroller. Eine ausführliche Beschreibung dieses Verfahrens finden Sie unter [Authentifizieren nachfolgender Anforderungen mit Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

Bei Verwendung von HTTP wird keine Verbindung zwischen Client und Server verwaltet. Um den Datenverkehr des Domänencontrollers zu reduzieren und die Leistung zu verbessern, Microsoft Digest informationen zwischenspeichern, die nach erfolgreicher Authentifizierung empfangen wurden. Informationen zu diesem Prozess finden Sie unter [Verwalten des Sicherheitskontexts zwischen Verbindungen.](maintaining-the-security-context-between-connections.md)

 

 
