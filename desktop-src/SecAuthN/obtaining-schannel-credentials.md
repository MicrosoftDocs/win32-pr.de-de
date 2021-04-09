---
description: Anmelde Informationen sind für den SChannel-Authentifizierungsprozess erforderlich. sowohl der Client als auch der Server müssen gültige Anmelde Informationen zum Einrichten eines Sicherheits Kontexts für den Nachrichtenaustausch erhalten. Ein Beispiel zur Veranschaulichung dieses Verfahrens finden Sie unter "erhalten von Anmelde Informationen".
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Abrufen von SChannel-Anmelde Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756438"
---
# <a name="obtaining-schannel-credentials"></a>Abrufen von SChannel-Anmelde Informationen

Anmelde Informationen sind für den SChannel-Authentifizierungsprozess erforderlich. sowohl der Client als auch der Server müssen gültige Anmelde Informationen zum Einrichten eines [*Sicherheits Kontexts*](../secgloss/s-gly.md) für den Nachrichtenaustausch erhalten. Ein Beispiel zur Veranschaulichung dieses Verfahrens finden Sie unter " [erhalten von Anmelde](getting-a-certificate-for-schannel.md)Informationen".

Die Anwendung erhält Anmelde Informationen, indem Sie die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion aufruft, die ein Handle für die angeforderten Anmelde Informationen zurückgibt. Da Anmelde Informationen zum Speichern von Konfigurationsinformationen verwendet werden, kann das gleiche Handle nicht sowohl für Client seitige als auch für serverseitige Vorgänge verwendet werden. Dies bedeutet, dass Anwendungen, die sowohl Client-als auch Serververbindungen unterstützen, mindestens zwei Handles für die Anmelde Informationen erhalten müssen.

In Windows XP gibt eine [**SChannel- \_ Kred-**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) Struktur Folgendes an:

-   Ein Sicherheitsprotokoll
-   Die zulässigen Chiffren
-   Minimale und maximale Verschlüsselungsstärke
-   Ein für die Authentifizierung verwendetes [*X. 509*](../secgloss/x-gly.md) -Zertifikat – erforderlich für den-Server, sofern der Server keine Client Authentifizierung anfordert.

Übergeben Sie die [**SChannel- \_ Kred-**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) Struktur (über den *pauthdata* -Parameter) an die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion. Diese Funktion gibt den Anmelde Informations Handle zurück, der zum Einrichten eines [*Sicherheits Kontexts*](../secgloss/s-gly.md)erforderlich ist.

Ausführliche Informationen zum Festlegen der mit SChannel verwendeten Chiffren finden Sie unter [Angeben von SChannel-Chiffren und Verschlüsselungs stärken](specifying-schannel-ciphers-and-cipher-strengths.md).

Weitere Informationen zu Zertifikaten finden Sie unter [Zertifikat-und Zertifikat Speicherfunktionen](../seccrypto/cryptography-functions.md).

Ein Beispiel für das Öffnen eines [*Zertifikat Speicher*](../secgloss/c-gly.md) und Suchen eines Zertifikats für die SChannel-Authentifizierung finden Sie unter [erhalten eines Zertifikats](getting-a-certificate-for-schannel.md).

 

 
