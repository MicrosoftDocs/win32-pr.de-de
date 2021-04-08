---
description: Um für jedes Erkennungs Ergebnis eine Vertrauens Ebene zu erhalten, können Sie entweder die Eigenschaft Vertrauen des Objekts "erkenntionalternate" oder die Eigenschaft "Vertrauen" des Gesten Objekts abrufen.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Confidence-Eigenschaft [Informationen zur Erkennung]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f436d17d5cb83901c7d19ef4beb6dfb7ce6199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861916"
---
# <a name="confidence-property-about-recognition"></a>Vertrauens Eigenschaft \[ für die Erkennung\]

Um für jedes Erkennungs Ergebnis eine Vertrauens Ebene zu erhalten, können Sie entweder die Eigenschaft [**Vertrauen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) des Objekts " [**erkenntionalternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) " oder die Eigenschaft " [**Vertrauen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) " des [**Gesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) Objekts abrufen. Der Vertrauensgrad ist eine Zahl, die den Grad der Vertrauenswürdigkeit für jedes Alternative Erkennungs Ergebnis angibt, das die Erkennung für ein entsprechendes Erkennungs Segment zurückgibt.

Das Vertrauen wird als niedrig, Mittelwert oder hoch zurückgegeben. Die Anwendung verwendet folgende Ergebnisse:

-   Geben Sie dem Benutzer an, dass mehrere Möglichkeiten vorhanden sind.
-   Ordnen Sie die Alternativen nach Vertrauensgrad zu.

## <a name="what-affects-confidence"></a>Auswirkungen auf das Vertrauen

Einige der Dinge, die die Handschrifterkennung erschweren und die Zuversicht beeinflussen, sind:

-   Schwierigkeiten beim Bestimmen der Wort Segmentierung

![Bild, das die zu schließende Schreibvorgänge anzeigt](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   Fall Schwierigkeiten

![Bild, das Schwierigkeiten mit handschriftlichen Versionen des Worts "Case" anzeigt](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   Ungewöhnliche Schreibstile
-   Isoliertes Satzzeichen

![Bild, das Anführungszeichen anzeigt, die zu weit von Text entfernt sind](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   Zeichen mit Akzent in englischer Sprache

> [!Note]  
> Die vertrauensbewertung ist nur für USA Englisch und alle Gesten erkenzer in dieser Version verfügbar. Methoden, die die Eigenschaft "Vertrauen" für alle anderen erkenungen bereitstellen, geben " **E \_ notimpl**" zurück.

 

 

 



