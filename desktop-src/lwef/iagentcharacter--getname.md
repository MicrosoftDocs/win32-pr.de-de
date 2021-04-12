---
title: Iagentcharacter GetName
description: Iagentcharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311603"
---
# <a name="iagentcharactergetname"></a>Iagentcharacter:: GetName

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

Ruft den Namen des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszname*
</dt> <dd>

Die Adresse eines BSTR-Werts, der den Wert des Namens für das Zeichen empfängt.

</dd> </dl>

Der Standardname eines Zeichens wird bei der Kompilierung mit dem Microsoft-Agent-Zeichen-Editor definiert. Der Name eines Zeichens kann je nach Sprach-ID des Zeichens variieren. Zeichen können mit unterschiedlichen Namen für verschiedene Sprachen kompiliert werden.

Sie können auch den Namen des Zeichens mithilfe von " **iagentcharacter: SetName**;" festlegen. Dadurch wird jedoch der Name für alle aktuellen Clients des Zeichens geändert.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: SetName**](iagentcharacter--setname.md)


 

 




