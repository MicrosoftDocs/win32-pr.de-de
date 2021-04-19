---
description: Erweiterungen der DVD-Wiedergabe in Windows Vista
ms.assetid: b3cf043f-c974-4240-8291-5c717bd8afaa
title: Erweiterungen der DVD-Wiedergabe in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159056d2c7acaec18a73a30b21f79bcd6267ca33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346399"
---
# <a name="dvd-playback-enhancements-in-windows-vista"></a>Erweiterungen der DVD-Wiedergabe in Windows Vista

In diesem Abschnitt werden die Verbesserungen der DVD-Wiedergabe und-Navigation in Windows Vista beschrieben

**Angeben eines Decoders**

In früheren Versionen von DirectShow war es schwierig, bei der Erstellung eines DVD-Wiedergabe Diagramms einen bestimmten MPEG-2-Decoder anzugeben. Ab Windows Vista kann eine Anwendung den Decoder wie folgt angeben:

1.  Fügen Sie den Decoder dem Diagramm hinzu, bevor Sie [**idvdgraphbuilder:: renderdvdvideovolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume)aufrufen.
2.  Nennen Sie **renderdvdvideovolume** , und legen \_ Sie das Flag am DVD- \_ \_ \_ Flag nicht löschen fest. Der DVD-Navigator wird dem von Ihnen hinzugefügten Decoder bevorzugt.

**Unterstützung für den erweiterten Videorenderer**

Es wird empfohlen, dass Anwendungen, die für Windows Vista oder höher geschrieben wurden, den [**erweiterten Videorenderer**](enhanced-video-renderer-filter.md) (EVR) für die Video Wiedergabe verwenden. Wenn Sie den EVR in einer DVD-Wiedergabe Anwendung verwenden möchten, legen \_ Sie das Flag am DVD-EVR Only fest, \_ \_ Wenn Sie **renderdvdvideovolume** aufruft.

Um den EVR vor dem Erstellen des Diagramms zu konfigurieren, nennen Sie [**idvdgraphbuilder:: getdvdinterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) , und Fragen Sie die **ievrfilterconfig** -Schnittstelle oder die **imfvideorenderer** -Schnittstelle ab. (Diese Schnittstellen sind in der Media Foundation SDK-Dokumentation dokumentiert.) Weitere Informationen zum Konfigurieren des Videorenderers in einem DVD-Wiedergabe Diagramm finden Sie unter [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).

Der DVD-Navigator verwendet nicht den EVR, es sei denn, die [**iamdecodercaps:: getdecodercaps**](/windows/desktop/api/Strmif/nf-strmif-iamdecodercaps-getdecodercaps) -Methode des Decoders gibt das \_ \_ \_ \_ unter stützungsflag "am getdecodercap Query EVR" zurück. Dieses Flag ist definiert, um sicherzustellen, dass Anwendungen mit vorhandenen Decodern kompatibel sind. Wenn **renderdvdvideovolume** nicht mit dem \_ Flag am DVD- \_ \_ rollonly ausgeführt wird, greifen Sie auf einen anderen Videorenderer zurück, indem Sie die Methode ohne das-Flag erneut aufrufen.

**Reibungslose umgekehrte Wiedergabe**

Der DVD-Navigator kann nun eine reibungslose umgekehrte Wiedergabe ausführen. Bei der nahtlosen umgekehrten Wiedergabe sendet der DVD-Navigator ganze Video Objekt Einheiten (vobus) an den Decoder, und der Decoder gibt die Frames in umgekehrter Reihenfolge aus. Für dieses Feature ist es erforderlich, dass die Decoder die nahtlose umgekehrte Wiedergabe unterstützen.

Wenn die Wiedergabe-Geschwindigkeit von der Anwendung auf einen negativen Wert festgelegt wird, fragt der DVD-Navigator die Decoder nach der " [**\_ Ate \_ reversemaxfulldatarate**](am-rate-reversemaxfulldatarate-property.md) "-Eigenschaft ab. Der Wert dieser Eigenschaft ist der absolute Wert der maximalen umgekehrten Geschwindigkeit x 10000. Wenn die maximale umgekehrte Geschwindigkeit beispielsweise-2,0 beträgt, ist der Wert 20000.

Wenn der Video-Decoder die-Eigenschaft unterstützt, verwendet der DVD-Navigator eine Smooth Reverse-Wiedergabe. Der Audiodatenstrom wird in umgekehrter Reihenfolge wiedergegeben, wenn der Audiodecoder die Eigenschaft unterstützt. Andernfalls wird der Audiodatenstrom stumm geschaltet. Wenn der Video Decoder die-Eigenschaft nicht unterstützt, oder wenn die Wiedergabe Rate die maximale Reverse-Rate des Video-Decoders überschreitet, wechselt der DVD-Navigator in den *Scanmodus*. Im Scanmodus sendet der DVD-Navigator nur I-Frames an den Decoder und löscht alle B-und P-Frames.

Während der nahtlosen umgekehrten Wiedergabe sendet der DVD-Navigator einen kompletten vobus an den Decoder. Der DVD-Navigator sendet den vobus in umgekehrter Reihenfolge, sendet die Rahmen in jeder vobu in der normalen Reihenfolge. Am Anfang jeder vobu legt der DVD-Navigator das Flag "am \_ reverseblockstart" für das Beispiel fest. Am Ende der vobu sendet der DVD-Navigator eine leere Stichprobe mit dem "am \_ reverseblockend"-Flag. Rufen Sie zum Abrufen dieser Flags [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) für das Beispiel auf. Die Flags werden im **dwtypespecificflags** -Member der [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur festgelegt.

Der Decoder speichert die Videodaten so lange zwischen, bis die Stichprobe mit dem "am \_ reverseblockend"-Flag empfangen wird. An diesem Punkt stellt der Decoder decodierte Frames in umgekehrter Reihenfolge bereit. Wenn vobu 1 z. b. Frames 1 – 4 enthält und vobu 2 Frames 5 – 8 enthält, sendet der DVD-Navigator die Frames in dieser Reihenfolge:

(Start blockieren) F5 F6 F7 F8 (Block Ende) (Block Start) F1 F2 F3 F4 (Block Ende)

Der Decoder sollte die Frames wie folgt verarbeiten:

1.  Decodieren Sie vobu 2.
2.  Ausgabe Frames: F8 F7 F6 F5
3.  Decodieren Sie vobu 1.
4.  Ausgabe Frames: F4 F3 F2 F1

Der DVD-Navigator legt den Zeitstempel auf dem ersten Beispiel in der vobu (F1 und F5 in diesem Beispiel) fest. der Zeitstempel enthält jedoch die Präsentationszeit des Starts des Blocks, sodass der Decoder diese Zeit auf das letzte Beispiel im Block anwenden muss (F4 und F8). Präsentations Zeiten erhöhen sich bei der umgekehrten Wiedergabe.

In der Regel enthält ein vobu bis zu 42 Frames und kann mehr als eine Gruppe von Bildern (GOP) enthalten. Damit der gesamte vobu decodiert werden kann, sollte der Decoder die decodierten I-und P-Frames Zwischenspeichern. Vobus auf DVDs sind keine geschlossenen GOPs, daher erfordert ein B-Frame in einem GOP möglicherweise das Decodieren aller Verweis Rahmen im vorherigen GOP. Wenn der Decoder nicht über genügend Oberflächen verfügt, um alle decodierten Frames aufzunehmen, muss er möglicherweise ausgewählte Frames erneut decodieren.

**Raten Änderungen**

Standardmäßig leert der DVD-Navigator das Diagramm zwischen Raten Änderungen. Wenn der Decoder die Eigenschaft [**" \_ Ate \_ rementontimedisc**](am-rate-resetontimedisc-property.md) " unterstützt, wird das Diagramm vom DVD-Navigator nicht geleert, was zu einem reibungsloseren Übergang zwischen den Wiedergabe Raten führt.

Der DVD-Navigator Zeitstempel für die Wiedergabe immer wieder mit einer Geschwindigkeit von 1 x, unabhängig von der tatsächlichen Wiedergabegeschwindigkeit. Der Decoder muss die Zeitstempel in den decodierten Beispielen entsprechend der tatsächlichen Wiedergabegeschwindigkeit skalieren. (Ausführliche Informationen finden Sie unter " [**\_ Raten \_ simpleratechange**](am-rate-simpleratechange-property.md)"-Eigenschaft.) Folglich weichen die Zeitstempel in den decodierten Frames bei anderen Geschwindigkeiten als 1 x von denen der codierten Frames ab. Immer wenn der DVD-Navigator das "am \_ Sample \_ timediscontinuity"-Flag für ein Beispiel festlegt, sollte der Decoder seine Zeitstempel neu synchronisieren. Anders ausgedrückt: der decodierte Frame sollte denselben Zeitstempel wie der Eingabe Rahmen aufweisen. Rufen Sie zum Abrufen des am \_ Sample Sample \_ timediscontinuity-Flags [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) für das Beispiel auf. Das-Flag wird im **dwsampleflags** -Member der [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur festgelegt.

**Energieverwaltung**

In Windows Vista ermöglicht der DVD-Navigator die folgenden Verbesserungen an der Energie Verwaltung:

-   Höhere Zeit Geber Auflösung
-   Größerer Daten Cache

Zeit Geber **Auflösung**: Anwendungen können eine minimale Zeit Geber Auflösung anfordern, indem Sie die **TimeBeginPeriod** -Funktion aufrufen. Eine höhere Auflösung (kürzerer Zeitraum) erhöht die Reaktionsfähigkeit des Systems auf regelmäßige Ereignisse, wie z. b. Timeouts, kann jedoch auch die Häufigkeit der Thread Kontextwechsel erhöhen.

Standardmäßig wird die Zeit Geber Auflösung in DirectShow auf 1 Millisekunde festgelegt. Bei dieser Lösung wird die CPU nicht in den Energiesparmodus wechseln. Ab Windows Vista überschreibt der DVD-Navigator das Standardverhalten der verweisuhr durch Aufrufen von [**ireferenceclocktimercontrol:: setdefaulttimerresolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) auf der Referenzuhr. Dadurch wird die Anforderung der Uhr für eine Zeit Geber Auflösung von 1 Millisekunde entfernt. Dadurch kann die CPU in einen Energiesparmodus wechseln.

Die Zeit Geber Auflösung ist eine globale Einstellung. Windows wählt den niedrigsten angeforderten Wert aus. Der Video Mischungs-Renderer (VMR)-Filter (VMR-7 und VMR-9) legen die Zeit Geber Auflösung auf 1 Millisekunde fest. Der EVR legt die Auflösung in der Regel auf einen Wert zwischen 4 und 8 Millisekunden fest, je nachdem, ob die Desktop Komposition aktiviert ist und ob sich der EVR im Vollbildmodus befindet. Andere Anwendungen können auch die Auflösung festlegen.

**Cache Größe**: Anwendungen können angeben, wie viele Daten der DVD-Navigator zwischenspeichert, indem Sie die Option "DVD \_ cachesizeinmb" in der [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) -Methode festlegen. Wenn das Flag von der Anwendung auf einen großen Wert (> 50 MB) festgelegt wird, wird das DVD-Laufwerk je nach der Hardware, die den Energieverbrauch reduzieren kann, nach dem anfänglichen Vorabruf möglicherweise heruntergefahren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



