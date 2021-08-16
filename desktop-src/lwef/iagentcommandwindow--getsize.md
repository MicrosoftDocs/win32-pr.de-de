---
title: IAgentCommandWindow GetSize
description: IAgentCommandWindow GetSize
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200853d88f4f4ea70fce0f80d73f343a2a4d46935a2dfca0ebf78021b0b884ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961580"
---
# <a name="iagentcommandwindowgetsize"></a>IAgentCommandWindow::GetSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

Ruft die aktuelle Größe des Fensters "Sprachbefehle" ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Adresse einer Variablen, die die Breite des Sprachbefehlsfensters in Pixel relativ zum Bildschirmursprung (oben links) empfängt.

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Adresse einer Variablen, die die Höhe des Sprachbefehlsfensters in Pixel relativ zum Ursprung des Bildschirms (oben links) empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandWindow::GetPosition**](iagentcommandwindow--getposition.md)


 

 




