---
description: Wenn Sie noch nicht mit digitalen Medien vertraut sind, werden in diesem Thema einige Konzepte vorgestellt, die Sie vor dem Schreiben einer Media Foundation Anwendung verstehen müssen.
ms.assetid: d76d655e-23f3-407c-97a1-be015b0de37d
title: 'Media Foundation: Grundlegende Konzepte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 825e84b3c7ad3060cae0a2530bc9a7af3155fd9113c490ce2c42f69771c1f9b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357262"
---
# <a name="media-foundation-essential-concepts"></a>Media Foundation: Grundlegende Konzepte

Wenn Sie noch nicht mit digitalen Medien vertraut sind, werden in diesem Thema einige Konzepte vorgestellt, die Sie vor dem Schreiben einer Media Foundation Anwendung verstehen müssen.

-   [Streams](#streams)
-   [Komprimierung](#compression)
-   [Mediencontainer](#media-containers)
-   [Formate](#formats)
-   [Zugehörige Themen](#related-topics)

## <a name="streams"></a>Datenströme

Ein *Stream* ist eine Sequenz von Mediendaten mit einem einheitlichen Typ. Die gängigsten Typen sind Audio und Video, aber ein Stream kann fast jede Art von Daten enthalten, einschließlich Text, Skriptbefehle und Stillbilder. Der Begriff *Stream* in dieser Dokumentation impliziert keine Übermittlung über ein Netzwerk. Eine Mediendatei, die für die lokale Wiedergabe vorgesehen ist, enthält auch Streams.

In der Regel enthält eine Mediendatei entweder einen einzelnen Audiostream oder genau einen Videostream und einen Audiostream. Eine Mediendatei kann jedoch mehrere Streams desselben Typs enthalten. Beispielsweise kann eine Videodatei Audiostreams in mehreren verschiedenen Sprachen enthalten. Zur Laufzeit wählt die Anwendung den zu verwendenden Stream aus.

## <a name="compression"></a>Komprimierung

*Komprimierung* bezieht sich auf jeden Prozess, der die Größe eines Datenstroms reduziert, indem redundante Informationen entfernt werden. Komprimierungsalgorithmen lassen sich in zwei allgemeine Kategorien unterteilen:

-   *Verlustfreie* Komprimierung. Mithilfe eines verlustfreien Algorithmus sind die rekonstruierten Daten identisch mit dem originalen Algorithmus.
-   *Verlustkomprimierung.* Bei Verwendung eines Verlustalgorithmus sind die rekonstruierten Daten eine Näherung des Originals, aber keine genaue Übereinstimmung.

In den meisten anderen Domänen ist die Verlustkomprimierung nicht akzeptabel. (Imagine eine "Näherung" einer Kalkulationstabelle zurückerstehen!) Aber verlustbetonte Komprimierungsschemas eignen sich aus mehreren Gründen gut für Audio und Video.

Der erste Grund liegt in der Physik der menschlichen Wahrnehmung. Wenn wir auf einen komplexen Sound lauschen, z. B. eine Musikaufzeichnung, sind einige der in diesem Sound enthaltenen Informationen für das Gehör nicht wahrnehmbar. Mithilfe der Signalverarbeitungsthematik ist es möglich, die Häufigkeiten zu analysieren und zu trennen, die nicht wahrgenommen werden können. Diese Häufigkeiten können ohne wahrnehmbare Auswirkung entfernt werden. Obwohl das rekonstruierte Audio nicht genau mit dem Original übereinstimmt, wird es für den Listener identisch *klingen.* Ähnliche Prinzipien gelten für Videos.

Zweitens kann eine Beeinträchtigung der Ton- oder Bildqualität je nach beabsichtigtem Zweck akzeptabel sein. Bei der Telefonie ist beispielsweise Audio häufig stark komprimiert. Das Ergebnis ist gut genug für eine Telefonkonversation, aber Sie möchten nicht über ein Telefon auf ein Orchestra lauschen.

Die Komprimierung wird auch als *Codierung* bezeichnet, und ein Gerät, das codiert, wird als *Encoder* bezeichnet. Der umgekehrte Prozess *decodiert*, und das Gerät ist ein natürlich als *Decoder* bezeichneter . Der allgemeine Begriff für Encoder und Decoder ist *Codec*. Codecs können in Hardware oder Software implementiert werden.

Die Komprimierungstechnologie hat sich seit der Einführung digitaler Medien schnell geändert, und heutzutage wird eine große Anzahl von Komprimierungsschemas verwendet. Dies ist eine der größten Herausforderungen bei der Programmierung digitaler Medien.

## <a name="media-containers"></a>Mediencontainer

Es ist selten, einen unformatierten Audio- oder Videodatenstrom als Computerdatei zu speichern oder direkt über das Netzwerk zu senden. Zum einen wäre es unmöglich, einen solchen Stream zu decodieren, ohne im Voraus zu wissen, welcher Codec verwendet werden soll. Daher enthalten Mediendateien in der Regel mindestens einige der folgenden Elemente:

-   Dateiheader, die die Anzahl der Datenströme, das Format jedes Streams usw. beschreiben.
-   Ein Index, der zufälligen Zugriff auf den Inhalt ermöglicht.
-   Metadaten, die den Inhalt beschreiben (z. B. den Interpreten oder Titel).
-   Paketheader, um die Netzwerkübertragung oder den zufälligen Zugriff zu ermöglichen.

In dieser Dokumentation wird der Begriff *Container* verwendet, um das gesamte Paket von Streams, Headern, Indizes, Metadaten usw. zu beschreiben. Der Grund für die Verwendung des *Begriffs Container* anstelle von *Datei* ist, dass einige Containerformate für Liveübertragungen konzipiert sind. Eine Anwendung könnte den Container in Echtzeit generieren, ohne ihn in einer Datei zu speichern.

Ein frühes Beispiel für einen Mediencontainer ist das AVI-Dateiformat. Weitere Beispiele sind MP4 und Advanced Systems Format (ASF). Container können anhand der Dateinamenerweiterung (z. B. .mp4) oder des MIME-Typs identifiziert werden.

Das folgende Diagramm zeigt eine typische Struktur für einen Mediencontainer. Das Diagramm stellt kein bestimmtes Format dar. Die Details der einzelnen Formate variieren stark.

![Diagramm eines typischen Mediencontainers](images/concepts01.png)

Beachten Sie, dass die im Diagramm dargestellte Struktur hierarchisch ist und Headerinformationen am Anfang des Containers angezeigt werden. Diese Struktur ist typisch für viele (aber nicht alle) Containerformate. Beachten Sie auch, dass der Datenabschnitt verschachtelte Audio- und Videopakete enthält. Diese Art der Überlappung ist in Mediencontainern üblich.

Der Begriff *Multiplexing* bezieht sich auf den Prozess der Paketisierung der Audio- und Videostreams und der Verschachtelung der Pakete in den Container. Der umgekehrte Prozess, bei dem die Datenströme aus den paketisierten Daten neu zusammengesetzt werden, wird als *demultiplexing* bezeichnet.

## <a name="formats"></a>Formate

In digitalen Medien ist der Begriff *Format* mehrdeutig. Ein Format kann auf den Typ der *Codierung* verweisen, z.B. H.264-Video oder den *Container*, z.B. MP4. Diese Unterscheidung ist für gewöhnliche Benutzer oft verwirrend. Die Namen, die Medienformaten gegeben werden, sind nicht immer hilfreich. Beispielsweise bezieht sich *MP3* sowohl auf ein Codierungsformat (MPEG-1 Audio Layer 3) als auch auf ein Dateiformat.

Die Unterscheidung ist jedoch wichtig, da das Lesen einer Mediendatei tatsächlich zwei Phasen umfasst:

1.  Zunächst muss der Container analysiert werden. In den meisten Fällen können die Anzahl der Datenströme und das Format der einzelnen Datenströme erst bekannt sein, wenn dieser Schritt abgeschlossen ist.
2.  Wenn die Streams komprimiert werden, müssen sie als Nächstes mit den entsprechenden Decodern decodiert werden.

Diese Tatsache führt ganz natürlich zu einem Softwareentwurf, bei dem separate Komponenten zum Analysieren von Containern und Decodieren von Streams verwendet werden. Darüber hinaus eignet sich dieser Ansatz für ein Plug-In-Modell, sodass Dritte ihre eigenen Parser und Codecs bereitstellen können. Auf Windows bietet der Component Object Model (COM) eine Standard-Möglichkeit, eine API von ihrer Implementierung zu trennen. Dies ist eine Voraussetzung für jedes Plug-In-Modell. Aus diesem Grund (unter anderem) verwendet Media Foundation COM-Schnittstellen.

Das folgende Diagramm zeigt die Komponenten, die zum Lesen einer Mediendatei verwendet werden:

![Diagramm mit den Komponenten zum Lesen einer Mediendatei](images/concepts02.png)

Das Schreiben einer Mediendatei erfordert außerdem zwei Schritte:

1.  Codieren der nicht komprimierten Audio-/Videodaten.
2.  Legen Sie die komprimierten Daten in einem bestimmten Containerformat ab.

Das folgende Diagramm zeigt die Komponenten, die zum Schreiben einer Mediendatei verwendet werden:

![Diagramm, das die Komponenten zum Schreiben einer Mediendatei zeigt.](images/concepts03.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Programmierhandbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 



