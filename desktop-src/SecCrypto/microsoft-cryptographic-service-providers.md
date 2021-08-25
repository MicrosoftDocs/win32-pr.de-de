---
description: Listet die kryptografischen Dienstanbieter auf, die von Microsoft verfügbar sind.
ms.assetid: 1461914e-5506-4f24-97da-3d2148aafd1c
title: Microsoft Cryptographic Service Providers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cac0ff0276a548e5855a3f2d0d69cac3dcdc2ab35001a7f8dcabdb5cfd62bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992820"
---
# <a name="microsoft-cryptographic-service-providers"></a>Microsoft Cryptographic Service Providers

Die folgenden [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (Cryptographic Service Providers, CSP) sind derzeit von Microsoft verfügbar.



| Anbieter                                                                                                                                 | Beschreibung                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md)                                                       | Eine breite Palette grundlegender kryptografischer Funktionen, die in andere Länder oder Regionen exportiert werden können.                                                                                                                                                     |
| [Microsoft starker Kryptografieanbieter](microsoft-strong-cryptographic-provider.md)                                                   | Eine Erweiterung des Microsoft Base Cryptographic Provider, die mit Windows XP und höher verfügbar ist.                                                                                                                                                           |
| [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md)                                               | Microsoft Base Cryptographic Provider mit über längere Schlüssel und zusätzliche Algorithmen.                                                                                                                                                                |
| [Microsoft AES-Kryptografieanbieter](microsoft-aes-cryptographic-provider.md)                                                         | Microsoft Enhanced Cryptographic Provider mit Unterstützung für AES-Verschlüsselungsalgorithmen.                                                                                                                                                                    |
| [Microsoft DSS-Kryptografieanbieter](microsoft-dss-cryptographic-provider.md)                                                         | Bietet Hashing-, Datensignatur- und Signaturüberprüfungsfunktionen mithilfe der Algorithmen Secure Hash Algorithm [*(SHA)*](../secgloss/s-gly.md)und Digital Signature Standard (DSS). |
| [Microsoft Base DSS und Diffie-Hellman Cryptographic Provider](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)         | Eine Obermenge des DSS-Kryptografieanbieters, der auch Diffie-Hellman-Schlüsselaustausch, Hashing, Datensignatur und Signaturüberprüfung mithilfe der Algorithmen Secure Hash Algorithm (SHA) und Digital Signature Standard (DSS) unterstützt.                    |
| [Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md) | Unterstützt Diffie-Hellman Schlüsselaustausch (eine 40-Bit-DES-Ableitung), SHA-Hashing, DSS-Datensignatur und DSS-Signaturüberprüfung.                                                                                                                           |
| [Microsoft DSS und Diffie-Hellman/Schannel Cryptographic Provider](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md) | Unterstützt Hashing, Datensignierung mit DSS, Generieren von Diffie-Hellman-Schlüsseln (D-H), Austauschen von D-H-Schlüsseln und Exportieren eines D-H-Schlüssels. Dieser CSP unterstützt die Schlüsselableitung für die Protokolle SSL3 und TLS1.                                                           |
| [Microsoft RSA/Schannel Cryptographic Provider](microsoft-rsa-schannel-cryptographic-provider.md)                                       | Unterstützt Hashing, Datensignatur und Signaturüberprüfung. Der Algorithmusbezeichner CALG \_ SSL3 SHAMD5 wird für die \_ SSL 3.0- und TLS 1.0-Clientauthentifizierung verwendet. Dieser CSP unterstützt die Schlüsselableitung für die Protokolle SSL2, PCT1, SSL3 und TLS1.             |
| [Microsoft RSA Signature Cryptographic Provider](microsoft-rsa-signature-cryptographic-provider.md)                                     | Bietet Datensignatur und Signaturüberprüfung.                                                                                                                                                                                                        |



 

 

 
