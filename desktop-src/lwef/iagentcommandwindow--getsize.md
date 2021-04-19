---
title: Iagentcommandwindow GetSize
description: Iagentcommandwindow GetSize
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cf42d98f811905590209b6fed70b28a5728903
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341870"
---
# <a name="iagentcommandwindowgetsize"></a>Iagentcommandwindow:: GetSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

Ruft die aktuelle Größe des Sprachbefehle Fensters ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plwidth*
</dt> <dd>

Adresse einer Variablen, die die Breite des sprach Befehls Fensters in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plheight*
</dt> <dd>

Adresse einer Variablen, die die Höhe des sprach Befehls Fensters in Pixel relativ zum Bildschirm Ursprung (oben links) empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandwindow:: GetPosition**](iagentcommandwindow--getposition.md)


 

 




