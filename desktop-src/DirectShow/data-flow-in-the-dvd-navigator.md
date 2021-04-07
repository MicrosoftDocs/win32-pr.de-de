---
description: Datenfluss im DVD-Navigator
ms.assetid: 14f9cfa3-5ef6-419c-9196-2e4060549c03
title: Datenfluss im DVD-Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a981d2d7b528163abb53478e9e8f2ab88d46c0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747425"
---
# <a name="data-flow-in-the-dvd-navigator"></a>Datenfluss im DVD-Navigator

Der DVD-Navigator verfügt über Methoden zum Anhalten und Anhalten der Wiedergabe. Diese **Methoden sind** ähnlich –, aber nicht identisch – mit den Methoden zum **Anhalten und anhalten** in [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol). Dies ist der Unterschied zwischen den folgenden:

-   Die **IDvdControl2** -Methoden ändern, was der DVD-Navigator aus dem Datenträger liest. Der Status des Diagramms wird nicht geändert.
-   Die **IMediaControl** -Methoden ändern den Status des Diagramms. Sie ändern nicht, was der DVD-Navigator aus dem Datenträger liest. (Es gibt eine wichtige Ausnahme, die im nächsten Abschnitt erläutert wird, die sich auf die Methode " **Ende** " bezieht.)

Beispielsweise gibt [**IDvdControl2::P ause**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause) -Methode den Anhang J "Pause \_ on"-Befehl aus, hält aber nicht das Filter Diagramm an. Die [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause) -Methode hält dagegen das Diagramm an, gibt jedoch keinen DVD-Befehl aus.

Verwenden Sie im Allgemeinen die Methoden **IMediaControl::P ause** und **Ende** anstelle der entsprechenden **IDvdControl2** -Methoden. Die **IMediaControl** -Methoden weisen sehr kleine Wartezeiten auf, während die **IDvdControl2** -Methoden bis zu zwei Sekunden Wartezeit haben können.

Beenden der Wiedergabe

Das Verhalten von [**IMediaControl:: Beendigung**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) hängt von einem Flag ab, das Sie mit der [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) -Methode festlegen können.

-   Wenn das DVD \_ -resetonstopp-Flag **false** ist, wird das Diagramm von **IMediaControl:: Stopp** beendet, aber die Domäne des DVD-Navigators wird nicht geändert. Wenn Sie erneut ausführen, wird die Wiedergabe von der aktuellen Position aus fortgesetzt.
-   Wenn die DVD- \_ reseetonstopps **true** ist, wird der DVD-Navigator von **IMediaControl:: Beendigung** zurückgesetzt. Wenn Sie [**IMediaControl:: Run erneut ausführen**](/windows/desktop/api/Control/nf-control-imediacontrol-run) , wird der DVD-Navigator von der ersten Wiedergabe Domäne abgespielt, als ob Sie die DVD zum ersten Mal eingefügt haben.

Das \_ Flag für die DVD resetonstoppist standardmäßig auf " **true** " gesetzt, um die Kompatibilität mit älteren Anwendungen zu Im Allgemeinen sollten Sie jedoch die Standardeinstellung überschreiben und das-Flag auf **false** festlegen. Der Grund dafür ist, dass bestimmte Ereignisse bewirken können, dass das Diagramm während der Wiedergabe angehalten wird. Wenn sich beispielsweise die Bildschirmauflösung ändert, wird das Filter Diagramm angehalten, der Videorenderer erneut verbunden und neu gestartet. Wenn \_ die DVD resetonstopps den Wert **true** hat, wird die Wiedergabe am Anfang der Festplatte neu gestartet. Das ist wahrscheinlich nicht das, was der Benutzer erwartet.

Starten Sie daher am Anfang der Anwendung " **SetOption** ", wobei DVD \_ resetonstoppauf **false** festgelegt ist. Wenn Sie die Wiedergabe wieder aufnehmen möchten und Sie am gleichen Speicherort fortsetzen möchten, nennen Sie **IMediaControl:: stoppoder** **IMediaControl::P ause**. Wenn Sie die Wiedergabe und den Datenträger wiederherstellen möchten, geben Sie **SetOption** mit DVD \_ resetonstopps gleich **true** ein, und klicken Sie dann auf **IMediaControl:: Ende**, und wählen Sie schließlich **SetOption** erneut aus, und setzen \_ Sie DVD resetonstoppauf **false** zurück.

Anhalten der Wiedergabe

Wenn Sie dem DVD-Navigator einen Befehl zur Verfügung stellen, während das Diagramm angehalten wird, wird der Befehl möglicherweise erst beendet, wenn das Diagramm erneut ausgeführt wird. In einigen Fällen kann dies zu einem Deadlock in der Anwendung führen. Es gibt zwei Regeln, die Sie befolgen sollten, um Deadlocks zu vermeiden:

-   Geben Sie bei angehaltenen Ausführung nicht mehr als einen asynchronen DVD-Befehl aus.
-   Blockieren Sie den UI-Thread der Anwendung oder den Thread, der den Status des Diagramms ändert, nicht, wenn der Thread angehalten wurde.

Die zweite Regel sollte genauer geprüft werden. Im folgenden finden Sie einige spezifische Szenarien, die möglicherweise einen Deadlock verursachen:

-   **Szenario**: während der angehaltenen Anwendung gibt die Anwendung einen DVD-Befehl mit dem blockierflag aus. Dies kann zu einem Deadlock führen, wenn der Thread, der den DVD-Befehl ausgibt, derselbe Thread ist, der den Befehl "Run" ausgibt. Der DVD-Befehl blockiert, bis das Diagramm ausgeführt wird, aber das Diagramm kann erst ausgeführt werden, wenn der Befehl abgeschlossen ist.

    **Empfehlung**: Geben Sie den DVD-Befehl in einem separaten Arbeits Thread aus, oder verwenden Sie das blockierflag nicht.

-   **Szenario**: bei angehaltenen Anwendungen gibt die Anwendung einen DVD-Befehl aus und ruft dann [**idvdcmd:: waitforend**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) für das Command-Objekt auf. Diese Situation entspricht dem vorherigen Beispiel. Wenn Sie **Wait** aus dem UI-Thread aufzurufen, kann der UI-Thread das Diagramm erst ausführen, wenn die **Wait** - **Methode die** Blockierung aufhebt, die Blockierung allerdings erst, wenn das Diagramm ausgeführt wird.

    **Empfehlung**: **warten** Sie auf einen Arbeits Thread.

-   **Szenario**: während das Diagramm ausgeführt wird, gibt die Anwendung einen DVD-Befehl mit dem blockierflag aus und ruft dann die Pause von einem anderen Thread auf. Dies ist eine mögliche Racebedingung, da das Diagramm angehalten werden kann, bevor der Befehl ausgegeben wird. Wenn einer der beiden Threads der UI-Thread ist, können Sie einen Deadlock ähnlich den beiden vorherigen Beispielen auslösen. Dieses Beispiel veranschaulicht die Wichtigkeit beim Schreiben von Thread sicherem Code, wenn Ihre Anwendung mehrere Threads verwendet.

    **Empfehlung**: Wenn Sie Arbeitsthreads verwenden, stellen Sie sicher, dass der Code Thread sicher ist.

-   **Szenario**: bei angehaltenen Anwendung deaktiviert die Anwendung den Befehl "Run" von der Benutzeroberfläche und gibt dann einen asynchronen DVD-Befehl aus. Bei diesem Fall handelt es sich nicht unbedingt um einen Deadlock, da der Anwendungs Thread noch ausgeführt wird. Der Benutzer kann das Diagramm jedoch nicht ausführen, und der Befehl wird daher nie ausgeführt.

    **Empfehlung**: Wenn Sie anhalten, lassen Sie den Befehl "Run" immer aktiviert.

Suchen einer DVD zu einem bestimmten Zeitpunkt

Um auf einer Festplatte genau zu einem bestimmten Zeitpunkt zu suchen, nennen Sie [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run). Geben Sie dann [**IDvdControl2::P layattime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)an, und geben Sie dabei die Zeit und das Festlegen von *dwFlags* auf das \_ Flush-cmd- \_ Flag an \_

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



