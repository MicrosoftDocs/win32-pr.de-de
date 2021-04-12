---
description: Komponenten Warteschlangen
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Komponenten Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393053"
---
# <a name="activating-component-queues"></a>Komponenten Warteschlangen

Durch das Ausführen von Methoden aufrufen für eine in der Warteschlange befindliche Komponente wird die Methode nicht direkt ausgeführt. Stattdessen [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshallt und speichert Methodenaufrufe und Parameter in einer Warteschlange, in der Sie später von der in der Warteschlange befindlichen Komponente abgerufen und ausgeführt werden. Im Gegensatz zum Aktivieren eines Remote-DCOM-Objekts wird die in der Warteschlange befindliche Komponente nicht instanziiert, wenn eine-Methode aufgerufen wird. Dies ist die grundlegende Idee der Verwendung von in der Warteschlange befindlichen Komponenten – in der Warteschlange befindliche Komponenten müssen nicht gleichzeitig mit der aufrufenden Anwendung instanziiert werden.

> [!Note]  
> In den Beschreibungen zum Aktivieren einer Anwendung in der Warteschlange wird davon ausgegangen, dass die Anwendung als in die Warteschlange eingereiht und das Kontrollkästchen Listener aktiviert ist.

 

Sie können Skripts verwenden, um eine Anwendung in der Warteschlange zu starten und zu starten. Sie können das Skript unter dem Steuerelement des Aufgaben Planers ablegen, um es bei Bedarf auszuführen. Beispielsweise kann das Skript bei einem Systemneustart ausgeführt werden, wenn die Anwendungen dauerhaft verfügbar sein sollen. Wenn die Anwendung Transaktionen im Batch Modus verarbeiten soll, kann das Skript zu einem bestimmten Zeitpunkt in Verbindung mit einem Skript zum Herunterfahren ausgeführt werden, um sicherzustellen, dass die Batch Verarbeitung zu einem bestimmten Zeitpunkt beendet wird.

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Führen Sie die folgenden Schritte aus, um eine Anwendung in der Warteschlange zu starten:

1.  Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Anwendung, deren Warteschlange Sie aktivieren möchten.

3.  Klicken Sie auf **Start**.

## <a name="visual-basic"></a>Visual Basic

Weitere Informationen finden Sie im Beispiel comadmincatalog. startapplikation.

## <a name="cc"></a>C/C++

Weitere Informationen finden Sie im Beispiel [**icomadmincatalog:: startapplikation**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Warteschlangen Monikers](using-the-queue-moniker.md)
</dt> </dl>

 

 



