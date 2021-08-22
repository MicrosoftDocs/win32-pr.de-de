---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63e75111b7694fcb993e141b8534e8f174efd1a1a252f250167ecb597149f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609990"
---
# <a name="iagentcharactergetposition"></a>IAgentCharacter::GetPosition

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

Ruft die Position des Animationsrahmens des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Adresse einer Variablen, die die Bildschirmkoordinate des linken Rands des Zeichenanimationsframes in Pixel relativ zum Bildschirmursprung (oben links) empfängt.

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Adresse einer Variablen, die die Bildschirmkoordinate des oberen Rands des Zeichenanimationsrahmens in Pixel relativ zum Bildschirmursprung (oben links) empfängt.

</dd> </dl>

Obwohl das Zeichen in einem unregelmäßig formten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf seinem rechteckigen Animationsrahmen.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [ **IAgentCharacter::GetSize**](iagentcharacter--getsize.md)


 

 




