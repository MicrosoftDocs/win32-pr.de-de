---
description: Der wichtigste Teil beim Schreiben von Komponenten besteht im Umgang mit möglichen Fehlern.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Behandeln von Fehlern in com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127793"
---
# <a name="handling-errors-in-com"></a>Behandeln von Fehlern in com+

Der wichtigste Teil beim Schreiben von Komponenten besteht im Umgang mit möglichen Fehlern. Der Versuch, herauszufinden, was schief gehen kann und was zu tun ist, kann unter den besten Bedingungen eine Herausforderung darstellen. Häufige Fehler, die von der Komponente überprüft und behandelt werden können, sind fehlerhafte Netzwerkverbindungen, Sicherheitsfehler und Fehler im Zusammenhang mit nicht erreichbaren Objekten.

Darüber hinaus können Sie eigene Fehlercodes entwickeln, um Schnittstellen spezifische Fehler zu melden, z. b. Wenn eine Geschäftsregel verletzt wurde.

In Übereinstimmung mit dem COM+-Programmiermodell kann ein Objekt (und häufig) Aufrufe von Schnittstellen Methoden für andere Objekte zum Ausführen von Arbeit ausführen. Da Programmierer Komponenten in verschiedenen Programmiersprachen schreiben können, erfordert com+, dass alle Fehler Behandlungs Mechanismen sprachneutral sind, z. b. HRESULTs-und [**errorInfo**](errorinfo.md) -Auflistungen.

Dieser Abschnitt enthält die in der folgenden Tabelle beschriebenen Themen, in denen Techniken zur Behandlung von Fehlern in com+-Anwendungen, Features in com+, die das Fehler Verhalten beeinflussen, und Vorschläge zur Diagnose von com+-Fehlern erörtert werden.



| Thema                                                                                           | BESCHREIBUNG                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Strategien für die Behandlung von Fehlern in com+](strategies-for-handling-errors-in-com-.md)<br/> | Listet und beschreibt die grundlegenden Richtlinien für die Behandlung von Fehlern in com+, einschließlich der Verwendung von HRESULTs-und [**errorInfo**](errorinfo.md) -Auflistungen.<br/> |
| [Ändern der Rückgabewerte durch com+](how-com--modifies-return-values.md)<br/>               | Identifiziert die einzige Bedingung, in der com+ ein HRESULT-Standard Objekt in einen com+-Fehlercode konvertiert, bevor es an den Aufrufer zurückgegeben wird.<br/>             |
| [Fehler Isolation und FailFast-Richtlinie](fault-isolation-and-failfast-policy.md)<br/>       | Zeigt, wie die Fehler Isolation und die FailFast-Richtlinie das com+-Verhalten beeinflussen.<br/>                                                                          |
| [Ermitteln der Fehlerquelle](finding-the-source-of-an-error.md)<br/>                 | Beschreibt, wie Sie die Quelle diagnostizieren und eine Beschreibung von Anwendungsfehlern abrufen können. <br/>                                                       |
| [Interpretieren von Fehler Codes](interpreting-error-codes.md)<br/>                             | Identifiziert den vorherrschenden Fehler Behandlungs Mechanismus für Microsoft Visual C++, die Java-Sprache und Microsoft Visual Basic. <br/>                    |
| [Problembehandlung](troubleshooting.md)<br/>                                               | Bietet zusätzliche Unterstützung bei der Diagnose von Fehlern.<br/>                                                                                             |
| [Kontaktieren des Supports](contacting-support.md)<br/>                                         | Identifiziert wichtige Informationen zur Problembehebung, die Sie beim Kontaktieren des Supports bereitstellen sollten.<br/>                                                     |



 

Ausführliche Informationen zur Behandlung von Fehlern, die mit verschiedenen COM+-Diensten verbunden sind, finden Sie in den folgenden Abschnitten:

-   [Beschleunigen von Transaktionen durch Benachrichtigen des root-Objekts](speeding-transactions-by-notifying-the-root-object.md)
-   [Behandeln von Fehlern](handling-errors-in-queued-components.md) (für in der Warteschlange befindliche Komponenten)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Anwendungen debuggen](debugging-com--applications.md)
</dt> </dl>

 

 




