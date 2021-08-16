---
title: IAgentBalloon GetBorderColor
description: IAgentBalloon GetBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ed636d5209402959adbb2a777577a87c8cc23f8eed4faeb8ac003981e5e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478634"
---
# <a name="iagentballoongetbordercolor"></a>IAgentBalloon::GetBorderColor

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

Ruft den Wert für die Rahmenfarbe ab, die für eine Wortsprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*
</dt> <dd>

Die Adresse einer Variablen, die die Farbeinstellung für den Sprechblasen-Rahmen empfängt.

</dd> </dl>

Die Rahmenfarbe für ein Sprechblasenzeichen wird im Microsoft Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden. Der Benutzer kann jedoch die Rahmenfarbe der Wortsprechblasen für alle Zeichen über das Microsoft Agent-Eigenschaftenblatt ändern.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md), [ **IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)


 

 




