---
title: Iagentballoon getnumcharsperline
description: Iagentballoon getnumcharsperline
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037548"
---
# <a name="iagentballoongetnumcharsperline"></a>Iagentballoon:: getnumcharsperline

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

Ruft den Wert für die durchschnittliche Anzahl von Zeichen pro Zeile ab, die in einer Wort Sprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbcharsperline*
</dt> <dd>

Die Adresse einer Variablen, die die Anzahl der Zeichen pro Zeile empfängt.

</dd> </dl>

Der Microsoft-Agent-Server führt automatisch einen Bildlauf der Zeilen aus, die für die gesprochene Ausgabe in der Wort Blase Die durchschnittliche Anzahl von Zeichen pro Zeile für die Word-Sprechblase eines Zeichens wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: getnumlines**](iagentballoon--getnumlines.md)


 

 




