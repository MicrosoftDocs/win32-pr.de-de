---
description: Eine Verschlüsselungssammlung ist ein Satz von Kryptografiealgorithmen.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Verschlüsselungs Sammlungen in TLS/SSL (Schannel SSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa8b47aed266c49ac306adfd2aef78af269a39
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106373429"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a>Verschlüsselungs Sammlungen in TLS/SSL (Schannel SSP)

Eine Verschlüsselungssammlung ist ein Satz von Kryptografiealgorithmen. Die Schannel SSP-Implementierung der TLS/SSL-Protokolle verwendet Algorithmen aus einer Verschlüsselungs Sammlung zum Erstellen von Schlüsseln und Verschlüsseln von Informationen. Eine Verschlüsselungssammlung gibt einen Algorithmus für jede der folgenden Aufgaben an:

-   Schlüsselaustausch
-   Massenverschlüsselung
-   Nachrichtenauthentifizierung

[*Schlüsselaustausch Algorithmen*](/windows/desktop/SecGloss/k-gly) schützen die Informationen, die zum Erstellen von freigegebenen Schlüsseln erforderlich sind Diese Algorithmen sind asymmetrisch ([*Algorithmen mit öffentlichem Schlüssel*](/windows/desktop/SecGloss/p-gly)) und eignen sich gut für relativ kleine Datenmengen.

Massen Verschlüsselungsalgorithmen verschlüsseln Nachrichten, die zwischen Clients und Servern ausgetauscht werden. Diese Algorithmen sind [*symmetrisch*](/windows/desktop/SecGloss/s-gly) und gut für große Datenmengen geeignet.

[Nachrichten Authentifizierungs](message-authentication-codes-in-schannel.md) Algorithmen generieren [*Nachrichtenhashes*](/windows/desktop/SecGloss/h-gly) und Signaturen, die die [*Integrität*](/windows/desktop/SecGloss/i-gly) einer Nachricht gewährleisten.

Entwickler geben diese Elemente mithilfe von [**ALG- \_ ID**](/windows/desktop/SecCrypto/alg-id) -Datentypen an. Weitere Informationen finden Sie unter [Angeben von SChannel-Chiffren und Verschlüsselungs stärken](specifying-schannel-ciphers-and-cipher-strengths.md).

In früheren Versionen von Windows wurden TLS-Verschlüsselungs Sammlungen und elliptische Kurven mithilfe einer einzelnen Zeichenfolge konfiguriert:

![Diagramm, das eine einzelne Zeichenfolge für eine Verschlüsselungs Sammlung anzeigt.](images/tls-cipher-suite.png)

Unterschiedliche Windows-Versionen unterstützen verschiedene TLS-Verschlüsselungs Sammlungen und Prioritäts Reihenfolge. Sehen Sie sich die entsprechende Windows-Version für die Standard Reihenfolge an, in der Sie vom Microsoft SChannel-Anbieter ausgewählt werden.

**Windows Server 2022:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter TLS-Verschlüsselungs Sammlungen [in Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md) .

**Windows 10, Version 1903:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter [TLS Chiffre Suites in Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)

**Windows 10, Version 1809:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter [TLS Chiffre Suites in Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)

**Windows 10, Version 1803:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter [TLS Chiffre Suites in Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)

**Windows 10, Version 1709:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter [TLS Chiffre Suites in Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)

**Windows 10, Version 1703:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter [TLS Chiffre Suites in Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)

**Windows Server 2016 und Windows 10, Version 1607:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter [TLS Chiffre Suites in Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)

**Windows 10, Version 1511:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter [TLS Chiffre Suites in Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)

**Windows 10, Version 1507:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter [TLS Chiffre Suites in Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)

**Windows Server 2012 R2 und Windows 8.1:** Weitere Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter TLS-Verschlüsselungs Sammlungen [in Windows 8.1](tls-cipher-suites-in-windows-8-1.md)

**Windows Server 2012 und Windows 8:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter TLS-Verschlüsselungs Sammlungen [in Windows 8](tls-cipher-suites-in-windows-8.md) .

**Windows Server 2008 R2 und Windows 7:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter TLS-Verschlüsselungs Sammlungen [in Windows 7](tls-cipher-suites-in-windows-7.md)

**Windows Server 2008 und Windows Vista:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie unter TLS-Verschlüsselungs Sammlungen [in Windows Vista](schannel-cipher-suites-in-windows-vista.md) .

**Windows Server 2003 und Windows XP:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie in den folgenden Themen.

| Thema                                                                         | BESCHREIBUNG                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [TLS-Verschlüsselungs Sammlungen](tls-cipher-suites.md)<br/>                         | Informationen zu den Verschlüsselungs Sammlungen, die mit dem TLS-Protokoll in Windows Server 2003 und Windows XP verfügbar sind.<br/>              |
| [Secure Sockets Layer-Protokoll](secure-sockets-layer-protocol.md)<br/> | Allgemeine Informationen zu SSL 2,0 und 3,0, einschließlich der verfügbaren Verschlüsselungs Sammlungen in Windows Server 2003 und Windows XP.<br/> |



 

> [!Note]  
> Vor Windows 10 wurden Chiffre Sammlungs Zeichenfolgen mit der elliptischen Kurve angehängt, um die Kurven Priorität zu bestimmen. Windows 10 unterstützt eine Einstellung für die Prioritäts Reihenfolge der elliptischen Kurven, damit das elliptische Kurven Suffix nicht erforderlich ist und von der neuen Priorität der elliptischen Kurven Priorität außer Kraft gesetzt wird, um Organisationen die Verwendung von Gruppenrichtlinien zum Konfigurieren verschiedener Versionen von Windows mit denselben Verschlüsselungs Sammlungen zu ermöglichen.

 

