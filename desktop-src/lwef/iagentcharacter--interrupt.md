---
title: IAgentCharacter-Interrupt
description: IAgentCharacter-Interrupt
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ea2529d4da78607d3ad22bf688857c8917e3317df17ae9a5eb99d0b184878e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750905"
---
# <a name="iagentcharacterinterrupt"></a>IAgentCharacter::Interrupt

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

Unterbricht die angegebene Animation (Anforderung) eines anderen Zeichens.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgegeben wird, *enthält pdwReqID* die ID der Anforderung.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

Eine ID der zu unterbrechenden Anforderung.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse einer Variablen, die die **Interruptanforderungs-ID** empfängt.

</dd> </dl>

Wenn Sie mehrere Zeichen laden, können Sie diese Methode verwenden, um Animationen zwischen Zeichen zu synchronisieren. Wenn sich beispielsweise ein anderes Zeichen in einer Schleifenanimation befindet, stoppt diese Methode die Schleifenanimation und startet die nächste Animation in der Warteschlange des Zeichens.

**Interrupt** hält die vorhandene Animation an, leert jedoch nicht die Animationswarteschlange des Zeichens. Sie startet die nächste Animation in der Warteschlange des Zeichens. Verwenden Sie die Stop-Methode, um die Warteschlange eines Zeichens [**anzuhalten und zu leeren.**](/windows/desktop/lwef/iagentcharacter--stop)

Sie können diese Methode nicht verwenden, um ein Zeichen zu unterbrechen, da der Microsoft Agent-Server die **Interrupt-Methode** in der Animationswarteschlange des Zeichens in die Warteschlange einreiht. Daher können Sie Interrupt nur verwenden, **um** die Animation eines anderen Zeichens anzuhalten, das Sie geladen haben.

 

 