---
title: Iagentballoon SetFontSize
description: Iagentballoon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311214"
---
# <a name="iagentballoonsetfontsize"></a>Iagentballoon:: SetFontSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

Legt die Größe der Schriftart fest, die in der Word-Sprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lfontsize*
</dt> <dd>

Der Schriftgrad.

</dd> </dl>

Der Standardschrift Grad, der in der Wort Sprechblase eines Zeichens verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert. Sie können es mit **iagentballoon:: SetFontSize** ändern. Der Benutzer kann jedoch die Einstellung für die Schriftgröße für alle Zeichen überschreiben, indem er das Eigenschaften Blatt "Microsoft-Agent" verwendet.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: GetFontSize**](iagentballoon--getfontsize.md)


 

 




