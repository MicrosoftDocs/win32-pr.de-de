---
title: Iagentcommandsex getfontname
description: Iagentcommandsex getfontname
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388415"
---
# <a name="iagentcommandsexgetfontname"></a>Iagentcommandsex:: getfontname

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

Ruft den Wert für die Schriftart ab, die im Popupmenü des Zeichens angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszfontname*
</dt> <dd>

Die Adresse eines BSTR, der den im Popupmenü des Zeichens angezeigten Schriftart Namen empfängt.

</dd> </dl>

Der zurückgegebene Schriftart Name entspricht der Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird, wenn die Client Anwendung aktiv ist. Der Standardwert für die Schriftart Einstellung basiert auf der Einstellung für die Menü Schriftart für die Sprach-ID-Einstellung des Zeichens oder, wenn nicht festgelegt, der Standardeinstellung für die Benutzereinstellung für die Sprache.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: setfontname**](iagentcommandsex--setfontname.md), [ **iagentcommandsex:: SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




