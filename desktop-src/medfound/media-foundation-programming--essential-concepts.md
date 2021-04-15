---
description: Wenn Sie noch nicht mit digitalen Medien vertraut sind, finden Sie in diesem Thema einige Konzepte, die Sie kennen müssen, bevor Sie eine Media Foundation Anwendung schreiben.
ms.assetid: d76d655e-23f3-407c-97a1-be015b0de37d
title: 'Media Foundation: Grundlegende Konzepte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0298a20518df91dab4439770e0f1193802969ae8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104393842"
---
# <a name="media-foundation-essential-concepts"></a>Media Foundation: Grundlegende Konzepte

Wenn Sie noch nicht mit digitalen Medien vertraut sind, finden Sie in diesem Thema einige Konzepte, die Sie kennen müssen, bevor Sie eine Media Foundation Anwendung schreiben.

-   [Streams](#streams)
-   [Komprimierung](#compression)
-   [Medien Container](#media-containers)
-   [Formate](#formats)
-   [Zugehörige Themen](#related-topics)

## <a name="streams"></a>Datenströme

Ein Daten *Strom* ist eine Sequenz von Mediendaten mit einem einheitlichen Typ. Die gängigsten Typen sind auditon und Video, aber ein Datenstrom kann nahezu jede Art von Daten enthalten, einschließlich Text, Skript Befehlen und nach wie vor Bilder. Der Begriff *Stream* in dieser Dokumentation impliziert nicht die Übermittlung über ein Netzwerk. Eine für die lokale Wiedergabe vorgesehene Mediendatei enthält auch Streams.

Normalerweise enthält eine Mediendatei entweder einen einzelnen Audiostream oder genau einen Videostream und einen Audiostream. Eine Mediendatei kann jedoch mehrere Streams desselben Typs enthalten. Beispielsweise kann eine Videodatei Audiodatenströme in verschiedenen Sprachen enthalten. Zur Laufzeit wählt die Anwendung den zu verwendenden Stream aus.

## <a name="compression"></a>Komprimierung

*Komprimierung* bezieht sich auf jeden Prozess, der die Größe eines Datenstroms verringert, indem redundante Informationen entfernt werden. Komprimierungs Algorithmen lassen sich in zwei allgemeine Kategorien unterteilen:

-   *Verlust lose* Komprimierung. Mit einem verlustfreien Algorithmus sind die rekonstruierten Daten identisch mit der ursprünglichen.
-   *Verlustfreie* Komprimierung. Bei Verwendung eines verlustfreien Algorithmus sind die rekonstruierten Daten ein Näherungswert des Originals, aber es handelt sich nicht um eine genaue Entsprechung.

In den meisten anderen Domänen ist eine verlustfreie Komprimierung nicht zulässig. (Stellen Sie sich vor, dass Sie eine "Näherung" eines Arbeitsblatts erhalten!) Allerdings sind die einstufigen Komprimierungs Schemas aus einer Reihe von Gründen gut für Audiodaten und Videos geeignet.

Der erste Grund ist die Physik der menschlichen Wahrnehmung. Wenn wir auf einen komplexen Sound wie eine Musik Aufzeichnung lauschen, sind einige der in diesem Sound enthaltenen Informationen für das Ohr nicht wahrnehmbar. Mithilfe von Signal Verarbeitungs Theorie ist es möglich, die Häufigkeiten zu analysieren und zu trennen, die nicht wahrgenommen werden können. Diese Frequenzen können ohne perzeptive Auswirkung entfernt werden. Obwohl die rekonstruierte Audiodatei nicht mit der ursprünglichen übereinstimmt, *klingt* Sie für den Listener identisch. Ähnliche Prinzipien gelten für Videos.

Zweitens kann eine Beeinträchtigung der Sound-oder Bildqualität je nach beabsichtigter Zweck akzeptabel sein. Beispielsweise ist die Audiodatei in telefonieweise häufig stark komprimiert. Das Ergebnis eignet sich gut für eine Telefon Konversation – Sie sollten jedoch nicht über ein Telefon auf ein Symphonie-Orchester lauschen.

Die Komprimierung wird auch als *Codierung* bezeichnet, und ein Gerät, das codiert, wird als *Encoder* bezeichnet. Der umgekehrte Prozess ist *Decodierung*, und das Gerät ist ein natürlich als *Decoder* bezeichnet. Der allgemeine Begriff für Encoder und Decoder ist *Codec*. Codecs können in Hardware oder Software implementiert werden.

Die Komprimierungs Technologie hat sich seit der Einführung digitaler Medien schnell geändert, und heute wird eine große Anzahl von Komprimierungs Schemas verwendet. Diese Tatsache ist eine der wichtigsten Herausforderungen bei der Programmierung digitaler Medien.

## <a name="media-containers"></a>Medien Container

Es ist selten, dass ein Rohdaten-oder Videostream als Computerdatei gespeichert oder direkt über das Netzwerk gesendet wird. Es ist nicht möglich, einen solchen Stream zu decodieren, ohne im Voraus zu wissen, welcher Codec verwendet werden muss. Daher enthalten Mediendateien normalerweise mindestens einige der folgenden Elemente:

-   Dateiheader, die die Anzahl der Streams, das Format der einzelnen Streams usw. beschreiben.
-   Ein Index, der den zufälligen Zugriff auf den Inhalt ermöglicht.
-   Metadaten, die den Inhalt beschreiben (z. b. den Künstler oder den Titel).
-   Paket Header, um die Netzwerkübertragung oder den Zufalls Zugriff zu ermöglichen.

In dieser Dokumentation wird der Begriff *Container* verwendet, um das gesamte Paket von Streams, Headern, Indizes, Metadaten usw. zu beschreiben. Der Grund für die Verwendung des Begriffs " *Container* " anstelle von " *File* " besteht darin, dass einige Containerformate für Live Broadcast entworfen wurden. Eine Anwendung kann den Container in Echtzeit generieren und niemals in einer Datei speichern.

Ein frühes Beispiel für einen Medien Container ist das AVI-Dateiformat. Weitere Beispiele hierfür sind MP4 und das Advanced Systems Format (ASF). Container können durch die Dateinamenerweiterung (z. b.. MP4) oder durch den MIME-Typ identifiziert werden.

Das folgende Diagramm zeigt eine typische Struktur für einen Medien Container. Das Diagramm stellt kein bestimmtes Format dar. die Details der einzelnen Formate variieren stark.

![Diagramm mit einem typischen Medien Container](images/concepts01.png)

Beachten Sie, dass die im Diagramm gezeigte Struktur hierarchisch ist, wobei Header Informationen am Anfang des Containers angezeigt werden. Diese Struktur ist typisch für viele (aber nicht alle) Containerformate. Beachten Sie auch, dass der Daten Abschnitt verschachtelte Audiodateien und Video Pakete enthält. Diese Art von Überlappung ist in Medien Containern üblich.

Der Begriff *Multiplexing* bezieht sich auf den Prozess, bei dem die Audiodaten und Videostreams in den Container integriert werden. Der umgekehrte Prozess, von dem die Datenströme aus den packetisiert-Daten wieder zusammengesetzt werden, wird als *Demultiplexing* bezeichnet.

## <a name="formats"></a>Formate

In digitalen Medien ist der Begriff *Format* mehrdeutig. Ein Format kann auf den *Codierungstyp*(z. b. H. 264-Video) oder auf den *Container*(z. b. MP4) verweisen. Dieser Unterschied ist für normale Benutzer häufig verwirrend. Die Namen, die den Medienformaten zugewiesen sind, werden nicht immer unterstützt. Beispielsweise bezieht sich *MP3* sowohl auf ein Codierungsformat (MPEG-1 Audiolayer 3) als auch auf ein Dateiformat.

Der Unterschied ist jedoch wichtig, da das Lesen einer Mediendatei tatsächlich zwei Phasen umfasst:

1.  Zuerst muss der Container analysiert werden. In den meisten Fällen sind die Anzahl der Streams und das Format der einzelnen Datenströme erst bekannt, wenn dieser Schritt beendet ist.
2.  Wenn die Datenströme komprimiert werden, müssen Sie als nächstes mithilfe der entsprechenden Decoders decodiert werden.

Diese Tatsache führt ganz natürlich zu einem Software Entwurf, bei dem separate Komponenten zum Analysieren von Containern und Decodieren von Streams verwendet werden. Außerdem eignet sich dieser Ansatz für ein Plug-in-Modell, sodass Dritte seine eigenen Parser und Codecs bereitstellen können. Unter Windows bietet die Component Object Model (com) eine Standardmethode zum Trennen einer API von ihrer Implementierung, die eine Anforderung für ein beliebiges Plug-in-Modell ist. Aus diesem Grund (unter anderem) verwendet Media Foundation com-Schnittstellen.

Das folgende Diagramm zeigt die Komponenten, die zum Lesen einer Mediendatei verwendet werden:

![Diagramm mit den Komponenten zum Lesen einer Mediendatei](images/concepts02.png)

Das Schreiben einer Mediendatei erfordert auch zwei Schritte:

1.  Codieren der nicht komprimierten Audiodaten und Videodaten.
2.  Einfügen der komprimierten Daten in ein bestimmtes Containerformat

Das folgende Diagramm zeigt die Komponenten, die zum Schreiben einer Mediendatei verwendet werden:

![das Diagramm zeigt die Komponenten zum Schreiben einer Mediendatei.](images/concepts03.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> </dl>

 

 



