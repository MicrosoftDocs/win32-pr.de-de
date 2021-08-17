---
description: Der Client muss dem Server eine Digest-Challenge-Antwort senden, wenn er eine Digest-Anforderung als Antwort auf eine Anforderung für eine Ressource empfängt.
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: Inhalt einer Digest-Challenge-Antwort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2a4fd199dfe9e97d69628adb0e6012bc4941929b9c1e96e00de8c42d53eba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141153"
---
# <a name="contents-of-a-digest-challenge-response"></a>Inhalt einer Digest-Challenge-Antwort

Der Client muss dem Server eine Digest-Challenge-Antwort senden, wenn er eine Digest-Anforderung als Antwort auf eine Anforderung für eine Ressource empfängt. Der Client muss die Anforderung erneut senden und einen Autorisierungsheader mit der Antwort auf die Aufforderung angeben. In der folgenden Tabelle werden die Anweisungen beschrieben, aus denen eine Digest-Challenge-Antwort besteht.



| Anweisung          | Beschreibung                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| username           | Der Kontoname des [*Sicherheitsprinzipals, der*](/windows/desktop/SecGloss/s-gly) die Ressource an fordert.                                                                  |
| Realm              | Der Name der Domäne, die das durch den Benutzernamen angegebene Konto enthält.                                                                                                                                                    |
| nonce              | Die nonce, die in der Digest-Herausforderung empfangen wurde.                                                                                                                                                                                |
| uri                | Der URI (Universal Resource Identifier) der angeforderten Ressource.                                                                                                                                                         |
| qop                | Die [Qualität des Schutzes.](quality-of-protection.md)                                                                                                                                                                    |
| Nc                 | Die Nonce-Anzahl. Gibt an, wie oft der Client mithilfe der Nonce eine Antwort auf die Herausforderung gesendet hat. Weitere Informationen finden Sie unter nonce-Direktive.                                                                              |
| cnonce             | Ein eindeutiger codierter Wert, der vom Client für jede Antwort auf die Herausforderung generiert wird.                                                                                                                                                |
| Antwort           | Ein Gemäß der Digestzugriffsspezifikation berechneter Wert ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)). Eine genaue Antwort ist ein eindeutiger Nachweis dafür, dass das Kennwort des Benutzers auf clientseitiger Seite bekannt ist. |
| Algorithmus          | Der in der Digest-Herausforderung empfangene Algorithmus.                                                                                                                                                                            |
| Undurchsichtig             | Der nicht transparente Wert, der in der Digest-Challenge empfangen wurde.                                                                                                                                                                         |
| Verschlüsselung (nur SASL) | Einer der Verschlüsselungswerte, die in der Digest-Herausforderung empfangen wurden. Weitere Informationen zu Verschlüsselungen finden Sie [unter Quality of Protection und Ciphers](quality-of-protection-and-ciphers.md).                                                             |



 

Microsoft Digest unterstützt die folgenden Benutzernamen-/Bereichsformulare:

-   Benutzernamesbereich
-   AccountName-Domäne (flach)
-   UPN "" (leer)
-   NetBIOS "" (leer)

Obwohl Großbuchstaben unterstützt werden, wird die Verwendung von Kleinbuchstaben empfohlen, um eine optimale Leistung mit den vorab berechneten Hashwerten des Servers zu erzielen.

Die Verwendung von vorab berechneten Hashes ist ein neues Feature, mit dem Systemoperatoren die Verwendung umkehrbarer verschlüsselter Kennwörter auf dem Domänencontroller überspringen können. Ein vorab berechneter Hash wird für einen Benutzer gebildet, wenn das Kennwort des Benutzers geändert wird.

Microsoft Digest generiert die Digest-Abfrageantwortzeichenfolge für Clientanwendungen. Weitere Informationen finden Sie unter [Generieren der Digest-Challenge-Antwort](generating-the-digest-challenge-response.md).

 

 
