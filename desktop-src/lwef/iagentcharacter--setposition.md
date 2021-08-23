---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973ec08cdab89c2d8c2501bd9ea1778866f5f7fa1757fe746e44495e41c275a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665640"
---
# <a name="iagentcharactersetposition"></a>IAgentCharacter::SetPosition

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

Legt die Position des Animationsrahmens des Zeichens fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*
</dt> <dd>

Bildschirmkoordinate des linken Rands des Zeichenanimationsrahmens in Pixel relativ zum Bildschirmursprung (oben links).

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*Ltop*
</dt> <dd>

Bildschirmkoordinate des oberen Rands des Zeichenanimationsrahmens in Pixel relativ zum Bildschirmursprung (oben links).

</dd> </dl>

Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens. Obwohl das Zeichen in einem unregelmäßig formten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf seinem rechteckigen Animationsrahmen.

> [!Note]  
> Im Gegensatz zur [**MoveTo-Methode**](https://www.bing.com/search?q=**MoveTo**) wird diese Funktion nicht in die Warteschlange eingereiht.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::GetPosition**](iagentcharacter--getposition.md)


 

 




