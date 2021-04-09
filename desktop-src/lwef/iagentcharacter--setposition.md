---
title: Iagentcharacter-SetPosition
description: Iagentcharacter-SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036742"
---
# <a name="iagentcharactersetposition"></a>Iagentcharacter:: SetPosition

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

Legt die Position des Animations Rahmens des Zeichens fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lleft*
</dt> <dd>

Die Bildschirm Koordinate der linken Kante des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*LTOP*
</dt> <dd>

Die Bildschirm Koordinate der oberen Kante des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> </dl>

Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens. Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf seinem rechteckigen Animations Rahmen.

> [!Note]  
> Anders als bei der Methode " [**muveto**](https://www.bing.com/search?q=**MoveTo**) " wird diese Funktion nicht in die Warteschlange gestellt.

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: GetPosition**](iagentcharacter--getposition.md)


 

 




