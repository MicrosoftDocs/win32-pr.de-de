---
title: IAgentPropertySheet GetSize
description: IAgentPropertySheet GetSize
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1907e011dfbd965eacdd0b37d9dad9b4540b20a381727b62e0880931093df27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692312"
---
# <a name="iagentpropertysheetgetsize"></a>IAgentPropertySheet::GetSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

Ruft die Größe des Eigenschaftenblattfensters des Microsoft-Agents ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Adresse einer Variablen, die die Breite des Eigenschaftenblatts relativ zum Bildschirmursprung (oben links) in Pixel empfängt.

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Adresse einer Variablen, die die Höhe des Eigenschaftenblatts relativ zum Bildschirmursprung (oben links) in Pixel empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentPropertySheet::GetPosition**](iagentpropertysheet--getposition.md)


 

 




