---
description: Informationen zu Topologien
ms.assetid: 4f69b099-0ca7-4ea6-8412-0f1ea02e1600
title: Informationen zu Topologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35008d839e8054554370039dd13297ae7a1f0b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567781"
---
# <a name="about-topologies"></a>Informationen zu Topologien

Eine Topologie ist ein Objekt, das die Art der Datenfluss in der Pipeline darstellt. Eine Anwendung erstellt eine Topologie, um den Pfad zu beschreiben, den jeder Stream von der Medienquelle an eine Medien Senke annimmt. Die Anwendung übergibt die Topologie an die Medien Sitzung, und die Medien Sitzung verwendet die Topologie, um den Datenfluss zu steuern.

Die Datenverarbeitungs Komponenten in der Pipeline (Medienquellen, Transformationen und Medien senken) werden in der Topologie als *Knoten* dargestellt. Der Datenfluss von einer Komponente zu einer anderen wird durch eine Verbindung zwischen den Knoten repräsentiert. Die folgenden Knoten Typen sind definiert:

-   Quellknoten: stellt einen Mediendaten Strom in einer Medienquelle dar.
-   Transformations Knoten: stellt eine Media Foundation Transformation (MFT) dar.
-   Ausgabe Knoten: stellt eine streamsenke für eine Medien Senke dar.
-   Tee-Knoten: stellt eine Verzweigung im Stream dar. Tee-Knoten stellen eine Ausnahme von der Regel dar, dass ein Knoten ein Pipeline Objekt darstellt. Im Gegensatz zu anderen Knoten Typen leitet der Tee-Knoten den Datenfluss einfach weiter.

Eine funktionierende Topologie muss mindestens einen Quellknoten enthalten, der mit einem Ausgabe Knoten verbunden ist, möglicherweise über einen oder mehrere Transformations Knoten. Das folgende Diagramm zeigt z. b. eine einfache Topologie mit einem Datenstrom.

![ein Diagramm, das eine Topologie mit einem Datenstrom anzeigt.](images/topology01.png)

Bei der Wiedergabe von Dateien stellt der Transformations Knoten möglicherweise einen Decoder dar, und der Ausgabe Knoten stellt den Audio-oder Videorenderer dar. Bei der Datei Codierung würde der Transformations Knoten einen Encoder darstellen, und der Ausgabe Knoten würde eine Archive-Senke darstellen, wie z. b. die ASF-Datei-Senke.

Wenn zwei Knoten verbunden sind, wird der Knoten *, der Daten* erzeugt, als upstreamknoten bezeichnet, und der Knoten, der Daten empfängt, wird als *Downstream* -Knoten bezeichnet. Beispielsweise ist im vorherigen Diagramm der Quellknoten vom Knoten transformieren.

In einem Paar verbundener Knoten wird der Verbindungspunkt auf dem upstreamknoten als *Ausgabe* bezeichnet. Der Verbindungspunkt auf dem Downstream-Knoten wird als *Eingabe* bezeichnet. Das folgende Diagramm zeigt ein Knoten Paar mit ihren Verbindungs Punkten und den Datenfluss zwischen Ihnen. Die Verbindungspunkte werden in der Topologie nicht als separate Objekte dargestellt. Sie werden durch den Indexwert für das Knoten Objekt angegeben.

![ein Diagramm, in dem zwei verbundene Knoten angezeigt werden.](images/topology04.png)

Ein Quellknoten darf keine Eingaben enthalten. Aus diesem Grund können keine Knoten von einem Quellknoten in den Upstream-upgrund vorhanden sein. Ebenso kann ein Ausgabe Knoten keine Ausgaben aufweisen, und es dürfen keine downstreamknoten von einem Ausgabe Knoten mehr vorhanden sein. Eine Kette von Knoten von einem Quellknoten zu einem Ausgabe Knoten wird als *Verzweigung* der Topologie bezeichnet. Das erste Diagramm in diesem Thema zeigt eine Topologie mit einer einzelnen Verzweigung. Im Allgemeinen ist ein Branch pro Stream vorhanden. Zum Abspielen einer Datei mit einem Audiostream und einem Videostream ist beispielsweise eine Topologie mit zwei Verzweigungen erforderlich.

## <a name="partial-topologies"></a>Partielle Topologien

Eine vollständige oder *voll* ständige Topologie enthält einen Knoten für jedes benötigte Pipeline Objekt. Allerdings muss die Anwendung nicht immer eine vollständige Topologie erstellen. Stattdessen wird eine *partielle* Topologie erstellt, in der ein oder mehrere Transformations Knoten ausgelassen werden.

Die Medien Sitzung schließt die Topologie mithilfe eines Objekts namens *topologielader* ab. Das topologielader konvertiert partielle Topologien in vollständige Topologien, indem die benötigten Transformationen eingefügt werden. Der Konvertierungs Vorgang wird als *Auflösen* der Topologie bezeichnet.

Um z. b. einen codierten Audiostream wiederzugeben, muss die Topologie über einen Decoder zwischen den Quell-und Ausgabe Knoten verfügen. Die Anwendung erstellt eine partielle Topologie, die den Quellknoten ohne den Decoder direkt mit dem Ausgabe Knoten verbindet. Das topologielader untersucht die Streamformate, sucht den richtigen Decoder und fügt einen Transformations Knoten in die Topologie ein.

Das folgende Diagramm zeigt die partielle Topologie, die von der Anwendung erstellt wurde.

![ein Diagramm, das eine partielle mit einem Quellknoten und einem Ausgabe Knoten anzeigt.](images/topology02.png)

Im nächsten Diagramm wird die vollständige Topologie angezeigt, nachdem Sie vom topologielader aufgelöst wurde. In diesem Beispiel hat der topologielader einen Transformations Knoten für den Decoder eingefügt.

![ein Diagramm, das eine vollständige Topologie anzeigt.](images/topology03.png)

In der aktuellen Version von Media Foundation unterstützt das topologielader Topologien für die Wiedergabe. Bei der Datei Codierung und anderen Szenarien muss die Anwendung eine vollständige Topologie erstellen.

Anwendungen können auch den topologielader erstellen und direkt verwenden. Beispielsweise können Sie mit dem topologielader eine partielle Topologie auflösen und dann die vollständige Topologie ändern, bevor Sie Sie an die Medien Sitzung weitergeben. Rufen Sie zum Erstellen des topologieladers [**mfkreatetopoloader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topologien](topologies.md)
</dt> </dl>

 

 



