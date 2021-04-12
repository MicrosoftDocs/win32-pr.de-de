---
title: Iagentballoonex setnumcharsperline
description: Iagentballoonex setnumcharsperline
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310964"
---
# <a name="iagentballoonexsetnumcharsperline"></a>Iagentballoonex:: setnumcharsperline

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

Legt die Anzahl von Zeichen pro Zeile fest, die in der Wort Sprechblase des Zeichens angezeigt werden können.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.
-   Gibt E \_ invalidArg zurück, wenn der-Parameter kleiner als acht ist.

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lcharsperline*
</dt> <dd>

Anzahl der Zeilen, die in der Wort Sprechblase angezeigt werden sollen.

</dd> </dl>

Die minimale Einstellung ist 8, und der Höchstwert ist 255. Wenn der in der Sprech [**Methode oder**](think-method.md) der Methode "Sprache" angegebene Text die Größe der aktuellen Sprechblase überschreitet, führt der-Agent automatisch einen Bildlauf im Text der [**Sprech**](speak-method.md) Blase

Die Standardeinstellung basiert auf den Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: getnumcharsperline**](iagentballoon--getnumcharsperline.md)


 

 




