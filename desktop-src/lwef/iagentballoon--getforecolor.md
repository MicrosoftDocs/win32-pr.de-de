---
title: Iagentballoon getForeColor
description: Iagentballoon getForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341677"
---
# <a name="iagentballoongetforecolor"></a>Iagentballoon:: getForeColor

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

Ruft den Wert für die Vordergrundfarbe ab, die in einer Wort Sprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*PLF-Farbe*
</dt> <dd>

Die Adresse einer Variablen, die die Farbeinstellung für den Sprechblasen-Vordergrund empfängt.

</dd> </dl>

Die in einer Wort Sprechblase verwendete Vordergrundfarbe wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden. Der Benutzer kann jedoch die Vordergrundfarbe der Wort Ballons für alle Zeichen über die Eigenschaften Seite des Microsoft-Agents überschreiben.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: GetBackColor**](iagentballoon--getbackcolor.md)


 

 




