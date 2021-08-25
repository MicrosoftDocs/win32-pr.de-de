---
description: 'Die sichere Kommunikation über unsichere Netzwerke umfasst im Allgemeinen drei wichtige Bereiche: Datenschutz, Authentifizierung und Integrität.'
ms.assetid: bfffe87d-8392-4b4a-8bbc-01b9c13fba47
title: Kryptografiekonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1909cf999bd5eb2f91bd5c7e0243b13969e692792c4ff32804e7c9a7d2940b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876155"
---
# <a name="cryptography-concepts"></a>Kryptografiekonzepte

Die sichere Kommunikation über unsichere Netzwerke umfasst im Allgemeinen drei wichtige Bereiche: [Datenschutz,](#privacy) [Authentifizierung](#authentication)und [Integrität.](#integrity) Die Microsoft-Kryptografie-API [*(CryptoAPI)*](../secgloss/c-gly.md)ist eine Reihe von Funktionen, Schnittstellen und Tools, mit denen Anwendungen das Vertrauen in die Sicherheit in diesen Bereichen verbessern können.

CryptoAPI bietet nicht nur Funktionen für [](../secgloss/c-gly.md) Datenschutz, Authentifizierung und Integrität, sondern auch Für:

-   Codieren von Nachrichten in asn.1-Formular [*(Abstract Syntax Notation One).*](../secgloss/a-gly.md)
-   Decodieren von ASN.1-Nachrichten.
-   Verwalten von [*Sammlungen*](../secgloss/c-gly.md) von Zertifikaten in [*Zertifikatspeichern.*](../secgloss/c-gly.md)
-   Arbeiten mit [*Zertifikatvertrauenslisten*](../secgloss/c-gly.md) und Zertifikatketten zur Überprüfung der Gültigkeit von Zertifikaten.

## <a name="privacy"></a>Datenschutz

Um Datenschutz zu gewährleisten, müssen Benutzer verhindern, dass jemand außer dem vorgesehenen Empfänger eine Nachricht liest. Um die Wahrscheinlichkeit des Datenschutzes zu verbessern, muss in der Regel eine Form der Kryptografie verwendet [*werden.*](../secgloss/c-gly.md) Kryptografische Techniken werden verwendet, um Nachrichten zu verschlüsseln (zu verschlüsseln), bevor die Nachrichten gespeichert oder übertragen werden.

Die Datenverschlüsselung transformiert [*Klartext*](../secgloss/p-gly.md) in [*Chiffretext.*](../secgloss/c-gly.md) Die zu verschlüsselnden Daten können [*ASCII-Text,*](../secgloss/a-gly.md) eine Datenbankdatei oder andere Daten sein. In dieser Dokumentation wird der Begriff [*Nachricht*](../secgloss/m-gly.md) verwendet, um auf alle Daten zu verweisen, Klartext bezieht sich auf Daten, die nicht verschlüsselt wurden, und *Ciphertext* bezieht sich auf Daten, die verschlüsselt wurden. Ein gutes Datenverschlüsselungssystem erschwert es, verschlüsselte Daten ohne geheimen Schlüssel wieder in Klartext zu transformieren.

Verschlüsselte Daten können auf nicht sicheren Medien gespeichert oder über ein nicht sicheres Netzwerk übertragen werden. Später können die Daten in ihrer ursprünglichen Form entschlüsselt werden. Dieser Prozess ist in der folgenden Abbildung dargestellt.

![Schutz des Datenschutzes während der verschlüsselungs- und entschlüsselung](images/capi01.png)

Wenn Daten verschlüsselt werden, werden die Nachricht und ein [*Verschlüsselungsschlüssel*](../secgloss/e-gly.md) an den Verschlüsselungsalgorithmus übergeben. Zum Entschlüsseln der Daten werden der Verschlüsselungstext und ein [*Entschlüsselungsschlüssel*](../secgloss/d-gly.md) an den Entschlüsselungsalgorithmus übergeben. Die Verschlüsselung und Entschlüsselung kann mithilfe eines einzelnen Schlüssels in einem Prozess erfolgen, der als symmetrische Verschlüsselung bezeichnet wird.

Schlüssel, die zum Entschlüsseln einer Nachricht verwendet werden, müssen so geheim und sicher wie möglich gehalten und mithilfe von Techniken zur Verbesserung der Sicherheit an andere Benutzer übertragen werden. Dies wird unter [Datenverschlüsselung und -entschlüsselung](data-encryption-and-decryption.md)näher erläutert. Die größte Herausforderung besteht darin, den Zugriff auf den Entschlüsselungsschlüssel ordnungsgemäß einzuschränken, da jeder, der ihn besitzt, alle Nachrichten entschlüsseln kann, die mit dem entsprechenden Verschlüsselungsschlüssel verschlüsselt wurden.

Um die genannten Ziele des Datenschutzes zu erreichen, können Entwickler [*CryptoAPI*](../secgloss/c-gly.md) verwenden, um Daten flexibel zu verschlüsseln und digital zu signieren, während sie gleichzeitig dabei helfen, den Schutz vertraulicher privater Schlüsseldaten des Benutzers bereitzustellen.

[*CryptoAPI*](../secgloss/c-gly.md) bietet die folgenden Funktionalitätsbereiche, um die Aufgaben der Verschlüsselung/Entschlüsselung, der Nachrichtensignatur und der Schlüsselspeicherung auszuführen:

-   [Grundlegende Kryptografiefunktionen](cryptography-functions.md)
-   [Vereinfachte Nachrichtenfunktionen](cryptography-functions.md)
-   [Low-Level-Nachrichtenfunktionen](cryptography-functions.md)

## <a name="authentication"></a>Authentifizierung

Die sichere Kommunikation erfordert, dass die Kommunizierenden die Identität der Personen kennen, mit denen sie kommunizieren. Bei der Authentifizierung wird die Identität einer Person oder Entität überprüft.

Im täglichen Leben wird beispielsweise die physische Dokumentation, die häufig als Anmeldeinformationen bezeichnet wird, verwendet, um die Identität einer Person zu überprüfen. Wenn eine Überprüfung einkassiert wird, kann die Person, die die Überprüfung abkassiert, um einen Fahrerlizenz bitten. Die Fahrerlizenz ist ein physisches Dokument, das das Vertrauen des Händlers in die Identität der Person erhöht, die die Überprüfung einlöst. In diesem Fall vertraut die Person, die die Überprüfung einlöst, darauf, dass der Status, der die Lizenz ausgibt, die Identität des Lizenzinhabers ordnungsgemäß überprüft hat.

Passports stellen ein weiteres Beispiel bereit. Ein Offizieller sieht sich einen Pass an und akzeptiert ihn als Nachweis dafür, dass eine Person ist, die er sagt, er sei. Der Offizielle vertraut darauf, dass die Regierung vor der Ausstellung des Passport einen angemessenen Auftrag zur Identifizierung des Passport-Besitzers erledigt hat. In beiden Beispielen ist eine Vertrauensebene im Aussteller des physischen Dokuments vorhanden.

Bei der Authentifizierung muss auch sichergestellt werden, dass es sich bei den empfangenen Daten um die gesendeten Daten handelt. Wenn Partei A eine Nachricht an Partei B sendet, muss Partei B nachweisen können, dass es sich bei der empfangenen Nachricht um die Von Partei A gesendete Nachricht und nicht um eine Nachricht handelt, die durch diese Nachricht ersetzt wurde. Um diese Form der Authentifizierung bereitzustellen, stellt [*CryptoAPI*](../secgloss/c-gly.md) Funktionen zum Signieren von Daten und Überprüfen von Signaturen mithilfe von Paaren aus öffentlichem und privatem Schlüssel bereit.

Da die Kommunikation über ein Computernetzwerk ohne physischen Kontakt zwischen den Kommunikationsatoren erfolgt, hängt die Überprüfung der Identität häufig von Anmeldeinformationen ab, die über ein Netzwerk gesendet und empfangen werden können. Solche Anmeldeinformationen müssen von einem vertrauenswürdigen Aussteller von Anmeldeinformationen ausgestellt werden. Digitale Zertifikate, die häufig als Zertifikate bezeichnet werden, sind nur solche Anmeldeinformationen. Sie sind eine Möglichkeit, die Identität zu überprüfen und eine Authentifizierung in einem Computernetzwerk zu erreichen.

Bei einem digitalen Zertifikat handelt es sich um Anmeldeinformationen, die von einer vertrauenswürdigen Organisation oder Entität ausgestellt werden, die als Zertifizierungsstelle bezeichnet wird. Diese Anmeldeinformationen enthalten einen öffentlichen Schlüssel (siehe Paare aus öffentlichen und [privaten Schlüsseln)](public-private-key-pairs.md)und Daten, die den Antragsteller des Zertifikats identifizieren. Ein Zertifikat wird von einer Zertifizierungsstelle erst ausgestellt, nachdem die Zertifizierungsstelle die Identität des Zertifikatsubjekts überprüft und bestätigt hat, dass der im Zertifikat enthaltene öffentliche Schlüssel zu diesem Antragsteller gehört.

Die Kommunikation zwischen einer Zertifizierungsstelle und einem Anforderer des Zertifikats kann durch den Anfordernden erreicht werden, der die erforderlichen Informationen, die möglicherweise auf einem Diskettendatenträger gespeichert sind, physisch an die Zertifizierungsstelle übermittelt. Die Kommunikation erfolgt jedoch in der Regel mit einer signierten Nachricht, die über ein Netzwerk gesendet wird. Die Zertifizierungsstelle verwendet häufig eine vertrauenswürdige Anwendung, die als Zertifikatserver bezeichnet wird, um Zertifikate ausstellen zu können.

[*CryptoAPI*](../secgloss/c-gly.md) unterstützt die Authentifizierung durch die Verwendung digitaler Zertifikate, mit Zertifikatcodierungs-/Decodierungsfunktionen und [*Zertifikatspeicherfunktionen.*](../secgloss/c-gly.md)

Weitere Informationen zur Identitätsüberprüfung und Authentifizierung durch die Verwendung von Zertifikaten finden Sie unter [Digitale Zertifikate.](digital-certificates.md)

## <a name="integrity"></a>Integrität

Alle Daten, die über ein nicht sicheres Medium gesendet werden, können zufällig oder absichtlich geändert werden. In der Praxis werden Versiegelungen verwendet, um Integrität bereitzustellen und nachzuweisen. So kann beispielsweise eine Packung mit manipulationssicherer Verpackung mit einem unbrokenen Versiegelungszeichen enthalten sein, um nachzuweisen, dass nach dem Verlassen des Pakets vom Hersteller nichts in das Paket aufgenommen wurde.

Auf die gleiche Weise muss ein Empfänger von Daten in der Lage sein, die Identität des Absenders der Daten zu überprüfen und sicherzustellen, dass es sich bei den empfangenen Daten genau um die gesendeten Daten handelt. das heißt, dass sie nicht manipuliert wurde. Die Integrität [*der*](../secgloss/i-gly.md) empfangenen Daten wird häufig dadurch erreicht, dass nicht nur die ursprünglichen Daten, sondern auch eine Überprüfungsnachricht, die als [*Hash*](../secgloss/h-gly.md)bezeichnet wird, über diese Daten gesendet wird. Sowohl die Daten als auch die Überprüfungsnachricht können mit einer [*digitalen Signatur*](../secgloss/d-gly.md) gesendet werden, die den Ursprung beider Bestätigt.

Integrität wird in CryptoAPI mithilfe von [digitalen Signaturen](digital-signatures.md) und [Datenhashes](data-hashes.md)bereitgestellt.

[*CryptoAPI*](../secgloss/c-gly.md) unterstützt Integrität durch die Verwendung von Nachrichtenfunktionen zum Signieren von Daten und zum Überprüfen digitaler Signaturen.

 

 
