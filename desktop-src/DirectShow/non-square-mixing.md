---
description: Nicht quadratische Mischung
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Nicht quadratische Mischung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4674891b7b9d44cb35522b6040723bc71436d677b10a4326d9f00a269ce3aff2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102410"
---
# <a name="non-square-mixing"></a>Nicht quadratische Mischung

Dieses Thema gilt für Windows XP Service Pack 2 oder höher.

Wenn VMR-9 zwei oder mehr Streams kombiniert, gibt es zwei Punkte, an denen die Skalierung erfolgen kann: Wenn der Mixer die Eingabestreams zusammengesetzt, und wenn der Allocator-Presenter das zusammengesetzte Bild rendert.

![VMR-Mischungsvorgänge](images/vmr-nonsquare-mixing.png)

In früheren Versionen von VMR-9 wurden die Eingabestreams immer mit einem quadratischen (1:1) Pixel-Seitenverhältnis (PAR) zusammengesetzt, auch wenn es nur einen einzelnen Videostream gab. Wenn der Eingabestream nicht quadratische Pixel auf hatte, verursachte dies einen unnötigen Skalierungsvorgang. Die Skalierung sollte natürlich so weit wie möglich vermieden werden, da sie die endgültige Qualität des Images beeinträchtigt.

Ab Windows XP Service Pack 2 unterstützt VMR-9 zwei verschiedene Möglichkeiten, um das Problem der doppelten Skalierung zu vermeiden:

-   Implementieren Sie eine benutzerdefinierte Allocator-Presenter-Schnittstelle, und unterstützen Sie die [**IVMRSurfaceAllocatorEx9-Schnittstelle.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9)
-   Verwenden Sie den Nicht-Quadrat-Mischungsmodus.

In diesem Abschnitt wird der nicht quadratische Mischungsmodus beschrieben. Anwendungen können beide Techniken kombinieren.

**Funktionsweise von nicht quadratischem Mischen**

Im nicht quadratischen Mischungsmodus wählt VMR-9 einen Eingabestream als Zielgröße und PAR aus. Der Mixer des virtuellen Computers skaliert das Video aus diesem Stream oder aus anderen Streams mit der gleichen Imagegröße und PAR nicht. Streams mit einer anderen Größe oder einem anderen Seitenverhältnis werden so skaliert, dass sie dem Ziel-PAR und letterboxed an die endgültige Größe des Ausgabebilds passen.

Die Auswahl der Streams hängt vom aktuellen Mischungsmodus ab:

-   Der YUV-Mischungsmodus ist auf einen Videostream an Pin 0 beschränkt. (Die anderen Stecknadeln können Unterbild- oder Untertitelstreams enthalten.) Daher wählt VMR-9 immer Pin 0 für die Größe des Zielimages und PAR aus.
-   Im RGB-Mischungsmodus wählt der VMR den Stream mit der größten Bildgröße aus. Wenn es mehrere gibt, wird die mit der höchsten Z-Reihenfolge ausgewählt. Und wenn immer noch ein Unentschieden vor sich geht, wird der Stream mit der niedrigsten Pinnummer ausgewählt.

**Beispiele für den Vorgang**

**1. Beispiel:** Stream 0 ist 720 x 480 Pixel mit einem Bildbild-Seitenverhältnis von 16:9. Stream 1 ist ein 640 x 480 Pixel mit einem Bildbild-Seitenverhältnis von 4:3.

In diesem Beispiel hat Stream 0 die größte Bildgröße, sodass der VMR diesen Stream unabhängig vom RGB-Mischungsmodus oder YUB-Mischungsmodus auswählt. Der PAR ist 32:27 (16:9 / 720:480), was bedeutet, dass das Bild horizontal um dieses Verhältnis gestreckt werden muss, um das richtige Seitenverhältnis von 16:9 zu erzeugen.

Zur Übereinstimmung mit dem Ziel-PAR skaliert der VMR-Mixer Stream 1 um das umgekehrte Verhältnis (27:32), was zu einem Bild von 540 x 480 führt. Die beiden Streams werden dann auf einer Oberfläche zusammengesetzt. Um das resultierende Bild korrekt anzuzeigen, muss die Zuweisungsanzeige das Bild horizontal strecken, damit es dem Seitenverhältnis von 16:9 des Bilds passt.

![Beispiel 1.](images/vmr-nonsquare-mixing2.png)

**2. Beispiel:** Stream 0 ist 720 x 480 Pixel mit einem Bildbild-Seitenverhältnis von 16:9. Stream 1 ist ein 1024 x 768 Pixel mit einem Bildbild-Seitenverhältnis von 4:3.

Wenn VMR-9 den YUV-Mischungsmodus verwendet, wird immer Stream 0 ausgewählt. Daher wird stream 1 auf 540 x 480 Pixel gestreckt, um dem PAR von Stream 0 zu passen.

Wenn VMR-9 den RGB-Mischungsmodus verwendet, wählt er Stream 1 als Ziel aus, da dieser Stream die größte Bildgröße hat. Stream 0 wird auf eine Bildgröße von 1.024 x 576 Pixel gestreckt. Beachten Sie, dass das zusammengesetzte Bild in diesem Fall einen PAR-1:1-Beschriftungswert hat, sodass der Allocator-Presenter nicht für nicht quadratische Pixel korrigieren muss. (Möglicherweise muss das Video trotzdem gestreckt werden, um das Zielrechteck zu berücksichtigen.)

**Verwenden des nicht quadratischen Mischungsmodus**

Der nicht quadratische Mischungsmodus wird empfohlen, wenn eine der folgenden Bedingungen zutrifft:

-   Ihre Anwendung sendet nie mehr als einen Videostream an VMR-9.
-   Ihre Anwendung rendert DVD-, Fernseh- oder ms-dvr-Dateien. Sie sollten in diesem Fall auch den YUV-Mischungsmodus verwenden, wenn die Grafikhardware dies unterstützt.

Wenn Ihre Anwendung mehrere Videostreams gemischt, die unterschiedliche Bildgrößen oder Pixel-Seitenverhältnisse haben können, wird der standardmäßige quadratische Mischungsmodus empfohlen.

Um den nicht quadratischen Mischungsmodus zu konfigurieren, muss das Filterdiagramm beendet und alle Eingabepins auf vmr-9 getrennt werden. Rufen Sie [**dann IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) mit dem MixerPref9 \_ NonSquareMixing-Flag auf:


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> Wenn Sie das MixerPref9 \_ NonSquareMixing-Flag mit dem MixerPref9-Flag \_ ARAdjustXorY kombinieren, ignoriert VMR-9 das MixerPref9-Flag \_ ARAdjustXorY.

 

Wenn Ihre Anwendung einen benutzerdefinierten Allocator-Presenter mit nicht quadratischem Mischungsmodus verwendet, beachten Sie, dass das zusammengesetzte Bild möglicherweise ein nicht quadratisches PAR hat. Der Allocator-Presenter muss das Bild auf ein quadratisches (1:1) PAR skalieren.

**Statische Bitmaps**

Wenn Sie die [**IVMRMixerBitmap9-Schnittstelle**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) verwenden, um eine statische Bitmap in das Video zu mischen, sollten Sie die Bitmap als zweiten Videostream für den VMR-Gemischtmodus betrachten.

Die VMR behandelt die Bitmap so, als habe sie den gleichen PAR wie das Ziel. Die Bitmap wird nicht skaliert, um das Pixel-Seitenverhältnis des Ziels anzupassen. In der Standardkonfiguration des virtuellen Computers hat das Ziel einen 1:1 PAR, der den meisten Bitmaps entspricht. Im nicht quadratischen Mischungsmodus kann das Ziel nicht quadratische Pixel aufweisen. Um sicherzustellen, dass die Bitmap ordnungsgemäß angezeigt wird, sollte die Anwendung ein Bild angeben, dessen PAR dem Ziel-PAR entspricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Gemischtmodus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



