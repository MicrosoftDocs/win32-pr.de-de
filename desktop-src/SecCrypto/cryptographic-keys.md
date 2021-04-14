---
description: Kryptografische Schlüssel sind für Kryptografievorgänge von zentraler Bedeutung.
ms.assetid: dda7b527-1522-4b43-8d8e-44ce7983a9aa
title: Kryptografische Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82858b26fa70ceacb4e7f9714e29983a773e66ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484619"
---
# <a name="cryptographic-keys"></a>Kryptografische Schlüssel

[*Kryptografische Schlüssel*](../secgloss/c-gly.md) sind für Kryptografievorgänge von zentraler Bedeutung. Viele kryptografieschemas bestehen aus paar Vorgängen, z. b. Verschlüsselung und Entschlüsselung oder Signierung und Überprüfung. Ein *Schlüssel* ist ein Teil der Variablen Daten, die als Eingabe in einen Kryptografiealgorithmus eingegeben werden, um einen solchen Vorgang auszuführen. In einem gut entworfenen kryptografieschema hängt die Sicherheit des Schemas nur von der Sicherheit der verwendeten Schlüssel ab.

Kryptografische Schlüssel können basierend auf ihrer Verwendung innerhalb eines kryptografischen Schemas als [symmetrische Schlüssel](symmetric-keys.md) oder [asymmetrische Schlüssel](public-private-key-pairs.md)klassifiziert werden. Ein [*symmetrischer Schlüssel*](../secgloss/s-gly.md) ist ein einzelner Schlüssel, der für beide Vorgänge in einem kryptografischen Schema verwendet wird (z. b. zum [*verschlüsseln*](../secgloss/e-gly.md) und [*entschlüsseln*](../secgloss/d-gly.md) der Daten). In der Regel ist die Sicherheit des Schemas davon abhängig, dass der Schlüssel nur den autorisierten Teilnehmern bekannt ist. Asymmetrische Schlüssel werden dagegen in kryptografieschemas verwendet, in denen für jeden Vorgang verschiedene Schlüssel benötigt werden. Häufige Beispiele für solche Schemas sind solche, die [*öffentliche/private Schlüsselpaare*](../secgloss/p-gly.md)verwenden, bei denen die Sicherheit des Schemas davon abhängt, dass der [*private Schlüssel*](../secgloss/p-gly.md) nur einer Partei bekannt ist. Beispielsweise verwenden öffentliche/private Verschlüsselungssysteme zwei Schlüssel, einen [*öffentlichen Schlüssel*](../secgloss/p-gly.md) , der von jedem verwendet werden kann, um Daten zu verschlüsseln, und einen [*privaten Schlüssel*](../secgloss/p-gly.md) , den nur der autorisierte Empfänger besitzt und der zum Entschlüsseln der Daten verwendet werden kann.

Kryptografische Schlüssel können nach dem Zweck, für den Sie verwendet werden, weiter klassifiziert werden. Diese Verwendungsmöglichkeiten umfassen die Generierung digitaler Signaturen, die Überprüfung der digitalen Signatur, die Nachrichten Authentifizierung, die Verschlüsselung und Entschlüsselung von Daten, das Schlüssel Wrapping und den Schlüssel Transport. Eine vollständige Liste der Schlüsseltypen, die vom [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) definiert werden, finden Sie in Abschnitt 5: Leitfaden zur allgemeinen Schlüsselverwaltung der [NIST Special Publication 800-57: Empfehlung für die Schlüsselverwaltung – Teil 1: Allgemein (überarbeitet)](https://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf).

 

 
