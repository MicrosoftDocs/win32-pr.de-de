---
description: Problembehandlung
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Problembehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338911"
---
# <a name="troubleshooting"></a>Problembehandlung

Wenn Sie Probleme mit der Diagnose ihrer Anwendungsfehler haben, lesen Sie die folgenden Tipps zur Problembehandlung:

-   Stellen Sie sicher, dass die Distributed Transaction Coordinator (DTC) auf allen Servern ausgeführt wird.
-   Überprüfen Sie die Netzwerkkommunikation, indem Sie zunächst auf einem lokalen Computer testen, ob die Anwendung funktioniert. Wenn Sie TCP/IP im Netzwerk ausführen, können Sie mit dem ping.exe-Hilfsprogramm überprüfen, ob sich die Computer im Netzwerk befinden.
-   Stellen Sie sicher, dass sich SQL und DTC auf demselben Computer befinden oder dass das DTC-Client Konfigurationsprogramm angibt, dass sich der DTC auf einem anderen Computer befindet. Wenn dies nicht der Fall ist, gibt SQLCONNECT intern einen Fehler zurück, wenn er von einer Transaktions Komponente aufgerufen wird.
-   Legen Sie den Timeout Wert für die Transaktion auf eine höhere Zahl als die Standard-60 Sekunden fest. Nachdem das Transaktions Timeout abgelaufen ist, bricht com+ die Transaktion ab. Alle nachfolgenden Aufrufe der Komponente kehren sofort zurück, wobei der Kontext \_ E \_ abgebrochen wurde.
-   Stellen Sie sicher, dass die ODBC-Treiber Thread sicher sind und nicht über Thread Affinität verfügen.
-   Wenn Sie Schwierigkeiten haben, eine Anwendung auf mehrere Server zu überarbeiten, starten Sie den Client neu, und überprüfen Sie dann, ob der Domänen Controller ordnungsgemäß konfiguriert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehler Isolation und FailFast-Richtlinie](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Ermitteln der Fehlerquelle](finding-the-source-of-an-error.md)
</dt> <dt>

[Ändern der Rückgabewerte durch com+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretieren von Fehler Codes](interpreting-error-codes.md)
</dt> <dt>

[Strategien für die Behandlung von Fehlern in com+](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



