---
description: Der von Microsoft erweiterte DSS- und Diffie-Hellman-Kryptografieanbieter unterstützt Diffie-Hellman-Schlüsselaustausch, SHA-Hashing, DSA-Datensignatur und -überprüfung (FIPS 186-2) und symmetrische RC4-Verschlüsselungsalgorithmen.
ms.assetid: 90eca1e0-960f-4355-aef7-6e923100a6d8
title: Microsoft Enhanced DSS & Diffie-Hellman Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3eb3e70d90224b2d97612c5d63380171d3239e11915da4cdd8a38a0faea0b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425440"
---
# <a name="microsoft-enhanced-dss--diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS & Diffie-Hellman Cryptographic Provider

Der von Microsoft erweiterte DSS- und Diffie-Hellman-Kryptografieanbieter unterstützt *Diffie-Hellman-Schlüsselaustausch,* SHA-Hashing, DSA-Datensignatur und -überprüfung (FIPS 186-2) und symmetrische RC4-Verschlüsselungsalgorithmen. [](../secgloss/d-gly.md)

<dl> Anbietertyp: **PROV \_ DSS \_ DH**  
Anbietername: **MS \_ ENH \_ DSS \_ DH \_ PROV**  
</dl>

Dieser Kryptografieanbieter unterstützt die folgenden Algorithmen.

| Algorithmus-ID          | Algorithmustyp  | Standardgröße (Bits) | Beschreibung                                                                                                                                                |
|-----------------------|-----------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CALG \_ CYLINK \_ MEK** | Datenverschlüsselung | 40                  | CYLINK-Nachrichtenverschlüsselungsalgorithmus.                                                                                                                       |
| **CALG \_ RC2**         | Datenverschlüsselung | 128                 | RSA RC2.                                                                                                                                                   |
| **CALG \_ RC4**         | Datenverschlüsselung | 128                 | RSA RC4.                                                                                                                                                   |
| **CALG \_ DES**         | Datenverschlüsselung | 56                  | Data Encryption Standard (DES).                                                                                                                            |
| **CALG \_ 3DES \_ 112**   | Datenverschlüsselung | 112                 | Zwei Schlüssel triple DES.                                                                                                                                        |
| **CALG \_ 3DES**        | Datenverschlüsselung | 168                 | Drei Schlüssel triple DES.                                                                                                                                      |
| **CALG \_ SHA1**        | Hash            | 160                 | Secure-Hash-Algorithmus 1 (SHA-1).                                                                                                                           |
| **CALG \_ MD5**         | Hash            | 128                 | Message Digest 5 (MD5).                                                                                                                                    |
| **\_CALG-DSS-SIGN \_**   | Signatur       | 1024                | Digital Signature Algorithm (DSA).                                                                                                                         |
| **CALG \_ DH \_ SF**      | Schlüsselaustausch    | 1024                | Store [*Diffie-Hellman-Schlüsselaustauschalgorithmus.*](../secgloss/d-gly.md) |
| **CALG \_ DH \_ EPHEM**   | Schlüsselaustausch    | 1024                | [*Kurzlebiger Diffie-Hellman-Algorithmus.*](../secgloss/d-gly.md)                      |



 

 

 
