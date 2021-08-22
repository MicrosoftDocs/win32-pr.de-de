---
description: Eine Verschlüsselungssammlung ist ein Satz von Kryptografiealgorithmen.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Cipher Suites in TLS/SSL (Schannel SSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590012b4a1ef0c84b8216fd970d1e60c8ed449294ec110dc566e7c3679b7bb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141218"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a>Cipher Suites in TLS/SSL (Schannel SSP)

Eine Verschlüsselungssammlung ist ein Satz von Kryptografiealgorithmen. Die Schannel-SSP-Implementierung der TLS/SSL-Protokolle verwendet Algorithmen aus einer Verschlüsselungssammlung, um Schlüssel zu erstellen und Informationen zu verschlüsseln. Eine Verschlüsselungssammlung gibt einen Algorithmus für jede der folgenden Aufgaben an:

-   Schlüsselaustausch
-   Massenverschlüsselung
-   Nachrichtenauthentifizierung

[*Schlüsselaustauschalgorithmen*](/windows/desktop/SecGloss/k-gly) schützen Informationen, die zum Erstellen von gemeinsam verwendeten Schlüsseln erforderlich sind. Diese Algorithmen sind asymmetrisch [*(Algorithmen mit öffentlichem Schlüssel)*](/windows/desktop/SecGloss/p-gly)und eignen sich gut für relativ kleine Datenmengen.

Massenverschlüsselungsalgorithmen verschlüsseln Nachrichten, die zwischen Clients und Servern ausgetauscht werden. Diese Algorithmen sind [*symmetrisch*](/windows/desktop/SecGloss/s-gly) und eignen sich gut für große Datenmengen.

[Nachrichtenauthentifizierungsalgorithmen](message-authentication-codes-in-schannel.md) generieren [*Nachrichtenhashes*](/windows/desktop/SecGloss/h-gly) und Signaturen, die die [*Integrität*](/windows/desktop/SecGloss/i-gly) einer Nachricht sicherstellen.

Entwickler geben diese Elemente mithilfe von [**\_ ALG-ID-Datentypen**](/windows/desktop/SecCrypto/alg-id) an. Weitere Informationen finden Sie unter [Angeben von Schannel-Verschlüsselungen und Verschlüsselungsstärken.](specifying-schannel-ciphers-and-cipher-strengths.md)

In früheren Versionen von Windows wurden TLS-Verschlüsselungssammlungen und elliptische Kurven mit einer einzelnen Zeichenfolge konfiguriert:

![Diagramm, das eine einzelne Zeichenfolge für eine Cipher Suite zeigt.](images/tls-cipher-suite.png)

Unterschiedliche Windows Versionen unterstützen unterschiedliche TLS-Verschlüsselungssammlungen und Prioritätsreihenfolge. Die Standardreihenfolge, in der sie vom Microsoft Schannel-Anbieter ausgewählt werden, finden Sie in der entsprechenden Windows Version.

**Windows Server 2022:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows Server 2022.](tls-cipher-suites-in-windows-server-2022.md)

**Windows 10, Version 1903:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 10 v1903.](tls-cipher-suites-in-windows-10-v1903.md)

**Windows 10, Version 1809:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 10 v1809.](tls-cipher-suites-in-windows-10-v1809.md)

**Windows 10, Version 1803:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 10 v1803.](tls-cipher-suites-in-windows-10-v1803.md)

**Windows 10, Version 1709:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 10 v1709.](tls-cipher-suites-in-windows-10-v1709.md)

**Windows 10, Version 1703:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 10 v1703.](tls-cipher-suites-in-windows-10-v1703.md)

**Windows Server 2016 und Windows 10, Version 1607:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 10 v1607.](tls-cipher-suites-in-windows-10-v1607.md)

**Windows 10 Version 1511:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 10 v1511.](tls-cipher-suites-in-windows-10-v1511.md)

**Windows 10, Version 1507:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 10 v1507.](./tls-cipher-suites-in-windows-10--version-1507.md)

**Windows Server 2012 R2 und Windows 8.1:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 8.1](tls-cipher-suites-in-windows-8-1.md)

**Windows Server 2012 und Windows 8:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 8](tls-cipher-suites-in-windows-8.md)

**Windows Server 2008 R2 und Windows 7:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows 7.](tls-cipher-suites-in-windows-7.md)

**Windows Server 2008 und Windows Vista:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie unter [TLS-Verschlüsselungssammlungen in Windows Vista.](schannel-cipher-suites-in-windows-vista.md)

**Windows Server 2003 und Windows XP:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie in den folgenden Themen.

| Thema                                                                         | Beschreibung                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [TLS-Verschlüsselungssammlungen](tls-cipher-suites.md)<br/>                         | Informationen zu den Verschlüsselungssammlungen, die mit dem TLS-Protokoll in Windows Server 2003 und Windows XP verfügbar sind.<br/>              |
| [Secure Sockets Layer-Protokoll](secure-sockets-layer-protocol.md)<br/> | Allgemeine Informationen zu SSL 2.0 und 3.0, einschließlich der verfügbaren Verschlüsselungssammlungen in Windows Server 2003 und Windows XP.<br/> |



 

> [!Note]  
> Vor Windows 10 wurden Verschlüsselungssammlungszeichenfolgen mit der elliptischen Kurve angefügt, um die Kurvenpriorität zu bestimmen. Windows 10 unterstützt eine Prioritätsreihenfolgeeinstellung für elliptische Kurven, sodass das Suffix der elliptischen Kurve nicht erforderlich ist und von der neuen Prioritätsreihenfolge der elliptischen Kurve überschrieben wird, sofern angegeben, damit Organisationen gruppenrichtlinien verwenden können, um verschiedene Versionen von Windows mit denselben Verschlüsselungssammlungen zu konfigurieren.

 

