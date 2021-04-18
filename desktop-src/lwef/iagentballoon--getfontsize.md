---
title: Iagentballoon GetFontSize
description: Iagentballoon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207400"
---
# <a name="iagentballoongetfontsize"></a>Iagentballoon:: GetFontSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

Ruft den Wert für die Größe der Schriftart ab, die in einer Word-Sprechblase angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plfontsize*
</dt> <dd>

Die Adresse eines Werts, der die Größe der Schriftart erhält.

</dd> </dl>

Der in einer Wort Sprechblase verwendete Standardschrift Grad wird im Microsoft-Agent-Zeichen-Editor definiert. Sie können es mit [**iagentballoon:: SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**)ändern. Der Benutzer kann jedoch die Schriftart Größen Einstellungen für alle Zeichen überschreiben, indem er das Eigenschaften Blatt "Microsoft-Agent" verwendet.

 

 




