---
description: Der Client muss dem Server eine digestaufforderungs-Antwort senden, wenn er eine Digest-Abfrage als Reaktion auf eine Anforderung für eine Ressource empfängt.
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: Inhalt einer digestaufforderungs-Antwort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7168a7e6a468ecc7d573ef0bd853ec6db255b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216539"
---
# <a name="contents-of-a-digest-challenge-response"></a>Inhalt einer digestaufforderungs-Antwort

Der Client muss dem Server eine digestaufforderungs-Antwort senden, wenn er eine Digest-Abfrage als Reaktion auf eine Anforderung für eine Ressource empfängt. Der Client muss die Anforderung erneut senden und einen Autorisierungs Header mit der Challenge-Antwort bereitstellen. In der folgenden Tabelle werden die Direktiven beschrieben, die eine digestaufforderungs-Antwort bilden.



| Anweisung          | Beschreibung                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| username           | Der Kontoname des [*Sicherheits Prinzipals*](/windows/desktop/SecGloss/s-gly) , der die Ressource anfordert.                                                                  |
| Bereich              | Der Name der Domäne, die das durch username festgestellte Konto enthält.                                                                                                                                                    |
| nonce              | Die Nonce, die in der Digest-Herausforderung empfangen wurde.                                                                                                                                                                                |
| uri                | Der URI (Universal Resource Identifier) der angeforderten Ressource.                                                                                                                                                         |
| QoP                | Die [Qualität des Schutzes](quality-of-protection.md).                                                                                                                                                                    |
| CS                 | Die Nonce-Anzahl. Gibt an, wie oft der Client eine Abfrage Antwort mithilfe der Nonce gesendet hat. Weitere Informationen finden Sie unter der Nonce-Direktive.                                                                              |
| cnonce             | Ein eindeutiger codierter Wert, der vom Client für jede Abfrage Antwort generiert wurde.                                                                                                                                                |
| Antwort           | Ein Wert, der gemäß der Digest-Zugriffs Spezifikation ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)) berechnet wird. Eine genaue Antwort ist ein eindeutiger Nachweis dafür, dass das Kennwort des Benutzers auf der Clientseite bekannt ist. |
| Algorithmus          | Der in der Digest-Abfrage empfangene Algorithmus.                                                                                                                                                                            |
| lässige             | Der in der Digest-Abfrage empfangene nicht transparente Wert.                                                                                                                                                                         |
| (Nur SASL) Chiffre | Einer der Verschlüsselungs Werte, die in der Digestherausforderung empfangen wurden. Weitere Informationen zur Verschlüsselung finden Sie unter [Qualität von Schutz und Chiffren](quality-of-protection-and-ciphers.md).                                                             |



 

Microsoft Digest unterstützt die folgenden Benutzername/Bereich-Formulare:

-   Benutzername Bereich
-   Accountname-Domäne (flach)
-   UPN "" (leer)
-   NetBIOS "" (leer)

Obwohl Großbuchstaben unterstützt werden, wird die Verwendung von Kleinbuchstaben empfohlen, um eine optimale Leistung zu erzielen, die den im Voraus berechneten Hash Werten des Servers entspricht.

Die Verwendung von vorab berechneten Hashes ist ein neues Feature, mit dem System Operatoren die Verwendung umkehrbarer verschlüsselter Kenn Wörter auf dem Domänen Controller überspringen können. Ein vorab berechneter Hash wird für einen Benutzer erstellt, wenn das Kennwort des Benutzers geändert wird.

Microsoft Digest generiert die digestaufforderungs-Antwort Zeichenfolge für Client Anwendungen. Weitere Informationen finden Sie unter [Erstellen der Digest](generating-the-digest-challenge-response.md)-Abfrage Antwort.

 

 
