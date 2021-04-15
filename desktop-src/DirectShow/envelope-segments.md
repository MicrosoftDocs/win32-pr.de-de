---
description: Umschlag Segmente
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Umschlag Segmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521635"
---
# <a name="envelope-segments"></a>Umschlag Segmente

Eine Parameter Kurve besteht aus einem oder mehreren Umschlag Segmenten, die mithilfe der [**MP- \_ Umschlag \_ Segment**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) Struktur definiert werden. Diese Struktur enthält die folgenden Informationen:

-   Die Start-und Endzeiten.
-   Die Anfangs-und Endwerte.
-   Der Kurven Typen (linear, Square usw.).
-   Optionale Flags, die in Kürze beschrieben werden.

Der Client fügt einem Parameter Umschlag Segmente hinzu, indem er die [**imediaparams:: addenvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) -Methode aufrufen und ein Array von **MP- \_ Umschlag \_ Segment** Strukturen übergibt. Der Client sollte die Segmente in aufsteigender Zeitreihen Folge sortieren, bevor die-Methode aufgerufen wird. Beim Verarbeiten von Daten durch DMO können Sie sich vorstellen, dass der Parameter über die einzelnen Umschlag Segmente hinausgeht, z. b. ein Auto, das eine Reihe von Hügeln steuert. Die [**imediaparams:: GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) -Methode gibt den letzten Wert zurück.

Zwei benachbarte Segmente können eine Lücke zwischen Ihnen aufweisen. Während der Lücken behält der-Parameter seinen vorherigen Wert wie folgt bei:

-   Vor dem ersten Segment ist der Wert der neutrale Wert.
-   Zwischen Segmenten ist der Wert der Endwert des vorherigen Segments.
-   Nach dem letzten Segment verbleibt der Wert am Endwert dieses Segments.
-   Wenn der Client den DMO leert, wird der Wert auf den neutralen Wert zurückgesetzt.

Sie können ein Segment ändern, indem Sie eines der folgenden Flags festlegen:

-   MPF- \_ VLP \_ Begin \_ CurrentVal. Der DMO verwendet den letzten Wert des-Parameters als Startwert für das Segment. Dies kann der neutrale Wert oder der Endwert des vorherigen Segments sein. Der DMO ignoriert den **valstart** -Member der **MP- \_ Umschlag \_ Segment** Struktur.
-   MPF- \_ VLP \_ Begin \_ neutralval. Der DMO verwendet den neutralen Wert des-Parameters als Startwert für das Segment. " **Valstart**" wird ignoriert.

Sie können sich diese Flags vorstellen, wenn Sie den Startpunkt des Segments erfassen und nach oben oder unten verschieben, während der Endwert korrigiert bleibt. Das Segment wird entsprechend "gestreckt".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Parameter](media-parameters.md)
</dt> </dl>

 

 



