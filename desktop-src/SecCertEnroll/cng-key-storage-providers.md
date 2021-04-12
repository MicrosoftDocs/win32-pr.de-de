---
description: 'Im Unterschied zur Cryptography API (CryptoAPI) trennt Cryptography API: Next Generation (CNG) Kryptografieanbieter von Schlüsselspeicher Anbietern (Key Storage Providers, kSPS).'
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: CNG-Schlüsselspeicher Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393402"
---
# <a name="cng-key-storage-providers"></a>CNG-Schlüsselspeicher Anbieter

Im Unterschied zur Cryptography API (CryptoAPI) trennt Cryptography API: Next Generation (CNG) Kryptografieanbieter von Schlüsselspeicher Anbietern (Key Storage Providers, kSPS). KSPS können zum Erstellen, löschen, exportieren, importieren, öffnen und Speichern von Schlüsseln verwendet werden. Abhängig von der Implementierung können Sie auch für die asymmetrische Verschlüsselung, geheime Vereinbarung und Signierung verwendet werden. Microsoft installiert die folgenden kSPS ab Windows Vista und Windows Server 2008. Anbieter können andere Anbieter erstellen und installieren.

## <a name="microsoft-software-key-storage-provider"></a>Microsoft-Software Schlüsselspeicher-Anbieter

Unterstützt die Erstellung und Speicherung von Software Schlüsseln sowie die folgenden Algorithmen.



| Algorithmus                                          | Zweck                           | Schlüssellänge (Bits)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (dh)                                | Geheimer Vertrag und Schlüsselaustausch | 512 bis 4096 in 64-Bit-Inkrementen  |
| Digital Signature-Algorithmus (DSA)                  | Signaturen                        | 512 bis 1024 in 64-Bit-Inkrementen  |
| ECDH (Elliptic Curve Diffie-Hellman)               | Geheimer Vertrag und Schlüsselaustausch | P256, P384, P521                  |
| ECDSA (Elliptic Curve Digital Signature-Algorithmus) | Signaturen                        | P256, P384, P521                  |
| RSA                                                | Asymmetrische Verschlüsselung und Signierung | 512 bis 16384 in 64-Bit-Inkrementen |



 

## <a name="microsoft-smart-card-key-storage-provider"></a>Microsoft-Smartcard-Schlüsselspeicher Anbieter

Unterstützt die Erstellung und Speicherung von smartcardschlüsseln sowie die folgenden Algorithmen.



| Algorithmus                                          | Zweck                           | Schlüssellänge (Bits)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (dh)                                | Geheimer Vertrag und Schlüsselaustausch | 512 bis 4096 in 64-Bit-Inkrementen  |
| ECDH (Elliptic Curve Diffie-Hellman)               | Geheimer Vertrag und Schlüsselaustausch | P256, P384, P521                  |
| ECDSA (Elliptic Curve Digital Signature-Algorithmus) | Signaturen                        | P256, P384, P521                  |
| RSA                                                | Asymmetrische Verschlüsselung und Signierung | 512 bis 16384 in 64-Bit-Inkrementen |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CNG-Algorithmusbezeichner**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[CNG-Schlüsselspeicher Funktionen](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[Grundlegendes zu Kryptografieanbietern](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
