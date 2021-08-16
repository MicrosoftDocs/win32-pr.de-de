---
description: Die CNG-API stellt eine Reihe von Funktionen bereit, die grundlegende kryptografische Vorgänge wie das Erstellen von Hashes oder das Verschlüsseln und Entschlüsseln von Daten ausführen. Weitere Informationen zu diesen Funktionen finden Sie unter Kryptografische primitive CNG-Funktionen.
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: Kryptografische Grundelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d65b37193ccf2f37a06dea0a994c40ea472c6041b451a1d2c31dd19b259b843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907803"
---
# <a name="cryptographic-primitives"></a>Kryptografische Grundelemente

Die CNG-API stellt eine Reihe von Funktionen bereit, die grundlegende kryptografische Vorgänge wie das Erstellen von Hashes oder das Verschlüsseln und Entschlüsseln von Daten ausführen. Weitere Informationen zu diesen Funktionen finden Sie unter [Kryptografische primitive CNG-Funktionen.](cng-cryptographic-primitive-functions.md)

CNG implementiert zahlreiche kryptografische Algorithmen. Jeder Algorithmus oder jede Algorithmusklasse macht seine eigene primitive API verfügbar. Mehrere Implementierungen eines bestimmten Algorithmus können gleichzeitig installiert werden. allerdings wird immer nur eine Implementierung als Standard verwendet.

Jede Algorithmusklasse in CNG wird durch einen primitiven Router dargestellt. Anwendungen, die die primitiven CNG-Funktionen verwenden, werden mit der Binärdatei des Routers Bcrypt.dll im Benutzermodus oder Ksecdd.sys Kernelmodus vor dem Aufrufen der Funktionen verbunden. Verschiedene Routerroutinen verwalten alle Algorithmusprimitiven. Diese Router verfolgen jede auf dem System installierte Algorithmusimplementierung nach und routen jeden Funktionsaufruf an das entsprechende primitive Anbietermodul.

CNG bietet Primitive für die folgenden Klassen von Algorithmen.



| Algorithm-Klasse                                                                                                                                                  | BESCHREIBUNG                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Zufallszahlengenerator<br/> | Pluggable Random Number Generation (RNG).<br/>                                                         |
| <span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hashing<br/>                                                                 | Algorithmen, die für hashing verwendet werden, z. B. SHA1 und SHA2.<br/>                                               |
| <span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Symmetrische Verschlüsselung<br/>             | Algorithmen, die für die symmetrische Verschlüsselung verwendet werden, z. B. AES, 3DES und RC4.<br/>                             |
| <span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Asymmetrische Verschlüsselung<br/>         | Asymmetrische Algorithmen (öffentlicher Schlüssel), die Verschlüsselung unterstützen, z. B. RSA.<br/>                          |
| <span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signatur<br/>                                                         | Signaturalgorithmen wie DSA und ECDSA. Diese Klasse kann auch mit RSA verwendet werden.<br/>                 |
| <span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Geheimer Vertrag<br/>                             | Geheime Vereinbarungsalgorithmen wie Diffie-Hellman (DH) und Elliptic Curve Diffie-Hellman (ECDH).<br/> |



 

Die folgende Abbildung zeigt den Entwurf und die Funktion der kryptografischen CNG-Primitive.

![Entwurf und Funktion von cng-Kryptografieprimitiven](images/ssdk-cng1c.png)

Die Headerdatei Bcrypt.h definiert die **MS \_ PRIMITIVE \_ PROVIDER-Konstante** als "Microsoft Primitive Provider". Um den primitiven Microsoft-Anbieter zu verwenden, übergeben Sie diesen Wert [**an BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).

 

 




