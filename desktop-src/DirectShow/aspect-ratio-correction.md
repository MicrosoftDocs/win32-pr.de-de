---
description: Seitenverhältnis Korrektur
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: Seitenverhältnis Korrektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342561"
---
# <a name="aspect-ratio-correction"></a>Seitenverhältnis Korrektur

Dieses Thema gilt für Windows XP Service Pack 2 oder höher.

Im Mischungs Modus wird das Video von VMR auf das richtige Seitenverhältnis fest. (Ausnahme: siehe [nicht quadratische Vermischung](non-square-mixing.md).) Dies erfordert möglicherweise die Streckung des Videos, wenn das gewünschte Seitenverhältnis nicht mit dem physischen Seitenverhältnis des Bilds identisch ist. Das Format Digital Video (DV) lautet z. b. 720 x 480 Pixel (3:2), sollte jedoch mit einem 4:3-Seitenverhältnis angezeigt werden.

VMR unterstützt zwei verschiedene Verhaltensweisen für die Seitenverhältnis Korrektur:

-   Passen Sie die horizontale oder vertikale Größe an, damit das Bild immer gestreckt und nie verkleinert wird. Dies ist nun das Standardverhalten.
-   Passen Sie die horizontale Größe an, indem Sie das Video entweder Strecken oder verkleinern.

Da das zweite Verhalten (nur horizontale Anpassung) das Verkleinern des Videos verursachen kann, kann das Ausgabe Bild weniger aufgelöst werden. Aus diesem Grund wird das erste Verhalten bevorzugt. Beispielsweise erzeugt das Standardverhalten im Fall von 720 x 480-Video mit 4:3 Seitenverhältnis ein 720 x 550-Image, während die horizontale Anpassung ein kleineres 640 x 480-Image erzeugt.

**VMR-7**: um die Einstellung für die Seitenverhältnis Korrektur festzulegen, rufen Sie [**ivmrmixercontrol:: setmixingprefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect)auf. Legen Sie das Flag "aranpassxory" für "mixerpref" \_ auf das Standardverhalten fest, oder löschen Sie dieses Flag nur für die horizontale Anpassung.

**VMR-9**: um die Einstellung für die Seitenverhältnis Korrektur festzulegen, rufen Sie [**IVMRMixerControl9:: setmixingprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs)auf. Legen Sie das \_ Flag "MixerPref9 aranpassxory" für das Standardverhalten fest, oder löschen Sie dieses Flag nur für die horizontale Anpassung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Mischungs Modus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



