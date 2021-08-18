---
description: Eine Erkennung kann mehrere Möglichkeiten finden, ein Ink-Beispiel in Erkennungssegmente zu unterteilen. Aus diesem Grund kann die Anzahl der Erkennungs alternativer Erkennungen auch für eine kleine Ink-Stichprobe gestaffelt sein.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Ink Segments and Alternates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 702c2da4984afd22490827acdf65962abc789d7ad9f0ddab3e602bc688ac6542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883990"
---
# <a name="ink-segments-and-alternates"></a>Ink Segments and Alternates

Eine Erkennung kann mehrere Möglichkeiten finden, ein Ink-Beispiel in Erkennungssegmente zu unterteilen. Aus diesem Grund kann die Anzahl der Erkennungs alternativer Erkennungen auch für eine kleine Ink-Stichprobe gestaffelt sein.

Beispielsweise kann "t o g e t h e r" die folgenden Ergebnisse liefern:

-   "to get her" (plus Alternativen für jedes Wort)
-   "to gather" (plus Alternativen für jedes Wort)
-   "tog ether" (plus Alternativen für jedes Wort)
-   "tog at her" (plus Alternativen für jedes Wort)
-   "together" (plus Alternativen für das Wort)

Das [**RecognitionResult-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) unterstützt die effiziente Speicherung vollständiger Erkennungsergebnisse innerhalb des [**Ink-Objekts.**](inkdisp-class.md) Das **Ink-Objekt** ordnet die Erkennungsverwechselungen den Strichen im **Ink-Objekt** zu und kann auch andere Informationen wie Baselineposition, Zeilenindizes und Sprachbereiche enthalten.

 

 



