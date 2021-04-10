---
title: Iagentballoon setfontname
description: Iagentballoon setfontname
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037547"
---
# <a name="iagentballoonsetfontname"></a>Iagentballoon:: setfontname

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

Legt die in der Wort Sprechblase angezeigte Schriftart fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszfontname*
</dt> <dd>

Ein BSTR, das die in der Wort Sprechblase angezeigte Schriftart festlegt.

</dd> </dl>

Die in der Wort Sprechblase eines Zeichens verwendete Standard Schriftart wird im Microsoft-Agent-Zeichen-Editor definiert. Sie können es mit **iagentballoon:: setfontname** ändern. Der Benutzer kann jedoch die Schriftart Einstellung für alle Zeichen mithilfe des Eigenschaften Blatts Microsoft-Agent überschreiben.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: getVisible**](iagentballoon--getvisible.md)


 

 




