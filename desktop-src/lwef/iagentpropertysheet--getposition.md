---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74609f2e5f3201be07c425db17456f17e5202e6497b8b137815ae6124335650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976140"
---
# <a name="iagentpropertysheetgetposition"></a>IAgentPropertySheet::GetPosition

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

Ruft die Position des Eigenschaftenblattfensters des Microsoft-Agents ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Adresse einer Variablen, die die Bildschirmkoordinate des linken Rands des Eigenschaftenblatts in Pixel empfängt, relativ zum Ursprung des Bildschirms (links oben).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Adresse einer Variablen, die die Bildschirmkoordinate des oberen Rands des Eigenschaftenblatts in Pixel empfängt, relativ zum Ursprung des Bildschirms (links oben).

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentPropertySheet::GetSize**](iagentpropertysheet--getsize.md)


 

 




