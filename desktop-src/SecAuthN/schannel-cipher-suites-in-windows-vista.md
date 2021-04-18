---
description: Ein Satz kryptografischer Algorithmen. Schannel-Protokolle verwenden Algorithmen einer Verschlüsselungssammlung zum Erstellen von Schlüsseln und Verschlüsseln von Informationen.
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: TLS Cipher-Suites in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cf270f0608666b7d766e3f063f24ea39204fd1
ms.sourcegitcommit: b022a50bc0d11975dad6337b8f399c47234dffcf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106354886"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>TLS Cipher-Suites in Windows Vista

Eine Verschlüsselungssammlung ist ein Satz von Kryptografiealgorithmen. Schannel-Protokolle verwenden Algorithmen einer Verschlüsselungssammlung zum Erstellen von Schlüsseln und Verschlüsseln von Informationen. Eine Verschlüsselungssammlung gibt einen Algorithmus für jede der folgenden Aufgaben an:

-   Schlüsselaustausch
-   Massenverschlüsselung
-   Nachrichtenauthentifizierung

[*Schlüsselaustausch Algorithmen*](../secgloss/k-gly.md) schützen die Informationen, die zum Erstellen von freigegebenen Schlüsseln erforderlich sind Diese Algorithmen sind asymmetrisch ([*Algorithmen mit öffentlichem Schlüssel*](../secgloss/p-gly.md)) und eignen sich gut für relativ kleine Datenmengen.

Massen Verschlüsselungsalgorithmen verschlüsseln Nachrichten, die zwischen Clients und Servern ausgetauscht werden. Diese Algorithmen sind [*symmetrisch*](../secgloss/s-gly.md) und gut für große Datenmengen geeignet.

[Nachrichten Authentifizierungs](message-authentication-codes-in-schannel.md) Algorithmen generieren [*Nachrichtenhashes*](../secgloss/h-gly.md) und Signaturen, die die [*Integrität*](../secgloss/i-gly.md) einer Nachricht gewährleisten.

Entwickler geben diese Elemente mithilfe von [**ALG- \_ ID**](../seccrypto/alg-id.md) -Datentypen an. Weitere Informationen finden Sie unter [Angeben von SChannel-Chiffren und Verschlüsselungs stärken](specifying-schannel-ciphers-and-cipher-strengths.md).

SChannel unterstützt die folgenden Verschlüsselungs Sammlungen. Die Suites werden in der Standard Reihenfolge aufgelistet, in der Sie vom Microsoft SChannel-Anbieter ausgewählt werden.

> [!IMPORTANT]
> HTTP/2-Webdienste schlagen mit nicht-http/2-kompatiblen Verschlüsselungs Sammlungen fehl. Informationen zum sicherstellen, dass Ihre Webdienste mit http/2-Clients und-Browsern funktionieren, finden Sie unter Bereitstellen einer [benutzerdefinierten Chiffre Sammlungs Bestellung](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 



| Verschlüsselungs Sammlung                                                 | Aktivierter fps-Modus | Exchange              | Verschlüsselung      | Hash            | Protokolle                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| TLS \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA<br/>                | Ja<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA<br/>                | Ja<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS- \_ RSA \_ mit \_ RC4 \_ 128 \_ SHA<br/>                     | Nein<br/>     | RSA<br/>        | RC4<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ mit \_ 3DES \_ Ede \_ CBC \_ SHA<br/>               | Ja<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/> | Ja<br/>    | ECDH- \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/> | Ja<br/>    | ECDH- \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/> | Ja<br/>    | ECDH- \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/> | Ja<br/>    | ECDH- \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/> | Ja<br/>    | ECDH- \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ ECDSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/> | Ja<br/>    | ECDH- \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/>   | Ja<br/>    | ECDH- \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/>   | Ja<br/>    | ECDH- \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/>   | Ja<br/>    | ECDH- \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>   | Ja<br/>    | ECDH- \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>   | Ja<br/>    | ECDH- \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ecdhe \_ RSA \_ mit \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/>   | Ja<br/>    | ECDH- \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ mit \_ AES \_ 128 \_ CBC \_ SHA<br/>           | Ja<br/>    | DH<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ mit \_ AES \_ 256 \_ CBC \_ SHA<br/>           | Ja<br/>    | DH<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ mit \_ 3DES \_ Ede \_ CBC \_ SHA<br/>          | Ja<br/>    | DH<br/>         | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA \_ mit \_ RC4 \_ 128 \_ MD5<br/>                     | Nein<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ mit \_ MD5<br/>                      | Nein<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ mit \_ MD5<br/>           | Nein<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| TLS- \_ RSA \_ mit \_ NULL \_ MD5<br/>                         | Nein<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS- \_ RSA \_ mit NULL- \_ \_ SHA<br/>                         | Nein<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Die folgenden Verschlüsselungs Sammlungen werden von SChannel unterstützt. Sie sind jedoch nicht standardmäßig vorhanden. Sie müssen nach Bedarf hinzugefügt werden. Weitere Informationen zum Hinzufügen von Verschlüsselungs Sammlungen zum Schannel-Anbieter finden Sie unter [Priorisieren von SChannel](prioritizing-schannel-cipher-suites.md)-Verschlüsselungs Sammlungen.

-   TLS- \_ RSA- \_ Export \_ mit \_ RC4 \_ 40 \_ MD5
-   TLS- \_ RSA- \_ EXPORT1024 \_ mit \_ RC4 \_ 56 \_ SHA
-   TLS- \_ RSA- \_ EXPORT1024 \_ mit \_ des \_ CBC \_ SHA
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   SSL \_ CK \_ des \_ 64 \_ CBC \_ mit \_ MD5
-   TLS- \_ RSA \_ mit \_ des \_ CBC \_ SHA
-   TLS- \_ RSA \_ mit \_ NULL \_ MD5
-   TLS- \_ RSA \_ mit NULL- \_ \_ SHA
-   TLS \_ dhe \_ DSS \_ EXPORT1024 \_ mit \_ des \_ CBC \_ SHA
-   TLS \_ dhe \_ DSS \_ mit \_ des \_ CBC \_ SHA

**Windows Server 2003 und Windows XP:** Informationen zu unterstützten Verschlüsselungs Sammlungen finden Sie in den folgenden Themen.

| Thema                                                                         | BESCHREIBUNG                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [TLS-Verschlüsselungs Sammlungen](tls-cipher-suites.md)<br/>                         | Informationen zu den Verschlüsselungs Sammlungen, die mit dem TLS-Protokoll in Windows Server 2003 und Windows XP verfügbar sind.<br/>              |
| [Secure Sockets Layer-Protokoll](secure-sockets-layer-protocol.md)<br/> | Allgemeine Informationen zu SSL 2,0 und 3,0, einschließlich der verfügbaren Verschlüsselungs Sammlungen in Windows Server 2003 und Windows XP.<br/> |



 

 

 
