---
description: Microsoft Digest führt eine anfängliche Authentifizierung aus, wenn der Server die erste Anforderungs Antwort von einem Client empfängt.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Microsoft Digest Authentication (Microsoft Digest-Authentifizierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362390"
---
# <a name="microsoft-digest-authentication"></a>Microsoft Digest Authentication (Microsoft Digest-Authentifizierung)

Microsoft Digest führt eine anfängliche Authentifizierung aus, wenn der Server die erste Anforderungs Antwort von einem Client empfängt. Der Server überprüft, ob der Client nicht authentifiziert wurde, und führt dann die anfängliche Authentifizierung durchzugreifen auf die Dienste eines Domänen Controllers durch. Eine ausführliche Beschreibung dieses Verfahrens finden [Sie unter erste Authentifizierung mit Microsoft Digest](initial-authentication-using-microsoft-digest.md).

Wenn die anfängliche Authentifizierung erfolgreich ist, erhält der Server einen Digest- [*Sitzungsschlüssel*](../secgloss/s-gly.md). Der Server speichert diesen Schlüssel zwischen und verwendet ihn, um nachfolgende Anforderungen für Ressourcen vom Client zu authentifizieren. Diese Authentifizierung ist lokal, d. h., Sie erfordert keinen Zugriff auf einen Domänen Controller. Eine ausführliche Beschreibung dieser Vorgehensweise finden [Sie unter Authentifizieren von nachfolgenden Anforderungen mit Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

Wenn Sie http verwenden, wird keine Verbindung zwischen Client und Server hergestellt. Um den Domänen Controller-Datenverkehr zu reduzieren und die Leistung zu verbessern, werden von Microsoft Digest Informationen zwischengespeichert Weitere Informationen zu diesem Prozess finden Sie unter [beibehalten des Sicherheits Kontexts zwischen Verbindungen](maintaining-the-security-context-between-connections.md).

 

 
