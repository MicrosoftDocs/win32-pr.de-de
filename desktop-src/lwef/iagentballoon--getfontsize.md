---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc392bd12fccfb01b8aee41a5a06ed50b388ac8223e622d75218c840f706c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962490"
---
# <a name="iagentballoongetfontsize"></a>IAgentBalloon::GetFontSize

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

Ruft den Wert für die Größe der Schriftart ab, die in einem Wortsprechblasenformat angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Die Adresse eines Werts, der den Schriftgrad empfängt.

</dd> </dl>

Der in einem Sprechblasenzeichen verwendete Standardschriftgrad wird im Microsoft Agent-Zeichen-Editor definiert. Sie können es mit [**IAgentBalloon::SetFontSize ändern.**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**) Der Benutzer kann jedoch die Schriftgradeinstellungen für alle Zeichen überschreiben, indem er das Microsoft Agent-Eigenschaftenblatt verwendet.

 

 




