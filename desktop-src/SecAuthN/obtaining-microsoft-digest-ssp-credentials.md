---
description: Benutzer Anmelde Informationen sind für Microsoft Digest erforderlich. sowohl der Client als auch der Server müssen gültige Anmelde Informationen aufweisen, bevor Sie einen Sicherheitskontext für den Nachrichtenaustausch einrichten können. Anmelde Informationen werden verwendet, um Anmelde Informationen abzurufen und zu präsentieren.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Abrufen von Microsoft Digest SSP-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484710"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a>Abrufen von Microsoft Digest SSP-Anmelde Informationen

Benutzer [*Anmelde*](../secgloss/c-gly.md) Informationen sind für Microsoft Digest erforderlich. sowohl der Client als auch der Server müssen gültige Anmelde Informationen aufweisen, bevor Sie einen [*Sicherheitskontext*](../secgloss/s-gly.md) für den Nachrichtenaustausch einrichten können. Anmelde Informationen werden verwendet, um Anmelde Informationen abzurufen und zu präsentieren.

Da das Anmelde Informationen-Handle zum Speichern von Konfigurationsinformationen verwendet wird, kann das gleiche Handle nicht sowohl für Client seitige als auch für serverseitige Vorgänge verwendet werden. Dies bedeutet, dass Anwendungen, die sowohl Client-als auch Serververbindungen unterstützen, mindestens zwei Handles für die Anmelde Informationen erhalten müssen.

Um ein Handle für die für Microsoft Digest erforderlichen Anmelde Informationen abzurufen, müssen Sie die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion aufrufen.

Die folgenden C-sprach Beispiele veranschaulichen das Abrufen von Anmelde Informationen.

-   [Abrufen der standardmäßigen Hashwert](obtaining-default-digest-credentials.md)
-   [Abrufen alternativer Digest-Anmelde Informationen](obtaining-alternate-digest-credentials.md)

 

 
