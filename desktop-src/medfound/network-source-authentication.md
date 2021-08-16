---
description: Netzwerkquellenauthentifizierung
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Netzwerkquellenauthentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e90ae7d7a8e4fb29b56aaa1296ba0c5aa44049f801b01a2c7797009ec736aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973039"
---
# <a name="network-source-authentication"></a>Netzwerkquellenauthentifizierung

Bestimmte Medienhosts erfordern möglicherweise Benutzeranmeldeinformationen von Clientanwendungen, bevor sie den Zugriff auf die Medien zulassen. Benutzeranmeldeinformationen enthalten identifikations- und identifikationsnachweise, z. B. Benutzername und Kennwort, die vom Medienserver verwendet werden, um Zugriff auf die Netzwerkquelle zu gewähren, die er hostet. Die Netzwerkquelle kann NTLM-, Digest- oder Standardauthentifizierung bereitstellen.

Anwendungen, die auf Media Foundation können Benutzeranmeldeinformationen  für eine bestimmte URL in einem Anmeldeinformationsobjekt speichern, das die [**BENUTZEROBERFLÄCHENTnetCredential verfügbar**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) macht. Das Anmeldeinformationsobjekt speichert verschlüsselte Anmeldeinformationen und stellt Methoden zum Zurückgeben von Informationen wie Benutzername, Kennwort und Domäne zur Verfügung.

Die Anmeldeinformationsobjekte werden in einem Cache erstellt und verwaltet. Das *Cacheobjekt für Anmeldeinformationen,* das von der [**BENUTZEROBERFLÄCHENetCredentialCache-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) verfügbar gemacht wird, stellt Methoden zum Abrufen der Anmeldeinformationsobjekte aus dem Anmeldeinformationscache bereit.

Eine Anwendung, die die Authentifizierung unterstützt, muss die [**SCHNITTSTELLE NSNETCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) implementieren. Media Foundation stellt keine Standardimplementierung dieser Schnittstelle bereit. Der Anmeldeinformations-Manager ist dafür verantwortlich, die erforderlichen Anmeldeinformationen für eine URL aus der Benutzereingabe zu erfassen oder aus dem persistenten Speicher zu lesen.

Dieser Abschnitt enthält die folgenden Themen:

-   [Festlegen einer Anmeldeinformationsverwaltung](setting-a-credential-manager.md)
-   [Verwenden des Anmeldeinformationscaches](using-the-credential-cache.md)
-   [Implementieren vonSTNETCredentialManager](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



