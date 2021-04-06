---
title: Iagentcharacter GetExtraData
description: Iagentcharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100822"
---
# <a name="iagentcharactergetextradata"></a>Iagentcharacter:: GetExtraData

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

Ruft zusätzliche Daten ab, die als Teil des Zeichens gespeichert werden.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszextradata*
</dt> <dd>

Die Adresse eines BSTR-Werts, der den Wert der zusätzlichen Daten für das Zeichen empfängt. Die zusätzlichen Daten eines Zeichens werden bei der Kompilierung mit dem Microsoft-Agent-Zeichen-Editor definiert. Ein Zeichen Entwickler kann diese Zeichenfolge bereitstellen, indem er den bearbeitet. ACD-Datei für ein Zeichen. Die Einstellung ist optional und kann nicht für alle Zeichen angegeben werden, und die Daten können zur Laufzeit nicht definiert oder geändert werden. Außerdem wird die Bedeutung der bereitgestellten Daten vom Zeichen Entwickler definiert.

</dd> </dl>

 

 




