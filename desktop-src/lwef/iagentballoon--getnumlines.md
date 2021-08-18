---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461ebc4fa7c7e0ae9080544e9114db9f8c179925dae665925d893288f95de027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478624"
---
# <a name="iagentballoongetnumlines"></a>IAgentBalloon::GetNumLines

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

Ruft den Wert der Anzahl der Zeilen ab, die in einer Wortsprechblase angezeigt werden.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*
</dt> <dd>

Die Adresse einer Variablen, die die Anzahl der angezeigten Zeilen empfängt.

</dd> </dl>

Der Microsoft-Agent-Server führt automatisch einen Bildlauf in den Zeilen durch, die für die gesprochene Ausgabe im Wortsprechblasen angezeigt werden. Die Anzahl der Zeilen für eine Zeichenwortsprechblase wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




