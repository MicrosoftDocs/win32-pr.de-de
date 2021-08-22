---
title: IAgentCharacter SetDescription
description: IAgentCharacter SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d96765d3faddafef00a28826ec5a9fdd92acb6884ac3aa659ad88ba2c091a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609820"
---
# <a name="iagentcharactersetdescription"></a>IAgentCharacter::SetDescription

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

Legt die Beschreibung des Zeichens fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*
</dt> <dd>

Ein BSTR, der die Beschreibung für das Zeichen fest legt. Die Standardbeschreibung eines Zeichens wird definiert, wenn es mit dem Microsoft Agent-Zeichen-Editor kompiliert wird. Die Beschreibungseinstellung ist optional und wird möglicherweise nicht für alle Zeichen angegeben. Sie können die Beschreibung des Zeichens mithilfe von **IAgentCharacter::setDescription ändern.** dieser Wert ist jedoch nicht persistent (dauerhaft gespeichert). Die Beschreibung des Zeichens wird auf die Standardeinstellung zurückverwendet, wenn das Zeichen zum ersten Mal von einem Client geladen wird.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::GetDescription**](iagentcharacter--getdescription.md)


 

 




