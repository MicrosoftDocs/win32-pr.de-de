---
description: Die folgenden Algorithmen berechnen Hashes und digitale Signaturen. Jeder dieser Algorithmen wird in den Kryptografieanbietern Microsoft Base, Strong und Enhanced unterstützt.
ms.assetid: 91bf898d-658a-4e45-aa6e-eded46657563
title: Hash- und Signaturalgorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c176b3a21ac5793f249f9aa7aceda897d53ea209f3e8e6bd260dc5ec529c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006608"
---
# <a name="hash-and-signature-algorithms"></a>Hash- und Signaturalgorithmen

Die folgenden Algorithmen berechnen [*Hashes und*](../secgloss/h-gly.md) [*digitale Signaturen.*](../secgloss/d-gly.md) Jeder dieser Algorithmen wird in den Kryptografieanbietern Microsoft Base, Strong und Enhanced unterstützt. Interne Details dieser Algorithmen gehen über den Rahmen dieser Dokumentation hinaus. Eine Liste der zusätzlichen Quellen finden Sie in der [zusätzlichen Dokumentation zur Kryptografie.](additional-documentation-on-cryptography.md)



| Algorithmen                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cipher Block Chaining (CBC) MAC<br/>     | Einer der von Microsoft-Anbietern implementierten Algorithmen (CALG MAC) ist \_ ein Blockchiffren-Nachrichtenauthentifizierungscode [](../secgloss/b-gly.md) [](../secgloss/m-gly.md) (MAC). Diese Methode verschlüsselt die Basisdaten mit einem Blockchiffren und verwendet dann den letzten verschlüsselten Block als [*Hashwert.*](../secgloss/h-gly.md) Der Verschlüsselungsalgorithmus, der zum Erstellen des MAC verwendet wird, wurde beim Erstellen des Sitzungsschlüssels angegeben. <br/>                                                                            |
| HMAC<br/>                                | Ein Algorithmus (CALG \_ HMAC), der von Microsoft-Anbietern implementiert wird. Dieser Algorithmus verwendet auch einen [*symmetrischen*](../secgloss/s-gly.md) Schlüssel, um den Hash zu [*erstellen,*](../secgloss/h-gly.md)ist jedoch komplexer als der einfache CBC-MAC-Algorithmus [*(Cipher Block Chaining).*](../secgloss/c-gly.md) Sie kann mit jedem iterierten kryptografischen Hashalgorithmus wie MD5 oder SHA-1 verwendet werden. Weitere Informationen finden Sie unter [Erstellen eines HMAC.](creating-an-hmac.md)<br/>                                                                                       |
| MD2, MD4 und MD5<br/>                   | Diese Hashalgorithmen wurden alle von RSA Data Security, Inc. entwickelt. Diese Algorithmen wurden in sequenzieller Reihenfolge entwickelt. Alle drei generieren 128-Bit-Hashwerte. Es ist bekannt, dass alle drei Schwachstellen haben, und sollten nur verwendet werden, wenn dies aus Kompatibilitätsgründen erforderlich ist. Für neuen Code empfehlen wir die SHA-2-Hashfamilie.<br/> Diese Algorithmen sind bekannt und können in jeder Referenz zur Kryptografie ausführlich [*überprüft werden.*](../secgloss/c-gly.md)<br/>                                                                                                                                                           |
| Nachrichtenauthentifizierungscode (MAC)<br/>   | MAC-Algorithmen ähneln [*Hashalgorithmen,*](../secgloss/h-gly.md) werden jedoch mithilfe eines symmetrischen [*Schlüssels*](../secgloss/s-gly.md) (Sitzungsschlüssel) berechnet. Der ursprüngliche [*Sitzungsschlüssel ist*](../secgloss/s-gly.md) erforderlich, um den Hashwert neu zu kompilen. Der neu berechnete Hashwert wird verwendet, um sicherzustellen, dass die Basisdaten nicht geändert wurden. Diese Algorithmen werden manchmal als Schlüsselhashalgorithmen bezeichnet. Informationen dazu, welche Microsoft-Anbieter MAC unterstützen, finden Sie unter [Microsoft Cryptographic Service Providers](microsoft-cryptographic-service-providers.md).<br/>    |
| Sicherer Hashalgorithmus (SHA-1)<br/>       | Dieser Hashalgorithmus wurde vom [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) und der National Security Agency (NSA) entwickelt. Dieser Algorithmus wurde für die Verwendung mit DSA (Digital Signature Algorithm) oder DSS (Digital Signature Standard) entwickelt. Dieser Algorithmus generiert einen 160-Bit-Hashwert. [](../secgloss/h-gly.md) SHA-1 ist bekannt, dass es Schwachstellen gibt, und sollte nur verwendet werden, wenn dies aus Kompatibilitätsgründen erforderlich ist. Für neuen Code empfehlen wir die SHA-2-Hashfamilie.<br/> |
| Sicherer Hashalgorithmus – 2 (SHA-2)<br/>   | Dieser Hashalgorithmus wurde als Nachfolger von SHA-1 vom [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) und der National Security Agency (NSA) entwickelt. Es verfügt über vier Varianten – SHA-224, SHA-256, SHA-384 und SHA-512 – die entsprechend der Anzahl der Bits in ihren Ausgaben benannt werden. Davon werden SHA-256, SHA-384 und SHA-512 im Microsoft AES Cryptographic Provider implementiert.<br/>                                                                                                                                |
| SSL3-Clientautorisierungsalgorithmus<br/> | Dieser Algorithmus wird für die SSL3-Clientauthentifizierung verwendet. Im SSL3-Protokoll wird eine Verkettung eines MD5-Hashs und eines SHA-Hashs mit einem privaten [*RSA-Schlüssel signiert.*](../secgloss/p-gly.md) CryptoAPI 2.0 und die Microsoft Base- und Enhanced Cryptographic Providers unterstützen dies mit dem [*Hashtyp*](../secgloss/h-gly.md) CALG \_ SSL3 \_ SHAMD5. Weitere Informationen finden Sie unter [Creating a CALG \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                                                                                                               |



 

 

 
