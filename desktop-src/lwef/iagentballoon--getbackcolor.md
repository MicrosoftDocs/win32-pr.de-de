---
title: Iagentballoon GetBackColor
description: Iagentballoon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037160"
---
# <a name="iagentballoongetbackcolor"></a>Iagentballoon:: GetBackColor

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

Ruft den Wert für die in einer Wort Sprechblase angezeigte Hintergrundfarbe ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plbgcolor*
</dt> <dd>

Die Adresse einer Variablen, die die Farbeinstellung für den Hintergrund der Sprechblase empfängt.

</dd> </dl>

Die in einer Wort Sprechblase verwendete Hintergrundfarbe wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden. Der Benutzer kann jedoch die Hintergrundfarbe der Wort Blasen für alle Zeichen über die Eigenschaften Seite des Microsoft-Agents ändern.

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: getForeColor**](iagentballoon--getforecolor.md)


 

 




