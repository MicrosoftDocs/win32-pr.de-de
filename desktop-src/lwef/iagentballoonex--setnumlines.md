---
title: Iagentballoonex-setnumlines
description: Iagentballoonex-setnumlines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471580"
---
# <a name="iagentballoonexsetnumlines"></a>Iagentballoonex:: setnumlines

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

Legt die Anzahl von Textausgabe Zeilen fest, die in der Wort Sprechblase des Zeichens angezeigt werden können.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.
-   Gibt E \_ invalidArg zurück, wenn der-Parameter NULL ist.

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*llines*
</dt> <dd>

Anzahl der Zeilen, die in der Wort Sprechblase angezeigt werden sollen.

</dd> </dl>

Die minimale Einstellung ist 1 und der Höchstwert 128. Wenn der in der Sprech [**Methode oder**](think-method.md) der Methode "Sprache" angegebene Text die Größe der aktuellen Sprechblase überschreitet, führt der-Agent automatisch einen Bildlauf im Text der [**Sprech**](speak-method.md) Blase

Bei dieser Methode tritt ein Fehler auf, wenn das **QuickInfo** -Sprechblasen-Stilbit festgelegt ist.

Die Standardeinstellung basiert auf den Einstellungen, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: getnumlines**](iagentballoon--getnumlines.md), [**iagentballoonex:: GetStyle**](iagentballoonex--getstyle.md), [**iagentballoonex:: SetStyle**](iagentballoonex--setstyle.md)


 

 




