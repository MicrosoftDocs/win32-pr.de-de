---
description: Beispiel für einen Synthesizer
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Beispiel für einen Synthesizer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868519"
---
# <a name="synth-filter-sample"></a>Beispiel für einen Synthesizer

## <a name="description"></a>BESCHREIBUNG

Der synfilterfilter ist ein Quell Filter, der audiowaveforms generiert.

Dieser Filter veranschaulicht das dynamische Diagramm. Er kann zwischen nicht komprimiertem PCM-Audiodaten und komprimiertem MS \_ ADPCM-Format (Microsoft Adaptive Delta Pulse Code Modulation) wechseln.

Dieser Filter wird in GraphEdit als "audiosynthesizer-Filter" angezeigt.

Weitere Informationen zum Aufbau dynamischer Diagramme finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="usage"></a>Verbrauch

Mithilfe des synthingfilters kann der Benutzer die Wellenform, Häufigkeit, Anzahl der Kanäle und andere Eigenschaften über die Eigenschaften Seite festlegen. Halten Sie die UMSCHALTTASTE gedrückt, während Sie den Schieberegler für die Häufigkeit anpassen. Der Filter unterstützt auch eine benutzerdefinierte Schnittstelle, ISynth2, um diese Eigenschaften festzulegen.

Führen Sie die folgenden Schritte aus, um die Funktion zum entwickeln dynamischer Diagramme zu veranschaulichen:

1.  Erstellen Sie den Filter, und registrieren Sie ihn mit dem regsvr32-Hilfsprogramm.
2.  Starten Sie GraphEdit.
3.  Fügen Sie den audiosynthesizer-Filter ein. Sie wird in der Kategorie DirectShow-Filter angezeigt.
4.  Renderdas Ausgabe-PIN des Filters.
5.  Klicken Sie auf die Schaltfläche **abspielen** .
6.  Öffnen Sie die Eigenschaften Seite des Filters.
7.  Wählen Sie im Bereich Ausgabe Format die Option PCM oder Microsoft ADPCM aus.

## <a name="programming-notes"></a>Programmier Hinweise

Dieses Beispiel enthält die folgenden Dateien:

-   Dynsrc. h, dynsrc. cpp: enthält zwei Basisklassen für Quell Filter, die die dynamische Diagramm Erbauung, cdynamicsource und cdynamicsourcestream unterstützen.
-   Isynth. h: deklariert die benutzerdefinierte ISynth2-Schnittstelle für das Festlegen von Eigenschaften für den Filter.
-   Resource. h: enthält Ressourcen Konstanten.
-   Synth. DEF: exportiert die DLL-Funktionen, die von der com-Bibliothek benötigt werden.
-   Synth. h, Synth. cpp: enthält die caudiosynth-Klasse, die die Audiodaten generiert, und die csynthfilter-Klasse, die den Filter implementiert.
-   Synth. RC: enthält Ressourcen, die vom Filter verwendet werden.
-   Synthprp. h, synthprp. cpp: Implementiert die Eigenschaften Seite des Filters.

Die cdynamicsource-Klasse wird von der [**CSource**](csource.md) -Basisklasse angepasst. Sie verwendet mindestens einen aus der cdynamicsourcestream-Klasse abgeleiteten Ausgabe Pins. Die cdynamicsourcestream-Klasse wird von der [**csourcestream**](csourcestream.md) -Klasse angepasst, wird jedoch von der [**cdynamicoutputpin**](cdynamicoutputpin.md) -Klasse anstelle der [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse abgeleitet.

Die cdynamicsource-Klasse verfügt über die folgenden Methoden, die in [**CSource**](csource.md)nicht gefunden werden:

-   Stop: signalisiert das Stop-Ereignis ([**cdynamicoutputpin:: m \_ hstopevent**](cdynamicoutputpin-m-hstopevent.md)) und fährt den Arbeits Thread für alle nicht verbundenen Pins herunter. Bei einer verbundenen PIN wird der Arbeitsthread von der inaktiven PIN der PIN heruntergefahren.
-   Anhalten: setzt das anhalteereignis zurück.
-   Joinfiltergraph: Ruft die [**cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md) -Methode für jede PIN auf.

Die cdynamicsourcestream-Klasse verfügt über die folgenden Methoden, die nicht in [**csourcestream**](csourcestream.md)gefunden wurden:

-   Destroysourcethread: schließt den Arbeits Thread.
-   FatalError: signalisiert dem Filter Diagramm-Manager einen Fehler.
-   Outputpinneedstobereconnected: signalisiert, dass die Ausgabe-PIN erneut verbunden werden soll. Wenn diese Methode aufgerufen wird, ruft der Arbeits Thread die [**cdynamicoutputpin::D ynamikreconnect**](cdynamicoutputpin-dynamicreconnect.md) -Methode auf, um die PIN erneut zu verbinden.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK \] root* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Synthesizer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



