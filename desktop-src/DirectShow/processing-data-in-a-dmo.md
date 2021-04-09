---
description: Verarbeiten von Daten in einem DMO
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: Verarbeiten von Daten in einem DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9f5d5d820dc1467c25f9d411d46a9c66935e8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860320"
---
# <a name="processing-data-in-a-dmo"></a>Verarbeiten von Daten in einem DMO

In diesem Abschnitt wird erläutert, wie ein Datenstrom mithilfe eines DMO verarbeitet wird. Die in diesem Abschnitt aufgeführten Schritte sind das Standardverhalten. Alle DMOS müssen die hier beschriebenen Methoden unterstützen. Diese Methoden verwenden separate Puffer für die Eingabe und die Ausgabe. Einige DMOS unterstützen auch die direkte Verarbeitung mithilfe eines einzelnen Puffers. Weitere Informationen zur direkten Verarbeitung finden Sie unter direkte [Verarbeitung](in-place-processing.md).

**Puffer werden zugewiesen.**

Der Client ist für die gesamte Puffer Zuordnung verantwortlich. Nachdem Sie die Medientypen im DMO festgelegt haben, Fragen Sie den DMO nach den Puffer Anforderungen jedes Streams ab. Diese können je nach Medientyp geändert werden. Für jeden Stream wird die [**imediaobject:: getinputsizeinfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) -Methode oder die [**imediaobject:: getoutputsizeinfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) -Methode aufgerufen. Diese Methoden geben die folgenden Informationen zurück:

-   Minimale Puffergröße in Bytes.
-   Ausrichtungs Anforderungen, falls vorhanden. Ein Puffer wird ausgerichtet, wenn die Startadresse ein Vielfaches einer angegebenen ganzen Zahl ist.
-   Die maximale Datenmenge, die das DMO für Lookahead hält. Diese Zahl gilt nur für Eingabestreams. Für einige Arten von Daten (z. b. MPEG-Codierung) muss ein DMO möglicherweise im Stream nach vorn suchen. Der lookaheadwert gibt an, wie viele Eingabedaten der DMO benötigt, bevor eine Ausgabe erstellt werden kann.

Der Client muss Puffer zuordnen, die diesen Anforderungen entsprechen. Darüber hinaus kann der DMO Anforderungen darüber haben, wie der Client die Eingabedaten verpackt. Der DMO könnte z. b. erfordern, dass jeder Puffer genau ein Beispiel (oder einen Video Frame) enthält. Um diese Anforderungen zu ermitteln, müssen Sie die [**imediaobject:: getinputstreaminfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) -Methode aufrufen. Die [**imediaobject:: getoutputstreaminfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) -Methode gibt ähnliche Informationen über einen Ausgabestream zurück.

Im standardstreamingmodell übergibt der Client keine rohpuffer Zeiger an den DMO. Stattdessen wird ein Lightweight com-Objekt verwendet, das die [**imediabuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) -Schnittstelle verfügbar macht. Die **imediabuffer** -Schnittstelle fungiert als COM-Wrapper für einen Speicherblock. Da es sich um ein COM-Objekt handelt, wird die Verweis Zählung unterstützt, wodurch sichergestellt wird, dass Puffer nicht freigegeben werden, während Sie noch verwendet werden.

> [!Note]  
> Die **imediabuffer** -Schnittstelle stellt eine Funktion ähnlich der **imediasample** -Schnittstelle in DirectShow dar.

 

Der Client muss das **imediabuffer** -Objekt implementieren. Weitere Informationen finden Sie unter [Implementieren von imediabuffer](implementing-imediabuffer.md).

**Verarbeiten der Daten**

Gehen Sie zum Verarbeiten von Daten wie folgt vor:

1.  Füllen Sie für jeden Eingabedaten Strom einen Puffer mit Eingabedaten aus.
2.  Aufrufen von [**imediaobject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) , um jeden Puffer zu übermitteln.
3.  Nennen Sie [**imediaobject::P rocess Output**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) , um die Daten zu verarbeiten. Diese Methode nimmt für jeden Ausgabestream ein Array von Puffern an.
4.  Wiederholen Sie den Vorgang, bis keine weiteren Eingabedaten vorhanden sind.

Die **ProcessInput** -Methode akzeptiert Eingaben für einen Stream gleichzeitig. In der Regel gibt die Methode sofort zurück, und der DMO enthält einen Verweis Zähler für das **imediabuffer** -Objekt. Das Objekt wird freigegeben, nachdem alle Daten im Puffer verarbeitet wurden, oder wenn die Anwendung den DMO leert. Verwenden Sie den Puffer erst wieder, wenn er vom DMO freigegeben wurde. Um zu ermitteln, ob ein Eingabedaten Strom mehr Daten akzeptieren kann, müssen Sie die [**imediaobject:: getinputstatus**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) -Methode aufrufen. Diese Methode gibt das DMO- \_ Eingabe- \_ statusf \_ Accept Data-Flag zurück, \_ Wenn der Stream mehr Eingaben akzeptieren kann.

Die **ProcessOutput** -Methode generiert die Ausgabe für alle Ausgabedaten Ströme gleichzeitig. Die Anwendung übergibt ein Array von [**DMO- \_ Ausgabe \_ Daten \_ Puffer**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) Strukturen, eines für jeden Ausgabestream. Jede Struktur im Array verfügt über einen Zeiger auf ein **imediabuffer** -Objekt. Der DMO schreibt so viele Ausgabedaten wie möglich in die Puffer. Außerdem werden verschiedene Flags festgelegt, um den Status des Vorgangs zu melden. Das Flag DMO- \_ ausgabedatenbufferf \_ \_ \_ unvollständig gibt an, dass der DMO eine höhere Ausgabe der vorhandenen Eingabe verursachen kann. In diesem Fall kann der Client **ProcessOutput** erneut aufzurufen. Andernfalls sollte **ProcessInput** mit weiteren Eingabedaten aufgerufen werden. Der DMO ändert die Daten in den Eingabe Puffern nie. Er schreibt nur in die Ausgabepuffer.

Nachdem Sie alle Daten in einen Eingabestream übermittelt haben, können Sie die [**imediaobject::D iscontinuity**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) -Methode abrufen. Der DMO akzeptiert keine weiteren Eingaben für diesen Stream, bis Sie die verbleibende Ausgabe verarbeiten (oder den DMO leeren).

Zu jedem Zeitpunkt nach dem Start des Streamings kann der DMO Eingaben empfangen oder eine Ausgabe oder beides liefern. Daher gibt entweder **getinputstatus** die DMO- \_ Eingabe \_ statusf \_ Accept-Daten zurück \_ , oder **ProcessOutput** gibt die DMO- \_ Ausgabedaten- \_ \_ bufferf \_ unvollständig zurück. Die Anwendung speichert Datenfluss, indem Sie diese Flags testet und **ProcessInput** oder **ProcessOutput** entsprechend anfordert. Um den Datenfluss zu unterbrechen, müssen Sie die [**imediaobject:: Flush**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) -Methode abrufen. Diese Methode bewirkt, dass der DMO alle Puffer, die er intern hält, verwirft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direktes Hosting eines DMO](directly-hosting-a-dmo.md)
</dt> <dt>

[Direkte Verarbeitung](in-place-processing.md)
</dt> </dl>

 

 



