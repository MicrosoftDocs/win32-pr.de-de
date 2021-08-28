---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3951cd4a8593d5e043e1571cdf24e14fdd9d93aef690c057860c2889022aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848720"
---
# <a name="iagentballoonexsetnumlines"></a>IAgentBalloonEx::SetNumLines

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

Legt die Anzahl der Zeilen der Textausgabe fest, die im Wortsprechblasen des Zeichens angezeigt werden können.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.
-   Gibt E \_ INVALIDARG zurück, wenn der Parameter 0 (null) ist.

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*
</dt> <dd>

Anzahl der Zeilen, die im Wortsprechblasen angezeigt werden sollen.

</dd> </dl>

Die Mindesteinstellung ist 1 und der Höchstwert 128. Wenn der in der [**Speak-**](speak-method.md) oder [**Think-Methode**](think-method.md) angegebene Text die Größe des aktuellen Sprechblasens überschreitet, führt der -Agent automatisch einen Bildlauf im Text in der Sprechblase durch.

Diese Methode schlägt fehl, wenn das **SizeToText-Sprechblasenformat** festgelegt ist.

Die Standardeinstellung basiert auf Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)


 

 




