---
description: Eine Erkennung kann verschiedene Möglichkeiten finden, ein Ink-Beispiel in Erkennungs Segmente zu unterteilen. Daher kann die Anzahl der Erkennungs Alternativen auch für ein kleines frei Hand Beispiel sehr erstaunlich sein.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Frei Hand Segmente und-Alternativen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041705"
---
# <a name="ink-segments-and-alternates"></a>Frei Hand Segmente und-Alternativen

Eine Erkennung kann verschiedene Möglichkeiten finden, ein Ink-Beispiel in Erkennungs Segmente zu unterteilen. Daher kann die Anzahl der Erkennungs Alternativen auch für ein kleines frei Hand Beispiel sehr erstaunlich sein.

Beispielsweise kann "t o g e t h e r" die folgenden Ergebnisse liefern:

-   "um Sie zu erhalten" (plus Alternativen für jedes Wort)
-   "to Gather" (plus-Alternativen für jedes Wort)
-   "ein-oder-Äther" (Pluszeichen für jedes Wort)
-   "ein/aus" (plus Schalter für jedes Wort)
-   "zusammen" (plus Alternativen für das Wort)

Das [**erkentionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt unterstützt die effiziente Speicherung vollständiger Erkennungsergebnisse innerhalb des [**Ink**](inkdisp-class.md) -Objekts. Das **Ink** -Objekt ordnet die Erkennungs Alternativen den Strichen im **Ink** -Objekt zu und kann auch andere Informationen enthalten, wie z. b. baselineposition, Linien Indizes und Sprachbereiche.

 

 



