---
title: Iagentpropertysheet GetPage
description: Iagentpropertysheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388380"
---
# <a name="iagentpropertysheetgetpage"></a>Iagentpropertysheet:: GetPage

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

Ruft die aktuelle Seite des Microsoft-Agent-Eigenschaften Blatts ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszpage*
</dt> <dd>

Adresse einer Variablen, die die aktuelle Seite des Eigenschaften Blatts empfängt (zuletzt angezeigte Seite, wenn das Fenster nicht geöffnet ist). Der Parameter kann eines der folgenden sein:



|                 |                        |
|-----------------|------------------------|
| **Sprache**    | Die Spracheingabe Seite. |
| **Ausgeben**    | Die Ausgabe Seite.       |
| **Copyright** | Die Seite Copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentpropertysheet:: setpage**](iagentpropertysheet--setpage.md)


 

 




