---
description: Die Nachrichten Funktionen auf niedriger Ebene codieren Daten für die Übertragung und Decodierung von Daten, die empfangen wurden. Auf Low-Level-Nachrichten Funktionen werden auch die Signaturen empfangener Nachrichten entschlüsselt und überprüft.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Nachrichten Funktionen auf niedriger Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752129"
---
# <a name="low-level-message-functions"></a>Nachrichten Funktionen auf niedriger Ebene

Die [*Nachrichten Funktionen auf niedriger Ebene*](../secgloss/l-gly.md) codieren Daten für die Übertragung und Decodierung von Daten, die empfangen wurden. Auf Low-Level-Nachrichten Funktionen werden auch die Signaturen empfangener Nachrichten entschlüsselt und überprüft.

Wenn eine Nachricht mithilfe einer Funktion zum Öffnen von Nachrichten auf niedriger Ebene geöffnet wird, bleibt sie offen und verfügbar (behält ihren [*Zustand*](../secgloss/s-gly.md)bei), bis Sie geschlossen wird. Dadurch kann eine Nachricht schrittweise mithilfe mehrerer Aufrufe der [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) -Funktion erstellt werden.

Die Verwendung von Nachrichten Funktionen auf niedriger Ebene erfordert mehr Funktionsaufrufe als die Verwendung von vereinfachten Nachrichten Funktionen (siehe [vereinfachte Meldungen](simplified-messages.md)). Wenn die vereinfachten Nachrichten Funktionen verwendet werden, wird mehr Arbeit innerhalb der Funktionen der API ausgeführt.

Die Verwendung von Nachrichten Funktionen auf niedriger Ebene umfasst die zusätzliche Arbeit bei Aufrufen von anderen Zertifikaten oder Kryptografiefunktionen. Beispielsweise können Daten aus Aufrufen von Zertifikat Funktionen zum Initialisieren von Strukturen benötigt werden, die von diesen Low-Level-Nachrichten Funktionen verwendet werden. Vereinfachte Nachrichten Funktionen initialisieren viele dieser Strukturen intern.

In der folgenden Tabelle sind Abschnitte mit Prozedur Beschreibungen und C-Codebeispiele für die Verwendung der Funktionen auf niedriger Ebene aufgeführt.



| `Section`                                                                               | Contents                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [Nachrichten Funktionen auf niedriger Ebene](cryptography-functions.md) | Listet die Nachrichten Funktionen auf niedriger Ebene auf.             |
| [Signieren von Daten](signing-data.md)                                                      | Erläutert die zum Signieren von Daten erforderlichen Aufgaben.             |
| [Codieren von eingeschlossenen Daten](encoding-enveloped-data.md)                                | Erläutert die Aufgaben, die zum Codieren von eingeschlossenen Daten erforderlich sind. |
| [Decodieren von eingeschlossenen Daten](decoding-enveloped-data.md)                                | Erläutert die Aufgaben, die zum Decodieren von eingeschlossenen Daten erforderlich sind. |



 

 

 
