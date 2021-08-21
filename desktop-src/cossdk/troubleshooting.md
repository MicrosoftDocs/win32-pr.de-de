---
description: Problembehandlung
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Problembehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e10877306dc17f0b04718037a4bc073c8a7ed7c7c4ac46b31cda90517d22b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812006"
---
# <a name="troubleshooting"></a>Problembehandlung

Wenn Sie Probleme bei der Diagnose Ihrer Anwendungsfehler haben, lesen Sie die folgenden Tipps zur Problembehandlung:

-   Stellen Sie sicher, dass Distributed Transaction Coordinator (DTC) auf allen Servern ausgeführt wird.
-   Überprüfen Sie die Netzwerkkommunikation, indem Sie zunächst auf einem lokalen Computer testen, um sicherzustellen, dass die Anwendung funktioniert. Wenn Sie TCP/IP in Ihrem Netzwerk ausführen, können Sie das Hilfsprogramm ping.exe verwenden, um zu überprüfen, ob sich die Computer im Netzwerk befinden.
-   Stellen Sie sicher, SQL und DTC sich auf demselben Computer befinden oder dass das DTC-Clientkonfigurationsprogramm angibt, dass sich der DTC auf einem anderen Computer befindet. Falls nicht, gibt SQLConnect intern einen Fehler zurück, wenn er von einer Transaktionskomponente aufgerufen wird.
-   Legen Sie das Transaktions-Time out auf eine höhere Zahl als die standardmäßigen 60 Sekunden fest. Nachdem das Transaktions-Time out abgelaufen ist, bricht COM+ die Transaktion ab. Alle nachfolgenden Aufrufe der Komponente geben sofort mit CONTEXT \_ E \_ ABORTED zurück.
-   Stellen Sie sicher, dass Ihre ODBC-Treiber threadsicher sind und keine Threadaffinität haben.
-   Wenn Sie Schwierigkeiten haben, eine Anwendung auf mehreren Servern zu verwenden, starten Sie den Client neu, und überprüfen Sie dann, ob Ihr Domänencontroller ordnungsgemäß konfiguriert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerisolation und Failfast-Richtlinie](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Suchen der Fehlerquelle](finding-the-source-of-an-error.md)
</dt> <dt>

[Ändern von Rückgabewerten durch COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretieren von Fehlercodes](interpreting-error-codes.md)
</dt> <dt>

[Strategien zum Behandeln von Fehlern in COM+](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



