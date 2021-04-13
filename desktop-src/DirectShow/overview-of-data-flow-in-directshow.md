---
description: Übersicht über den Datenfluss in DirectShow
ms.assetid: a1b30592-5106-44f5-8ee0-577573670167
title: Übersicht über den Datenfluss in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5a34444991d6cba62026935f5ec2d7aa4eba77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482259"
---
# <a name="overview-of-data-flow-in-directshow"></a>Übersicht über den Datenfluss in DirectShow

In diesem Abschnitt erhalten Sie einen umfassenden Überblick über die Funktionsweise des Datenflusses in DirectShow. Details finden Sie in den anderen Abschnitten der Dokumentation.

Daten werden in Puffern gespeichert, bei denen es sich um einfache Arrays von Bytes handelt. Jeder Puffer wird von einem COM-Objekt umschließt, das als *Medien Beispiel* bezeichnet wird, das die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle implementiert. Beispiele werden von einem anderen Objekttyp erstellt, der als Zuweiser bezeichnet wird und die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle implementiert. Eine Zuweisung wird für jede Pin-Verbindung zugewiesen, obwohl zwei oder mehr Pin-Verbindungen dieselbe Zuweisung gemeinsam verwenden können. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![Puffer, Beispiele und Zuweisungen](images/dataflow.png)

Jeder Zuweiser erstellt einen Pool mit Medien Beispielen und ordnet die Puffer für jede Stichprobe zu. Wenn ein Filter einen Puffer mit Daten füllen muss, fordert er eine Stichprobe von der Zuweisung an, indem [**imemzuordcator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)aufgerufen wird. Wenn die Zuweisung über Beispiele verfügt, die zurzeit nicht von einem anderen Filter verwendet werden, gibt die **GetBuffer** -Methode sofort einen Zeiger auf das Beispiel zurück. Wenn alle Beispiele der Zuweiser verwendet werden, wird die-Methode blockiert, bis eine Stichprobe verfügbar ist. Wenn die Methode ein Beispiel zurückgibt, fügt der Filterdaten in den Puffer ein, legt die entsprechenden Flags für das Beispiel fest (in der Regel mit einem Zeitstempel) und übermittelt das Beispiel Downstream.

Wenn ein rendererfilter ein Beispiel empfängt, überprüft er den Zeitstempel und hält den Zeitstempel auf dem Beispiel, bis die Referenz Uhr des Filter Diagramms anzeigt, dass die Daten gerendert werden sollen. Nachdem der Filter die Daten gerendert hat, wird das Beispiel freigegeben. Das Beispiel wechselt nicht zurück in den Pool der zuordnerpools, bis der Verweis Zähler der Stichprobe NULL ist, was bedeutet, dass jeder Filter das Beispiel freigegeben hat. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![Decoder, der auf ein Beispiel für ein kostenloses Medium wartet](images/dataflow2.png)

Der upstreamfilter kann vor dem Renderer ausgeführt werden, d. –., er kann Puffer schneller auffüllen, als er von dem Renderer verarbeitet wird. Auch hier werden die Beispiele nicht frühzeitig gerendert, da der Renderer diese bis zur Präsentationszeit speichert. Außerdem werden Puffer nicht versehentlich überschrieben, da **getSample** nur Beispiele zurückgibt, die andernfalls nicht verwendet werden. Der Betrag, um den der upstreamfilter ausgeführt werden kann, richtet sich nach der Anzahl der Stichproben im Pool des zuordcators.

Das vorherige Diagramm zeigt nur eine Zuweisung, aber in der Regel sind mehrere Zuweisungen pro Stream vorhanden. Wenn der Renderer ein Beispiel freigibt, kann er daher einen kaskadierenden Effekt haben. Das folgende Diagramm zeigt eine Situation, in der ein Decoder einen komprimierten Videorahmen enthält, während er darauf wartet, dass der Renderer ein Beispiel freigibt. Ein Parserfilter wartet auch darauf, dass der Decoder ein Beispiel freigibt.

![zwei Filter, die auf Beispiele warten](images/dataflow3.png)

Wenn der Renderer das Beispiel freigibt, gibt der vom Decoder ausstehend aufrufende **GetBuffer** zurück. Der Decoder kann dann den komprimierten Videorahmen decodieren und das aufgehaltener Beispiel freigeben. Dadurch wird die Blockierung des ausstehenden **GetBuffer** -Aufrufens des Parsers aufgehoben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



