---
description: Benutzeranmeldeinformationen sind für Microsoft Digest; Sowohl der Client als auch der Server müssen gültige Anmeldeinformationen angeben, bevor sie einen Sicherheitskontext für den Nachrichtenaustausch einrichten können. Anmeldeinformationenhandles werden verwendet, um Anmeldeinformationen zu erhalten und zu präsentieren.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Abrufen Microsoft Digest SSP-Anmeldeinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea17889331453f009d0d19b7b834e9a4b1301636ec41ef73e6557f79419b461
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921279"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a>Abrufen Microsoft Digest SSP-Anmeldeinformationen

[*Benutzeranmeldeinformationen*](../secgloss/c-gly.md) sind für Microsoft Digest; Sowohl der Client als auch der Server müssen gültige Anmeldeinformationen angeben, bevor sie einen [*Sicherheitskontext*](../secgloss/s-gly.md) für den Nachrichtenaustausch einrichten können. Anmeldeinformationenhandles werden verwendet, um Anmeldeinformationen zu erhalten und zu präsentieren.

Da das Anmeldeinformationshand handle zum Speichern von Konfigurationsinformationen verwendet wird, kann dasselbe Handle nicht sowohl für clientseitige als auch für serverseitige Vorgänge verwendet werden. Dies bedeutet, dass Anwendungen, die sowohl Client- als auch Serververbindungen unterstützen, mindestens zwei Anmeldeinformationenhandles erhalten müssen.

Rufen Sie die [**AcquireCredentialsHandle-Funktion**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) auf, um Microsoft Digest anmeldeinformationen zu erhalten.

Die folgenden C-Sprachbeispiele veranschaulichen das Abrufen von Anmeldeinformationen.

-   [Abrufen von Standard-Digestanmeldeinformationen](obtaining-default-digest-credentials.md)
-   [Abrufen alternativer Digestanmeldeinformationen](obtaining-alternate-digest-credentials.md)

 

 
