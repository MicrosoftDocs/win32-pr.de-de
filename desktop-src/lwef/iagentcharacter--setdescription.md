---
title: Iagentcharacter setDescription
description: Iagentcharacter setDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388806"
---
# <a name="iagentcharactersetdescription"></a>Iagentcharacter:: setDescription

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

Legt die Beschreibung des Zeichens fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszdescription*
</dt> <dd>

Ein BSTR, der die Beschreibung für das Zeichen festlegt. Die Standardbeschreibung eines Zeichens wird bei der Kompilierung mit dem Microsoft-Agent-Zeichen-Editor definiert. Die Beschreibungs Einstellung ist optional und kann nicht für alle Zeichen angegeben werden. Sie können die Beschreibung des Zeichens mithilfe von **iagentcharacter:: setDescription**; ändern. Dieser Wert ist jedoch nicht persistent (wird permanent gespeichert). Die Zeichen Beschreibung wird immer wieder auf die Standardeinstellung festgelegt, wenn das Zeichen zuerst von einem Client geladen wird.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: GetDescription**](iagentcharacter--getdescription.md)


 

 




