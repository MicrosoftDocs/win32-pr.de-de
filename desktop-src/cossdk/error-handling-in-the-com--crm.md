---
description: Fehlerbehandlung in com+ CRM
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Fehlerbehandlung in com+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483451"
---
# <a name="error-handling-in-the-com-crm"></a>Fehlerbehandlung in com+ CRM

Com+-Server Anwendungen implementieren eine FailFast-Richtlinie. Wenn ein schwerwiegender interner Fehler erkannt wird, wird der Server Anwendungsprozess beendet und eine Fehlermeldung in das Windows-Ereignisprotokoll geschrieben. Dies ermöglicht eine schnelle Erkennung von Problemen und ist aufgrund des Schutzes von Anwendungsdaten durch die Transaktionsverarbeitung möglich. Überprüfen Sie im Windows-Ereignisprotokoll immer, ob während der Entwicklung oder während der letzten Bereitstellung Fehler aus dem CRM vorhanden sind.

Grundlegende Fehler bei der Verwendung von CRM-Schnittstellen, wie z. b. ungültige Argumente oder Sequenz Fehler (z. b. das Schreiben eines Protokolldaten Satzes vor der Registrierung des CRM-Compensators), geben Fehlercodes zurück und sollten FailFast nicht lösen. Bei der Entwicklung von CRM können Sie den Registrierungsschlüssel VTRACE1 festlegen (siehe [com+ CRM-Registrierungs Einstellungen](com--crm-registry-settings.md)), der bewirkt, dass im Debugger-Ausgabefenster für jeden Fehler eine Meldung angezeigt wird.

Vorübergehende Fehler können ebenfalls auftreten. Diese Fehler werden in der Regel durch Zeit Steuerungs Bedingungen verursacht und führen dazu, dass ein Fehlercode zurückgegeben wird. Der CRM-Entwickler sollte sicherstellen, dass diese Fehlerbedingungen behandelt werden. Beim Schreiben eines Protokolldaten Satzes könnte die Transaktion z. b. aufgrund eines Timeouts abgebrochen werden. Die-Methode gibt dann einen Fehler zurück, den der Aufrufer entsprechend überprüfen und behandeln soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



