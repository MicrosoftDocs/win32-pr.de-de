---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92f2ce1908ea5f37d24fb8a085204917440f61ae30feb1e596639d0240c353d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976270"
---
# <a name="iagentcommandsexgetfontsize"></a>IAgentCommandsEx::GetFontSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

Ruft den Wert für die Größe der Schriftart ab, die im Popupmenü des Zeichens angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Die Adresse eines Werts, der die Schriftgröße empfängt.

</dd> </dl>

Die Punktgröße der zurückgegebenen Schriftart entspricht der Größe, die für die Anzeige von Text im Popupmenü des Zeichens definiert ist, wenn der Client eingabeaktiv ist. Der Standardwert für die Schriftarteinstellung basiert auf der Einstellung für die Menüschriftart für die Sprach-ID des Zeichens oder, falls nicht festgelegt, auf der Standardspracheinstellung des Benutzers.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md), [ **IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)


 

 




