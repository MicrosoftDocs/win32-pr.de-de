---
title: IAgentBalloon GetBackColor
description: IAgentBalloon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c58a913332d01f2982c28003c146420d34a86e96f3c833f667c968bd22ef19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888420"
---
# <a name="iagentballoongetbackcolor"></a>IAgentBalloon::GetBackColor

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

Ruft den Wert für die Hintergrundfarbe ab, die in einem Wortsprechblasen angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*
</dt> <dd>

Die Adresse einer Variablen, die die Farbeinstellung für den Sprechblasenhintergrund empfängt.

</dd> </dl>

Die in einem Sprechblasen eines Zeichenworts verwendete Hintergrundfarbe wird im Microsoft-Agent-Zeichen-Editor definiert. Sie kann nicht von einer Anwendung geändert werden. Der Benutzer kann jedoch die Hintergrundfarbe der Wortsprechblasen für alle Zeichen über das Eigenschaftenblatt des Microsoft-Agents ändern.

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)


 

 




