---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320572322d7a28b52693c80eb918ebf78fcb50083e012e35c65df3a7bffdf0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976400"
---
# <a name="iagentcharacterplay"></a>IAgentCharacter::P lay

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

Gibt die angegebene Animation wieder.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgegeben wird, enthält *pdwReqID* die ID der Anforderung.

<dl> <dt>

<span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*
</dt> <dd>

Der Name einer Animation.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse einer Variablen, die die Anforderungs-ID **IAgentCharacter::P lay** empfängt.

</dd> </dl>

Der Name einer Animation wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird. Vor dem Wiedergeben der angegebenen Animation versucht der Server, die **Return-Animation** für die vorherige Animation wiederzuspielen (sofern eine zugewiesen wurde).

Wenn die Animationsdaten eines Zeichens auf dem lokalen Computer des Benutzers gespeichert werden, können Sie die **IAgentCharacter::P lay-Methode** verwenden und den Namen der Animation angeben. Wenn Sie das HTTP-Protokoll für den Zugriff auf Animationsdaten verwenden, verwenden [**Sie**](iagentcharacter--prepare.md) die Prepare-Methode, um die Verfügbarkeit der Animation sicherzustellen, bevor Sie diese Methode aufrufen.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::P repare**](iagentcharacter--prepare.md)


 

 




