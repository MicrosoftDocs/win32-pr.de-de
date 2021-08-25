---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107e6fdb6be3e79dee14177d9f56ee7d258f3455d578641e7d3a3b3cf044c741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962273"
---
# <a name="iagentcharactergetname"></a>IAgentCharacter::GetName

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

Ruft den Namen des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

Die Adresse eines BSTR, der den Wert des Namens für das Zeichen empfängt.

</dd> </dl>

Der Standardname eines Zeichens wird definiert, wenn es mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird. Der Name eines Zeichens kann je nach Sprach-ID des Zeichens variieren. Zeichen können mit unterschiedlichen Namen für verschiedene Sprachen kompiliert werden.

Sie können den Namen des Zeichens auch mit **IAgentCharacter:SetName** festlegen. Dadurch wird jedoch der Name für alle aktuellen Clients des Zeichens geändert.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::SetName**](iagentcharacter--setname.md)


 

 




