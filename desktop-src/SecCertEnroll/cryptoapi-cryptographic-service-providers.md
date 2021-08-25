---
description: Anbieter, die der Kryptografie-API (CryptoAPI) zugeordnet sind, werden in dieser Dokumentation als Kryptografiedienstanbieter (Cryptographic Service Providers, CSPs) bezeichnet.
ms.assetid: 28c9d348-7a37-4346-8b75-396d1349b152
title: Kryptografiedienstanbieter für CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c095fe4801cd57d4665fed0deec1649eb0a64420c13e4e5f486c7afc805447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906580"
---
# <a name="cryptoapi-cryptographic-service-providers"></a>Kryptografiedienstanbieter für CryptoAPI

Anbieter, die der Kryptografie-API [*(CryptoAPI)*](/windows/desktop/SecGloss/c-gly)zugeordnet sind, werden in dieser Dokumentation als Kryptografiedienstanbieter (Cryptographic Service Providers, CSPs) bezeichnet. CSPs implementieren in der Regel kryptografische Algorithmen und stellen Schlüsselspeicher zur Verfügung. Anbieter, die CNG zugeordnet sind, trennen hingegen die Algorithmusimplementierung vom Schlüsselspeicher. Die folgenden Microsoft CSPs werden mit Windows Vista und Windows Server 2008 verteilt.

## <a name="microsoft-base-cryptographic-provider-v10"></a>Microsoft Basis-Kryptografieanbieter v1.0

Implementiert die folgenden Algorithmen zum Hashen, Signieren und Verschlüsseln von Inhalten.



| Name                                            | Zweck          | type  | Schlüsselgröße (Standard/Min./Max.) |
|-------------------------------------------------|--------------|-------|----------------------------|
| Data Encryption Standard (DES)                  | Verschlüsselung   | Blockieren | 56/56/56                   |
| Hashed Message Authentication Checksum (HMAC)   | Hashing      | Any   | 0/0/0                      |
| Nachrichtenauthentifizierungs-Prüfsumme (MAC)           | Hashing      | Any   | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Any   | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Any   | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Any   | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung   | Blockieren | 40/40/56                   |
| RSA Data Security 4 (RC4)                       | Verschlüsselung   | Blockieren | 40/40/56                   |
| RSA-Exchange                                | Schlüsselaustausch | RSA   | 512/384/1024               |
| RSA-Signatur                                   | signatur-      | RSA   | 512/384/16384              |
| Sicherer Hashalgorithmus (SHA1)                    | Hashing      | Any   | 160/160/160                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing      | Any   | 288/288/288                |



 

## <a name="microsoft-base-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Base DSS und Diffie-Hellman Cryptographic Provider

Implementiert die folgenden Algorithmen, um Hashing, Signierung, Verschlüsselung und Diffie-Hellman Schlüsselaustausch zu unterstützen.



| Name                                  | Zweck          | type           | Schlüsselgröße (Standard/Min./Max.) |
|---------------------------------------|--------------|----------------|----------------------------|
| CYLINK Message Encryption-Algorithmus   | Verschlüsselung   | Blockieren          | 40/40/40                   |
| Data Encryption Standard (DES)        | Verschlüsselung   | Blockieren          | 56/56/56                   |
| Diffie-Hellman Key Exchange Algorithm | Schlüsselaustausch | Diffie-Hellman | 512/512/1024               |
| Diffie-Hellman Kurzlebiger Algorithmus    | Schlüsselaustausch | Diffie-Hellman | 512/512/1024               |
| Digital Signature Algorithm (DSA)     | signatur-      | Dss            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hashing      | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Verschlüsselung   | Blockieren          | 40/40/56                   |
| RSA Data Security 4 (RC4)             | Verschlüsselung   | STREAM         | 40/40/56                   |
| Sicherer Hashalgorithmus (SHA1)          | Hashing      | Any            | 160/160/160                |



 

## <a name="microsoft-base-dss-cryptographic-provider"></a>Microsoft Basis-DSS-Kryptografieanbieter

Implementiert die folgenden Algorithmen zum Signieren und Hashen von Inhalt:



| Name                              | Zweck     | type | Schlüsselgröße (Standard/Min./Max.) |
|-----------------------------------|---------|------|----------------------------|
| Digital Signature Algorithm (DSA) | signatur- | Dss  | 1024/512/1024              |
| Message Digest 5 (MD5)            | Hashing | Any  | 128/128/128                |
| Sicherer Hashalgorithmus (SHA1)      | Hashing | Any  | 160/160/160                |



 

## <a name="microsoft-base-smart-card-crypto-provider"></a>Microsoft BasisSmartcard-Kryptografieanbieter

Unterstützt Smartcards und implementiert die folgenden Algorithmen zum Hashen, Signieren und Verschlüsseln von Inhalten.

| Name                                            | Zweck          | type   | Schlüsselgröße (Standard/Min./Max.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Verschlüsselung   | Blockieren  | 128/128/128                |
| Advanced Encryption Standard 192 (AES192)       | Verschlüsselung   | Blockieren  | 192/192/192                |
| Advanced Encryption Standard 256 (AES256)       | Verschlüsselung   | Blockieren  | 256/256/256                |
| Data Encryption Standard (DES)                  | Verschlüsselung   | Blockieren  | 56/56/56                   |
| Two Key Triple DES                              | Verschlüsselung   | Blockieren  | 112/112/112                |
| Three Key Triple DES                            | Verschlüsselung   | Blockieren  | 168/168/168                |
| Hashed Message Authentication Checksum (HMAC)   | Hashing      | Any    | 0/0/0                      |
| Nachrichtenauthentifizierungs-Prüfsumme (MAC)           | Hashing      | Any    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung   | Blockieren  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Verschlüsselung   | STREAM | 128/40/128                 |
| RSA-Exchange                                | Schlüsselaustausch | RSA    | 1024/1024/4096             |
| RSA-Signatur                                   | signatur-      | RSA    | 1024/1024/4096             |
| Sicherer Hashalgorithmus (SHA1)                    | Hashing      | Any    | 160/160/160                |
| Sicherer Hashalgorithmus 256 (SHA256)              | Hashing      | Any    | 256/256/256                |
| Sicherer Hashalgorithmus 384 (SHA384)              | Hashing      | Any    | 384/384/384                |
| Sicherer Hashalgorithmus 512 (SHA512)              | Hashing      | Any    | 512/512/512                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing      | Any    | 288/288/288                |



 

## <a name="microsoft-dh-schannel-cryptographic-provider"></a>Microsoft DH Schannel Cryptographic Provider

Unterstützt das Schannel-Sicherheitspaket (Secure Channel), das die Authentifizierungsprotokolle Secure Sockets Layer (SSL) und Transport Layer Security (TLS) implementiert. Dieser CSP unterstützt auch Diffie-Hellman Schlüsselaustausch und implementiert die folgenden Algorithmen.



| Name                                   | Zweck                | type           | Schlüsselgröße (Standard/Min./Max.) |
|----------------------------------------|--------------------|----------------|----------------------------|
| CYLINK Message Encryption-Algorithmus    | Verschlüsselung         | Blockieren          | 40/40/40                   |
| Data Encryption Standard (DES)         | Verschlüsselung         | Blockieren          | 56/56/56                   |
| Two Key Triple DES                     | Verschlüsselung         | Blockieren          | 112/112/112                |
| Three Key Triple DES                   | Verschlüsselung         | Blockieren          | 168/168/168                |
| Diffie-Hellman Key Exchange Algorithm  | Schlüsselaustausch       | Diffie-Hellman | 512/512/4096               |
| Diffie-Hellman Kurzlebiger Algorithmus     | Schlüsselaustausch       | Diffie-Hellman | 512/512/4096               |
| Digital Signature Algorithm (DSA)      | signatur-            | Dss            | 1024/512/1024              |
| Message Digest 5 (MD5)                 | Hashing            | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)              | Verschlüsselung         | Blockieren          | 40/40/128                  |
| RSA Data Security 4 (RC4)              | Verschlüsselung         | STREAM         | 40/40/128                  |
| Sicherer Hashalgorithmus (SHA1)           | Hashing            | Any            | 160/160/160                |
| Schannel-Verschlüsselungsschlüssel                | Verschlüsselung         | Schannel       | 0/0/-1                     |
| Schannel-MAC-Taste                       | Verschlüsselung/Hashing | Schannel       | 0/0/-1                     |
| Schannel Master Hash                   | Verschlüsselung/Hashing | Schannel       | 0/0/-1                     |
| Secure Sockets Layer (SSL3) Master     | Verschlüsselung         | Schannel       | 384/384/384                |
| Transport Layer Security (TLS1) Master | Verschlüsselung         | Schannel       | 384/384/384                |



 

## <a name="microsoft-enhanced-cryptographic-provider-v10"></a>Microsoft erweiterter Kryptografieanbieter v1.0

Bietet höhere Sicherheit als der Microsoft Base Cryptographic Provider v1.0, indem längere Schlüssel mit einigen der vorhandenen Algorithmen verwendet und zusätzliche Algorithmen implementiert werden.



| Name                                            | Zweck          | type   | Schlüsselgröße (Standard/Min./Max.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Data Encryption Standard (DES)                  | Verschlüsselung   | Blockieren  | 56/56/56                   |
| Two Key Triple DES                              | Verschlüsselung   | Blockieren  | 112/112/112                |
|                                                 | Verschlüsselung   | Blockieren  | 168/168/168                |
| Hashed Message Authentication Checksum (HMAC)   | Hashing      | Any    | 0/0/0                      |
| Nachrichtenauthentifizierungs-Prüfsumme (MAC)           | Hashing      | Any    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung   | Blockieren  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Verschlüsselung   | STREAM | 128/40/128                 |
| RSA-Exchange                                | Schlüsselaustausch | RSA    | 1024/384/16384             |
| RSA-Signatur                                   | signatur-      | RSA    | 1024/384/16384             |
| Sicherer Hashalgorithmus (SHA1)                     | Hashing      | Any    | 160/160/160                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing      | Any    | 288/288/288                |



 

## <a name="microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider

Bietet höhere Sicherheit als der Microsoft Base-DSS- und Diffie-Hellman Cryptographic Provider-CSP, indem längere Schlüssel mit einigen der vorhandenen Algorithmen verwendet und zusätzliche Algorithmen implementiert werden.



| Name                                  | Zweck          | type           | Schlüsselgröße (Standard/Min./Max.) |
|---------------------------------------|--------------|----------------|----------------------------|
| CYLINK Message Encryption-Algorithmus   | Verschlüsselung   | Blockieren          | 40/40/40                   |
| Data Encryption Standard (DES)        | Verschlüsselung   | Blockieren          | 56/56/56                   |
| Two Key Triple DES                    | Verschlüsselung   | Blockieren          | 112/112/112                |
| Three Key Triple DES                  | Verschlüsselung   | Blockieren          | 168/168/168                |
| Diffie-Hellman Key Exchange Algorithm | Schlüsselaustausch | Diffie-Hellman | 1024/512/4096              |
| Diffie-Hellman Kurzlebiger Algorithmus    | Schlüsselaustausch | Diffie-Hellman | 1024/512/4096              |
| Digital Signature Algorithm (DSA)     | signatur-      | Dss            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hashing      | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Verschlüsselung   | Blockieren          | 128/128/128                |
| RSA Data Security 4 (RC4)             | Verschlüsselung   | STREAM         | 128/128/128                |
| Sicherer Hashalgorithmus (SHA1)          | Hashing      | Any            | 160/160/160                |



 

## <a name="microsoft-enhanced-rsa-and-aes-cryptographic-provider"></a>Microsoft Enhanced RSA and AES Cryptographic Provider

Implementiert die folgenden Algorithmen zum Signieren, Verschlüsseln und Hashinhalt.



| Name                                            | Zweck          | type   | Schlüsselgröße (Standard/Min./Max.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Verschlüsselung   | Blockieren  | 128/128/128                |
| Advanced Encryption Standard 192 (AES192)       | Verschlüsselung   | Blockieren  | 192/192/192                |
| Advanced Encryption Standard 256 (AES256)       | Verschlüsselung   | Blockieren  | 256/256/256                |
| Data Encryption Standard (DES)                  | Verschlüsselung   | Blockieren  | 56/56/56                   |
| Two Key Triple DES                              | Verschlüsselung   | Blockieren  | 112/112/112                |
| Three Key Triple DES                            | Verschlüsselung   | Blockieren  | 168/168/168                |
| Hashed Message Authentication Checksum (HMAC)   | Hashing      | Any    | 0/0/0                      |
| Prüfsumme der Nachrichtenauthentifizierung (MAC)           | Hashing      | Any    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung   | Blockieren  | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Verschlüsselung   | STREAM | 128/128/128                |
| RSA Key Exchange                                | Schlüsselaustausch | RSA    | 1024/384/16384             |
| RSA-Signatur                                   | signatur-      | RSA    | 1024/384/16384             |
| Secure Hash Algorithm (SHA1)                    | Hashing      | Any    | 160/160/160                |
| Secure Hash Algorithm (SHA256)                  | Hashing      | Any    | 256/256/256                |
| Sicherer Hashalgorithmus (SHA384)                  | Hashing      | Any    | 384/384/384                |
| Secure Hash Algorithm (SHA512)                  | Hashing      | Any    | 512/512/512                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing      | Any    | 288/288/288                |



 

## <a name="microsoft-rsa-schannel-cryptographic-provider"></a>Microsoft RSA Schannel Cryptographic Provider

Unterstützt das Schannel-Sicherheitspaket (RSA Secure Channel), das die Authentifizierungsprotokolle Secure Sockets Layer (SSL) und Transport Layer Security (TLS) implementiert.



| Name                                            | Zweck                | type     | Schlüsselgröße (Standard/Min./Max.) |
|-------------------------------------------------|--------------------|----------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Verschlüsselung         | Blockieren    | 128/128/128                |
| Advanced Encryption Standard 256 (AES256)       | Verschlüsselung         | Blockieren    | 256/256/256                |
| Data Encryption Standard (DES)                  | Verschlüsselung         | Blockieren    | 56/56/56                   |
| Two Key Triple DES                              | Verschlüsselung         | Blockieren    | 112/112/112                |
| Three Key Triple DES                            | Verschlüsselung         | Blockieren    | 168/168/168                |
| Hashed Message Authentication Checksum (HMAC)   | Hashing            | Any      | 0/0/0                      |
| Nachrichtenauthentifizierungs-Prüfsumme (MAC)           | Hashing            | Any      | 0/0/0                      |
| Message Digest 5 (MD5)                          | Hashing            | Any      | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung         | Blockieren    | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Verschlüsselung         | STREAM   | 128/128/128                |
| RSA-Exchange                                | Schlüsselaustausch       | RSA      | 1024/384/16384             |
| Schannel-Verschlüsselungsschlüssel                         | Verschlüsselung         | Schannel | 0/0/-1                     |
| Schannel Master Hash                            | Verschlüsselung/Hashing | Schannel | 0/0/-1                     |
| Schannel-MAC-Taste                                | Verschlüsselung/Hashing | Schannel | 0/0/-1                     |
| Sicherer Hashalgorithmus (SHA1)                    | Hashing            | Any      | 160/160/160                |
| Ssl2-Master (Secure Socket Layer 2)             | Verschlüsselung         | Schannel | 40/40/192                  |
| Ssl3-Master (Secure Socket Layer 3)             | Verschlüsselung         | Schannel | 384/384/384                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing            | Any      | 288/288/288                |
| Transport Layer Security (TLS1) Master          | Verschlüsselung         | Schannel | 384/384/384                |



 

## <a name="microsoft-strong-cryptographic-provider"></a>Microsoft starker Kryptografieanbieter

Implementiert die folgenden Algorithmen.



| Name                                            | Zweck          | type   | Schlüsselgröße (Standard/Min./Max.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Data Encryption Standard (DES)                  | Verschlüsselung   | Blockieren  | 56/56/56                   |
| Two Key Triple DES                              | Verschlüsselung   | Blockieren  | 112/112/112                |
| Three Key Triple DES                            | Verschlüsselung   | Blockieren  | 168/168/168                |
| Hashed Message Authentication Checksum (HMAC)   | Hashing      | Any    | 0/0/0                      |
| Nachrichtenauthentifizierungs-Prüfsumme (MAC)           | Hashing      | Any    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung   | Blockieren  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Verschlüsselung   | STREAM | 128/40/128                 |
| RSA-Exchange                                | Schlüsselaustausch | RSA    | 1024/384/16384             |
| RSA-Signatur                                   | signatur-      | RSA    | 1024/384/16384             |
| Sicherer Hashalgorithmus (SHA1)                    | Hashing      | Any    | 160/160/160                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing      | Any    | 288/288/288                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Kryptografieanbietern](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
