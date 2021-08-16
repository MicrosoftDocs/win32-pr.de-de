---
title: IAgentCharacterEx GetGUID
description: IAgentCharacterEx GetGUID
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e43a98617b1e2d25a25167ad5b95462eeb462f40f5a353b5a5ec45ffb3a9cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477968"
---
# <a name="iagentcharacterexgetguid"></a>IAgentCharacterEx::GetGUID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

Ruft die eindeutige ID für das Zeichen ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*
</dt> <dd>

Adresse eines BSTR, der die ID für das Zeichen empfängt.

</dd> </dl>

Die -Eigenschaft gibt eine Zeichenfolgendarstellung der GUID (formatiert mit geschweiften Klammern und Bindestrichen) zurück, die der Server verwendet, um das Zeichen eindeutig zu identifizieren. Ein Zeichenbezeichner wird festgelegt, wenn er mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird. Die Eigenschaft ist schreibgeschützt.

 

 




