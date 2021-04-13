---
title: Iagentballoon getfontname
description: Iagentballoon getfontname
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388719"
---
# <a name="iagentballoongetfontname"></a>Iagentballoon:: getfontname

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

Ruft den Wert für die Schriftart ab, die in einer Word-Sprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszfontname*
</dt> <dd>

Die Adresse eines BSTR, der den in einer Wort Sprechblase angezeigten Schriftart Namen empfängt.

</dd> </dl>

Die in einer Wort Sprechblase verwendete Standard Schriftart wird im Microsoft-Agent-Zeichen-Editor definiert. Sie können es mit [**iagentballoon:: setfontname**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**)ändern. Der Benutzer kann die Schriftart Einstellung für alle Zeichen mithilfe des Eigenschaften Blatts Microsoft-Agent überschreiben.

 

 




