---
description: Verschlüsselung ist der Prozess der Übersetzung von Nur-Text-Daten (Klartext) in etwas, das zufällig und bedeutungslos erscheint (Chiffretext). Entschlüsselung ist der Prozess der Konvertierung von Chiffretext zurück in Klartext.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Datenverschlüsselung und -entschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba508eeb67570d1f293ae55e1b6bff5217529663a6682a17d9817a9dc0834803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100910"
---
# <a name="data-encryption-and-decryption"></a>Datenverschlüsselung und -entschlüsselung

Verschlüsselung ist der Prozess der Übersetzung von Nur-Text-Daten ([*Klartext*](../secgloss/p-gly.md)) in etwas, das zufällig und bedeutungslos zu sein scheint [*(Chiffretext*](../secgloss/c-gly.md)). Entschlüsselung ist der Prozess der Konvertierung von Chiffretext zurück in Klartext.

Um mehr als eine kleine Datenmenge zu verschlüsseln, wird [*symmetrische Verschlüsselung*](../secgloss/s-gly.md) verwendet. Ein [*symmetrischer Schlüssel*](../secgloss/s-gly.md) wird sowohl während des Verschlüsselungs- als auch des Entschlüsselungsprozesses verwendet. Um einen bestimmten Chiffretext zu entschlüsseln, muss der Schlüssel verwendet werden, der zum Verschlüsseln der Daten verwendet wurde.

Das Ziel jedes Verschlüsselungsalgorithmus besteht darin, das Entschlüsseln des generierten Chiffretexts ohne Verwendung des Schlüssels so schwierig wie möglich zu gestalten. Wenn ein wirklich guter Verschlüsselungsalgorithmus verwendet wird, gibt es keine Technik, die wesentlich besser ist, als jeden möglichen Schlüssel methodisch auszuprobieren. Je länger der Schlüssel für einen solchen Algorithmus ist, desto schwieriger ist es, einen Chiffretext zu entschlüsseln, ohne den Schlüssel zu besitzen.

Es ist schwierig, die Qualität eines Verschlüsselungsalgorithmus zu bestimmen. Algorithmen, die mäßig aussehen, sind angesichts des richtigen Angriffs manchmal sehr einfach zu unterbrechen. Wenn Sie einen Verschlüsselungsalgorithmus auswählen, empfiehlt es sich, einen zu wählen, der seit mehreren Jahren verwendet wird und erfolgreich alle Angriffe verhindert hat.

Weitere Informationen finden Sie unter [Datenverschlüsselungs- und Entschlüsselungsfunktionen.](cryptography-functions.md)

 

 
