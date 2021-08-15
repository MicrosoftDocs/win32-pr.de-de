---
title: IAgentCommandsEx SetFontSize
description: IAgentCommandsEx SetFontSize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92319178f2fbceb7b2e0cad9bdb35b740ebeaf108f864edb84b4413353e85e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477202"
---
# <a name="iagentcommandsexsetfontsize"></a>IAgentCommandsEx::SetFontSize

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

Legt den Schriftgrad fest, der im Popupmenü des Zeichens angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Der Schriftgrad.

</dd> </dl>

Diese Eigenschaft bestimmt den Punktgrad der Schriftart, die zum Anzeigen von Text im Popupmenü des Zeichens verwendet wird, wenn Ihre Clientanwendung eingabeaktiv ist. Der Standardwert für die Schriftarteinstellung basiert auf der Menüschriftarteinstellung für die Sprach-ID-Einstellung des Zeichens oder , wenn dies nicht auf die Standardspracheinstellung des Benutzers festgelegt ist. Wenn die Eingabe nicht aktiv ist, wird der Befehlsbeschriftungstext Ihrer Clientanwendung in der für den eingabeaktiven Client angegebenen Punktgröße angezeigt. [](/windows/desktop/lwef/the-command-object) [](caption-property.md)

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)


 

 