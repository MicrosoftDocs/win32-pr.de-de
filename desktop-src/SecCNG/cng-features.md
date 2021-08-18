---
description: CNG verfügt über die folgenden Features.
ms.assetid: 400a2b6e-6bbe-4ba4-abde-a2f625007517
title: CNG-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434c72075c04b0c280c85831ca78d930c0fcc047de19609d11764bcf63ddad56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908447"
---
# <a name="cng-features"></a>CNG-Funktionen

CNG verfügt über die folgenden Features.

-   [Kryptografische Agilität](#cryptographic-agility)
-   [Zertifizierung und Compliance](#certification-and-compliance)
-   [Suite B-Unterstützung](#suite-b-support)
-   [Legacyunterstützung](#legacy-support)
-   [Kernelmodusunterstützung](#kernel-mode-support)
-   [Überwachung](#auditing)
-   [Ersetzbare Zufallszahlengeneratoren](#replaceable-random-number-generators)
-   [Threadsicherheit](#thread-safety)
-   [Betriebsmodus](#mode-of-operation)

## <a name="cryptographic-agility"></a>Kryptografische Agilität

Eines der wichtigsten Nutzenversprechen von CNG ist kryptografische Agilität, die manchmal auch als kryptografische Agnostik bezeichnet wird. Die Konvertierung von Protokollen wie [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) (SSL) oder Transport [*Layer Security*](/windows/desktop/SecGloss/t-gly) (TLS), CMS (S/MIME), IPsec, Kerberos und so weiter in CNG war jedoch erforderlich, um diese Fähigkeit wertvoll zu machen. Auf CNG-Ebene war es erforderlich, die Ersetzung und Aufschlüsselbarkeit für alle Algorithmustypen (symmetrische, asymmetrische, Hashfunktionen), Zufallszahlengenerierung und andere Hilfsfunktionen zu ermöglichen. Die Änderungen auf Protokollebene sind wichtiger, da in vielen Fällen die Protokoll-APIs erforderlich sind, um die Algorithmusauswahl und andere Flexibilitätsoptionen hinzuzufügen, die zuvor nicht vorhanden waren.

CNG ist erstmals in Windows Vista verfügbar und ist positioniert, um vorhandene Verwendungen von [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) im gesamten Microsoft-Softwarestapel zu ersetzen. Entwickler von Drittanbietern werden viele neue Features in CNG finden, darunter:

-   Ein neues Kryptografiekonfigurationssystem, das eine bessere kryptografische Agilität unterstützt.
-   Eine feiner abstrahierte Abstraktion für die Schlüsselspeicherung (und Trennung des Speichers von Algorithmusvorgängen).
-   Prozessisolation für Vorgänge mit langfristigen Schlüsseln.
-   Ersetzbare Zufallszahlengeneratoren.
-   Abgesehen von Einschränkungen bei der Exportsignatur.
-   Threadsicherheit im gesamten Stapel.
-   Kryptografische API im Kernelmodus.

Darüber hinaus bietet CNG Unterstützung für alle erforderlichen Suite B, einschließlich ECC [*(Elliptic Curve Cryptography).*](/windows/desktop/SecGloss/e-gly) Vorhandene CryptoAPI-Anwendungen funktionieren weiterhin, sobald CNG verfügbar wird.

## <a name="certification-and-compliance"></a>Zertifizierung und Compliance

CNG wird anhand der Federal Information Processing Standards (FIPS) 140-2 überprüft und ist Teil des Evaluierungsziels für die Windows Common Criteria-Zertifizierung. CNG wurde entwickelt, um als Komponente in einem fips level 2-validierten System verwendet werden zu können.

CNG erfüllt die Common Criteria-Anforderungen, indem langlebige Schlüssel in einem sicheren Prozess gespeichert und verwendet werden.

## <a name="suite-b-support"></a>Suite B-Unterstützung

Ein wichtiges Feature von CNG ist die Unterstützung der Suite B Algorithmen. Im Februar 2005 hat die National Security Agency (NSA) der USA einen koordinierten Satz von symmetrischer Verschlüsselung, asymmetrischem Geheimvertrag (auch als Schlüsselaustausch bezeichnet), digitale Signatur und Hashfunktionen für die zukünftige Verwendung durch US-Regierungsbehörden namens *Suite B angekündigt.* Die NSA hat angekündigt, dass zertifizierte Suite B-Implementierungen für den Schutz von Informationen verwendet werden können und werden, die als Oberstes Geheimnis, Geheimnis und private Informationen bezeichnet wurden, die in der Vergangenheit als Vertraulich,aber nicht klassifiziert beschrieben wurden. Aus diesem Grund ist Suite B Unterstützung für Anwendungssoftwareanbieter und Systemintegratoren sowie für Microsoft sehr wichtig.

Alle Suite B algorithmen sind öffentlich bekannt. Sie wurden außerhalb des Bereichs der Geheimnisse der Regierung entwickelt, die in der Vergangenheit mit der Entwicklung kryptografischer Algorithmen in Zusammenhang steht. In diesem Zeitraum haben einige europäische Länder und Regionen auch die gleichen Suite B zum Schutz ihrer Informationen vorgeschlagen.

Suite B-Kryptografie empfiehlt die Verwendung von ELLIPTIC Curve Diffie-Hellman (ECDH) in vielen vorhandenen Protokollen, z. B. internet key Exchange (IKE, hauptsächlich in IPsec verwendet), [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) (TLS) und Secure MIME (S/MIME).

CNG bietet Unterstützung für Suite B, die sich auf alle erforderlichen Algorithmen erstreckt: AES (alle Schlüsselgrößen), die SHA-2-Familie (SHA-256, SHA-384 und SHA-512) von Hashalgorithmen, ECDH und Elliptic Curve DSA (ECDSA) gegenüber den NIST-Standardprimitkurven P-256, P-384 und P-521. Binäre Kurven, Kobppe-Kurven, benutzerdefinierte Primkurven und Elliptic Curve Menezes-Qu-Vanstone (ECMQV) werden von den Microsoft-Algorithmusanbietern, die in Windows Vista enthalten sind, nicht unterstützt.

## <a name="legacy-support"></a>Legacyunterstützung

CNG bietet Unterstützung für den aktuellen Satz von Algorithmen in [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) 1.0. Jeder Algorithmus, der derzeit in *CryptoAPI* 1.0 unterstützt wird, wird weiterhin in CNG unterstützt.

## <a name="kernel-mode-support"></a>Kernelmodusunterstützung

CNG unterstützt Kryptografie im Kernelmodus. Die gleichen APIs werden sowohl im Kernel- als auch im Benutzermodus verwendet, um die Kryptografiefeatures vollständig zu unterstützen. Sowohl SSL/TLS als auch IPsec arbeiten im Kernelmodus zusätzlich zu Startprozessen, die CNG verwenden. Nicht alle CNG-Funktionen können über den Kernelmodus aufgerufen werden. Das Referenzthema für die Funktionen, die nicht aus dem Kernelmodus aufgerufen werden können, gibt explizit an, dass die Funktion nicht aus dem Kernelmodus aufgerufen werden kann. Andernfalls können alle CNG-Funktionen aus dem Kernelmodus aufgerufen werden, wenn der Aufrufer auf **PASSIVER \_ EBENE** [*IRQL ausgeführt wird.*](/windows/desktop/SecGloss/i-gly) Darüber hinaus können einige CNG-Funktionen im Kernelmodus abhängig von den Funktionen des Anbieters auf **\_ DISPATCH-EBENE IRQL** aufrufbar sein.

Die Microsoft Kernel Security Support Provider-Schnittstelle (Ksecdd.sys) ist ein allgemeines, softwarebasiertes kryptografisches Modul, das sich auf Kernelmodusebene Windows. Ksecdd.sys wird als Kernelmodus-Exporttreiber ausgeführt und stellt kryptografische Dienste über ihre dokumentierten Schnittstellen für Kernelkomponenten bereit. DSA ist der einzige integrierte Microsoft-Anbieteralgorithmus, der von Ksecdd.sys nicht unterstützt wird.

**Windows Server 2008 und Windows Vista:** CNG unterstützt keine pluggable-Algorithmen und Anbieter im Kernelmodus. Die einzigen unterstützten kryptografischen Algorithmen, die im Kernelmodus verfügbar sind, sind die Implementierungen, die von Microsoft über die CNG-APIs im Kernelmodus bereitgestellt werden.

## <a name="auditing"></a>Überwachung

Um einige der Common Criteria-Anforderungen zu erfüllen und zusätzlich eine umfassende Sicherheit zu bieten, werden viele Aktionen, die auf der CNG-Ebene durchgeführt werden, im Microsoft-Softwareschlüsselspeicheranbieter (KSP) überwacht. Der Microsoft KSP befolgt die folgenden Richtlinien zum Erstellen von Überwachungsdatensätzen im Sicherheitsprotokoll:

-   Fehler bei der Schlüssel- und Schlüsselpaargenerierung, einschließlich Selbsttestfehlern, müssen überwacht werden.
-   Schlüsselimport und -export müssen überwacht werden.
-   Fehler bei der Schlüsselvernichtung müssen überwacht werden.
-   Persistente Schlüssel müssen überwacht werden, wenn sie in Dateien geschrieben und daraus gelesen werden.
-   Fehler bei der Paarkonsistenzprüfung müssen überwacht werden.
-   Fehler bei der Überprüfung geheimer Schlüssel (falls möglich) müssen überwacht werden, z. B. Paritätsprüfungen für 3DES-Schlüssel.
-   Fehler bei Verschlüsselung, Entschlüsselung, Hashing, Signatur, Überprüfung, Schlüsselaustausch und Zufallszahlengenerierung müssen überwacht werden.
-   Kryptografische Selbsttests müssen überwacht werden.

Wenn ein Schlüssel keinen Namen hat, handelt es sich im Allgemeinen um einen kurzlebigen Schlüssel. Ein kurzlebiger Schlüssel wird nicht beibehalten, und der Microsoft KSP generiert keine Überwachungsdatensätze für kurzlebigen Schlüssel. Der Microsoft KSP generiert Überwachungsdatensätze nur im Benutzermodus im LSA-Prozess. Vom Kernelmodus CNG wird kein Überwachungsdatensatz generiert. Administratoren müssen die Überwachungsrichtlinie konfigurieren, um alle KSP-Überwachungsprotokolle aus dem Sicherheitsprotokoll zu erhalten. Ein Administrator muss die folgende Befehlszeile ausführen, um zusätzliche Überwachungen zu konfigurieren, die von KSPs generiert werden:

**auditpol /set /subcategory:"other system events" /success:enable /failure:enable**

## <a name="replaceable-random-number-generators"></a>Ersetzbare Zufallszahlengeneratoren

Eine weitere Verbesserung, die CNG bietet, ist die Möglichkeit, den Standardgenerator für Zufallszahlen (Random Number Generator, RNG) zu ersetzen. In CryptoAPI ist es möglich, ein alternatives RNG als Teil eines Kryptografiedienstanbieters (Cryptographic Service Provider, CSP) zur Verfügung zu stellen, aber es ist nicht möglich, die Microsoft Base CSPs zur Verwendung eines anderen RNG umzuleiten. CNG ermöglicht es, explizit einen bestimmten RNG anzugeben, der in bestimmten Aufrufen verwendet werden soll.

## <a name="thread-safety"></a>Threadsicherheit

Alle Funktionen, die denselben Speicherbereich gleichzeitig ändern (kritische Abschnitte), wenn sie von separaten Threads aufgerufen werden, sind nicht threadsicher.

## <a name="mode-of-operation"></a>Betriebsmodus

CNG unterstützt fünf Betriebsmodi, die mit symmetrischen Blockchiffren über die Verschlüsselungs-APIs verwendet werden können. Diese Modi und ihre Unterstützungsfähigkeit sind in der folgenden Tabelle aufgeführt. Der Betriebsmodus kann durch Festlegen der [**BCRYPT \_ CHAINING \_ MODE-Eigenschaft**](cng-property-identifiers.md) für den Algorithmusanbieter mithilfe der [**BCryptSetProperty-Funktion geändert**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) werden.



| Betriebsmodus           | Wert des \_ BCRYPT-VERKETTUNGSMODUS \_ | Algorithmen              | Standard  |
|-----------------------------|------------------------------|-------------------------|-----------|
| ABER (Elektronisches Codebook)   | **BCRYPT \_ CHAIN \_ MODE \_ VERKETTET** | Symmetrische Blockchiffren | SP800-38A |
| CBC (Cipher Block Chaining) | **BCRYPT \_ CHAIN \_ MODE \_ CBC** | Symmetrische Blockchiffren | SP800-38A |
| CFB (Cipher Feedback)       | **BCRYPT \_ CHAIN \_ MODE \_ CFB** | Symmetrische Blockchiffren | SP800-38A |
| CCM (Counter mit CBC)      | **BCRYPT \_ CHAIN \_ MODE \_ CCM** | AES                     | SP800-38C |
| GCM (Galois-/Indikatormodus)   | **BCRYPT \_ CHAIN \_ MODE \_ GCM** | AES                     | SP800-38D |



 

> [!Note]  
> In Vista werden nur die Betriebsmodi FÜR DIE, CBC und CFB Windows definiert. GCM und CCM erfordern Windows Vista mit Service Pack 1 (SP1) oder Windows Server 2008.

 

 

 
