---
description: Erläutert die CryptoAPI-Systemarchitektur.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: CryptoAPI-Systemarchitektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791ed0ebfc82df1dc7b6e9600d4e0455ae60df3da35cfe3f8fd613f7b230ebd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768806"
---
# <a name="cryptoapi-system-architecture"></a>CryptoAPI-Systemarchitektur

Die CryptoAPI-Systemarchitektur besteht aus fünf hauptfunktionalen Bereichen:

-   [Grundlegende kryptografische Funktionen](#base-cryptographic-functions)
-   [Funktionen zum Codieren/Decodieren von Zertifikaten](#certificate-encodedecode-functions)
-   [Certificate Store Functions](#certificate-store-functions)
-   [Vereinfachte Nachrichtenfunktionen](#simplified-message-functions)
-   [Nachrichtenfunktionen auf niedriger Ebene](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a>Grundlegende kryptografische Funktionen

-   *Kontextfunktionen,* die zum Herstellen einer Verbindung mit einem CSP verwendet werden. Diese Funktionen ermöglichen Es Anwendungen, einen bestimmten CSP anhand des Namens auszuwählen oder einen bestimmten CSP auszuwählen, der eine erforderliche Funktionsklasse bereitstellen kann.
-   [*Schlüsselgenerierungsfunktionen,*](../secgloss/k-gly.md) die zum Generieren und Speichern [*kryptografischer Schlüssel*](../secgloss/c-gly.md)verwendet werden. Vollständige Unterstützung ist für das Ändern von [*Verkettungsmodi,*](../secgloss/c-gly.md) [*Initialisierungsvektoren*](../secgloss/i-gly.md)und anderen Verschlüsselungsfunktionen enthalten. Weitere Informationen finden Sie unter [Schlüsselgenerierung und Exchange Functions](cryptography-functions.md).
-   *Schlüsselaustauschfunktionen,* die zum Austauschen oder Übertragen von Schlüsseln verwendet werden. Weitere Informationen finden Sie unter [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md) and Key Generation and Exchange [Functions](cryptography-functions.md).

## <a name="certificate-encodedecode-functions"></a>Funktionen zum Codieren/Decodieren von Zertifikaten

-   Funktionen, die zum Verschlüsseln oder Entschlüsseln von Daten verwendet werden. Die Unterstützung für [*Hashdaten*](../secgloss/h-gly.md) ist ebenfalls enthalten. Weitere Informationen finden Sie unter [Datenverschlüsselungs- und Entschlüsselungsfunktionen](cryptography-functions.md) und [Datenverschlüsselung und -entschlüsselung.](data-encryption-and-decryption.md)

## <a name="certificate-store-functions"></a>Certificate Store Functions

-   Funktionen, die zum Verwalten von Sammlungen digitaler Zertifikate verwendet werden. Weitere Informationen finden Sie unter [Digitale Zertifikate](digital-certificates.md) und Zertifikat [Store Functions.](cryptography-functions.md)

## <a name="simplified-message-functions"></a>Vereinfachte Nachrichtenfunktionen

-   Funktionen zum Verschlüsseln und Entschlüsseln von Nachrichten und Daten.
-   Funktionen, die zum Signieren von Nachrichten und Daten verwendet werden.
-   Funktionen, die verwendet werden, um die Authentizität von Signaturen für empfangene Nachrichten und zugehörige Daten zu überprüfen.

Weitere Informationen finden Sie unter [Vereinfachte Nachrichten](simplified-messages.md) und [vereinfachte Nachrichtenfunktionen.](cryptography-functions.md)

## <a name="low-level-message-functions"></a>Nachrichtenfunktionen auf niedriger Ebene

-   Funktionen, die zum Ausführen aller Aufgaben verwendet werden, die von den vereinfachten Nachrichtenfunktionen ausgeführt werden. Die Nachrichtenfunktionen auf niedriger Ebene bieten mehr Flexibilität als die vereinfachten Nachrichtenfunktionen, erfordern jedoch mehr Funktionsaufrufe. Weitere Informationen finden Sie unter [Low-level Messages (Meldungen auf niedriger Ebene)](low-level-messages.md) und [Low-level Message Functions (Nachrichtenfunktionen auf niedriger Ebene).](cryptography-functions.md)

![cryptoapi-Architektur](images/cryparch.png)

Jeder Funktionsbereich hat ein Schlüsselwort im Funktionsnamen, das seinen Funktionsbereich angibt.



| Funktionsbereich              | Funktionsnamenskonvention |
|------------------------------|--------------------------|
| Grundlegende kryptografische Funktionen | Krypta                    |
| Codierungs-/Decodierungsfunktionen  | Krypta                    |
| Zertifikatspeicherfunktionen  | Speicher                    |
| Vereinfachte Nachrichtenfunktionen | `Message`                  |
| Nachrichtenfunktionen auf niedriger Ebene  | Msg                      |



 

Anwendungen verwenden Funktionen in all diesen Bereichen. Diese Funktionen bilden zusammen CryptoAPI. Die [*grundlegenden kryptografischen Funktionen*](../secgloss/b-gly.md) verwenden die CSPs für die erforderlichen kryptografischen Algorithmen und für die Generierung und sichere Speicherung von [kryptografischen Schlüsseln.](cryptographic-keys.md)

Zwei verschiedene Arten von kryptografischen Schlüsseln werden verwendet: [*Sitzungsschlüssel*](../secgloss/s-gly.md), die für eine einzelne Verschlüsselung/Entschlüsselung verwendet werden, und [*öffentliche/private Schlüsselpaare,*](../secgloss/p-gly.md)die dauerhafter verwendet werden.

> [!Note]  
> Obwohl eine Anwendung direkt mit einem der fünf Funktionsbereiche kommunizieren kann, kann sie nicht direkt mit einem CSP kommunizieren. Die gesamte Kommunikation zwischen Anwendung und CSP erfolgt über die [*grundlegenden kryptografischen Funktionen*](../secgloss/b-gly.md). Kryptografische Basisfunktionen verfügen über einen Parameter, der angibt, welcher CSP verwendet werden soll. Dieser Parameter kann auf **NULL** festgelegt werden, um einen Standard-CSP auszuwählen.

 

 

 
