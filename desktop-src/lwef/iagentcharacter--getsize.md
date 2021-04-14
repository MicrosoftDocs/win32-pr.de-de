---
title: Iagentcharacter GetSize
description: Iagentcharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311597"
---
# <a name="iagentcharactergetsize"></a>Iagentcharacter:: GetSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Ruft die Größe des Animations Rahmens des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plwidth*
</dt> <dd>

Die Adresse einer Variablen, die die Breite des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung (oben links) empfängt.

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plheight*
</dt> <dd>

Die Adresse einer Variablen, die die Höhe des Zeichen Animations Rahmens in Pixel relativ zum Bildschirm Ursprung (oben links) empfängt.

</dd> </dl>

Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf seinem rechteckigen Animations Rahmen.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: SetSize**](iagentcharacter--setsize.md)


 

 




