---
description: Netzwerk Quellen Authentifizierung
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Netzwerk Quellen Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041905"
---
# <a name="network-source-authentication"></a>Netzwerk Quellen Authentifizierung

Für bestimmte Medien Hosts sind möglicherweise Benutzer Anmelde Informationen von Client Anwendungen erforderlich, bevor der Zugriff auf die Medien zugelassen wird. Zu den Benutzer Anmelde Informationen gehören Identifizierung und Nachweis der Identifizierung, wie z. b. Benutzername und Kennwort, die vom Medienserver verwendet werden, um den Zugriff auf die von ihm gehosteten Netzwerkquelle zu gewähren. Die Netzwerkquelle kann die NTLM-, Digest-oder Standard Authentifizierung bereitstellen.

Anwendungen, die auf Media Foundation basieren, können Benutzer Anmelde Informationen für eine bestimmte URL in einem *Anmelde Informationen* -Objekt speichern, das die [**IMF netcredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) -Schnittstelle verfügbar macht. Das Anmelde Informationen-Objekt speichert verschlüsselte Anmelde Informationen und stellt Methoden zum Zurückgeben von Informationen wie Benutzername, Kennwort und Domäne bereit.

Die Anmelde Informationsobjekte werden in einem Cache erstellt und verwaltet. Das-Anmelde Informations *Cache* -Objekt, das von der [**IMF netkredentialcache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) -Schnittstelle verfügbar gemacht wird, stellt Methoden zum Abrufen der Anmelde Informationsobjekte aus dem Anmelde Informations Cache bereit.

Eine Anwendung, die die Authentifizierung unterstützt, muss die [**IMF netkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) -Schnittstelle implementieren. Media Foundation stellt keine Standard Implementierung dieser Schnittstelle bereit. Die Anmelde Informationsverwaltung ist dafür verantwortlich, die erforderlichen Anmelde Informationen für eine URL aus der Benutzereingabe oder das Lesen aus dem persistenten Speicher zu erfassen.

Dieser Abschnitt enthält die folgenden Themen:

-   [Festlegen eines Credential-Managers](setting-a-credential-manager.md)
-   [Verwenden des Anmelde Informations Caches](using-the-credential-cache.md)
-   [Implementieren von IMF netkredentialmanager](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



