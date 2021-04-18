---
title: Iagentcharacter setsounentffectson
description: Iagentcharacter setsounentffectson
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a454a6ebeecc763cb7e5a964bb1f2897df6c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341667"
---
# <a name="iagentcharactersetsoundeffectson"></a>Iagentcharacter:: setsounde ffectson

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

Bestimmt, ob die Soundeffekte des Zeichens wiedergegeben werden.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Böller*
</dt> <dd>

Einstellung für Sound Effekte. Wenn dieser Parameter **true** ist, werden die Soundeffekte für Animationen bei der Wiedergabe der Animation wiedergegeben. **false** gibt an, dass keine Soundeffekte wiedergegeben werden.

</dd> </dl>

Diese Einstellung bestimmt, ob Soundeffekte, die als Teil des Zeichens kompiliert werden, wiedergegeben werden, wenn Sie eine zugeordnete Animation wiedergeben. Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens. Die Einstellung unterliegt auch der Einstellung globaler Soundeffekte des Benutzers in [**iagentaudiooutputproperties:: getusingsoundebug**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: getsounbinffectson**](iagentcharacter--getsoundeffectson.md), [ **iagentaudiooutputproperties:: getusingsoundebug**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




