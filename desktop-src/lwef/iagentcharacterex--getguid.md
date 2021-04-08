---
title: Iagentcharakteriex GetGuid
description: Iagentcharakteriex GetGuid
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947919"
---
# <a name="iagentcharacterexgetguid"></a>Iagentcharakteriex:: GetGuid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

Ruft die eindeutige ID für das Zeichen ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszguid*
</dt> <dd>

Adresse eines BSTR, der die ID für das Zeichen empfängt.

</dd> </dl>

Die-Eigenschaft gibt eine Zeichen folgen Darstellung der GUID (formatiert mit geschweiften Klammern und Bindestrichen) zurück, die der Server zum eindeutigen Identifizieren des Zeichens verwendet. Eine Zeichen Kennung wird festgelegt, wenn Sie mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird. Die Eigenschaft ist schreibgeschützt.

 

 




