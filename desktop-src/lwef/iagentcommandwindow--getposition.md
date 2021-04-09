---
title: Iagentcommandwindow GetPosition
description: Iagentcommandwindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947802"
---
# <a name="iagentcommandwindowgetposition"></a>Iagentcommandwindow:: GetPosition

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

Ruft die Position des sprach Befehls Fensters ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plleft*
</dt> <dd>

Adresse einer Variablen, die die Bildschirm Koordinate des linken Rands des sprach Befehls Fensters in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*pltop*
</dt> <dd>

Adresse einer Variablen, die die Bildschirm Koordinate des oberen Rands des sprach Befehls Fensters in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandwindow:: GetSize**](iagentcommandwindow--getsize.md)


 

 




