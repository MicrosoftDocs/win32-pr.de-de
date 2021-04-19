---
description: 'CNG verfügt über die folgenden Funktionen:'
ms.assetid: 400a2b6e-6bbe-4ba4-abde-a2f625007517
title: CNG-Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df40606a255adc90bd36540571979c1c34579611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343036"
---
# <a name="cng-features"></a>CNG-Features

CNG verfügt über die folgenden Funktionen:

-   [Kryptografische Agilität](#cryptographic-agility)
-   [Zertifizierung und Konformität](#certification-and-compliance)
-   [Suite B-Unterstützung](#suite-b-support)
-   [Legacy Unterstützung](#legacy-support)
-   [Kernel Modus-Unterstützung](#kernel-mode-support)
-   [Überwachung](#auditing)
-   [Austauschbare Zufallszahlengeneratoren](#replaceable-random-number-generators)
-   [Threadsicherheit](#thread-safety)
-   [Betriebsmodus](#mode-of-operation)

## <a name="cryptographic-agility"></a>Kryptografische Agilität

Eines der wichtigsten Wertbeiträge von CNG ist kryptografische Agilität, auch als kryptografieagnostizismus bezeichnet. Die Implementierung von Protokollen wie [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) (SSL) oder [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) (TLS), CMS (S/MIME), IPSec, Kerberos usw. in CNG war jedoch erforderlich, um diese Möglichkeit zu Verb legen. Auf der CNG-Ebene musste die Ersetzung und Erkennbarkeit für alle Algorithmustypen (symmetrische, asymmetrische, Hash Funktionen), Zufallszahlengenerierung und andere Hilfsfunktionen bereitgestellt werden. Die Änderungen auf Protokollebene sind signifikanter, weil die Protokoll-APIs in vielen Fällen zum Hinzufügen der Algorithmusauswahl und anderer Optionen für die Flexibilität benötigt werden, die zuvor noch nicht vorhanden waren.

CNG ist zuerst in Windows Vista verfügbar und wird so positioniert, dass im gesamten Microsoft-Software Stapel vorhandene Verwendungen von [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) ersetzt werden. Entwickler von Drittanbietern werden viele neue Features in CNG finden, einschließlich:

-   Ein neues Kryptografiekonfigurationssystem, das eine bessere kryptografische Agilität unterstützt.
-   Präzisere Abstraktion für den Schlüsselspeicher (und die Trennung des Speichers von algorithmusvorgängen).
-   Prozess Isolation für Vorgänge mit langfristigen Schlüsseln.
-   Ersatz Bare Zufallszahlengeneratoren.
-   Erleichterung von Einschränkungen beim Exportieren von Signaturen.
-   Thread Sicherheit im Stapel.
-   Kernelmoduskryptografieapi.

Außerdem bietet CNG Unterstützung für alle erforderlichen Suite B Algorithmen, einschließlich der [*Kryptografie für elliptische Kurven*](/windows/desktop/SecGloss/e-gly) (ECC). Vorhandene CryptoAPI-Anwendungen funktionieren weiterhin, wenn CNG verfügbar wird.

## <a name="certification-and-compliance"></a>Zertifizierung und Konformität

CNG wird gemäß Federal Information Processing Standards (FIPS) 140-2 überprüft und ist Bestandteil des Evaluierungs Ziels für die Windows Common Criteria-Zertifizierung. CNG wurde so konzipiert, dass es als Komponente in einem überprüften System mit der Ebene 2 auf der Ebene 2 verwendet werden kann.

CNG erfüllt gängige kriterienanforderungen, indem lange gelebte Schlüssel in einem sicheren Prozess gespeichert und verwendet werden.

## <a name="suite-b-support"></a>Suite B-Unterstützung

Ein wichtiges Feature von CNG ist die Unterstützung der Suite B Algorithmen. Im Februar von 2005 hat die National Security Agency (NSA) des USA einen koordinierten Satz symmetrischer Verschlüsselung, eine asymmetrische geheime Vereinbarung (auch als Schlüsselaustausch bezeichnet), digitale Signaturen und Hash Funktionen für die zukünftige Verwendung *Suite B* der US-Regierung angekündigt. Die NSA hat angekündigt, dass zertifizierte Suite B Implementierungen zum Schutz von Informationen verwendet werden können, die als geheime Schlüssel, geheime Schlüssel und private Informationen festgelegt sind, die in der Vergangenheit als vertraulich, aber-nicht klassifiziert beschrieben wurden. Aus diesem Grund ist die Suite B Unterstützung für Anwendungssoftware Hersteller und Systemintegratoren sowie für Microsoft sehr wichtig.

Alle Suite B Algorithmen sind öffentlich bekannt. Sie wurden außerhalb des Umfangs des Regierungs Geheimnisses entwickelt, das in der Vergangenheit mit der Entwicklung kryptografischer Algorithmen verbunden war. Im gleichen Zeitrahmen haben auch in einigen europäischen Ländern und Regionen dieselben Suite B Anforderungen zum Schutz Ihrer Informationen vorgeschlagen.

Suite B Kryptografie empfiehlt die Verwendung von ECDH (Elliptic Curve Diffie-Hellman) in vielen vorhandenen Protokollen, wie z. b. dem Internetschlüsselaustausch (IKE, hauptsächlich in IPSec), [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) (TLS) und Secure MIME (S/MIME).

CNG bietet Unterstützung für Suite B, die sich auf alle erforderlichen Algorithmen erstreckt: AES (alle Schlüsselgrößen), SHA-2-Familie (SHA-256, SHA-384 und SHA-512) von Hash Algorithmen, ECDH und Elliptic Curve DSA (ECDSA) über die NIST-Standard-Prim Kurven p-256, p-384 und p-521. Binäre Kurven, Koblitz-Kurven, benutzerdefinierte primkurven und elliptische Kurven Menezes-qu-Vanstone (ecmqv) werden von den in Windows Vista enthaltenen Microsoft-Algorithmusanbietern nicht unterstützt.

## <a name="legacy-support"></a>Legacy Unterstützung

CNG bietet Unterstützung für den aktuellen Satz von Algorithmen in [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) 1,0. Jeder Algorithmus, der derzeit in *CryptoAPI* 1,0 unterstützt wird, wird in CNG weiterhin unterstützt.

## <a name="kernel-mode-support"></a>Kernel Modus-Unterstützung

CNG unterstützt Kryptografie im Kernel Modus. Die gleichen APIs werden sowohl im Kernel-als auch im Benutzermodus verwendet, um die Kryptografiefeatures vollständig zu unterstützen. Sowohl SSL/TLS als auch IPSec werden neben Start Prozessen, die CNG verwenden, im Kernel Modus ausgeführt. Nicht alle CNG-Funktionen können aus dem Kernel Modus aufgerufen werden. Das Referenz Thema für die Funktionen, die nicht aus dem Kernel Modus aufgerufen werden können, gibt explizit an, dass die Funktion nicht aus dem Kernel Modus aufgerufen werden kann. Andernfalls können alle CNG-Funktionen aus dem Kernel Modus aufgerufen werden, wenn der Aufrufer auf der **passiven \_ Ebene** " [*unql*](/windows/desktop/SecGloss/i-gly)" ausgeführt wird. Außerdem kann es sein, dass einige CNG-Funktionen für den kernelmodusvorgang auf der **\_ dispatchebene "unql**", abhängig von den Funktionen des Anbieters

Bei der Microsoft Kernel Security Support Provider Interface (Ksecdd.sys) handelt es sich um ein allgemeines, softwarebasiertes kryptografiemodul, das sich auf der kernelmodusebene von Windows befindet. Ksecdd.sys wird als Export Treiber für den Kernel Modus ausgeführt und stellt Kryptografiedienste über die dokumentierten Schnittstellen für Kernel Komponenten bereit. Der einzige integrierte Microsoft-Anbieter Algorithmus, der nicht von Ksecdd.sys unterstützt wird, ist DSA.

**Windows Server 2008 und Windows Vista:** CNG unterstützt keine austauschbaren Algorithmen und Anbieter im Kernel Modus. Die einzigen unterstützten Kryptografiealgorithmen, die im Kernel Modus verfügbar sind, sind die von Microsoft bereitgestellten Implementierungen über die CNG-APIs des Kernelmodus

## <a name="auditing"></a>Überwachung

Um einige der allgemeinen kriterienanforderungen zu erfüllen, zusätzlich zur Bereitstellung umfassender Sicherheit, werden viele Aktionen in der CNG-Schicht im Microsoft-Software Schlüsselspeicher-Anbieter (KSP) überwacht. Die Microsoft-KSP befolgt die folgenden Richtlinien, um Überwachungsdaten Sätze im Sicherheitsprotokoll zu erstellen:

-   Fehler bei der Generierung von Schlüsseln und Schlüsselpaaren, einschließlich Selbsttest Fehlern, müssen überwacht werden.
-   Schlüssel Import und-Export müssen überwacht werden.
-   Fehler bei der Schlüssel Zerstörung müssen überwacht werden.
-   Persistente Schlüssel müssen überwacht werden, wenn Sie in Dateien geschrieben und aus diesen gelesen werden.
-   Fehler bei der paar weisen Konsistenzprüfung müssen überwacht werden.
-   Fehler bei der Überprüfung des geheimen Schlüssels (falls vorhanden) müssen überprüft werden, z. b. bei Paritäts Überprüfungen auf 3DES-Schlüsseln
-   Fehler bei Verschlüsselung, Entschlüsselung, Hashwert, Signatur, Überprüfung, Schlüsselaustausch und Zufallszahlengenerierung müssen überwacht werden.
-   Kryptografische Self-Tests müssen überwacht werden.

Im Allgemeinen handelt es sich bei einem Schlüssel, der keinen Namen hat, um einen kurzlebigen Schlüssel. Ein kurzlebiger Schlüssel wird nicht beibehalten, und der Microsoft KSP generiert keine Überwachungsdaten Sätze für kurzlebige Schlüssel. Der Microsoft-KSP generiert nur im LSA-Prozess Überwachungsdaten Sätze im Benutzermodus. Von der kernelmoduscng wird kein Überwachungsdaten Satz generiert. Administratoren müssen die Überwachungsrichtlinie so konfigurieren, dass alle KSP-Überwachungs Protokolle aus dem Sicherheitsprotokoll abgerufen werden. Ein Administrator muss die folgende Befehlszeile ausführen, um zusätzliche Überwachungen zu konfigurieren, die von kSPS generiert werden:

**Auditpol/Set/SubCategory: "Sonstige Systemereignisse"/Success: enable/Failure: enable**

## <a name="replaceable-random-number-generators"></a>Austauschbare Zufallszahlengeneratoren

Eine weitere Verbesserung, die CNG bietet, ist die Möglichkeit, den standardmäßigen Zufallszahlengenerator (RNG) zu ersetzen. In CryptoAPI ist es möglich, eine Alternative RNG als Teil eines Kryptografiedienstanbieters (kryptografischen Service Provider, CSP) bereitzustellen, aber es ist nicht möglich, die Microsoft Base-CSPs zur Verwendung eines anderen RNG umzuleiten. CNG ermöglicht das explizite Angeben eines bestimmten RNG, der in bestimmten Aufrufen verwendet werden soll.

## <a name="thread-safety"></a>Threadsicherheit

Alle Funktionen, die den gleichen Arbeitsspeicher Bereich gleichzeitig ändern (kritische Abschnitte), wenn Sie von separaten Threads aufgerufen werden, sind nicht Thread sicher.

## <a name="mode-of-operation"></a>Betriebsmodus

CNG unterstützt fünf Betriebsmodi, die mit symmetrischen Blockchiffren durch die Verschlüsselungs-APIs verwendet werden können. Diese Modi und deren unter Stütz barkeit sind in der folgenden Tabelle aufgeführt. Der Vorgangs Modus kann durch Festlegen der [**bcrypt- \_ Verkettungs \_ Modus**](cng-property-identifiers.md) -Eigenschaft für den Algorithmusanbieter mithilfe der [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) -Funktion geändert werden.



| Betriebsmodus           | Wert des bcrypt- \_ Verkettungs \_ Modus | Algorithmen              | Standard  |
|-----------------------------|------------------------------|-------------------------|-----------|
| ECB (elektronisches Codebook)   | **bcrypt- \_ Ketten \_ Modus- \_ ECB** | Symmetrische Blockchiffren | SP800-38A |
| CBC (Chiffre Block Verkettung) | **bcrypt- \_ Ketten \_ Modus ( \_ CBC)** | Symmetrische Blockchiffren | SP800-38A |
| CFB (Chiffre Feedback)       | **bcrypt- \_ Ketten \_ Modus ( \_ CFB)** | Symmetrische Blockchiffren | SP800-38A |
| CCM (Counter mit CBC)      | **bcrypt- \_ Ketten \_ Modus- \_ ccm** | AES                     | SP800-38c |
| GCM (Galois/Counter-Modus)   | **bcrypt- \_ Ketten \_ Modus- \_ GCM** | AES                     | SP800-38d |



 

> [!Note]  
> In Windows Vista werden nur die Betriebsmodi "ECB", "CBC" und "CFB" definiert. GCM und CCM erfordern Windows Vista mit Service Pack 1 (SP1) oder Windows Server 2008.

 

 

 
