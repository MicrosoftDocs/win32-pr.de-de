---
description: In diesem Abschnitt wird beschrieben, wie Sie aus einem systemeigenen Windows-Programm drucken.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Gewusst wie: Drucken von einem Windows-Programm'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349686"
---
# <a name="how-to-print-from-a-windows-program"></a>Gewusst wie: Drucken von einem Windows-Programm

In diesem Abschnitt wird beschrieben, wie Sie aus einem systemeigenen Windows-Programm drucken.

## <a name="overview"></a>Übersicht

Der Druckvorgang ist in der Regel ein wesentlicher Bestandteil eines nativen Windows-Programms. Daher ist es kein Feature, das Sie nach dem Schreiben des Programms problemlos hinzufügen können. Das heißt, wenn das Programm für die Verwendung von XPS-Dokumenten konzipiert ist, benötigen Sie ggf. zusätzlichen Code, um den Dokumentinhalt für den Druck zu rendieren. Die XPS-Dokumente der Anwendung können direkt an einen Drucker gesendet werden, der über einen XPSDrv-Druckertreiber verfügt.

Verwenden Sie die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) , um den Dokumentinhalt und die [XPS-Druck-API](xps-printing.md) zu erstellen, um den Dokumentinhalt an den Drucker zu senden. Die XPS-Druck-API verarbeitet den Dokumentinhalt für den Ziel Drucker. Wenn der ausgewählte Drucker über einen XPSDrv-Druckertreiber verfügt, wird das Dokument ohne zusätzliche Konvertierung an den Drucker gesendet. Wenn der ausgewählte Drucker über einen GDI-basierten Druckertreiber verfügt, kann das Programm den Inhalt auch an den Drucker senden, und die XPS-Druck-API konvertiert den Dokumentinhalt so, dass er mit dem GDI-basierten Druckertreiber kompatibel ist. In beiden Fällen ist die Verarbeitung, die die Anwendung ausführt, identisch.

## <a name="printing-tasks"></a>Drucken von Aufgaben

In den folgenden Themen werden die grundlegenden Schritte zum Drucken von Programminhalten beschrieben.

1.  **Sammeln von Druckauftrags Informationen vom Benutzer.**

    In der Regel initiiert ein Benutzer einen Druckauftrag, wenn die Option Drucken in einem Menü ausgewählt wird, und das Programm zeigt ein Druck Dialogfeld an, in dem die Details des Druckauftrags erfasst werden. Der Benutzer wählt in der Regel den Drucker, die Anzahl der Kopien und die Drucker Konfigurationsdetails aus, z. b. zweiseitiges Drucken und Heften.

    Weitere Informationen hierzu finden Sie unter Gewusst [wie: Sammeln von Druckauftrags Informationen vom Benutzer](preparing-to-print.md).

2.  **Statusanzeige erstellen.**

    Eine Statusanzeige bietet dem Benutzer Feedback darüber, wie der Druckauftrag fortgesetzt wird. Die Statusanzeige kann eine Statusanzeige sein, die Teil eines Dialog Felds ist, das die Schaltfläche **Abbrechen** für den Auftrag enthält, oder es kann sich um eine Statusleiste in der Statusleiste am unteren Rand des Hauptfensters handeln.

    Weitere Informationen zur Funktions Anzeige finden Sie unter Gewusst [wie: Anzeigen des Status des Druckauftrags](cancel-dialog-box.md).

    Weitere Ideen zum Anzeigen des Status des Druckauftrags finden Sie in den Informationen in den Entwicklungs Richtlinien für die [Windows-Anwendungs Benutzeroberfläche](/windows/desktop/windows-application-ui-development) .

3.  **Starten Sie den Druck Thread.**

    Nachdem das Programm die Druckauftrags Informationen vom Benutzer gesammelt hat, kann es den Druck Thread starten, um die tatsächliche Verarbeitung des Dokuments zum Drucken auszuführen.

    Weitere Informationen zum Druck Thread finden Sie unter Gewusst [wie: starten und Abbrechen eines Druck Threads](how-to--start-and-stop-a-printing-thread.md).

4.  **Renderdruck Auftragsdaten.**

    Der Druck Thread rendert die Dokument Daten zum Drucken. Sie sollten diese Verarbeitung in diskrete Verarbeitungsschritte unterbrechen, damit der Benutzer die Verarbeitung unterbrechen und den Auftrag abbrechen und den Verarbeitungs Thread nicht zulassen kann, um andere Threads und Prozesse zu blockieren.

    Informationen dazu, wie die Druckauftrags Daten rendert, finden [Sie unter Gewusst wie: Rendern von Druckauftrags Daten](how-to--render-the-print-job-data.md).

5.  **Überwachen des Status des Druckauftrags.**

    Aktualisieren Sie die Statusanzeige, wenn jeder Verarbeitungsschritt ausgeführt wird, um die Verwendung zu informieren. Berechnen Sie die Verarbeitungsschritte, um den angeforderten Auftrag abzuschließen, und aktualisieren Sie dann die Statusanzeige, wenn diese Schritte ausgeführt werden.

6.  **Druckauftrag schließen und Druck Thread beenden.**

    Nachdem das Programm den Druckauftrag an den Drucker gesendet hat, oder wenn der Benutzer den Druckauftrag abgebrochen hat, müssen Sie den Druckauftrag schließen und die vom Druckauftrag verwendeten Ressourcen freigeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gewusst wie: Sammeln von Druckauftrags Informationen vom Benutzer](preparing-to-print.md)
</dt> </dl>

 

 
