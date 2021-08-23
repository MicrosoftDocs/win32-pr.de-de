---
description: YUV-Mischungsmodus
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: YUV-Mischungsmodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 957c5345eb80576ad0371558bb60d0b6651221bd98d7830cb968f39c16330fb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290750"
---
# <a name="yuv-mixing-mode"></a>YUV-Mischungsmodus

Dieses Thema gilt für Windows XP Service Pack 2 oder höher.

Ab Windows XP Service Pack 2 unterstützt der VMR einen Gemischtmodus namens YUV-Mischungsmodus. Dieser Modus ist besonders nützlich für erweiterte TV- oder DVD-Anwendungen. Ein Teil der Leistungsfähigkeit des VMR-Mixers wird auf Low-End-Grafikhardware, die einen einheitlichen Speicherarchitekturentwurf verwendet, um eine bessere Leistung zu erzielen. Der YUV-Mischungsmodus wird sowohl für VMR-7 als auch für VMR-9 unterstützt.

**Vorteile**

Der YUV-Mischungsmodus hat im Hinblick auf die Renderingleistung gegenüber dem ursprünglichen RGB-Mischungsmodus, der von der VMR unterstützt wird, mehrere Vorteile:

-   Wenn sich die VMR im YUV-Mischungsmodus befindet, werden alle De-Interlacing- und Videostream-Kompositionsvorgänge im YUV-Farbraum ausgeführt. YUV-Oberflächen erfordern in der Regel zwischen 50 % und 60 % weniger Arbeitsspeicherbandbreite als entsprechende RGB-Oberflächen.
-   Die Deinterlacing- und Streamkomposition werden durch einen einzelnen Aufruf des Grafiktreibers ausgeführt. Der Treiber kann die Multitexturfunktionen der Grafikhardware verwenden, was zu zusätzlichen Einsparungen bei der Arbeitsspeicherbandbreite führt.

Obwohl jede Videoanwendung den YUV-Mischungsmodus verwenden kann, ist sie in erster Linie für zwei Arten von Videowiedergabeanwendung vorgesehen:

1.  TV-Anwendungen, die Untertitel oder Teletext anzeigen.
2.  DVD-Anwendungen zeigen DVD-Unterabbilddaten oder Untertitel an.

**Einschränkungen**

Die VMR erzwingt eine Reihe von Einschränkungen, wenn sie in den YUV-Gemischtmodus wechseln:

-   Stream 0 (der stream connected to Input Pin 0) kann progressiv oder interlaced sein. alle anderen Streams müssen progressiv sein.
-   GUID \_ NULL (Webmodus) ist für Stream 0 nicht zulässig.
-   DeinterlacePref Weave kann nicht als Fallbackmodus verwendet werden, da dies verhindern könnte, dass ein \_ Deinterlace-Gerät erstellt wird. Der YUV-Mischungsmodus erfordert ein Deinterlace-Gerät, auch wenn das eingehende Video nicht verschachtelt ist.
-   Es können keine Änderungen am planaren Alphawert vorgenommen werden, der jedem VMR-Eingabestream zugeordnet ist.
-   Der Benutzer kann die Z-Reihenfolge der verbundenen Videostreams nicht ändern. Die Standardmäßige Z-Reihenfolge wird aus der Pin-Reihenfolge übernommen.
-   Die Farbschlüsselung wird nicht unterstützt.
-   Der Eingabepin 0 muss den Videostream empfangen.
-   Die anderen Eingabepins können nur Videounterdatenstromdaten empfangen, z. B. DVD-Unterbild, Untertitel oder Teletext.
-   Die anderen Eingabepins können nur alpha-YUV-Formate pro Pixel akzeptieren, z. B. AYUV, AI44 und IA44.
-   Keiner der VMR-Eingabepins kann RGB-Formate akzeptieren.
-   Von der Anwendung bereitgestellte Bitmapbilder können vor der Präsentation nicht mehr mit dem Video kombiniert werden.
-   Einzelne Unterstreams können nicht horizontal oder vertikal mithilfe der "Ausgaberechteck"-Funktionen des VMR-Mixers invertiert werden. Eine "normale" Neupositionierung und Größenbestimmung des Streams wird unterstützt.
-   Die mischende Hintergrundfarbe (angegeben durch [**IVMRMixerControl::SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) wird weiterhin im RGB-Farbraum angegeben, genau wie im RGB-Mischungsmodus.

**Configuration**

Anwendungen müssen die VMR explizit konfigurieren, um den YUV-Mischungsmodus nutzen zu können. Der ursprüngliche RGB-Mischungsmodus bleibt der Standardmischungsmodus. Um den YUV-Mischungsmodus in VMR-7 zu aktivieren, rufen Sie [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) mit dem MixerPref-Flag \_ RenderTargetYUV auf. Dieser Aufruf muss ausgeführt werden, bevor die Eingabepins des virtuellen Computers verbunden sind. Um den YUV-Mischungsmodus in VMR-9 zu aktivieren, rufen Sie [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) mit dem MixerPref9-Flag \_ RenderTargetYUV auf.

Die einzige Möglichkeit, zu ermitteln, ob VMR-7 den neuen YUV-Gemischtmodus unterstützt, besteht im Versuch, die VMR in diesen Modus zu setzen. Wenn der Aufruf erfolgreich ist, können Sie die VMR bei Bedarf wieder in den RGB-Mischungsmodus setzen. Nachdem der VMR in den YUV-Mischungsmodus gesetzt wurde, kann er erst wieder in den RGB-Mischungsmodus geändert werden, nachdem alle Eingabepins getrennt wurden.

Im YUV-Gemischtmodus können Sie die Last der Grafikprozessor (GPU) verringern, indem Sie die folgenden Flags in der **SetMixingPrefs-Methode** anwenden:



| Flag                                                                                 | Beschreibung                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| VMR-7: MixerPref \_ DynamicSwitchToBOBVMR-9: MixerPref9 \_ DynamicSwitchToBOB<br/> | Wechseln Sie zu bob deinterlacing.                                     |
| VMR-7: MixerPref \_ DynamicDecimateBy2VMR-9: MixerPref \_ DynamicDecimateBy2<br/>  | Dezimieren Sie das Bild um den Faktor 2 horizontal und vertikal. |



 

Sie können diese Flags hinzufügen oder entfernen, während das Filterdiagramm ausgeführt wird. Die Änderung wird angewendet, wenn der VMR-Mixer den nächsten Videoframe erstellt. Die Flags schließen sich nicht gegenseitig aus. Diese Einstellungen verringern die Qualität des Bilds, daher würden Sie sie in der Regel nur anwenden, wenn die Videoqualität weniger wichtig ist, z. B. wenn Das Video in einem kleinen Teil der Benutzeroberfläche abspielt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Gemischtmodus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




