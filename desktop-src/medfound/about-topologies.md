---
description: Informationen zu Topologien
ms.assetid: 4f69b099-0ca7-4ea6-8412-0f1ea02e1600
title: Informationen zu Topologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9410207ed5f235f61e167564f7a5dee8a1367044032be0a15cef9ac3b95fb9e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975126"
---
# <a name="about-topologies"></a>Informationen zu Topologien

Eine Topologie ist ein Objekt, das darstellt, wie Daten in der Pipeline fließen. Eine Anwendung erstellt eine Topologie, um den Pfad zu beschreiben, den jeder Stream von der Medienquelle zu einer Mediensenke nimmt. Die Anwendung übergibt die Topologie an die Mediensitzung, und die Mediensitzung verwendet die Topologie, um den Datenfluss zu steuern.

Die Datenverarbeitungskomponenten in der Pipeline (Medienquellen, Transformationen und Mediensenken) werden in der Topologie als *Knoten* dargestellt. Der Datenfluss von einer Komponente zu einer anderen wird durch eine Verbindung zwischen den Knoten dargestellt. Die folgenden Knotentypen sind definiert:

-   Quellknoten: Stellt einen Medienstream auf einer Medienquelle dar.
-   Transformationsknoten: Stellt eine Media Foundation-Transformation (MFT) dar.
-   Ausgabeknoten: Stellt eine Streamsenke auf einer Mediensenke dar.
-   Tee-Knoten: Stellt eine Verzweigung im Stream dar. Tee-Knoten stellen eine Ausnahme von der Regel dar, dass ein Knoten ein Pipelineobjekt darstellt. Im Gegensatz zu anderen Knotentypen leitet der Tee-Knoten einfach den Datenfluss weiter.

Eine funktionierende Topologie muss mindestens einen Quellknoten enthalten, der mit einem Ausgabeknoten verbunden ist, möglicherweise über einen oder mehrere Transformationsknoten. Das folgende Diagramm zeigt beispielsweise eine einfache Topologie mit einem Stream.

![Ein Diagramm, das eine Topologie mit einem Datenstrom zeigt.](images/topology01.png)

Bei der Dateiwiedergabe kann der Transformationsknoten einen Decoder darstellen, und der Ausgabeknoten stellt den Audio- oder Videorenderer dar. Bei der Dateicodierung stellt der Transformationsknoten einen Encoder dar, und der Ausgabeknoten stellt eine Archivsenke dar, z. B. die ASF-Dateisenke.

Wenn zwei Knoten verbunden sind, wird der Knoten, der Daten erzeugt, als *Upstreamknoten* bezeichnet, und der Knoten, der Daten empfängt, wird als *Downstreamknoten* bezeichnet. Im vorherigen Diagramm befindet sich der Quellknoten beispielsweise vor dem Transformationsknoten.

In einem Paar verbundener Knoten wird der Verbindungspunkt auf dem Upstreamknoten als *Ausgabe* bezeichnet. Der Verbindungspunkt auf dem Downstreamknoten wird als *Eingabe* bezeichnet. Das folgende Diagramm zeigt ein Knotenpaar mit ihren Verbindungspunkten und den Datenfluss zwischen ihnen. Die Verbindungspunkte werden nicht als separate Objekte in der Topologie dargestellt. Sie werden durch den Indexwert für das Knotenobjekt angegeben.

![Ein Diagramm, das zwei verbundene Knoten zeigt.](images/topology04.png)

Ein Quellknoten darf keine Eingaben enthalten. Daher können von einem Quellknoten keine Upstreamknoten vorhanden sein. Ebenso kann ein Ausgabeknoten keine Ausgaben aufweisen, und es können keine Knoten nach einem Ausgabeknoten vorhanden sein. Eine Kette von Knoten von einem Quellknoten zu einem Ausgabeknoten wird als *Branch* der Topologie bezeichnet. Das erste Diagramm in diesem Thema zeigt eine Topologie mit einem einzelnen Branch. Im Allgemeinen gibt es einen Branch pro Stream. Zum Wiedergeben einer Datei mit einem Audiostream und einem Videostream ist beispielsweise eine Topologie mit zwei Verzweigungen erforderlich.

## <a name="partial-topologies"></a>Teiltopologien

Eine vollständige oder *vollständige* Topologie enthält einen Knoten für jedes erforderliche Pipelineobjekt. Die Anwendung muss jedoch nicht immer eine vollständige Topologie erstellen. Stattdessen wird eine *partielle* Topologie erstellt, die einen oder mehrere Transformationsknoten auslässt.

Die Mediensitzung schließt die Topologie mithilfe eines Objekts ab, das als *Topologieladeprogramm* bezeichnet wird. Das Topologieladeprogramm konvertiert Teiltopologien in vollständige Topologien, indem die erforderlichen Transformationen eingefügt werden. Der Konvertierungsprozess wird als *Auflösen* der Topologie bezeichnet.

Um beispielsweise einen codierten Audiostream wiederzugeben, muss die Topologie über einen Decoder zwischen dem Quell- und dem Ausgabeknoten verfügen. Die Anwendung erstellt eine Teiltopologie, die den Quellknoten direkt mit dem Ausgabeknoten ohne den Decoder verbindet. Das Topologieladeprogramm untersucht die Streamformate, findet den richtigen Decoder und fügt einen Transformationsknoten in die Topologie ein.

Das folgende Diagramm zeigt die partielle Topologie, die von der Anwendung erstellt wurde.

![Ein Diagramm, das einen Teil mit einem Quellknoten und einem Ausgabeknoten zeigt.](images/topology02.png)

Das nächste Diagramm zeigt die vollständige Topologie, nachdem sie vom Topologieladeprogramm aufgelöst wurde. In diesem Beispiel hat das Topologieladeprogramm einen Transformationsknoten für den Decoder eingefügt.

![Ein Diagramm, das eine vollständige Topologie zeigt.](images/topology03.png)

In der aktuellen Version von Media Foundation unterstützt das Topologieladeprogramm Topologien für die Wiedergabe. Für die Dateicodierung und andere Szenarien muss die Anwendung eine vollständige Topologie erstellen.

Anwendungen können auch das Topologieladeprogramm erstellen und direkt verwenden. Beispielsweise können Sie das Topologieladeprogramm verwenden, um eine Teiltopologie aufzulösen und dann die vollständige Topologie zu ändern, bevor Sie sie an die Mediensitzung weitergibt. Um das Topologieladeprogramm zu erstellen, rufen [**Sie MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topologien](topologies.md)
</dt> </dl>

 

 



