---
description: YUV-Mischungs Modus
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: YUV-Mischungs Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867484"
---
# <a name="yuv-mixing-mode"></a>YUV-Mischungs Modus

Dieses Thema gilt für Windows XP Service Pack 2 oder höher.

Ab Windows XP Service Pack 2 unterstützt VMR einen Mischungs Modus mit dem Namen YUV-Mischungs Modus. Dieser Modus ist am nützlichsten für erweiterte TV-oder DVD-Anwendungen. Es wird ein Teil der Leistungsfähigkeit des VMR-Mischers eingesetzt, um eine bessere Leistung auf Low-End-Grafikhardware zu erzielen Der YUV-Mischungs Modus wird sowohl für VMR-7 als auch für VMR-9 unterstützt.

**Vorteile**

Der YUV-Mischungs Modus bietet mehrere Vorteile im Zusammenhang mit der Renderingleistung im ursprünglichen RGB-Mischungs Modus, der von der VMR

-   Wenn sich der VMR im YUV-Mischungs Modus befindet, werden alle Vorgänge zum Aufheben der Interlacing-und Videodaten Strom Komposition in einem YUV-Farbraum ausgeführt. YUV-Oberflächen erfordern normalerweise zwischen 50% und 60% weniger Speicherbandbreite als äquivalente RGB-Oberflächen.
-   Die Deinterlacing-und Datenstrom Komposition erfolgt durch einen einzelnen-Befehl des Grafik Treibers. Der Treiber kann die multitexturierungsfunktionen der Grafikhardware verwenden, was zu zusätzlichen Einsparungen bei der Speicherbandbreite führt.

Obwohl jede Video Anwendung den YUV-Mischungs Modus verwenden kann, ist Sie in erster Linie für zwei Arten von Videowiedergabe Anwendungen gedacht:

1.  TV-Anwendungen, die Untertitel oder Teletext anzeigen.
2.  DVD-Anwendungen zeigen DVD-subbilddaten oder Untertitel an.

**Einschränkungen**

Eine Reihe von Einschränkungen werden von der VMR erzwungen, wenn Sie in den YUV-Mischungs Modus versetzt wird:

-   Stream 0 (der mit der Eingabe-PIN "0" verbundene Stream) kann progressiv oder Zeilen Sprung sein. alle anderen Streams müssen progressiv sein.
-   GUID \_ NULL (Weave-Modus) ist für Stream 0 nicht zulässig.
-   Das Debuggen "deinterlacepref" \_ kann nicht als Fall Back Modus verwendet werden, da dadurch verhindert werden kann, dass ein deinterlace-Gerät erstellt wird. Der YUV-Mischungs Modus erfordert ein Deinterlacing-Gerät, auch wenn das eingehende Video nicht mit Zeilen Sprung verknüpft ist.
-   Es können keine Änderungen an dem planaren Alpha-Wert vorgenommen werden, der mit den einzelnen VMR-Eingabedaten strömen verknüpft ist.
-   Der Benutzer kann die Z-Reihenfolge der verbundenen Videostreams nicht ändern. Die standardmäßige Z-Reihenfolge wird aus der PIN-Reihenfolge entnommen.
-   Die Farb Erstellung wird nicht unterstützt.
-   Die Eingabe-PIN 0 muss den Videostream erhalten.
-   Die anderen Eingabe Pins können nur Video-substreamdaten empfangen, z. b. DVD-Untertitel, Untertitel oder Teletext.
-   Die anderen Eingabe Pins können nur Pixel übergreifende Alpha YUV-Formate wie z. b. ayuv, AI44 und IA44 akzeptieren.
-   Keiner der Eingabe Pins von VMR kann RGB-Formate annehmen.
-   Die von der Anwendung bereitgestellten Bitmap-Bilder können nicht mehr mit dem Video kombiniert werden, bevor die Darstellung der Anzeige angezeigt wird.
-   Einzelne untergeordnete Datenströme können nicht horizontal oder vertikal mithilfe der Funktionen des VMR-Mischers "Ausgabe Rechteck" invertiert werden. Die Neupositionierung und Neudimensionierung von Datenströmen wird unterstützt.
-   Die Hintergrundfarbe für das Mischen (angegeben durch [**ivmrmixercontrol:: setbackgroundclr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) ist nach wie vor im RGB-Farbraum angegeben, ebenso wie im RGB-Mischungs Modus.

**Configuration**

Anwendungen müssen VMR explizit so konfigurieren, dass Sie den YUV-Mischungs Modus nutzen. der ursprüngliche RGB-Mischungs Modus bleibt der standardmäßige Mischungs Modus. Um den YUV-Mischungs Modus in VMR-7 zu aktivieren, rufen Sie [**ivmrmixercontrol:: setmixingprefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) mit dem Flag mixerpref \_ rendertargetyuv auf. Dieser Rückruf muss erfolgen, bevor eine der VMR-Eingabe Pins verbunden ist. Um den YUV-Mischungs Modus in VMR-9 zu aktivieren, rufen Sie [**IVMRMixerControl9:: setmixingprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) mit dem MixerPref9 \_ rendertargetyuv-Flag auf.

Die einzige Möglichkeit, zu bestimmen, ob VMR-7 den neuen YUV-Mischungs Modus unterstützt, besteht darin, den VMR in diesem Modus festzulegen. Wenn der-Vorgang erfolgreich ist, können Sie den VMR bei Bedarf weiterhin in den RGB-Mischungs Modus versetzen. Nachdem Sie den YUV-Mischungs Modus festgelegt haben, kann der VMR nur wieder in den RGB-Mischungs Modus geändert werden, nachdem alle Eingabe Pins getrennt wurden.

Im YUV-Mischungs Modus können Sie die Auslastung der Grafikverarbeitungseinheit (GPU) verringern, indem Sie die folgenden Flags in der **setmixingprefs** -Methode anwenden:



| Flag                                                                                 | Beschreibung                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| VMR-7: mixerpref \_ dynamicswitchumbobvmr-9: MixerPref9 \_ dynamicswitchto Bob<br/> | Wechseln Sie zu Bob Deinterlacing.                                     |
| VMR-7: mixerpref \_ DynamicDecimateBy2VMR-9: mixerpref \_ DynamicDecimateBy2<br/>  | Dezimieren Sie das Bild mit dem Faktor 2 horizontal und vertikal. |



 

Sie können diese Flags hinzufügen oder entfernen, während das Filter Diagramm ausgeführt wird. die Änderung wird angewendet, wenn der VMR-Mixer den nächsten Videoframe verfasst. Die Flags schließen sich nicht gegenseitig aus. Durch diese Einstellungen wird die Qualität des Abbilds reduziert, sodass Sie diese nur dann anwenden können, wenn die Videoqualität weniger wichtig ist – z. b. Wenn Videos in einem kleinen Teil der Benutzeroberfläche abgespielt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Mischungs Modus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




