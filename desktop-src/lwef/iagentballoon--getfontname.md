---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb0bceae040f9261d2530b19d074df937dbdaf80d91a27f57b5cf9c1fd8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725317"
---
# <a name="iagentballoongetfontname"></a>IAgentBalloon::GetFontName

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

Ruft den Wert für die Schriftart ab, die in einer Wortsprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Die Adresse eines BSTR, der den in einer Wortsprechblase angezeigten Schriftartnamen empfängt.

</dd> </dl>

Die Standardschriftart, die in einem Sprechblasenzeichen für Zeichen verwendet wird, wird im Zeichen-Editor für den Microsoft-Agent definiert. Sie können sie mit [**IAgentBalloon::SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**)ändern. Der Benutzer kann die Schriftarteinstellung für alle Zeichen über das Eigenschaftenblatt des Microsoft-Agents überschreiben.

 

 




