---
description: 'Die sichere Kommunikation über nicht sichere Netzwerke umfasst in der Regel drei Hauptbereiche: Datenschutz, Authentifizierung und Integrität.'
ms.assetid: bfffe87d-8392-4b4a-8bbc-01b9c13fba47
title: Kryptografiekonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aad1528032c20c5492a98798f8a175ca331e462
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350406"
---
# <a name="cryptography-concepts"></a>Kryptografiekonzepte

Die sichere Kommunikation über nicht sichere Netzwerke umfasst in der Regel drei Hauptbereiche: [Datenschutz](#privacy), [Authentifizierung](#authentication)und [Integrität](#integrity). Bei der Microsoft Kryptografie API ([*CryptoAPI*](../secgloss/c-gly.md)) handelt es sich um eine Reihe von Funktionen, Schnittstellen und Tools, mit denen Anwendungen die Sicherheit der Sicherheit in diesen Bereichen verbessern können.

Zusätzlich zu den Funktionen für Datenschutz, Authentifizierung und Integrität bietet [*CryptoAPI*](../secgloss/c-gly.md) auch Folgendes:

-   Codieren von Nachrichten in ein Format der [*abstrakten Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1).
-   Decodieren von ASN. 1-Nachrichten.
-   Verwalten von Sammlungen von [*Zertifikaten*](../secgloss/c-gly.md) in [*Zertifikat speichern*](../secgloss/c-gly.md).
-   Arbeiten mit [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) und Zertifikats Ketten für die Überprüfung der Gültigkeit von Zertifikaten.

## <a name="privacy"></a>Datenschutz

Um den Datenschutz zu erreichen, muss der Benutzer verhindern, dass eine Nachricht durch den vorgesehenen Empfänger gelesen wird. Das verbessern der Datenschutz Wahrscheinlichkeit umfasst in der Regel die Verwendung einer [*kryptografieform*](../secgloss/c-gly.md). Kryptografietechniken werden verwendet, um Nachrichten zu verschlüsseln, bevor die Nachrichten gespeichert oder übertragen werden.

Die Datenverschlüsselung wandelt [*Klartext*](../secgloss/p-gly.md) in [*Chiffre Text*](../secgloss/c-gly.md)um. Die zu verschlüsselnden Daten können [*ASCII*](../secgloss/a-gly.md) -Text, eine Datenbankdatei oder beliebige andere Daten sein. In dieser Dokumentation wird der Begriff [*Nachricht*](../secgloss/m-gly.md) verwendet, um auf alle Daten zu verweisen. Klartext bezieht sich auf Daten, die nicht verschlüsselt wurden, und *Chiffre Text* bezieht sich auf verschlüsselte Daten. Ein gutes Daten Verschlüsselungssystem erschwert das Umwandeln verschlüsselter Daten in Klartext ohne einen geheimen Schlüssel.

Verschlüsselte Daten können auf nicht sicheren Medien gespeichert oder über ein nicht sicheres Netzwerk übertragen werden. Später können die Daten in ihrer ursprünglichen Form entschlüsselt werden. Dieser Vorgang wird in der folgenden Abbildung dargestellt.

![Unterstützung der Datenschutz in der Verschlüsselung und Entschlüsselung](images/capi01.png)

Wenn die Daten verschlüsselt werden, werden die Nachricht und ein [*Verschlüsselungs*](../secgloss/e-gly.md) Schlüssel an den Verschlüsselungsalgorithmus übermittelt. Zum Entschlüsseln der Daten werden der Chiffre Text und ein [*Entschlüsselungs*](../secgloss/d-gly.md) Schlüssel an den Entschlüsselungs Algorithmus übermittelt. Verschlüsselung und Entschlüsselung können mithilfe eines einzelnen Schlüssels in einem Prozess, der als symmetrische Verschlüsselung bezeichnet wird, durchgeführt werden.

Schlüssel, die verwendet werden, um eine Nachricht zu entschlüsseln, müssen so geheim und sicher wie möglich aufbewahrt werden und müssen mithilfe von Sicherheits fördernden Techniken an andere Benutzer übermittelt werden. Dies wird unter [Datenverschlüsselung und Entschlüsselung](data-encryption-and-decryption.md)erläutert. Die Hauptaufgabe besteht darin, den Zugriff auf den Entschlüsselungsschlüssel ordnungsgemäß einzuschränken, da jeder, der ihn besitzt, alle Nachrichten entschlüsseln kann, die mit dem entsprechenden Verschlüsselungsschlüssel verschlüsselt wurden.

Um den genannten Zielen des Datenschutzes gerecht zu werden, können Entwickler die [*kryptoapi*](../secgloss/c-gly.md) verwenden, um Daten flexibel zu verschlüsseln und Digital zu signieren, während gleichzeitig der Schutz der sensiblen Daten des privaten Schlüssels des Benutzers gewährleistet ist.

[*CryptoAPI*](../secgloss/c-gly.md) bietet die folgenden Funktionsbereiche, um die Aufgaben der Verschlüsselung/Entschlüsselung, der Nachrichten Signierung und des Schlüssel Speichers auszuführen:

-   [Grundlegende Kryptografiefunktionen](cryptography-functions.md)
-   [Vereinfachte Nachrichten Funktionen](cryptography-functions.md)
-   [Nachrichten Funktionen auf niedriger Ebene](cryptography-functions.md)

## <a name="authentication"></a>Authentifizierung

Sichere Kommunikation erfordert, dass die Personen mit der Identität der Personen kommunizieren, mit denen Sie kommunizieren. Die Authentifizierung ist der Prozess der Überprüfung der Identität einer Person oder Entität.

Beispielsweise werden im täglichen Leben die physische Dokumentation, die häufig als Anmelde Informationen bezeichnet wird, zum Überprüfen der Identität einer Person verwendet. Wenn eine Überprüfung durchlaufen wird, kann die Person, die die Überprüfung eingibt, aufgefordert werden, die Lizenz eines Treibers anzuzeigen. Die Lizenz des Treibers ist ein physisches Dokument, das die Vertrauenswürdigkeit des Händlers in der Identität der Person, die die Überprüfung durchläuft, erhöht. In diesem Fall vertraut die Person, die die Überprüfung eingibt, dass der Status, der die Lizenz ausgibt, die Identität des Lizenzinhabers ordnungsgemäß überprüft hat.

Die Pässe stellen ein weiteres Beispiel dar. Eine Zoll-offizielle untersucht einen Passport und akzeptiert ihn als Nachweis, dass eine Person die Person ist, die er sagt. Die offizielle Vertrauensstellung hat festgelegt, dass die Regierung den Passport-Inhaber vor der Ausstellung des Passport identifiziert hat. In beiden Beispielen ist eine Vertrauens Ebene im Aussteller des physischen Dokuments vorhanden.

Die Authentifizierung umfasst auch die Sicherstellung, dass die empfangenen Daten die gesendeten Daten sind. Wenn Partei a eine Nachricht an Partei b sendet, muss Partei b beweisen können, dass die empfangene Nachricht die Nachricht war, die von Partei a gesendet wurde, und keine Nachricht, die diese Nachricht ersetzt hat. Um diese Form der Authentifizierung bereitzustellen, bietet [*CryptoAPI*](../secgloss/c-gly.md) Funktionen zum Signieren von Daten und Überprüfen von Signaturen mithilfe von öffentlichen/privaten Schlüsselpaaren.

Da die Kommunikation über ein Computernetzwerk ohne physischen Kontakt zwischen den Communicators stattfindet, hängt die Überprüfung der Identität häufig von Anmelde Informationen ab, die über ein Netzwerk gesendet und empfangen werden können. Solche Anmelde Informationen müssen von einem vertrauenswürdigen Aussteller von Anmelde Informationen ausgestellt werden. Digitale Zertifikate, häufig als Zertifikate bezeichnet, sind nur solche Anmelde Informationen. Sie sind eine Möglichkeit zum Überprüfen der Identität und zum Erreichen der Authentifizierung in einem Computernetzwerk.

Bei einem digitalen Zertifikat handelt es sich um Anmelde Informationen, die von einer vertrauenswürdigen Organisation oder als Zertifizierungsstelle (Certification Authority, ca) bezeichnet werden. Diese Anmelde Informationen enthalten einen öffentlichen Schlüssel (siehe [öffentliche/private Schlüsselpaare](public-private-key-pairs.md)) und Daten, die den Betreff des Zertifikats identifizieren. Ein Zertifikat wird nur dann von einer Zertifizierungsstelle ausgestellt, wenn die Zertifizierungsstelle die Identität des Zertifikat Antragstellers überprüft hat und bestätigt hat, dass der im Zertifikat enthaltene öffentliche Schlüssel zu diesem Betreff gehört.

Die Kommunikation zwischen einer Zertifizierungsstelle und einem Zertifikatanforderer kann von der anfordernden Person durchgeführt werden, die die erforderlichen Informationen, die möglicherweise auf einer Diskette gespeichert sind, an die Zertifizierungsstelle übertragen. Die Kommunikation wird jedoch in der Regel mit einer signierten Nachricht durchgeführt, die über ein Netzwerk gesendet wird. Die Zertifizierungsstelle verwendet häufig eine vertrauenswürdige Anwendung, die als Zertifikat Server bezeichnet wird, um Zertifikate auszustellen.

[*CryptoAPI*](../secgloss/c-gly.md) unterstützt die Authentifizierung durch die Verwendung digitaler Zertifikate, mit Zertifikaten zum Codieren/Decodieren von Funktionen und [*Zertifikat Speicher*](../secgloss/c-gly.md) Funktionen.

Weitere Informationen zur Identitätsüberprüfung und Authentifizierung durch die Verwendung von Zertifikaten finden Sie unter [digitale Zertifikate](digital-certificates.md).

## <a name="integrity"></a>Integrität

Alle Daten, die über ein nicht sicheres Medium gesendet werden, können entweder versehentlich oder nach Zweck geändert werden. In der realen Welt werden Dichtungen verwendet, um die Integrität zu gewährleisten und zu beweisen. Eine Flasche von Aspirin kann z. b. eine Manipulations geschützte Verpackung mit einem ununterbrochenen Siegel enthalten, um zu beweisen, dass das Paket nicht in das Paket eingefügt wurde, nachdem das Paket den Hersteller verlassen hat.

Auf dieselbe Weise muss ein Datenempfänger in der Lage sein, die Identität des Absenders der Daten zu überprüfen und sicherzustellen, dass es sich bei den empfangenen Daten genau um die gesendeten Daten handelt. Das heißt, dass Sie nicht manipuliert wurde. Das Einrichten der [*Integrität*](../secgloss/i-gly.md) der empfangenen Daten erfolgt häufig darin, dass nicht nur die ursprünglichen Daten, sondern auch eine Verifizierungs Nachricht, die als [*Hash*](../secgloss/h-gly.md)bezeichnet wird, über diese Daten gesendet werden. Sowohl die Daten als auch die Verifizierungs Nachricht können mit einer [*digitalen Signatur*](../secgloss/d-gly.md) gesendet werden, die den Ursprung beider Daten beweist.

Die Integrität wird in CryptoAPI mithilfe [digitaler Signaturen](digital-signatures.md) und [datenhashes](data-hashes.md)bereitgestellt.

[*CryptoAPI*](../secgloss/c-gly.md) unterstützt die Integrität durch die Verwendung von Nachrichten Funktionen, um Daten zu signieren und digitale Signaturen zu überprüfen.

 

 
