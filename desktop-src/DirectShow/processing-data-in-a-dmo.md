---
description: Verarbeiten von Daten in einem DMO
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: Verarbeiten von Daten in einem DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd4dd05df960bd27b34eb55b604c8469e7bbaedd57ea928f5b4f412ad4bff04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748240"
---
# <a name="processing-data-in-a-dmo"></a>Verarbeiten von Daten in einem DMO

In diesem Abschnitt wird erläutert, wie ein Datenstrom mithilfe eines DMO verarbeitet wird. Die in diesem Abschnitt aufgeführten Schritte sind das Standardverhalten. alle DMOs müssen die hier beschriebenen Methoden unterstützen. Diese Methoden verwenden separate Puffer für die Ein- und Ausgabe. Einige DMOs unterstützen auch die ortsbezogene Verarbeitung mit einem einzelnen Puffer. Weitere Informationen zur verarbeitungsbereiten Verarbeitung finden Sie unter [In-Place Processing](in-place-processing.md).

**Zuordnen von Puffern**

Der Client ist für die gesamte Pufferzuordnung verantwortlich. Nachdem Sie die Medientypen auf dem DMO festgelegt haben, fragen Sie die DMO für die Pufferanforderungen jedes Streams ab. Diese können sich je nach Medientyp ändern. Rufen Sie für jeden Stream die [**IMediaObject::GetInputSizeInfo-**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) oder [**IMediaObject::GetOutputSizeInfo-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) auf. Diese Methoden geben die folgenden Informationen zurück:

-   Minimale Puffergröße in Bytes.
-   Ausrichtungsanforderungen, falls vorhanden. Ein Puffer wird ausgerichtet, wenn die Startadresse ein Vielfaches einer angegebenen ganzen Zahl ist.
-   Die maximale Datenmenge, die der DMO für Lookahead speichern soll. Diese Zahl gilt nur für Eingabestreams. Für einige Arten von Daten (z. B. MPEG-Codierung) muss ein DMO möglicherweise im Stream nach vorne blicken. Der Lookaheadwert gibt an, wie viele Eingabedaten der DMO benötigt, bevor eine Ausgabe erzeugt werden kann.

Der Client muss Puffer zuordnen, die diesen Anforderungen entsprechen. Darüber hinaus kann der DMO Anforderungen darüber haben, wie der Client die Eingabedaten packt. Beispielsweise kann die DMO erfordern, dass jeder Puffer genau eine Stichprobe (oder einen Videoframe) enthält. Um diese Anforderungen zu bestimmen, rufen Sie die [**IMediaObject::GetInputStreamInfo-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) auf. Die [**IMediaObject::GetOutputStreamInfo-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) gibt ähnliche Informationen zu einem Ausgabestream zurück.

Im Standardstreamingmodell übergibt der Client keine rohen Pufferzeiger an die DMO. Stattdessen wird ein einfaches COM-Objekt verwendet, das die [**IMediaBuffer-Schnittstelle**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) verfügbar macht. Die **IMediaBuffer-Schnittstelle** fungiert als COM-Wrapper für einen Speicherblock. Da es sich um ein COM-Objekt handelt, unterstützt es die Verweiszählung, um sicherzustellen, dass Puffer nicht freigegeben werden, während sie noch verwendet werden.

> [!Note]  
> Die **IMediaBuffer-Schnittstelle** stellt eine Funktion bereit, die der **IMediaSample-Schnittstelle** in DirectShow ähnelt.

 

Der Client muss das **IMediaBuffer-Objekt** implementieren. Weitere Informationen finden Sie unter [Implementieren von IMediaBuffer.](implementing-imediabuffer.md)

**Verarbeiten der Daten**

Gehen Sie wie folgt vor, um Daten zu verarbeiten:

1.  Füllen Sie für jeden Eingabestream einen Puffer mit Eingabedaten aus.
2.  Rufen Sie [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) auf, um jeden Puffer zu übermitteln.
3.  Rufen Sie [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) auf, um die Daten zu verarbeiten. Diese Methode verwendet ein Array von Puffern, eines für jeden Ausgabestream.
4.  Wiederholen Sie den Vorgang, bis keine Eingabedaten mehr vorhanden sind.

Die **ProcessInput-Methode** akzeptiert Eingaben für jeweils einen Stream. In der Regel gibt die Methode sofort zurück, und die DMO enthält einen Verweiszähler für das **IMediaBuffer-Objekt.** Es gibt das -Objekt frei, nachdem alle Daten im Puffer verarbeitet wurden oder wenn die Anwendung die DMO leert. Verwenden Sie einen Puffer erst wieder, wenn der DMO ihn freigegeben hat. Um zu bestimmen, ob ein Eingabestream mehr Daten akzeptieren kann, rufen Sie die [**IMediaObject::GetInputStatus-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) auf. Diese Methode gibt das DMO \_ INPUT \_ STATUSF \_ ACCEPT \_ DATA-Flag zurück, wenn der Stream weitere Eingaben akzeptieren kann.

Die **ProcessOutput-Methode** generiert die Ausgabe für alle Ausgabestreams gleichzeitig. Die Anwendung übergibt ein Array von [**DMO \_ OUTPUT DATA \_ \_ BUFFER-Strukturen,**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) eine für jeden Ausgabestream. Jede Struktur im Array verfügt über einen Zeiger auf ein **IMediaBuffer-Objekt.** Der DMO schreibt so viele Ausgabedaten wie immer in die Puffer. Außerdem werden verschiedene Flags festgelegt, um den Status des Vorgangs zu melden. Das DMO \_ OUTPUT \_ DATA \_ BUFFERF \_ INCOMPLETE-Flag gibt an, dass die DMO mehr Ausgabe aus der vorhandenen Eingabe erzeugen kann. In diesem Fall kann der Client **ProcessOutput** erneut aufrufen. Andernfalls sollte **ProcessInput** mit weiteren Eingabedaten aufgerufen werden. Der DMO ändert nie die Daten in den Eingabepuffern. er schreibt nur in die Ausgabepuffer.

Nachdem Sie alle Daten an einen Eingabestream übermittelt haben, rufen Sie die [**IMediaObject::D iscontinuity-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) auf. Die DMO akzeptiert keine weiteren Eingaben in diesen Stream, bis Sie die verbleibende Ausgabe verarbeiten (oder die DMO leeren).

Zu jedem Zeitpunkt nach Beginn des Streamings kann der DMO Eingaben empfangen, Ausgaben erzeugen oder beides. Daher gibt **Entweder GetInputStatus** DMO \_ \_ EINGABESTATUSF \_ ACCEPT DATA oder \_ **ProcessOutput** DMO \_ OUTPUT DATA \_ \_ BUFFERF INCOMPLETE \_ zurück. Die Anwendung führt den Datenfluss durch, indem sie auf diese Flags testet und **ProcessInput** oder **ProcessOutput** entsprechend aufruft. Um den Datenfluss zu unterbrechen, rufen Sie die [**IMediaObject::Flush-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) auf. Diese Methode bewirkt, dass die DMO alle Puffer verwirft, die sie intern hält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direktes Hosten eines DMO](directly-hosting-a-dmo.md)
</dt> <dt>

[In-Place Processing](in-place-processing.md)
</dt> </dl>

 

 



