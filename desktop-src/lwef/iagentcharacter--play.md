---
title: Iagentcharacter abspielen
description: Iagentcharacter abspielen
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037650"
---
# <a name="iagentcharacterplay"></a>Iagentcharacter::P Lay

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

Gibt die angegebene Animation wieder.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.

<dl> <dt>

<span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszanimation*
</dt> <dd>

Der Name einer Animation.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen, die das **iagentcharacter-Element empfängt::P Lay** -Anforderungs-ID.

</dd> </dl>

Der Name einer Animation wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird. Vor der Wiedergabe der angegebenen Animation versucht der Server, die Rückgabe Animation für die vorherige Animation **wiederzugeben** (sofern eine zugewiesen wurde).

Wenn die Animationsdaten eines Zeichens auf dem lokalen Computer des Benutzers gespeichert werden, können Sie die **iagentcharacter::P Lay** -Methode verwenden und den Namen der Animation angeben. Wenn Sie das HTTP-Protokoll für den Zugriff auf Animationsdaten verwenden, verwenden Sie die [**Prepare**](iagentcharacter--prepare.md) -Methode, um die Verfügbarkeit der Animation vor dem Aufrufen dieser Methode sicherzustellen.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter::P repare**](iagentcharacter--prepare.md)


 

 




