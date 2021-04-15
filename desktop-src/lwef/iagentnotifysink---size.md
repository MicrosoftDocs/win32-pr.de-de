---
title: Iagentnotifysink-Größe
description: Iagentnotifysink-Größe
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515908"
---
# <a name="iagentnotifysinksize"></a>Iagentnotifysink:: size

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

Benachrichtigt eine Client Anwendung, wenn die Größe des Zeichens geändert wurde.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Der Bezeichner des Zeichens, dessen Größe geändert wurde.

</dd> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lwidth*
</dt> <dd>

Die Breite des Animations Rahmens des Zeichens in Pixel.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lheight*
</dt> <dd>

Die Höhe des Animations Rahmens des Zeichens in Pixel.

</dd> </dl>

Dieses Ereignis wird an alle Clients des Zeichens gesendet.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: GetSize**](iagentcharacter--getsize.md), [ **iagentcharacter:: SetSize**](iagentcharacter--setsize.md)


 

 




