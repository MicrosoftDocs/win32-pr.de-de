---
description: Der problematischste Teil beim Schreiben von Komponenten ist der Umgang mit möglichen Fehlern.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Behandeln von Fehlern in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b66ecfd2d66d30b601fdc9e3e580d258ab912db5c10e3af422b9e7fde2b7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306549"
---
# <a name="handling-errors-in-com"></a>Behandeln von Fehlern in COM+

Der problematischste Teil beim Schreiben von Komponenten ist der Umgang mit möglichen Fehlern. Unter den besten Bedingungen kann es schwierig sein, zu ermitteln, was schief gehen kann und was dagegen vorzugehen ist. Häufige Fehler, die ihre Komponente möglicherweise überprüft und behandelt, sind fehlerhafte Netzwerkverbindungen, Sicherheitsfehler und Fehler im Zusammenhang mit nicht erreichbaren Objekten.

Darüber hinaus können Sie eigene Fehlercodes entwickeln, um schnittstellenspezifische Fehler zu melden, z. B. wenn eine Geschäftsregel verletzt wurde.

In Übereinstimmung mit dem COM+-Programmiermodell kann ein Objekt Schnittstellenmethoden für andere Objekte aufrufen (und dies häufig auch auch). Da Programmierer Komponenten in verschiedenen Programmiersprachen schreiben können, erfordert COM+, dass alle Fehlerbehandlungsmechanismen [](errorinfo.md) sprachneutral sind, z. B. HRESULTs und ErrorInfo-Sammlungen.

Dieser Abschnitt enthält Themen, die in der folgenden Tabelle beschrieben werden, in denen Verfahren zum Behandeln von Fehlern in COM+-Anwendungen, Features in COM+ beschrieben werden, die sich auf das Fehlerverhalten auswirken, und Vorschläge zur Diagnose von COM+-Fehlern.



| Thema                                                                                           | BESCHREIBUNG                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Strategien zur Behandlung von Fehlern in COM+](strategies-for-handling-errors-in-com-.md)<br/> | Listet die grundlegenden Richtlinien für die Behandlung von Fehlern in COM+ auf, einschließlich der Verwendung von HRESULTs und [**ErrorInfo-Sammlungen.**](errorinfo.md)<br/> |
| [Ändern von Rückgabewerten durch COM+](how-com--modifies-return-values.md)<br/>               | Identifiziert die einzelne Bedingung, in der COM+ ein Standard-HRESULT in einen COM+-Fehlercode konvertiert, bevor es an den Aufrufer zurückgegeben wird.<br/>             |
| [Fehlerisolation und Failfast-Richtlinie](fault-isolation-and-failfast-policy.md)<br/>       | Zeigt, wie sich die Fehlerisolation und die Failfast-Richtlinie auf das COM+-Verhalten auswirken.<br/>                                                                          |
| [Suchen der Fehlerquelle](finding-the-source-of-an-error.md)<br/>                 | Beschreibt, wie Sie die Quelle diagnostizieren und eine Beschreibung von Anwendungsfehlern abrufen können. <br/>                                                       |
| [Interpretieren von Fehlercodes](interpreting-error-codes.md)<br/>                             | Identifiziert den vorherrschenden Fehlerbehandlungsmechanismus für Microsoft Visual C++, die Java-Sprache und Microsoft Visual Basic. <br/>                    |
| [Problembehandlung](troubleshooting.md)<br/>                                               | Bietet zusätzliche Unterstützung bei der Fehlerdiagnose.<br/>                                                                                             |
| [Kontaktieren des Supports](contacting-support.md)<br/>                                         | Identifiziert wichtige Informationen zur Problemlösung, die Sie beim Kontaktieren des Supports angeben sollten.<br/>                                                     |



 

Ausführliche Informationen zur Behandlung von Fehlern im Zusammenhang mit verschiedenen COM+-Diensten finden Sie in den folgenden Abschnitten:

-   [Beschleunigen von Transaktionen durch Benachrichtigen des Stammobjekts](speeding-transactions-by-notifying-the-root-object.md)
-   [Behandeln von Fehlern](handling-errors-in-queued-components.md) (für Komponenten in der Warteschlange)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen von COM+-Anwendungen](debugging-com--applications.md)
</dt> </dl>

 

 




