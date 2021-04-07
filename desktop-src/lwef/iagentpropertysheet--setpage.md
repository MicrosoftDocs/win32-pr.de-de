---
title: Iagentpropertysheet (setpage)
description: Iagentpropertysheet (setpage)
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711352"
---
# <a name="iagentpropertysheetsetpage"></a>Iagentpropertysheet:: setpage

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

Legt die aktuelle Seite des Eigenschaften Blatts von Microsoft-Agent fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszpage*
</dt> <dd>

Ein BSTR, das die aktuelle Seite der Eigenschaft festlegt. Der Parameter kann eines der folgenden sein:



|                 |                        |
|-----------------|------------------------|
| **Sprache**    | Die Spracheingabe Seite. |
| **Ausgeben**    | Die Ausgabe Seite.       |
| **Copyright** | Die Seite Copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentpropertysheet:: GetPage**](iagentpropertysheet--getpage.md)


 

 




