---
title: IAgentBalloon SetFontName
description: IAgentBalloon SetFontName
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1091fd0b0e5834ca687a6c9e66d59bdb186dcdfd9122e3200dce10db64e068a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693315"
---
# <a name="iagentballoonsetfontname"></a>IAgentBalloon::SetFontName

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

Legt die im Wortsprechblasen angezeigte Schriftart fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

Ein BSTR, der die im Wortsprechblasen angezeigte Schriftart festlegt.

</dd> </dl>

Die Standardschriftart, die im Wortsprechblasen eines Zeichens verwendet wird, wird im Microsoft-Agent-Zeichen-Editor definiert. Sie können sie mit **IAgentBalloon::SetFontName** ändern. Allerdings kann der Benutzer die Schriftarteinstellung für alle Zeichen über das Eigenschaftenblatt des Microsoft-Agents überschreiben.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::GetVisible**](iagentballoon--getvisible.md)


 

 




