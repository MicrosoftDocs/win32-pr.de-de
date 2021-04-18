---
title: Iagentpropertysheet GetSize
description: Iagentpropertysheet GetSize
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341240"
---
# <a name="iagentpropertysheetgetsize"></a>Iagentpropertysheet:: GetSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

Ruft die Größe des Eigenschaften Blatt Fensters von Microsoft-Agent ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plwidth*
</dt> <dd>

Adresse einer Variablen, die die Breite des Eigenschaften Blatts in Pixel relativ zum Bildschirm Ursprung (oben links) empfängt.

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plheight*
</dt> <dd>

Adresse einer Variablen, die die Höhe des Eigenschaften Blatts in Pixel relativ zum Bildschirm Ursprung (oben links) empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentpropertysheet:: GetPosition**](iagentpropertysheet--getposition.md)


 

 




