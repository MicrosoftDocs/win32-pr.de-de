---
title: Iagentpropertysheet GetPosition
description: Iagentpropertysheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342277"
---
# <a name="iagentpropertysheetgetposition"></a>Iagentpropertysheet:: GetPosition

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

Ruft die Position des Eigenschaften Blatt Fensters des Microsoft-Agents ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plleft*
</dt> <dd>

Adresse einer Variablen, die die Bildschirm Koordinate des linken Rands des Eigenschaften Blatts in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*pltop*
</dt> <dd>

Adresse einer Variablen, die die Bildschirm Koordinate des oberen Rands des Eigenschaften Blatts in Pixel relativ zum Bildschirm Ursprung empfängt (oben links).

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentpropertysheet:: GetSize**](iagentpropertysheet--getsize.md)


 

 




