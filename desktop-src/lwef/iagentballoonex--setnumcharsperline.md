---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098a89500606482914bfb31303a2cd79cac88f6d96d17abec58c75759f7abedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976460"
---
# <a name="iagentballoonexsetnumcharsperline"></a>IAgentBalloonEx::SetNumCharsPerLine

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

Legt die Anzahl der Zeichen pro Zeile fest, die im Wortsprechblasen des Zeichens angezeigt werden können.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.
-   Gibt E \_ INVALIDARG zurück, wenn der Parameter kleiner als acht ist.

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*
</dt> <dd>

Anzahl der Zeilen, die im Wortsprechblasen angezeigt werden sollen.

</dd> </dl>

Die Mindesteinstellung ist 8 und der Höchstwert 255. Wenn der in der [**Speak-**](speak-method.md) oder [**Think-Methode**](think-method.md) angegebene Text die Größe des aktuellen Sprechblasens überschreitet, führt der -Agent automatisch einen Bildlauf im Text in der Sprechblase durch.

Die Standardeinstellung basiert auf Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




