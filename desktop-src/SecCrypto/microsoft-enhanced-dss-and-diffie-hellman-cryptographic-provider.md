---
description: Der von Microsoft erweiterte DSS und Diffie-Hellman Kryptografieanbieter unterstützt Diffie-Hellman Key Exchange, SHA-Hashwert, DSA-Daten Signierung und-Verifizierung (fps 186-2) und symmetrische RC4-Verschlüsselungsalgorithmen.
ms.assetid: 90eca1e0-960f-4355-aef7-6e923100a6d8
title: Microsoft Enhanced DSS & Diffie-Hellman Kryptografieanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c42b4e504c1e5d4cb8ccfea7405580e37362f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356506"
---
# <a name="microsoft-enhanced-dss--diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS & Diffie-Hellman Kryptografieanbieter

Der Microsoft Enhanced DSS [*-und Diffie-Hellman-*](../secgloss/d-gly.md) Kryptografieanbieter unterstützt *Diffie-Hellman-* Schlüsselaustausch, SHA-Hashwert, DSA-Daten Signierung und-Verifizierung (fps 186-2) und symmetrische RC4-Verschlüsselungsalgorithmen.

<dl> Anbietertyp: **Prov \_ DSS \_ dh**  
Anbieter Name: **MS \_ Enh \_ DSS \_ dh \_ Prov**  
</dl>

Dieser Kryptografieanbieter unterstützt die folgenden Algorithmen.

| Algorithmuskennung          | Algorithmustyp  | Standardgröße (Bits) | BESCHREIBUNG                                                                                                                                                |
|-----------------------|-----------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **calg \_ Cylink \_ MEK** | Datenverschlüsselung | 40                  | Algorithmus für die Cylink-Nachrichten Verschlüsselung.                                                                                                                       |
| **Calg \_ RC2**         | Datenverschlüsselung | 128                 | RSA RC2.                                                                                                                                                   |
| **Calg \_ RC4**         | Datenverschlüsselung | 128                 | RSA RC4.                                                                                                                                                   |
| **" \_ calg"**         | Datenverschlüsselung | 56                  | Daten Verschlüsselungs Standard (Data Encryption Standard, des).                                                                                                                            |
| **Calg \_ 3DES \_ 112**   | Datenverschlüsselung | 112                 | Zwei wichtige Triple des.                                                                                                                                        |
| **Calg \_ 3DES**        | Datenverschlüsselung | 168                 | Drei wichtige Triple des.                                                                                                                                      |
| **Calg \_ SHA1**        | Hash            | 160                 | Secure-Hash-Algorithmus 1 (SHA-1).                                                                                                                           |
| **Calg \_ MD5**         | Hash            | 128                 | Message Digest 5 (MD5).                                                                                                                                    |
| **calg- \_ DSS- \_ Zeichen**   | Signatur       | 1024                | Digital Signature-Algorithmus (DSA).                                                                                                                         |
| **"calg \_ dh \_ SF"**      | Schlüsselaustausch    | 1024                | Der Algorithmus zum Speichern und Weiterleiten von [*Diffie-Hellman-*](../secgloss/d-gly.md) Schlüsselaustausch. |
| **calg \_ dh- \_ ephem**   | Schlüsselaustausch    | 1024                | Der kurzlebige [*Diffie-Hellman-*](../secgloss/d-gly.md) Algorithmus.                      |



 

 

 
