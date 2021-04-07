---
title: Iagentcharacter getidleon
description: Iagentcharacter getidleon
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714592"
---
# <a name="iagentcharactergetidleon"></a>Iagentcharacter:: getidleon

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

Gibt den automatischen Leerlauf Verarbeitungs Status für ein Zeichen an.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbon*
</dt> <dd>

Die Adresse einer Variablen, die " **true** " empfängt, wenn der Microsoft-Agent-Server für ein Zeichen automatisch **idlinger** -Zustands Animationen abspielt, andernfalls " **false** ".

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter::/tidleon**](iagentcharacter--setidleon.md)


 

 




