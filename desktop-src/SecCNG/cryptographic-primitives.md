---
description: Die CNG-API bietet eine Reihe von Funktionen, mit denen grundlegende kryptografische Vorgänge wie das Erstellen von Hashes oder das Verschlüsseln und Entschlüsseln von Daten durchgeführt werden. Weitere Informationen zu diesen Funktionen finden Sie unter CNG-kryptografieprimitive-Funktionen.
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: Kryptografische Grundelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0f390b36bc500bf80b5b2ef0065651cf99f5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524866"
---
# <a name="cryptographic-primitives"></a>Kryptografische Grundelemente

Die CNG-API bietet eine Reihe von Funktionen, mit denen grundlegende kryptografische Vorgänge wie das Erstellen von Hashes oder das Verschlüsseln und Entschlüsseln von Daten durchgeführt werden. Weitere Informationen zu diesen Funktionen finden Sie unter [CNG-kryptografieprimitive-Funktionen](cng-cryptographic-primitive-functions.md).

CNG implementiert zahlreiche Kryptografiealgorithmen. Jeder Algorithmus oder jede Klasse von Algorithmen macht seine eigene primitive API verfügbar. Mehrere Implementierungen eines bestimmten Algorithmus können gleichzeitig installiert werden. Allerdings ist jeweils nur eine Implementierung der Standardwert.

Jede Algorithmusklasse in CNG wird durch einen primitiven Router dargestellt. Anwendungen, die die primitiven CNG-Funktionen verwenden, verknüpfen die Binärdatei des Routers Bcrypt.dll im Benutzermodus oder Ksecdd.sys im Kernel Modus, bevor die Funktionen aufgerufen werden. Verschiedene routerroutinen verwalten alle algorithmusprimitiver. Diese Router verfolgen jede auf dem System installierte algorithmumplementierung nach und leiten jeden Funktions aufzurufen an das entsprechende primitive Anbieter Modul weiter.

CNG stellt primitive für die folgenden Klassen von Algorithmen bereit.



| Algorithmusklasse                                                                                                                                                  | BESCHREIBUNG                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Zufallszahlengenerator<br/> | Austauschbare Zufallszahlengenerierung (RNG).<br/>                                                         |
| <span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hash<br/>                                                                 | Für hashung verwendete Algorithmen, wie z. b. SHA1 und SHA2.<br/>                                               |
| <span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Symmetrische Verschlüsselung<br/>             | Algorithmen, die für die symmetrische Verschlüsselung verwendet werden, z. b. AES, 3DES und RC4.<br/>                             |
| <span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Asymmetrische Verschlüsselung<br/>         | Asymmetrische Algorithmen (Public Key), die die Verschlüsselung unterstützen, z. b. RSA.<br/>                          |
| <span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Unter<br/>                                                         | Signatur Algorithmen wie DSA und ECDsa. Diese Klasse kann auch mit RSA verwendet werden.<br/>                 |
| <span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Geheimer Vertrag<br/>                             | Geheime Vertrags Algorithmen, wie z. b. Diffie-Hellman (dh) und elliptische Kurven Diffie-Hellman (ECDH).<br/> |



 

Die folgende Abbildung zeigt den Entwurf und die Funktion der kryptografischen CNG-primitive.

![Entwurf und Funktion der kryptografischen CNG-primitive](images/ssdk-cng1c.png)

In der Header Datei bcrypt. h wird die **MS- \_ primitive \_ Anbieter** Konstante als "Microsoft primitiver Anbieter" definiert. Wenn Sie den primitiven Microsoft-Anbieter verwenden möchten, übergeben Sie diesen Wert an [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).

 

 




