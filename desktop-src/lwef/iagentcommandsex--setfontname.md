---
title: Iagentcommandsex setfontname
description: Iagentcommandsex setfontname
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708159"
---
# <a name="iagentcommandsexsetfontname"></a>Iagentcommandsex:: setfontname

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

Legt die im Popupmenü des Zeichens angezeigte Schriftart fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszfontname*
</dt> <dd>

Ein BSTR, das die im Popupmenü des Zeichens angezeigte Schriftart festlegt.

</dd> </dl>

Diese Eigenschaft bestimmt die Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird. Der Standardwert für die Schriftart Einstellung basiert auf der Menü Schriftart Einstellung für die Sprach-ID-Einstellung des Zeichens-oder, wenn dies nicht festgelegt ist, der Standardeinstellung für die Benutzereinstellung für die Sprache.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: getfontname**](iagentcommandsex--getfontname.md), [**iagentcommandsex:: GetFontSize**](iagentcommandsex--getfontsize.md), [**iagentcommandsex:: SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




