---
description: Anmeldeinformationen sind für den Schannel-Authentifizierungsprozess erforderlich. Sowohl der Client als auch der Server müssen gültige Anmeldeinformationen abrufen, um einen Sicherheitskontext für den Nachrichtenaustausch zu erstellen. Ein Beispiel, das dieses Verfahren veranschaulicht, finden Sie unter Abrufen von Anmeldeinformationen.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Abrufen von Schannel-Anmeldeinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216965d5b6fb1b21c36425242f54150112b2dcfb00dd7184c828aba865bbb5a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921198"
---
# <a name="obtaining-schannel-credentials"></a>Abrufen von Schannel-Anmeldeinformationen

Anmeldeinformationen sind für den Schannel-Authentifizierungsprozess erforderlich. Sowohl der Client als auch der Server müssen gültige Anmeldeinformationen abrufen, um einen [*Sicherheitskontext für den*](../secgloss/s-gly.md) Nachrichtenaustausch zu erstellen. Ein Beispiel, das dieses Verfahren veranschaulicht, finden Sie unter [Abrufen von Anmeldeinformationen.](getting-a-certificate-for-schannel.md)

Ihre Anwendung ruft Anmeldeinformationen ab, indem sie die [**AcquireCredentialsHandle-Funktion**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) aufruft, die ein Handle für die angeforderten Anmeldeinformationen zurückgibt. Da Anmeldeinformationshandles zum Speichern von Konfigurationsinformationen verwendet werden, kann dasselbe Handle nicht sowohl für clientseitige als auch für serverseitige Vorgänge verwendet werden. Dies bedeutet, dass Anwendungen, die sowohl Client- als auch Serververbindungen unterstützen, mindestens zwei Anmeldeinformationenhandles erhalten müssen.

In Windows XP gibt eine [**SCHANNEL \_ CRED-Struktur**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) Folgendes an:

-   Ein Sicherheitsprotokoll
-   Die zulässigen Verschlüsselungen
-   Minimale und maximale Verschlüsselungsstärke
-   Ein [*X.509-Zertifikat,*](../secgloss/x-gly.md) das für die Authentifizierung verwendet wird– Erforderlich für server, optional für Client, es sei denn, der Server fordert clientauthentifizierung an.

Übergeben Sie [**die SCHANNEL \_ CRED-Struktur**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (über den *pAuthData-Parameter)* an die [**AcquireCredentialsHandle-Funktion.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) Diese Funktion gibt das Anmeldeinformationenhand handle zurück, das zum Einrichten eines [*Sicherheitskontexts erforderlich ist.*](../secgloss/s-gly.md)

Ausführliche Informationen zum Festlegen der mit Schannel verwendeten Verschlüsselungen finden Sie unter [Specifying Schannel Ciphers and Cipher Strengths (Angeben von Schannel-Verschlüsselungen und Verschlüsselungsstärken).](specifying-schannel-ciphers-and-cipher-strengths.md)

Informationen zu Zertifikaten finden Sie unter [Certificate and Certificate Store Functions](../seccrypto/cryptography-functions.md).

Ein Beispiel, das das [](../secgloss/c-gly.md) Öffnen eines Zertifikatspeichers und das Suchen eines Zertifikats für die Schannel-Authentifizierung veranschaulicht, finden Sie unter [Abrufen eines Zertifikats.](getting-a-certificate-for-schannel.md)

 

 
