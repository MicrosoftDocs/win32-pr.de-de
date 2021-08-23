---
description: Um ein Vertrauensniveau für jedes Erkennungsergebnis zu erhalten, können Sie entweder die Confidence-Eigenschaft des RecognitionAlternate-Objekts oder die Confidence-Eigenschaft des Gesture-Objekts abrufen.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Confidence-Eigenschaft [Informationen zur Erkennung]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3316e9637fe6dcf820f8412724363a25dab65ce9a291b8c3c70c5bcf9c83bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093029"
---
# <a name="confidence-property-about-recognition"></a>Confidence-Eigenschaft \[ zur Erkennung\]

Um ein Vertrauensniveau für jedes Erkennungsergebnis zu erhalten, können Sie entweder die [**Confidence-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) des [**RecognitionAlternate-Objekts**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) oder die [**Confidence-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) des [**Gesture-Objekts**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) abrufen. Der Konfidenzgrad ist eine Zahl, die den Grad der Konfidenz für jedes alternative Erkennungsergebnis angibt, das die Erkennung für ein entsprechendes Erkennungssegment zurückgibt.

Die Zuverlässigkeit wird als niedrig, durchschnittlich oder hoch zurückgegeben. Die Anwendung verwendet diese Ergebnisse für Folgendes:

-   Geben Sie dem Benutzer an, dass mehrere Möglichkeiten vorhanden sind.
-   Ordnen Sie die Alternativen nach Konfidenzgrad an.

## <a name="what-affects-confidence"></a>Was wirkt sich auf die Zuverlässigkeit aus?

Folgende Punkte erschweren die Handschrifterkennung und wirken sich auf die Zuverlässigkeit aus:

-   Schwierigkeiten beim Bestimmen der Wortsegmentierung

![Bild, das das Schreiben zeigt, das zu nah ist](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   Probleme bei Der Fall

![Abbildung, die Probleme mit handschriftlichen Versionen des Worts "Case" zeigt](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   Ungewöhnliche Schreibstile
-   Isolierte Interpunktion

![Abbildung mit Anführungszeichen, die zu weit vom Text entfernt sind](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   Akzentzeichen in englischen Erkennungen

> [!Note]  
> Die Zuverlässigkeitsauswertung ist nur für USA Englisch und alle Gestenerkennungen in dieser Version verfügbar. Methoden, die die Konfidenzeigenschaft für jede andere Erkennung bereitstellen, geben **E \_ NOTIMPL** zurück.

 

 

 



