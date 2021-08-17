---
description: Ein Satz kryptografischer Algorithmen. Schannel-Protokolle verwenden Algorithmen einer Verschlüsselungssammlung zum Erstellen von Schlüsseln und Verschlüsseln von Informationen.
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: TLS Cipher-Suites in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf77d821612093e3015a0f8dee4cf51ae5bd9b95c653b61fe7a36271ba81ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918653"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>TLS Cipher-Suites in Windows Vista

Eine Verschlüsselungssammlung ist ein Satz von Kryptografiealgorithmen. Schannel-Protokolle verwenden Algorithmen einer Verschlüsselungssammlung zum Erstellen von Schlüsseln und Verschlüsseln von Informationen. Eine Verschlüsselungssammlung gibt einen Algorithmus für jede der folgenden Aufgaben an:

-   Schlüsselaustausch
-   Massenverschlüsselung
-   Nachrichtenauthentifizierung

[*Schlüsselaustauschalgorithmen schützen Informationen,*](../secgloss/k-gly.md) die zum Erstellen gemeinsam verwendeter Schlüssel erforderlich sind. Diese Algorithmen sind asymmetrisch [*(Algorithmen für öffentliche Schlüssel)*](../secgloss/p-gly.md)und gut für relativ kleine Datenmengen.

Massenverschlüsselungsalgorithmen verschlüsseln Nachrichten, die zwischen Clients und Servern ausgetauscht werden. Diese Algorithmen sind [*symmetrisch und*](../secgloss/s-gly.md) gut für große Datenmengen.

[Nachrichtenauthentifizierungsalgorithmen](message-authentication-codes-in-schannel.md) generieren [*Nachrichtenhashes*](../secgloss/h-gly.md) und Signaturen, die die [*Integrität*](../secgloss/i-gly.md) einer Nachricht sicherstellen.

Entwickler geben diese Elemente mithilfe von [**\_ ALG-ID-Datentypen**](../seccrypto/alg-id.md) an. Weitere Informationen finden Sie unter [Specifying Schannel Ciphers and Cipher Strengths (Angeben von Schannel-Verschlüsselungen und Verschlüsselungsstärken).](specifying-schannel-ciphers-and-cipher-strengths.md)

Schannel unterstützt die folgenden Verschlüsselungssammlungen. Die Suiten werden in der Standard reihenfolge aufgelistet, in der sie vom Microsoft Schannel-Anbieter ausgewählt werden.

> [!IMPORTANT]
> HTTP/2-Webdienste führen zu einem Fehler mit nicht HTTP/2-kompatiblen Verschlüsselungssammlungen. Um sicherzustellen, dass Ihre Webdienste mit HTTP/2-Clients und -Browsern funktionieren, lesen Sie How to deploy custom cipher suite ordering (Bereitstellen einer [benutzerdefinierten Verschlüsselungssammlungsbestellung).](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 



| Cipher Suite                                                 | FIPS-Modus aktiviert | Exchange              | Verschlüsselung      | Hash            | Protokolle                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| TLS \_ RSA \_ MIT \_ AES \_ 128 \_ CBC \_ SHA<br/>                | Ja<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ MIT \_ AES \_ 256 \_ CBC \_ SHA<br/>                | Ja<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ MIT \_ RC4 \_ 128 \_ SHA<br/>                     | Nein<br/>     | RSA<br/>        | RC4<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ MIT \_ 3DES \_ EDE \_ CBC \_ SHA<br/>               | Ja<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/> | Ja<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/> | Ja<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/> | Ja<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC SHA \_ \_ P256<br/> | Ja<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC SHA \_ \_ P384<br/> | Ja<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ MIT \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/> | Ja<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/>   | Ja<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/>   | Ja<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/>   | Ja<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P256<br/>   | Ja<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P384<br/>   | Ja<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA MIT \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/>   | Ja<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 128 \_ CBC \_ SHA<br/>           | Ja<br/>    | DH<br/>         | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ AES \_ 256 \_ CBC \_ SHA<br/>           | Ja<br/>    | DH<br/>         | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ MIT \_ 3DES \_ EDE \_ CBC \_ SHA<br/>          | Ja<br/>    | DH<br/>         | 3DES<br/> | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ MIT \_ RC4 \_ 128 \_ MD5<br/>                     | Nein<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ MIT \_ MD5<br/>                      | Nein<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC MIT \_ \_ MD5<br/>           | Nein<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| TLS \_ RSA MIT NULL \_ \_ \_ MD5<br/>                         | Nein<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA MIT NULL \_ \_ \_ SHA<br/>                         | Nein<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |



 

Die folgenden Verschlüsselungssammlungen werden von Schannel unterstützt: sie sind jedoch nicht standardmäßig vorhanden. Sie müssen nach Bedarf hinzugefügt werden. Informationen zum Hinzufügen von Verschlüsselungssammlungen zum Schannel-Anbieter finden Sie unter [Priorisieren von Schannel Cipher Suites.](prioritizing-schannel-cipher-suites.md)

-   TLS \_ RSA \_ EXPORT \_ WITH \_ RC4 \_ 40 \_ MD5
-   TLS \_ RSA \_ EXPORT1024 \_ MIT \_ RC4 \_ 56 \_ SHA
-   TLS \_ RSA \_ EXPORT1024 \_ MIT DES \_ \_ CBC \_ SHA
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   SSL \_ CK \_ DES \_ 64 \_ CBC MIT \_ \_ MD5
-   TLS \_ RSA MIT DES \_ \_ \_ CBC \_ SHA
-   TLS \_ RSA MIT NULL \_ \_ \_ MD5
-   TLS \_ RSA MIT NULL \_ \_ \_ SHA
-   TLS \_ DHE \_ DSS \_ EXPORT1024 \_ MIT DES \_ \_ CBC \_ SHA
-   TLS \_ DHE \_ DSS \_ MIT DES \_ \_ CBC \_ SHA

**Windows Server 2003 und Windows XP:** Informationen zu unterstützten Verschlüsselungssammlungen finden Sie in den folgenden Themen.

| Thema                                                                         | BESCHREIBUNG                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [TLS-Verschlüsselungssammlungen](tls-cipher-suites.md)<br/>                         | Informationen zu den Verschlüsselungssammlungen, die mit dem TLS-Protokoll in Windows Server 2003 und Windows XP verfügbar sind.<br/>              |
| [Secure Sockets Layer-Protokoll](secure-sockets-layer-protocol.md)<br/> | Allgemeine Informationen zu SSL 2.0 und 3.0, einschließlich der verfügbaren Verschlüsselungssammlungen in Windows Server 2003 und Windows XP.<br/> |



 

 

 
