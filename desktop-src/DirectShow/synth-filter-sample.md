---
description: Synth-Filterbeispiel
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Synth-Filterbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a3a366a6612aadf653b5af13099dbc8a4f08c2fb828bca6e64514cb1801e4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119291191"
---
# <a name="synth-filter-sample"></a>Synth-Filterbeispiel

## <a name="description"></a>BESCHREIBUNG

Der Synth-Filter ist ein Quellfilter, der Audio-Waveforms generiert.

Dieser Filter veranschaulicht das Erstellen dynamischer Diagramme. Sie kann zwischen unkomprimiertem PCM-Audio und komprimiertem MS \_ ADPCM-Format (Microsoft Adaptive Delta Pulse Code Codes Codes) wechseln.

Dieser Filter wird in GraphEdit als "Audiosynthetizerfilter" angezeigt.

Weitere Informationen zum Erstellen von dynamischen Diagrammen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="usage"></a>Verbrauch

Mit dem Synth-Filter kann der Benutzer die Wellenform, Häufigkeit, Anzahl von Kanälen und andere Eigenschaften über die Eigenschaftenseite festlegen. Um entweder den oberen oder unteren Endpunkt des Swept-Frequenzbereichs einzustellen, halten Sie die UMSCHALT-Schieberegler fest, während Sie den Schieberegler für die Häufigkeit anpassen. Der Filter unterstützt auch die benutzerdefinierte Schnittstelle ISynth2 zum Festlegen dieser Eigenschaften.

Gehen Sie wie folgt vor, um das Feature zum Erstellen dynamischer Graphen zu veranschaulichen:

1.  Erstellen Sie den Filter, und registrieren Sie ihn mit dem Regsvr32-Hilfsprogramm.
2.  Starten Sie GraphEdit.
3.  Fügen Sie den Filter AudioSynthetizer ein. Sie wird in der Kategorie DirectShow-Filter angezeigt.
4.  Rendern Sie den Ausgabepin des Filters.
5.  Klicken Sie auf **die Schaltfläche Wiedergabe.**
6.  Öffnen Sie die Eigenschaftenseite des Filters.
7.  Wählen Sie im Bereich Ausgabeformat die Option PCM oder Microsoft ADPCM aus.

## <a name="programming-notes"></a>Programmierhinweise

Dieses Beispiel enthält die folgenden Dateien:

-   Dynsrc.h, Dynsrc.cpp: Enthält zwei Basisklassen für Quellfilter, die das Erstellen dynamischer Diagramme unterstützen: CDynamicSource und CDynamicSourceStream.
-   ISynth.h: Deklariert die benutzerdefinierte ISynth2-Schnittstelle zum Festlegen von Eigenschaften für den Filter.
-   Resource.h: Enthält Ressourcenkonst constants.
-   Synth.def: Exportiert die dll-Funktionen, die von der COM-Bibliothek benötigt werden.
-   Synth.h, Synth.cpp: Enthält die CAudioSynth-Klasse, die die Audiodaten generiert, und die CSynthFilter-Klasse, die den Filter implementiert.
-   Synth.rc: Enthält ressourcen, die vom Filter verwendet werden.
-   Synthprp.h, Synthprp.cpp: Implementiert die Eigenschaftenseite des Filters.

Die CDynamicSource-Klasse wird von der [**CSource-Basisklasse**](csource.md) angepasst. Sie verwendet einen oder mehrere Ausgabepins, die von der CDynamicSourceStream-Klasse abgeleitet wurden. Die CDynamicSourceStream-Klasse wird von der [**CSourceStream-Klasse**](csourcestream.md) angepasst, wird jedoch von der [**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md) und nicht von der [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) ableiten.

Die CDynamicSource-Klasse verfügt über die folgenden Methoden, die in [**CSource nicht gefunden wurden:**](csource.md)

-   Stop: Signalisiert das Stop-Ereignis ([**CDynamicOutputPin::m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) und fährt den Arbeitsthread für alle nicht verbundenen Pins herunter. Bei einem verbundenen Pin fährt die Inaktiv-Methode des Pins den Arbeitsthread herunter.
-   Anhalten: Setzt das Stoppereignis zurück.
-   JoinFilterGraph: Ruft die [**CDynamicOutputPin::SetConfigInfo-Methode**](cdynamicoutputpin-setconfiginfo.md) für jeden Pin auf.

Die CDynamicSourceStream-Klasse verfügt über die folgenden Methoden, die in [**CSourceStream nicht gefunden wurden:**](csourcestream.md)

-   DestroySourceThread: Fährt den Arbeitsthread herunter.
-   FatalError: Signalisiert einen Fehler an den Filtergraph-Manager.
-   OutputPinNeedsToBeReconnected: Signalisiert, dass der Ausgabepin erneut verbunden werden soll. Wenn diese Methode aufgerufen wird, ruft der Arbeitsthread die [**CDynamicOutputPin::D ynamicReconnect-Methode**](cdynamicoutputpin-dynamicreconnect.md) auf, um die Verbindung mit dem Pin wiederherzustellen.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Um die DirectShow SDK-Beispiele herunterzuladen, installieren Sie die neueste Version des [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Dieses Beispiel wird unter dem folgenden Pfad installiert: *\[ SDK \] Root* Samples Multimedia \\ \\ \\ DirectShow Filters \\ \\ Synth.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



