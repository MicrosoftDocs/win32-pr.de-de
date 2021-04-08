---
title: Iagentballoon getBorderColor
description: Iagentballoon getBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712047"
---
# <a name="iagentballoongetbordercolor"></a>Iagentballoon:: getBorderColor

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

Ruft den Wert für die Rahmenfarbe ab, die für eine Wort Sprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plbordercolor*
</dt> <dd>

Die Adresse einer Variablen, die die Farbeinstellung für den Sprechblasen Rahmen empfängt.

</dd> </dl>

Die Rahmenfarbe für eine Zeichen Wort Sprechblase wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden. Der Benutzer kann jedoch die Rahmenfarbe der Wort Blasen für alle Zeichen über das Eigenschaften Blatt "Microsoft-Agent" ändern.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: GetBackColor**](iagentballoon--getbackcolor.md), [ **iagentballoon:: getForeColor**](iagentballoon--getforecolor.md)


 

 




