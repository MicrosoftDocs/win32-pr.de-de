---
description: Es wurde eine Gruppe von Funktionen auf hoher Ebene bereitgestellt, um die erforderliche Menge an Code zu vereinfachen und zu verkürzen, um die üblichen Aufgaben zur Nachrichten Bearbeitung auszuführen.
ms.assetid: 7c1a4d6e-9b9d-43c8-b094-3c98b9a68490
title: Vereinfachte Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbacaac4dd8ef32b7bab1ff4e57ad04aa1263c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129660"
---
# <a name="simplified-messages"></a>Vereinfachte Nachrichten

Es wurde eine Gruppe von Funktionen auf hoher Ebene bereitgestellt, um die erforderliche Menge an Code zu vereinfachen und zu verkürzen, um die üblichen Aufgaben zur Nachrichten Bearbeitung auszuführen. Diese Funktionen werden als "vereinfachte Nachrichten Funktionen" bezeichnet. Die Namen aller vereinfachten Nachrichten Funktionen enthalten das Wort "Message".

[*Vereinfachte Nachrichten Funktionen*](../secgloss/s-gly.md) befinden sich auf einer höheren Ebene als die grundlegenden Kryptografiefunktionen oder die Funktionen auf niedriger Ebene. Sie wrappen einige der grundlegenden Kryptografiefunktionen, der Low-Level-Nachricht und der Zertifikat Funktionen in eine einzelne Funktion, die eine bestimmte Aufgabe auf bestimmte Weise ausführt, z. b. das Verschlüsseln einer PKCS \# 7-Nachricht oder das Signieren einer Nachricht. Vereinfachte Nachrichten Funktionen bieten eine schnelle Möglichkeit für den Einstieg in die Verwendung von CryptoAPI, indem Sie die Anzahl von Funktionsaufrufen verringern, die zum Ausführen einer Aufgabe benötigt werden.

In der folgenden Tabelle sind Abschnitte aufgelistet, die ausführliche Beschreibungen der Prozeduren oder C-Programmbeispiele für die Verwendung der vereinfachten Nachrichten Funktionen enthalten.



| `Section`                                                                                                                                         | Contents                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Vereinfachte Nachrichten Funktionen](cryptography-functions.md)                                                         | Listet die vereinfachten Nachrichten Funktionen auf.                                                     |
| [Erstellen einer signierten Nachricht](creating-a-signed-message.md)                                                                                      | Erläutert den Prozess der Erstellung einer signierten Nachricht.                                           |
| [Verfahren zum Signieren von Daten](procedure-for-signing-data.md)                                                                                    | Stellt eine Prozedur zum Verwenden der vereinfachten Nachrichten Funktionen zum Erstellen einer signierten Nachricht bereit. |
| [Überprüfen einer signierten Nachricht](verifying-a-signed-message.md)                                                                                    | Erläutert einen Prozess zum Überprüfen der Signatur in einer signierten Nachricht.                          |
| [Verschlüsseln einer Nachricht](../secauthn/encrypting-a-message.md)                                                                                           | Erläutert die Aufgaben, die zum Verschlüsseln und Entschlüsseln einer Nachricht erforderlich sind.                                  |
| [Entschlüsseln einer Nachricht](../secauthn/decrypting-a-message.md)                                                                                           | Erläutert die Aufgaben, die zum Entschlüsseln einer Nachricht erforderlich sind.                                              |
| [Beispiel-C-Programm: Verwenden von cryptencryptmessage und cryptdecryptmessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) | Stellt eine Prozedur und einen Beispielcode zum Verschlüsseln und Entschlüsseln von Nachrichten bereit.               |



 

 

 
