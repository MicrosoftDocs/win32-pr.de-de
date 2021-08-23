---
title: IAgentBalloon SetFontSize
description: IAgentBalloon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6e19d79429ddf98f67a281cd11aefb1dc6bc2e54b1289e36c7cfb5a62bd538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976470"
---
# <a name="iagentballoonsetfontsize"></a>IAgentBalloon::SetFontSize

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

Legt den Schriftgrad fest, der im Wort balloon angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Der Schriftgrad.

</dd> </dl>

Der Standardschriftgrad, der in der Wortsprechblase eines Zeichens verwendet wird, wird im Microsoft Agent-Zeichen-Editor definiert. Sie können es mit **IAgentBalloon::SetFontSize ändern.** Der Benutzer kann jedoch die Schriftgradeinstellung für alle Zeichen mithilfe des Microsoft Agent-Eigenschaftenblatts überschreiben.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::GetFontSize**](iagentballoon--getfontsize.md)


 

 




