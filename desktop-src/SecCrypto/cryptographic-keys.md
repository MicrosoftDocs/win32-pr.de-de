---
description: Kryptografische Schlüssel sind für kryptografische Vorgänge von zentraler Bedeutung.
ms.assetid: dda7b527-1522-4b43-8d8e-44ce7983a9aa
title: Kryptografische Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25647d64aafa8d996c60df37d1f5b5a86226451e1a0f3a3cfefc7ef405f3a11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876300"
---
# <a name="cryptographic-keys"></a>Kryptografische Schlüssel

[*Kryptografische Schlüssel*](../secgloss/c-gly.md) sind für kryptografische Vorgänge von zentraler Bedeutung. Viele kryptografische Schemas bestehen aus Paaren von Vorgängen, z. B. Verschlüsselung und Entschlüsselung oder Signierung und Überprüfung. Ein *Schlüssel* ist ein Teil variabler Daten, der als Eingabe in einen kryptografischen Algorithmus eingegeben wird, um einen solchen Vorgang durchzuführen. In einem gut entworfenen kryptografischen Schema hängt die Sicherheit des Schemas nur von der Sicherheit der verwendeten Schlüssel ab.

Kryptografische Schlüssel können basierend auf ihrer Verwendung innerhalb eines kryptografischen Schemas als [symmetrische](symmetric-keys.md) Schlüssel oder asymmetrische [Schlüssel klassifiziert werden.](public-private-key-pairs.md) Ein [*symmetrischer Schlüssel*](../secgloss/s-gly.md) ist ein einzelner Schlüssel, der für beide Vorgänge [](../secgloss/e-gly.md) in einem kryptografischen Schema verwendet wird (z. B. zum Verschlüsseln und Entschlüsseln [*Ihrer*](../secgloss/d-gly.md) Daten). In der Regel hängt die Sicherheit des Schemas davon ab, dass der Schlüssel nur den autorisierten Teilnehmern bekannt ist. Asymmetrische Schlüssel werden dagegen in kryptografischen Schemas verwendet, bei denen für jeden Vorgang unterschiedliche Schlüssel benötigt werden. Gängige Beispiele für solche Schemas sind solche, die Paare aus öffentlichem [*und*](../secgloss/p-gly.md)privatem Schlüssel verwenden, bei denen die Sicherheit des Schemas davon abhängt, sicherzustellen, dass der [*private*](../secgloss/p-gly.md) Schlüssel nur einer Partei bekannt ist. Beispielsweise verwenden Verschlüsselungssysteme mit öffentlichem/privatem [](../secgloss/p-gly.md) Schlüssel zwei Schlüssel: einen öffentlichen [](../secgloss/p-gly.md) Schlüssel, den jeder zum Verschlüsseln von Daten verwenden kann, und einen privaten Schlüssel, den nur der autorisierte Empfänger besitzt und der zum Entschlüsseln der Daten verwendet werden kann.

Kryptografische Schlüssel können weiter nach dem Zweck klassifiziert werden, für den sie verwendet werden. Zu diesen Verwendungsmöglichkeiten gehören digitale Signaturgenerierung, Überprüfung der digitalen Signatur, Nachrichtenauthentifizierung, Datenverschlüsselung und -entschlüsselung, Schlüsselumbruch und Schlüsseltransport. Eine vollständige Liste der Schlüsseltypen, die vom [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) definiert werden, finden Sie in Abschnitt 5 GENERAL KEY MANAGEMENT GUIDANCE of [NIST Special Publication 800-57: Recommendation for Key Management – Part 1: General (Revised)](https://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf).

 

 
