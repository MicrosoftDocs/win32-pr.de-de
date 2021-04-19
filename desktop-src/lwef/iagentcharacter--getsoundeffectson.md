---
title: Iagentcharacter getsoundebug
description: Iagentcharacter getsoundebug
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a40f18a4fb8e7778c116c54391a7dc50e5267af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341888"
---
# <a name="iagentcharactergetsoundeffectson"></a>Iagentcharacter:: getsounentffectson

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

Ruft ab, ob die Einstellung für die Soundeffekte des Zeichens aktiviert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbon*
</dt> <dd>

Die Adresse einer Variablen, die **true** empfängt, wenn die Einstellung für die Soundeffekte des Zeichens aktiviert ist, und **false** , wenn Sie deaktiviert ist.

</dd> </dl>

Die Einstellung Soundeffekte des Zeichens bestimmt, ob Soundeffekte, die als Teil des Zeichens kompiliert werden, beim Abspielen einer zugeordneten Animation wiedergegeben werden. Die Einstellung unterliegt der Einstellung globaler Soundeffekte des Benutzers in [**iagentaudiooutputproperties:: getusingsoundebug**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: setsounbinffectson**](iagentcharacter--setsoundeffectson.md), [ **iagentaudiooutputproperties:: getusingsoundebug**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




