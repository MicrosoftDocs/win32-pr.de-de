---
title: Unterbrechung von iagentcharacter
description: Unterbrechung von iagentcharacter
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948604"
---
# <a name="iagentcharacterinterrupt"></a>Iagentcharacter:: Interrupt

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

Unterbricht die angegebene Animation (Anforderung) eines anderen Zeichens.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwreqid*
</dt> <dd>

Eine ID der zu unterbrechenden Anforderung.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen, die die **interruptanforderungs** -ID empfängt.

</dd> </dl>

Wenn Sie mehrere Zeichen laden, können Sie mit dieser Methode die Animation zwischen Zeichen synchronisieren. Wenn sich z. b. ein anderes Zeichen in einer Schleifen Animation befindet, beendet diese Methode die Schleifen Animation und startet die nächste Animation in der Warteschlange des Zeichens.

Der **Interrupt** stoppt die vorhandene Animation, aber die Animations Warteschlange des Zeichens wird nicht geleert. Die nächste Animation wird in der Warteschlange des Zeichens gestartet. Verwenden Sie die Stop-Methode, um die Warteschlange eines Zeichens [**anzuhalten**](/windows/desktop/lwef/iagentcharacter--stop) und zu leeren.

Sie können diese Methode nicht verwenden, um ein Zeichen selbst zu unterbrechen, da der Microsoft-Agent-Server die **Interrupt** -Methode in der Animations Warteschlange des Zeichens zur warte Daher können Sie nur **Interrupt** verwenden, um die Animation eines anderen Zeichens anzuhalten, das Sie geladen haben.

 

 