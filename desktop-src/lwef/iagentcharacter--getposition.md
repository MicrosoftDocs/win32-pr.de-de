---
title: Iagentcharacter GetPosition
description: Iagentcharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311598"
---
# <a name="iagentcharactergetposition"></a>Iagentcharacter:: GetPosition

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

Ruft die Animations Frame Position des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plleft*
</dt> <dd>

Adresse einer Variablen, die die Bildschirm Koordinate der linken Kante des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*pltop*
</dt> <dd>

Adresse einer Variablen, die die Bildschirm Koordinate des oberen Rands des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).

</dd> </dl>

Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf seinem rechteckigen Animations Rahmen.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: SetPosition**](iagentcharacter--setposition.md), [ **iagentcharacter:: GetSize**](iagentcharacter--getsize.md)


 

 




