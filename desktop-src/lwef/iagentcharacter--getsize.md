---
title: IAgentCharacter GetSize
description: IAgentCharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af078eb9980399793e00f8bd3deaefef7f048a900423c1ee50ac8d4f4a310b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962230"
---
# <a name="iagentcharactergetsize"></a>IAgentCharacter::GetSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Ruft die Größe des Animationsrahmens des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Adresse einer Variablen, die die Breite des Zeichenanimationsframes in Pixel relativ zum Bildschirmursprung (oben links) empfängt.

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Adresse einer Variablen, die die Höhe des Zeichenanimationsframes in Pixel relativ zum Bildschirmursprung (oben links) empfängt.

</dd> </dl>

Obwohl das Zeichen in einem unregelmäßig formten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf seinem rechteckigen Animationsrahmen.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::SetSize**](iagentcharacter--setsize.md)


 

 




