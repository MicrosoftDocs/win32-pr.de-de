---
title: IAgentCommandWindow GetPosition
description: IAgentCommandWindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52571311a87ee0846dcaf515912762069fe3025a25c5a2589770ee9738bb2de7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716100"
---
# <a name="iagentcommandwindowgetposition"></a>IAgentCommandWindow::GetPosition

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

Ruft die Position des Sprachbefehlsfensters ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Adresse einer Variablen, die die Bildschirmkoordinate des linken Rands des Sprachbefehlsfensters in Pixel relativ zum Bildschirmursprung (oben links) empfängt.

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Adresse einer Variablen, die die Bildschirmkoordinate des oberen Rands des Sprachbefehlsfensters in Pixel relativ zum Bildschirmursprung (oben links) empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandWindow::GetSize**](iagentcommandwindow--getsize.md)


 

 




