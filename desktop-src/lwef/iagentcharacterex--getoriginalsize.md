---
title: Iagentcharakteriex getoriginalsize
description: Iagentcharakteriex getoriginalsize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036778"
---
# <a name="iagentcharacterexgetoriginalsize"></a>Iagentcharakteriex:: getoriginalsize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Ruft die ursprüngliche Größe des Animations Rahmens des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plwidth*
</dt> <dd>

Adresse einer Variablen, die die ursprüngliche Breite des Zeichen Animations Rahmens in Pixel empfängt.

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plheight*
</dt> <dd>

Adresse einer Variablen, die die ursprüngliche Höhe des Zeichen Animations Rahmens in Pixel empfängt.

</dd> </dl>

Dieser Befehl gibt die ursprüngliche Größe des Zeichen Rahmens zurück, wie er im Microsoft-Agent-Zeichen-Editor erstellt wurde.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: GetSize**](iagentcharacter--getsize.md)


 

 




