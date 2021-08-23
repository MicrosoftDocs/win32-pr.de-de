---
description: Verbesserungen der DVD-Wiedergabe in Windows Vista
ms.assetid: b3cf043f-c974-4240-8291-5c717bd8afaa
title: Verbesserungen der DVD-Wiedergabe in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5757f5dd73dc547ae123490fd8de84b0606d1ade8490c9600486df0b846541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148713"
---
# <a name="dvd-playback-enhancements-in-windows-vista"></a>Verbesserungen der DVD-Wiedergabe in Windows Vista

In diesen Abschnitten werden die Verbesserungen der DVD-Wiedergabe und -Navigation in Windows Vista beschrieben.

**Angeben eines Decoders**

In früheren Versionen von DirectShow war es schwierig, beim Erstellen eines DVD-Wiedergabediagramms einen bestimmten MPEG-2-Decoder anzugeben. Ab Windows Vista kann eine Anwendung den Decoder wie folgt angeben:

1.  Fügen Sie dem Diagramm den Decoder hinzu, bevor [**Sie IDvdGraphBuilder::RenderDvdVideoVolume aufrufen.**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume)
2.  Rufen **Sie RenderDvdVideoVolume auf,** und legen Sie das FLAG AM \_ DVD DO NOT CLEAR \_ \_ \_ fest. Der DVD-Navigator bevorzugt den Decoder, den Sie hinzugefügt haben.

**Unterstützung für den erweiterten Videorenderer**

Es wird empfohlen, dass Anwendungen, die für Windows Vista oder höher geschrieben wurden, den [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) für die Videowiedergabe verwenden. Um evr in einer DVD-Wiedergabeanwendung zu verwenden, legen Sie das FLAG AM DVD EVR ONLY fest, wenn Sie \_ \_ \_ **RenderDvdVideoVolume aufrufen.**

Um die EVR vor dem Erstellen des Graphen zu konfigurieren, rufen Sie [**IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) auf, und fragen Sie die **IEVRFilterConfig-Schnittstelle** oder **DIE BENUTZEROBERFLÄCHEVideoRenderer-Schnittstelle** ab. (Diese Schnittstellen sind in der Dokumentation zum Media Foundation SDK dokumentiert.) Weitere Informationen zum Konfigurieren des Videorenderers in einem DVD-Wiedergabediagramm finden Sie unter [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).

Der DVD-Navigator verwendet den EVR nur, wenn die [**IAMDecoderCaps::GetDecoderCaps-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamdecodercaps-getdecodercaps) des Decoders das AM \_ GETDECODERCAP \_ QUERY \_ EVR SUPPORT-Flag zurückgibt. \_ Dieses Flag wird definiert, um sicherzustellen, dass Anwendungen mit vorhandenen Decodern kompatibel sind. Wenn **RenderDvdVideoVolume** mit dem EVR ONLY-Flag der AM DVD fehlschlägt, können Sie auf einen anderen Videorenderer zurückfallen, indem Sie die -Methode erneut ohne das \_ \_ \_ -Flag aufrufen.

**Smooth Reverse Playback**

Der DVD-Navigator kann jetzt eine reibungslose Reversewiedergabe durchführen. Bei der nahtlosen Umgekehrt-Wiedergabe sendet der DVD-Navigator ganze Videoobjekteinheiten (VOBUs) an den Decoder, und der Decoder gibt die Frames in umgekehrter Reihenfolge aus. Dieses Feature erfordert, dass die Decoder eine reibungslose Reversewiedergabe unterstützen.

Wenn die Anwendung die Wiedergabegeschwindigkeit auf einen negativen Wert festsetzt, fragt der DVD-Navigator die Decoder nach der [**AM \_ RATE \_ ReverseMaxFullDataRate-Eigenschaft**](am-rate-reversemaxfulldatarate-property.md) ab. Der Wert dieser Eigenschaft ist der absolute Wert der maximalen Umgekehrte Geschwindigkeit x 10000. Wenn die maximale Umgekehrt-Geschwindigkeit beispielsweise -2,0 beträgt, ist der Wert 20000.

Wenn der Videodecoder die -Eigenschaft unterstützt, verwendet der DVD-Navigator eine reibungslose Reversewiedergabe. Der Audiostream wird umgekehrt abgespielt, wenn der Audiodecoder die -Eigenschaft unterstützt. Andernfalls ist der Audiostream stummgeschaltet. Wenn der Videodecoder die -Eigenschaft nicht unterstützt oder die Wiedergaberate die maximale Umgekehrt-Rate des Videodecoders überschreitet, wechselt der DVD-Navigator in den *Scanmodus*. Im Scanmodus sendet der DVD-Navigator nur I-Frames an den Decoder und löscht alle B- und P-Frames.

Während der nahtlosen Umgekehrt-Wiedergabe sendet der DVD-Navigator vollständige VOBUs an den Decoder. Der DVD-Navigator sendet die VOBUs in umgekehrter Reihenfolge, aber die Frames innerhalb jedes VOBU in ihrer normalen Vorwärts reihenfolge. Am Anfang jedes VOBU legt der DVD-Navigator das AM \_ ReverseBlockStart-Flag für das Beispiel fest. Am Ende des VOBU sendet der DVD-Navigator ein leeres Beispiel mit dem FLAG AM \_ ReverseBlockEnd. Rufen Sie zum Abrufen dieser Flags im Beispiel [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) auf. Die Flags werden im **dwTypeSpecificFlags-Member** der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) festgelegt.

Der Decoder speichert die Videodaten zwischen, bis er das Beispiel mit dem AM \_ ReverseBlockEnd-Flag empfängt. An diesem Punkt liefert der Decoder decodierte Frames in umgekehrter Reihenfolge. Wenn VOBU 1 beispielsweise die Frames 1 bis 4 und VOBU 2 die Frames 5 bis 8 enthält, sendet der DVD-Navigator die Frames in der folgenden Reihenfolge:

(Start blockieren) F5 F6 F7 F8 (Blockende) (Blockstart) F1 F2 F3 F4 (Blockende)

Der Decoder sollte die Frames wie folgt verarbeiten:

1.  Decodieren Sie VOBU 2.
2.  Ausgabeframes: F8 F7 F6 F5
3.  Decodieren Sie VOBU 1.
4.  Ausgabeframes: F4 F3 F2 F1

Der DVD-Navigator legt den Zeitstempel für das erste Beispiel im VOBU fest (in diesem Beispiel F1 und F5), aber der Zeitstempel enthält die Präsentationszeit des Blocks, sodass der Decoder dieses Mal auf das letzte Beispiel im Block (F4 und F8) angewendet werden sollte. Die Präsentationszeiten erhöhen sich während der umgekehrten Wiedergabe.

In der Regel enthält ein VOBU bis zu 42 Frames und kann mehr als eine Gruppe von Bildern (GOP) enthalten. Damit der gesamte VOBU decodiert werden kann, sollte der Decoder die decodierten I- und P-Frames zwischenspeichern. VOBUs auf DVDs sind keine geschlossenen GOPs, sodass ein B-Frame innerhalb eines GOP möglicherweise das Decodieren aller Referenzframes im vorherigen GOP erfordert. Wenn der Decoder nicht über genügend Oberflächen verfügt, um alle decodierten Frames zu halten, muss er möglicherweise ausgewählte Frames neu decodieren.

**Änderungen der Rate**

Standardmäßig leert der DVD-Navigator das Diagramm zwischen Denkratenänderungen. Wenn der Decoder jedoch die [**AM \_ RATE \_ ResetOnTimeDisc-Eigenschaft**](am-rate-resetontimedisc-property.md) unterstützt, leert der DVD-Navigator das Diagramm nicht, was zu einem reibungsloseren Übergang zwischen den Wiedergaberaten führt.

Der DVD-Navigator stempelt immer Stichproben für die Wiedergabe mit 1-facher Geschwindigkeit, unabhängig von der tatsächlichen Wiedergabegeschwindigkeit. Der Decoder muss die Zeitstempel auf den decodierten Stichproben skalieren, um die tatsächliche Wiedergabegeschwindigkeit zu erhalten. (Weitere Informationen finden Sie unter [**AM \_ RATE \_ SimpleRateChange Property**](am-rate-simpleratechange-property.md).) Daher unterscheiden sich die Zeitstempel der decodierten Frames bei der Wiedergabe mit anderen Geschwindigkeiten als dem 1-Fachen von denen in den codierten Frames. Wenn der DVD-Navigator das AM \_ SAMPLE TIMEDISCONTINUITY-Flag für ein Beispiel legt, sollte der Decoder seine Zeitstempel \_ neusynchronisieren. Anders ausgedrückt: Der decodierte Frame sollte denselben Zeitstempel wie der Eingaberahmen haben. Rufen Sie zum Abrufen des AM \_ SAMPLE \_ TIMEDISCONTINUITY-Flags im Beispiel [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) auf. Das Flag wird im **dwSampleFlags-Member** der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) festgelegt.

**Energieverwaltung**

In Windows Vista ermöglicht der DVD-Navigator die folgenden Verbesserungen der Energieverwaltung:

-   Höhere Timerauflösung
-   Größerer Datencache

**Timerauflösung:** Anwendungen können eine minimale Timerauflösung anfordern, indem sie die **timeBeginPeriod-Funktion** aufrufen. Eine höhere Auflösung (kürzerer Zeitraum) erhöht die Reaktionsfähigkeit des Systems auf periodische Ereignisse wie Timeouts, kann aber auch die Häufigkeit von Threadkontextwechseln erhöhen.

Standardmäßig legt die Referenzuhr in DirectShow die Timerauflösung auf 1 Millisekunde fest. Bei dieser Auflösung wird die CPU in keine Energiesparmodi wechseln. Ab Windows Vista überschreibt der DVD-Navigator das Standardverhalten der Referenzuhr durch Aufrufen von [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) auf der Referenzuhr. Dadurch wird die Anforderung der Uhr nach einer Timerauflösung von 1 Millisekunde entfernt. Dadurch kann die CPU in einen Energiesparmodus wechseln.

Die Timerauflösung ist eine globale Einstellung. Windows wählt den niedrigsten angeforderten Wert aus. Die Filter des Videomischen renderers (VMR) (VMR-7 und VMR-9) legen die Timerauflösung auf 1 Millisekunde fest. Der EVR legt die Auflösung in der Regel auf einen Wert zwischen 4 und 8 Millisekunden fest, je nachdem, ob die Desktopkomposition aktiviert ist und ob sich die EVR im Vollbildmodus befindet. Andere Anwendungen können auch die Auflösung festlegen.

**Cachegröße:** Anwendungen können angeben, wie viele Daten der DVD-Navigator zwischenspeichert, indem sie die Option DVD \_ CacheSizeInMB in der [**IDvdControl2::SetOption-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) festlegen. Wenn die Anwendung dieses Flag auf einen großen Wert (> 50 MB) setzt, kann das DVD-Laufwerk nach dem anfänglichen Vorababruf abhängig von der Hardware heruntergefahren werden, wodurch der Energieverbrauch reduziert werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



