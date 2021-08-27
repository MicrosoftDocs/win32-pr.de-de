---
description: In diesem Abschnitt wird beschrieben, wie Sie aus einem nativen Windows-Programm drucken.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Vorgehensweise: Drucken aus einem Windows-Programm'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999f112285dfff389583b15f7c7c2913a3e125bc58713e2ba5f18973aa6e1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971339"
---
# <a name="how-to-print-from-a-windows-program"></a>Vorgehensweise: Drucken aus einem Windows-Programm

In diesem Abschnitt wird beschrieben, wie Sie aus einem nativen Windows-Programm drucken.

## <a name="overview"></a>Übersicht

Das Drucken ist in der Regel ein integraler Bestandteil eines nativen Windows-Programms. Daher ist es kein Feature, das Sie einfach hinzufügen können, nachdem Sie das Programm geschrieben haben. Wenn das Programm für die Verwendung von XPS-Dokumenten konzipiert ist, ist jedoch ggf. nicht viel zusätzlicher Code erforderlich, um den Dokumentinhalt zum Drucken zu rendern. Die XPS-Dokumente der Anwendung können direkt an einen Drucker mit einem XPSDrv-Druckertreiber gesendet werden.

Verwenden Sie die [XPS-Dokument-API,](/previous-versions/windows/desktop/dd316976(v=vs.85)) um den Dokumentinhalt zu erstellen, und die [XPS-Druck-API,](xps-printing.md) um den Dokumentinhalt an den Drucker zu senden. Die XPS-Druck-API verarbeitet den Dokumentinhalt für den Zieldrucker. Wenn der ausgewählte Drucker über einen XPSDrv-Druckertreiber verfügt, wird das Dokument ohne zusätzliche Konvertierung an den Drucker gesendet. Wenn der ausgewählte Drucker über einen GDI-basierten Druckertreiber verfügt, kann das Programm den Inhalt auch an den Drucker senden, und die XPS-Druck-API konvertiert den Dokumentinhalt so, dass er mit dem GDI-basierten Druckertreiber kompatibel ist. In beiden Fällen ist die Verarbeitung, die von der Anwendung ausgeführt wird, identisch.

## <a name="printing-tasks"></a>Druckaufgaben

In den folgenden Themen werden die grundlegenden Schritte zum Drucken von Programminhalten beschrieben.

1.  **Sammeln von Druckauftragsinformationen vom Benutzer.**

    In der Regel initiiert ein Benutzer einen Druckauftrag, wenn er die Druckoption in einem Menü auswählt und das Programm ein Druckdialogfeld anzeigt, um die Details des Druckauftrags zu erfassen. Der Benutzer wählt in der Regel den Drucker, die Anzahl der Kopien und Details zur Druckerkonfiguration aus, z. B. zweiseitiges Drucken und Stapling.

    Informationen dazu finden Sie unter [Vorgehensweise: Sammeln von Druckauftragsinformationen vom Benutzer](preparing-to-print.md).

2.  **Statusanzeige erstellen.**

    Ein Statusindikator gibt dem Benutzer Feedback zum Fortschritt des Druckauftrags. Die Statusanzeige kann eine Statusanzeige sein, die Teil eines Dialogfelds ist, das die Schaltfläche **Abbrechen** für den Auftrag enthält, oder eine Statusanzeige in der Statusleiste am unteren Rand des Hauptfensters.

    Informationen zur Funktionsweise der Statusanzeige finden Sie unter [Vorgehensweise: Anzeigen des Status des Druckauftrags.](cancel-dialog-box.md)

    Weitere Ideen zum Anzeigen des Status des Druckauftrags finden Sie in den Informationen in den Richtlinien für die Entwicklung der [Windows-Anwendungs-UI.](/windows/desktop/windows-application-ui-development)

3.  **Starten Sie den Druckthread.**

    Nachdem das Programm die Druckauftragsinformationen vom Benutzer gesammelt hat, kann es den Druckthread starten, um die eigentliche Verarbeitung des Dokuments zum Drucken durchzuführen.

    Informationen zum Druckthread finden Sie unter [Vorgehensweise: Starten und Beenden eines Druckthreads.](how-to--start-and-stop-a-printing-thread.md)

4.  **Rendern von Druckauftragsdaten.**

    Der Druckthread rendert die Dokumentdaten zum Drucken. Sie sollten diese Verarbeitung in diskrete Verarbeitungsschritte aufgliedern, damit der Benutzer die Verarbeitung unterbrechen und den Auftrag abbrechen kann und der Verarbeitungsthread nicht andere Threads und Prozesse blockieren darf.

    Informationen dazu, wie die Druckauftragsdaten rendert, finden Sie unter [Vorgehensweise: Rendern von Druckauftragsdaten.](how-to--render-the-print-job-data.md)

5.  **Überwachen sie den Status des Druckauftrags.**

    Wenn jeder Verarbeitungsschritt ausgeführt wird, aktualisieren Sie die Statusanzeige, um die Verwendung zu informieren. Berechnen Sie die Verarbeitungsschritte, um den angeforderten Auftrag abzuschließen, und aktualisieren Sie dann die Statusanzeige, während diese Schritte ausgeführt werden.

6.  **Schließen Sie den Druckauftrag, und beenden Sie den Druckthread.**

    Nachdem das Programm den Druckauftrag an den Drucker gesendet hat oder der Benutzer den Druckauftrag abgebrochen hat, müssen Sie den Druckauftrag schließen und die vom Druckauftrag verwendeten Ressourcen freigeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorgehensweise: Sammeln von Druckauftragsinformationen vom Benutzer](preparing-to-print.md)
</dt> </dl>

 

 
