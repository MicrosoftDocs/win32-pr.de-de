---
description: Die Verschlüsselung ist der Prozess der Übersetzung von Klartext-Daten (Klartext) in etwas, das zufällig und bedeutungslos erscheint (Chiffre Text). Bei der Entschlüsselung handelt es sich um den Prozess, bei dem Chiffre Text zurück in Klartext umgerechnet wird.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Verschlüsselung und Entschlüsselung von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128792"
---
# <a name="data-encryption-and-decryption"></a>Verschlüsselung und Entschlüsselung von Daten

Die Verschlüsselung ist der Prozess der Übersetzung von Klartext-[*Daten (Klartext*](../secgloss/p-gly.md)) in etwas, das zufällig und bedeutungslos erscheint ([*Chiffre Text*](../secgloss/c-gly.md)). Bei der Entschlüsselung handelt es sich um den Prozess, bei dem Chiffre Text zurück in Klartext umgerechnet wird.

Zum Verschlüsseln von mehr als einer kleinen Datenmenge wird die [*symmetrische Verschlüsselung*](../secgloss/s-gly.md) verwendet. Ein [*symmetrischer Schlüssel*](../secgloss/s-gly.md) wird während der Verschlüsselungs-und Entschlüsselungs Prozesse verwendet. Zum Entschlüsseln eines bestimmten Chiffre Texts muss der Schlüssel verwendet werden, der zum Verschlüsseln der Daten verwendet wurde.

Das Ziel der einzelnen Verschlüsselungsalgorithmen besteht darin, den generierten Chiffre Text ohne Verwendung des Schlüssels so schwierig wie möglich zu entschlüsseln. Wenn ein wirklich guter Verschlüsselungsalgorithmus verwendet wird, gibt es keine Technik, die wesentlich besser ist als methodisch versucht, jeden möglichen Schlüssel zu verwenden. Bei einem solchen Algorithmus ist der Schlüssel umso schwieriger, wenn ein Teil des Chiffre Texts entschlüsselt wird, ohne den Schlüssel zu besitzen.

Es ist schwierig, die Qualität eines Verschlüsselungsalgorithmus zu ermitteln. Algorithmen, die vielversprechend aussehen, werden bei einem angemessenen Angriff manchmal sehr einfach zu unterbrechen. Wenn Sie einen Verschlüsselungsalgorithmus auswählen, empfiehlt es sich, einen Wert auszuwählen, der bereits seit mehreren Jahren verwendet wurde, und sich erfolgreich gegen alle Angriffe gewehrt hat.

Weitere Informationen finden Sie unter [Datenverschlüsselungs-und Entschlüsselungs Funktionen](cryptography-functions.md).

 

 
