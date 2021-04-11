---
description: Die Größe einer digestzugriffschallenge muss kleiner als 2048 Byte sein.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Inhalt einer Digestherausforderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128316"
---
# <a name="contents-of-a-digest-challenge"></a>Inhalt einer Digestherausforderung

Die Größe einer digestzugriffschallenge muss kleiner als 2048 Byte sein. Das folgende Beispiel zeigt eine Anforderung, die der Zeichenfolge szchallenge zugewiesen ist.


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> Die Abfrage Zeichenfolge wird in doppelte Anführungszeichen eingeschlossen und enthält eingebettete doppelte Anführungszeichen. Eingebetteten doppelten Anführungszeichen muss ein umgekehrter Schrägstrich () vorangestellt werden \\ .

 

Eine Digestherausforderung kann die folgenden Direktiven enthalten.



| Anweisung         | Beschreibung                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| realm             | Ein von der Implementierung definierter Hinweis für den Client, welche [*Anmelde*](/windows/desktop/SecGloss/c-gly) Informationen erforderlich sind. Der Client sollte diese Informationen für den Benutzer anzeigen, wenn er zur Eingabe von Anmelde Informationen aufgefordert wird.                                                  |
| Algorithmus         | Microsoft Digest unterstützt MD5 und MD5-sess. Verwenden Sie für eine optimale Leistung MD5-sess.                                                                                                                                                                                                                     |
| QoP               | Diese Direktive kann auf "auth", "auth-int" oder "auth-conf" festgelegt werden. Weitere Informationen finden Sie unter [Qualität von Schutz und Chiffren](quality-of-protection-and-ciphers.md).                                                                                                                                       |
| nonce             | Ein eindeutiger codierter Wert, der vom Server für jede Abfrage generiert wird. Dieser Wert darf nicht vom Client geändert werden.                                                                                                                                                                                       |
| lässige            | Enthält einen Verweis für den [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) , der festgelegt wird. Weitere Informationen finden Sie unter Verwalten [des Sicherheits Kontexts zwischen Verbindungen](maintaining-the-security-context-between-connections.md). |
| Chiffre (nur SASL) | Die Liste der Chiffren, die der Server unterstützt. Dieses Element kann in einer Digest-SASL-Abfrage nur vorhanden sein, wenn die QoP-Direktive auth-conf angibt. Weitere Informationen finden Sie unter [Qualität von Schutz und Chiffren](quality-of-protection-and-ciphers.md).                                              |
| charset           | Diese Direktive kann auf UTF-8 festgelegt werden, wenn der Server UTF-8 – codierte Benutzernamen und Bereiche verarbeiten kann. Wenn der Client die charset-Direktive versteht, kann er mithilfe von UTF-8 – codierten Werten Antworten.                                                                                                       |



 

Microsoft Digest generiert die digestaufforderungs-Zeichenfolge für Server Anwendungen. Weitere Informationen finden Sie unter [Erstellen der Digest-Herausforderung](generating-the-digest-challenge.md).

 

 
