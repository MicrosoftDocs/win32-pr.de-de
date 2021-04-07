---
title: Iagentcharacter ausblenden
description: Iagentcharacter ausblenden
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038913"
---
# <a name="iagentcharacterhide"></a>Iagentcharacter:: Hide

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

Blendet das Zeichen aus.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*BFAST*
</dt> <dd>

Flag zum Ausblenden **des Zustands der** Animation. Wenn dieser Parameter **true** ist, wird die verborgene Animation nicht abgespielt, **bevor der Zeichen** Rahmen ausgeblendet wird. **false** gibt an, dass die Animation wiedergegeben wird.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen, die die **Ausblenden** der Anforderungs-ID empfängt.

</dd> </dl>

Der Server fügt die Animation, die der **Hide** -Methode zugeordnet ist, in die Warteschlange des Zeichens ein. Dies ermöglicht es Ihnen, das Zeichen nach einer Sequenz von anderen Animationen auszublenden. Sie können die Aktion sofort wiedergeben, indem Sie die Methode " [**Ende**](iagentcharacter--stop.md) " verwenden, bevor Sie die **Hide** -Methode aufrufen

Wenn Sie das HTTP-Protokoll für den Zugriff auf Zeichen-und Animationsdaten verwenden, verwenden Sie die [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode, um sicherzustellen, dass die **Animation zum Ausblenden des Zustands verfügbar** ist

Das Ausblenden eines Zeichens kann auch dazu führen, dass das [**iagentnotifysink:: activateinputstate**](iagentnotifysink--activateinputstate.md) -Ereignis eines anderen sichtbaren Zeichens ausgelöst wird.

Versteckte Zeichen können nicht auf den Audiokanal zugreifen. Der Server übergibt einen Fehlerstatus im [**requestcomplete**](iagentnotifysink--requestcomplete.md) -Ereignis zurück, wenn Sie eine Animations Anforderung generieren und das Zeichen ausgeblendet ist.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: Show**](iagentcharacter--show.md)


 

 