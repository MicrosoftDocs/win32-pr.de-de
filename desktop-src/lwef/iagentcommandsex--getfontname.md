---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 757b2d7554f1efcee27a519b9df61b4601a237b557c3aa26b6575864144a2850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105236"
---
# <a name="iagentcommandsexgetfontname"></a>IAgentCommandsEx::GetFontName

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

Ruft den Wert für die Schriftart ab, die im Popupmenü des Zeichens angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Die Adresse eines BSTR, der den im Popupmenü des Zeichens angezeigten Schriftartnamen empfängt.

</dd> </dl>

Der zurückgegebene Schriftartname entspricht der Schriftart, die verwendet wird, um Text im Popupmenü des Zeichens anzuzeigen, wenn Ihre Clientanwendung eingabeaktiv ist. Der Standardwert für die Schriftarteinstellung basiert auf der Menüschriftarteinstellung für die Sprach-ID-Einstellung des Zeichens oder, falls nicht festgelegt, der Einstellung der Standardsprach-ID des Benutzers.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




