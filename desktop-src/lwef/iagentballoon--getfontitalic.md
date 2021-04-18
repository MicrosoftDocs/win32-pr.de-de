---
title: Iagentballoon getfontitalic
description: Iagentballoon getfontitalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340835"
---
# <a name="iagentballoongetfontitalic"></a>Iagentballoon:: getfontitalic

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

Gibt an, ob die in einer Word-Sprechblase verwendete Schriftart kursiv formatiert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbfontitalic*
</dt> <dd>

Die Adresse eines Werts, der **true** erhält, wenn die Schriftart kursiv ist, und **false** , wenn Sie nicht kursiv formatiert ist.

</dd> </dl>

Der Schriftart Stil, der in der Wort Sprechblase eines Zeichens verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden. Der Benutzer kann jedoch die Schriftart Einstellungen für alle Zeichen über die Eigenschaften Seite des Microsoft-Agents überschreiben.

 

 




