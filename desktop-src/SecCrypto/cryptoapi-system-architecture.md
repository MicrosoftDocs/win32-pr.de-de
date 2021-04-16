---
description: Erläutert die kryptoapi-Systemarchitektur.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Kryptoapi-System Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343139"
---
# <a name="cryptoapi-system-architecture"></a>Kryptoapi-System Architektur

Die kryptoapi-Systemarchitektur besteht aus fünf Haupt Funktionsbereichen:

-   [Grundlegende Kryptografiefunktionen](#base-cryptographic-functions)
-   [Zertifikatcodieren/Decodieren von Funktionen](#certificate-encodedecode-functions)
-   [Zertifikat Speicherfunktionen](#certificate-store-functions)
-   [Vereinfachte Nachrichten Funktionen](#simplified-message-functions)
-   [Nachrichten Funktionen auf niedriger Ebene](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a>Grundlegende Kryptografiefunktionen

-   *Kontextfunktionen* , die zum Herstellen einer Verbindung mit einem CSP verwendet werden. Mit diesen Funktionen können Anwendungen einen bestimmten CSP nach Namen auswählen oder einen bestimmten CSP auswählen, der eine erforderliche Funktionsklasse bereitstellen kann.
-   [*Schlüssel Generierungs Funktionen*](../secgloss/k-gly.md) , die zum Generieren und Speichern von [*kryptografischen Schlüsseln*](../secgloss/c-gly.md)verwendet werden. Vollständige Unterstützung für das Ändern von [*Verkettungs Modi*](../secgloss/c-gly.md), [*Initialisierungs Vektoren*](../secgloss/i-gly.md)und anderen Verschlüsselungsfunktionen. Weitere Informationen finden Sie unter [Schlüsselgenerierung und Exchange-Funktionen](cryptography-functions.md).
-   *Schlüsselaustausch Funktionen* , die zum austauschen oder übertragen von Schlüsseln verwendet werden. Weitere Informationen finden Sie unter [kryptografieschlüsselspeicher und Exchange](cryptographic-key-storage-and-exchange.md) -und [Schlüssel Generierungs-und Exchange-Funktionen](cryptography-functions.md).

## <a name="certificate-encodedecode-functions"></a>Zertifikatcodieren/Decodieren von Funktionen

-   Funktionen, die zum Verschlüsseln oder Entschlüsseln von Daten verwendet werden. Die Unterstützung ist auch für das [*hashingdata*](../secgloss/h-gly.md) enthalten. Weitere Informationen finden Sie unter [Datenverschlüsselungs-und Entschlüsselungs Funktionen](cryptography-functions.md) und [Datenverschlüsselung und Entschlüsselung](data-encryption-and-decryption.md).

## <a name="certificate-store-functions"></a>Zertifikat Speicherfunktionen

-   Funktionen, die zum Verwalten von Sammlungen digitaler Zertifikate verwendet werden. Weitere Informationen finden Sie unter [digitale Zertifikate](digital-certificates.md) und [Zertifikat Speicherfunktionen](cryptography-functions.md).

## <a name="simplified-message-functions"></a>Vereinfachte Nachrichten Funktionen

-   Funktionen, die zum Verschlüsseln und Entschlüsseln von Nachrichten und Daten verwendet werden.
-   Funktionen zum Signieren von Nachrichten und Daten.
-   Funktionen, die verwendet werden, um die Authentizität von Signaturen in empfangenen Nachrichten und zugehörigen Daten zu überprüfen.

Weitere Informationen finden Sie unter [vereinfachte Meldungen](simplified-messages.md) und [vereinfachte Nachrichten Funktionen](cryptography-functions.md).

## <a name="low-level-message-functions"></a>Nachrichten Funktionen auf niedriger Ebene

-   Funktionen, die verwendet werden, um alle Aufgaben auszuführen, die von den vereinfachten Nachrichten Funktionen ausgeführt werden. Die Nachrichten Funktionen auf niedriger Ebene bieten mehr Flexibilität als die vereinfachten Nachrichten Funktionen, erfordern jedoch mehr Funktionsaufrufe. Weitere Informationen finden Sie unter [Nachrichten auf niedriger Ebene](low-level-messages.md) und auf [Low-Level-Nachrichten Funktionen](cryptography-functions.md).

![kryptoapi-Architektur](images/cryparch.png)

Jeder Funktionsbereich verfügt über ein Schlüsselwort im Funktionsnamen, das den Funktionsbereich angibt.



| Funktionsbereich              | Funktionsnamens Konvention |
|------------------------------|--------------------------|
| Grundlegende Kryptografiefunktionen | Schlendern                    |
| Codierung/Decodierung von Funktionen  | Schlendern                    |
| Zertifikat Speicherfunktionen  | Speicher                    |
| Vereinfachte Nachrichten Funktionen | `Message`                  |
| Nachrichten Funktionen auf niedriger Ebene  | Meldung                      |



 

Anwendungen verwenden Funktionen in allen diesen Bereichen. Diese Funktionen bilden eine kryptografieapi. Die [*grundlegenden Kryptografiefunktionen*](../secgloss/b-gly.md) verwenden die CSPs für die erforderlichen Kryptografiealgorithmen und für die Generierung und sichere Speicherung von [Kryptografieschlüsseln](cryptographic-keys.md).

Es werden zwei verschiedene Arten von Kryptografieschlüsseln verwendet: [*Sitzungsschlüssel*](../secgloss/s-gly.md), die für einzelne Verschlüsselungs-/Entschlüsselungs-und [*öffentliche/private Schlüsselpaare*](../secgloss/p-gly.md)verwendet werden, die permanent verwendet werden.

> [!Note]  
> Obwohl eine Anwendung direkt mit jedem der fünf Funktionsbereiche kommunizieren kann, kann Sie nicht direkt mit einem CSP kommunizieren. Die gesamte Kommunikation zwischen Anwendungen und CSP erfolgt über die [*grundlegenden Kryptografiefunktionen*](../secgloss/b-gly.md). Grundlegende Kryptografiefunktionen verfügen über einen Parameter, der angibt, welcher CSP verwendet werden soll. Dieser Parameter kann auf **null** festgelegt werden, um einen Standard-CSP auszuwählen.

 

 

 
