---
description: Der kryptografieapi (CryptoAPI) zugeordnete Anbieter werden in dieser Dokumentation als Kryptografiedienstanbieter (Kryptografiedienstanbieter) bezeichnet.
ms.assetid: 28c9d348-7a37-4346-8b75-396d1349b152
title: Kryptografiedienstanbieter von CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b3820a0d45534bc5c492d843352be038f7ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129889"
---
# <a name="cryptoapi-cryptographic-service-providers"></a>Kryptografiedienstanbieter von CryptoAPI

Der kryptografieapi ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) zugeordnete Anbieter werden in dieser Dokumentation als Kryptografiedienstanbieter (Kryptografiedienstanbieter) bezeichnet. CSPs implementieren in der Regel kryptografische Algorithmen und stellen Schlüsselspeicher bereit. Mit CNG verknüpfte Anbieter hingegen trennen die Algorithmusimplementierung von Key Storage. Die folgenden Microsoft-CSPs werden mit Windows Vista und Windows Server 2008 verteilt.

## <a name="microsoft-base-cryptographic-provider-v10"></a>Microsoft Basis-Kryptografieanbieter v1.0

Implementiert die folgenden Algorithmen zum Hashen, Signieren und Verschlüsseln von Inhalten.



| Name                                            | Zweck          | type  | Schlüsselgröße (Standard/min/max) |
|-------------------------------------------------|--------------|-------|----------------------------|
| Data Encryption Standard (des)                  | Verschlüsselung   | Blockieren | 56/56/56                   |
| Prüfsumme für Hash Nachrichten Authentifizierung (HMAC)   | Hashing      | Any   | 0/0/0                      |
| Prüfsumme für Nachrichten Authentifizierung (Mac)           | Hashing      | Any   | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Any   | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Any   | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Any   | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung   | Blockieren | 40/40/56                   |
| RSA Data Security 4 (RC4)                       | Verschlüsselung   | Blockieren | 40/40/56                   |
| RSA-Schlüsselaustausch                                | Schlüsselaustausch | RSA   | 512/384/1024               |
| RSA-Signatur                                   | signatur-      | RSA   | 512/384/16384              |
| Secure Hash-Algorithmus (SHA1)                    | Hashing      | Any   | 160/160/160                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing      | Any   | 288/288/288                |



 

## <a name="microsoft-base-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Base DSS und Diffie-Hellman Kryptografieanbieter

Implementiert die folgenden Algorithmen, um Hash-, Signatur-, Verschlüsselungs-und Diffie-Hellman Schlüsselaustausch zu unterstützen.



| Name                                  | Zweck          | type           | Schlüsselgröße (Standard/min/max) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algorithmus für Cylink-Nachrichten Verschlüsselung   | Verschlüsselung   | Blockieren          | 40/40/40                   |
| Data Encryption Standard (des)        | Verschlüsselung   | Blockieren          | 56/56/56                   |
| Diffie-Hellman Schlüsselaustausch Algorithmus | Schlüsselaustausch | Diffie-Hellman | 512/512/1024               |
| Diffie-Hellman kurzlebigen Algorithmus    | Schlüsselaustausch | Diffie-Hellman | 512/512/1024               |
| Digital Signature-Algorithmus (DSA)     | signatur-      | DSS            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hashing      | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Verschlüsselung   | Blockieren          | 40/40/56                   |
| RSA Data Security 4 (RC4)             | Verschlüsselung   | Datenstrom         | 40/40/56                   |
| Secure Hash-Algorithmus (SHA1)          | Hashing      | Any            | 160/160/160                |



 

## <a name="microsoft-base-dss-cryptographic-provider"></a>Microsoft Basis-DSS-Kryptografieanbieter

Implementiert die folgenden Algorithmen zum Signieren und zum Hash von Inhalten:



| Name                              | Zweck     | type | Schlüsselgröße (Standard/min/max) |
|-----------------------------------|---------|------|----------------------------|
| Digital Signature-Algorithmus (DSA) | signatur- | DSS  | 1024/512/1024              |
| Message Digest 5 (MD5)            | Hashing | Any  | 128/128/128                |
| Secure Hash-Algorithmus (SHA1)      | Hashing | Any  | 160/160/160                |



 

## <a name="microsoft-base-smart-card-crypto-provider"></a>Microsoft BasisSmartcard-Kryptografieanbieter

Unterstützt Smartcards und implementiert die folgenden Algorithmen zum Hashen, Signieren und Verschlüsseln von Inhalten.

| Name                                            | Zweck          | type   | Schlüsselgröße (Standard/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Verschlüsselung   | Blockieren  | 128/128/128                |
| Advanced Encryption Standard 192 (AES192)       | Verschlüsselung   | Blockieren  | 192/192/192                |
| Advanced Encryption Standard 256 (AES256)       | Verschlüsselung   | Blockieren  | 256/256/256                |
| Data Encryption Standard (des)                  | Verschlüsselung   | Blockieren  | 56/56/56                   |
| Zwei wichtige Dreifache des                              | Verschlüsselung   | Blockieren  | 112/112/112                |
| Drei wichtige Dreifache des                            | Verschlüsselung   | Blockieren  | 168/168/168                |
| Prüfsumme für Hash Nachrichten Authentifizierung (HMAC)   | Hashing      | Any    | 0/0/0                      |
| Prüfsumme für Nachrichten Authentifizierung (Mac)           | Hashing      | Any    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung   | Blockieren  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Verschlüsselung   | Datenstrom | 128/40/128                 |
| RSA-Schlüsselaustausch                                | Schlüsselaustausch | RSA    | 1024/1024/4096             |
| RSA-Signatur                                   | signatur-      | RSA    | 1024/1024/4096             |
| Secure Hash-Algorithmus (SHA1)                    | Hashing      | Any    | 160/160/160                |
| Secure Hash-Algorithmus 256 (SHA256)              | Hashing      | Any    | 256/256/256                |
| Secure Hash-Algorithmus 384 (SHA384)              | Hashing      | Any    | 384/384/384                |
| Secure Hash-Algorithmus 512 (SHA512)              | Hashing      | Any    | 512/512/512                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing      | Any    | 288/288/288                |



 

## <a name="microsoft-dh-schannel-cryptographic-provider"></a>Kryptografieanbieter für Microsoft DH SChannel

Unterstützt das SChannel-Sicherheitspaket (Secure Channel), das Secure Sockets Layer Authentifizierungsprotokolle (SSL) und Transport Layer Security (TLS) implementiert. Dieser CSP unterstützt auch Diffie-Hellman Schlüsselaustausch und implementiert die folgenden Algorithmen.



| Name                                   | Zweck                | type           | Schlüsselgröße (Standard/min/max) |
|----------------------------------------|--------------------|----------------|----------------------------|
| Algorithmus für Cylink-Nachrichten Verschlüsselung    | Verschlüsselung         | Blockieren          | 40/40/40                   |
| Data Encryption Standard (des)         | Verschlüsselung         | Blockieren          | 56/56/56                   |
| Zwei wichtige Dreifache des                     | Verschlüsselung         | Blockieren          | 112/112/112                |
| Drei wichtige Dreifache des                   | Verschlüsselung         | Blockieren          | 168/168/168                |
| Diffie-Hellman Schlüsselaustausch Algorithmus  | Schlüsselaustausch       | Diffie-Hellman | 512/512/4096               |
| Diffie-Hellman kurzlebigen Algorithmus     | Schlüsselaustausch       | Diffie-Hellman | 512/512/4096               |
| Digital Signature-Algorithmus (DSA)      | signatur-            | DSS            | 1024/512/1024              |
| Message Digest 5 (MD5)                 | Hashing            | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)              | Verschlüsselung         | Blockieren          | 40/40/128                  |
| RSA Data Security 4 (RC4)              | Verschlüsselung         | Datenstrom         | 40/40/128                  |
| Secure Hash-Algorithmus (SHA1)           | Hashing            | Any            | 160/160/160                |
| SChannel-Verschlüsselungsschlüssel                | Verschlüsselung         | Schannel       | 0/0/-1                     |
| SChannel-Mac-Taste                       | Verschlüsselung/Hashvorgang | Schannel       | 0/0/-1                     |
| SChannel-Master Hash                   | Verschlüsselung/Hashvorgang | Schannel       | 0/0/-1                     |
| Secure Sockets Layer (SSL3) Master     | Verschlüsselung         | Schannel       | 384/384/384                |
| Transport Layer Security (das TLS1 verwendet) Master | Verschlüsselung         | Schannel       | 384/384/384                |



 

## <a name="microsoft-enhanced-cryptographic-provider-v10"></a>Microsoft erweiterter Kryptografieanbieter v1.0

Bietet eine höhere Sicherheit als der Microsoft-Basis-Kryptografieanbieter v 1.0, indem längere Schlüssel mit einigen der vorhandenen Algorithmen verwendet werden und zusätzliche Algorithmen implementiert werden.



| Name                                            | Zweck          | type   | Schlüsselgröße (Standard/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Data Encryption Standard (des)                  | Verschlüsselung   | Blockieren  | 56/56/56                   |
| Zwei wichtige Dreifache des                              | Verschlüsselung   | Blockieren  | 112/112/112                |
|                                                 | Verschlüsselung   | Blockieren  | 168/168/168                |
| Prüfsumme für Hash Nachrichten Authentifizierung (HMAC)   | Hashing      | Any    | 0/0/0                      |
| Prüfsumme für Nachrichten Authentifizierung (Mac)           | Hashing      | Any    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung   | Blockieren  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Verschlüsselung   | Datenstrom | 128/40/128                 |
| RSA-Schlüsselaustausch                                | Schlüsselaustausch | RSA    | 1024/384/16384             |
| RSA-Signatur                                   | signatur-      | RSA    | 1024/384/16384             |
| Secure Hash-Algorithmus (SHA1                     | Hashing      | Any    | 160/160/160                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing      | Any    | 288/288/288                |



 

## <a name="microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS und Diffie-Hellman Kryptografieanbieter

Bietet eine höhere Sicherheit als das Microsoft Base DSS und Diffie-Hellman Kryptografieanbieter-CSP, indem längere Schlüssel mit einigen der vorhandenen Algorithmen verwendet werden und zusätzliche Algorithmen implementiert werden.



| Name                                  | Zweck          | type           | Schlüsselgröße (Standard/min/max) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algorithmus für Cylink-Nachrichten Verschlüsselung   | Verschlüsselung   | Blockieren          | 40/40/40                   |
| Data Encryption Standard (des)        | Verschlüsselung   | Blockieren          | 56/56/56                   |
| Zwei wichtige Dreifache des                    | Verschlüsselung   | Blockieren          | 112/112/112                |
| Drei wichtige Dreifache des                  | Verschlüsselung   | Blockieren          | 168/168/168                |
| Diffie-Hellman Schlüsselaustausch Algorithmus | Schlüsselaustausch | Diffie-Hellman | 1024/512/4096              |
| Diffie-Hellman kurzlebigen Algorithmus    | Schlüsselaustausch | Diffie-Hellman | 1024/512/4096              |
| Digital Signature-Algorithmus (DSA)     | signatur-      | DSS            | 1024/512/1024              |
| Message Digest 5 (MD5)                | Hashing      | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Verschlüsselung   | Blockieren          | 128/128/128                |
| RSA Data Security 4 (RC4)             | Verschlüsselung   | Datenstrom         | 128/128/128                |
| Secure Hash-Algorithmus (SHA1)          | Hashing      | Any            | 160/160/160                |



 

## <a name="microsoft-enhanced-rsa-and-aes-cryptographic-provider"></a>Microsoft Enhanced RSA und AES-Kryptografieanbieter

Implementiert die folgenden Algorithmen zum Signieren, verschlüsseln und Hash von Inhalten.



| Name                                            | Zweck          | type   | Schlüsselgröße (Standard/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Verschlüsselung   | Blockieren  | 128/128/128                |
| Advanced Encryption Standard 192 (AES192)       | Verschlüsselung   | Blockieren  | 192/192/192                |
| Advanced Encryption Standard 256 (AES256)       | Verschlüsselung   | Blockieren  | 256/256/256                |
| Data Encryption Standard (des)                  | Verschlüsselung   | Blockieren  | 56/56/56                   |
| Zwei wichtige Dreifache des                              | Verschlüsselung   | Blockieren  | 112/112/112                |
| Drei wichtige Dreifache des                            | Verschlüsselung   | Blockieren  | 168/168/168                |
| Prüfsumme für Hash Nachrichten Authentifizierung (HMAC)   | Hashing      | Any    | 0/0/0                      |
| Prüfsumme für Nachrichten Authentifizierung (Mac)           | Hashing      | Any    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung   | Blockieren  | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Verschlüsselung   | Datenstrom | 128/128/128                |
| RSA-Schlüsselaustausch                                | Schlüsselaustausch | RSA    | 1024/384/16384             |
| RSA-Signatur                                   | signatur-      | RSA    | 1024/384/16384             |
| Secure Hash-Algorithmus (SHA1)                    | Hashing      | Any    | 160/160/160                |
| Secure Hash-Algorithmus (SHA256)                  | Hashing      | Any    | 256/256/256                |
| Secure Hash-Algorithmus (SHA384)                  | Hashing      | Any    | 384/384/384                |
| Secure Hash-Algorithmus (SHA512)                  | Hashing      | Any    | 512/512/512                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing      | Any    | 288/288/288                |



 

## <a name="microsoft-rsa-schannel-cryptographic-provider"></a>Kryptografieanbieter für Microsoft RSA SChannel

Unterstützt das Sicherheitspaket RSA Secure Channel (SChannel), das Secure Sockets Layer Authentifizierungsprotokolle (SSL) und Transport Layer Security (TLS) implementiert.



| Name                                            | Zweck                | type     | Schlüsselgröße (Standard/min/max) |
|-------------------------------------------------|--------------------|----------|----------------------------|
| Advanced Encryption Standard 128 (AES128)       | Verschlüsselung         | Blockieren    | 128/128/128                |
| Advanced Encryption Standard 256 (AES256)       | Verschlüsselung         | Blockieren    | 256/256/256                |
| Data Encryption Standard (des)                  | Verschlüsselung         | Blockieren    | 56/56/56                   |
| Zwei wichtige Dreifache des                              | Verschlüsselung         | Blockieren    | 112/112/112                |
| Drei wichtige Dreifache des                            | Verschlüsselung         | Blockieren    | 168/168/168                |
| Prüfsumme für Hash Nachrichten Authentifizierung (HMAC)   | Hashing            | Any      | 0/0/0                      |
| Prüfsumme für Nachrichten Authentifizierung (Mac)           | Hashing            | Any      | 0/0/0                      |
| Message Digest 5 (MD5)                          | Hashing            | Any      | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung         | Blockieren    | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Verschlüsselung         | Datenstrom   | 128/128/128                |
| RSA-Schlüsselaustausch                                | Schlüsselaustausch       | RSA      | 1024/384/16384             |
| SChannel-Verschlüsselungsschlüssel                         | Verschlüsselung         | Schannel | 0/0/-1                     |
| SChannel-Master Hash                            | Verschlüsselung/Hashvorgang | Schannel | 0/0/-1                     |
| SChannel-Mac-Taste                                | Verschlüsselung/Hashvorgang | Schannel | 0/0/-1                     |
| Secure Hash-Algorithmus (SHA1)                    | Hashing            | Any      | 160/160/160                |
| Secure Socket Layer 2-Master (SSL2 verwendet)             | Verschlüsselung         | Schannel | 40/40/192                  |
| Secure Socket Layer 3-Master (SSL3)             | Verschlüsselung         | Schannel | 384/384/384                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing            | Any      | 288/288/288                |
| Transport Layer Security (das TLS1 verwendet) Master          | Verschlüsselung         | Schannel | 384/384/384                |



 

## <a name="microsoft-strong-cryptographic-provider"></a>Microsoft starker Kryptografieanbieter

Implementiert die folgenden Algorithmen.



| Name                                            | Zweck          | type   | Schlüsselgröße (Standard/min/max) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Data Encryption Standard (des)                  | Verschlüsselung   | Blockieren  | 56/56/56                   |
| Zwei wichtige Dreifache des                              | Verschlüsselung   | Blockieren  | 112/112/112                |
| Drei wichtige Dreifache des                            | Verschlüsselung   | Blockieren  | 168/168/168                |
| Prüfsumme für Hash Nachrichten Authentifizierung (HMAC)   | Hashing      | Any    | 0/0/0                      |
| Prüfsumme für Nachrichten Authentifizierung (Mac)           | Hashing      | Any    | 0/0/0                      |
| Message Digest 2 (MD2)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 4 (MD4)                          | Hashing      | Any    | 128/128/128                |
| Message Digest 5 (MD5)                          | Hashing      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Verschlüsselung   | Blockieren  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Verschlüsselung   | Datenstrom | 128/40/128                 |
| RSA-Schlüsselaustausch                                | Schlüsselaustausch | RSA    | 1024/384/16384             |
| RSA-Signatur                                   | signatur-      | RSA    | 1024/384/16384             |
| Secure Hash-Algorithmus (SHA1)                    | Hashing      | Any    | 160/160/160                |
| Secure Socket Layer 3 SHA und MD5 (SSL3 SHAMD5) | Hashing      | Any    | 288/288/288                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Kryptografieanbietern](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
