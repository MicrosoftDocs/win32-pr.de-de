---
description: Nicht quadratische Vermischung
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Nicht quadratische Vermischung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522051"
---
# <a name="non-square-mixing"></a>Nicht quadratische Vermischung

Dieses Thema gilt für Windows XP Service Pack 2 oder höher.

Wenn VMR-9 zwei oder mehr Streams kombiniert, gibt es zwei Punkte, an denen die Skalierung stattfinden kann: Wenn der Mixer die Eingabestreams zusammensetzt und der zuordnerpresenter das zusammengesetzte Bild rendert.

![VMR-Mischungs Vorgänge](images/vmr-nonsquare-mixing.png)

In früheren Versionen von VMR-9 wurden die Eingabedaten Ströme stets mithilfe eines quadratischen (1:1) Pixel Seitenverhältnisses (par) zusammengesetzt, auch wenn nur ein einzelner Videostream vorhanden war. Wenn der Eingabedaten Strom nicht quadratische Pixel enthielt, verursachte dies einen unnötigen Skalierungs Vorgang. Die Skalierung sollte so weit wie möglich vermieden werden, da Sie die endgültige Bildqualität beeinträchtigt.

Ab Windows XP Service Pack 2 unterstützt VMR-9 zwei verschiedene Möglichkeiten, um das Problem der doppelten Skalierung zu vermeiden:

-   Implementieren Sie einen benutzerdefinierten Zuweiser und unterstützen Sie die [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) -Schnittstelle.
-   Verwenden Sie den nicht quadratischen Mischungs Modus.

In diesem Abschnitt wird der nicht quadratische Mischungs Modus beschrieben. Beide Verfahren können von Anwendungen kombiniert werden.

**Funktionsweise der nicht quadratischen Vermischung**

Im nicht quadratischen Mischungs Modus wählt VMR-9 einen Eingabedaten Strom als Zielgröße und par aus. Der Mixer von VMR skaliert das Video nicht aus diesem Stream oder aus anderen Streams mit der gleichen Bildgröße und dem gleichen Wert. Datenströme mit einer anderen Größe oder einem anderen Seitenverhältnis werden so skaliert, dass Sie mit der Ziel Größe übereinstimmen, die der Größe des endgültigen Ausgabe Bilds entspricht.

Die Auswahl der Streams hängt vom aktuellen Mischungs Modus ab:

-   Der YUV-Mischungs Modus ist auf einen Videodaten Strom auf Pin 0 beschränkt. (Die anderen Pins können über untergeordnete oder geschlossene Beschriftungs Datenströme verfügen.) Daher wählt VMR-9 immer Pin 0 für die zielbildgröße und-Größe aus.
-   Im RGB-Mischungs Modus wählt der VMR den Stream mit der größten Bildgröße aus. Wenn mehr als ein Wert vorhanden ist, wählt er den Wert mit der höchsten z-Reihenfolge aus. und wenn immer noch eine Verknüpfung vorhanden ist, wird der Stream mit der niedrigsten PIN-Nummer ausgewählt.

**Beispiele für Vorgänge**

**1. Beispiel:** Stream 0 ist 720 x 480 Pixel mit einem Bildseiten Verhältnis von 16:9. Stream 1 ist ein 640 x 480 Pixel mit einem Bildseiten Verhältnis von 4:3.

In diesem Beispiel hat Stream 0 die größte Bildgröße. Daher wählt VMR diesen Stream aus, unabhängig vom RGB-Mischungs Modus oder dem yub-Mischungs Modus. Die par ist 32:27 (16:9/720:480). das bedeutet, dass das Bild horizontal durch dieses Verhältnis gestreckt werden muss, um das richtige 16:9 Bildseiten Verhältnis zu schaffen.

Um dem Zielwert zu entsprechen, skaliert der VMR-Mixer den Stream 1 mit dem umgekehrten Verhältnis (27:32), was zu einem 540 x 480-Bild führt. Die beiden Streams werden dann auf eine Oberfläche zusammengesetzt. Um das resultierende Bild ordnungsgemäß anzuzeigen, muss der zuordnerpräsentator das Bild horizontal Strecken, um das Seitenverhältnis von 16:9 Bild anzupassen.

![Beispiel 1.](images/vmr-nonsquare-mixing2.png)

**2. Beispiel:** Stream 0 ist 720 x 480 Pixel mit einem Bildseiten Verhältnis von 16:9. Stream 1 ist ein 1024 x 768 Pixel mit einem Bildseiten Verhältnis von 4:3.

Wenn VMR-9 den YUV-Mischungs Modus verwendet, wählt er immer Stream 0 aus. Daher wird der Stream 1 auf 540 x 480 Pixel gestreckt, sodass er mit dem par von Stream 0 übereinstimmt.

Wenn VMR-9 den RGB-Mischungs Modus verwendet, wählt er Stream 1 als Ziel aus, da dieser Stream die größte Bildgröße aufweist. Der Stream 0 wird auf eine Bildgröße von 1024 x 576 Pixel gestreckt. Beachten Sie, dass das zusammengesetzte Image in diesem Fall ein par von 1:1 hat, sodass der Zuordnungs-Presenter nicht für nicht quadratische Pixel korrekt ist. (Möglicherweise muss das Video nach wie vor für das Ziel Rechteck gestreckt werden.)

**Verwenden des nicht quadratischen Mischungs Modus**

Der nicht quadratische Mischungs Modus wird empfohlen, wenn eine der folgenden Bedingungen zutrifft:

-   Die Anwendung sendet nie mehr als einen Videodaten Strom an VMR-9.
-   Ihre Anwendung rendert DVD-, Fernseh-oder MS-DVR-Dateien. Sie sollten in diesem Fall auch den YUV-Mischungs Modus verwenden, wenn er von der Grafikhardware unterstützt wird.

Wenn Ihre Anwendung mehrere Videostreams mit unterschiedlichen Bildgrößen oder Pixel Seitenverhältnissen kombiniert, wird der standardmäßige quadratische Mischungs Modus empfohlen.

Um den nicht quadratischen Mischungs Modus zu konfigurieren, muss das Filter Diagramm angehalten werden, und alle Eingabe Pins sind auf VMR-9 getrennt. Rufen Sie dann [**IVMRMixerControl9:: setmixingprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) mit dem MixerPref9 \_ nonsquaremischungsflag auf:


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> Wenn Sie das MixerPref9 \_ nonsquaremischungsflag mit dem MixerPref9 \_ arsexory-Flag kombinieren, ignoriert VMR-9 das MixerPref9 \_ arsexory-Flag.

 

Wenn Ihre Anwendung einen benutzerdefinierten zuordnerpräsentator mit einem nicht quadratischen Mischungs Modus verwendet, beachten Sie, dass das zusammengesetzte Bild möglicherweise eine nicht quadratische par-ID hat. Der zuordnerpräsentator muss das Bild auf einen quadratischen (1:1) par skalieren.

**Statische Bitmaps**

Wenn Sie die [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) -Schnittstelle verwenden, um eine statische Bitmap in das Video zu mischen, sollten Sie die Bitmap als zweiten Videostream für den VMR-Mischungs Modus in Erwägung ziehen.

Die Bitmap wird von VMR als identisch mit dem Ziel behandelt. Die Bitmap wird nicht skaliert, um das Pixel Seitenverhältnis des Ziels anzupassen. In der Standardkonfiguration von VMR hat das Ziel eine 1:1-Entsprechung, die den meisten Bitmaps entspricht. Im nicht quadratischen Mischungs Modus hat das Ziel möglicherweise nicht eckige Pixel. Um sicherzustellen, dass die Bitmap ordnungsgemäß angezeigt wird, sollte die Anwendung ein Bild bereitstellen, dessen par der Ziel-par entspricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Mischungs Modus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



