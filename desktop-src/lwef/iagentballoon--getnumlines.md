---
title: Iagentballoon getnumlines
description: Iagentballoon getnumlines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388716"
---
# <a name="iagentballoongetnumlines"></a>Iagentballoon:: getnumlines

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

Ruft den Wert der Anzahl der Zeilen ab, die in einer Wort Sprechblase angezeigt werden.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pclines*
</dt> <dd>

Die Adresse einer Variablen, die die Anzahl der angezeigten Zeilen erhält.

</dd> </dl>

Der Microsoft-Agent-Server führt automatisch einen Bildlauf der Zeilen aus, die für die gesprochene Ausgabe in der Wort Blase Die Anzahl der Zeilen für eine Zeichen Wort Sprechblase wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: getnumcharsperline**](iagentballoon--getnumcharsperline.md)


 

 




