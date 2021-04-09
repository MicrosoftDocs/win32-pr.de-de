---
title: Iagentcharacter-muveto
description: Iagentcharacter-muveto
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038865"
---
# <a name="iagentcharactermoveto"></a>Iagentcharacter:: muveto

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

Gibt die zugehörige **Bewegungs** Zustands Animation wieder und verschiebt den Zeichen Rahmen an die angegebene Position.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgibt, enthält diese Variable die ID der Anforderung.

<dl> <dt>

<span id="x"></span><span id="X"></span>*Stuben*
</dt> <dd>

Die x-Koordinate der neuen Position in Pixel relativ zum Bildschirm Ursprung (oben links). Der Speicherort eines Zeichens basiert auf der linken oberen Ecke des Animations Rahmens.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Teenie*
</dt> <dd>

Die y-Koordinate der neuen Position in Pixel relativ zum Bildschirm Ursprung (oben links). Der Speicherort eines Zeichens basiert auf der linken oberen Ecke des Animations Rahmens.

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lspeed*
</dt> <dd>

Ein Parameter, der in Millisekunden angibt, wie schnell der Rahmen des Zeichens bewegt wird. Der empfohlene Wert ist 1000. Durch die Angabe von NULL (0) wird der Frame verschoben, ohne eine Animation zu spielen.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen, [**die die Anforderung**](https://www.bing.com/search?q=**MoveTo**) -ID für das anforderungspaar empfängt.

</dd> </dl>

Wenn Sie das HTTP-Protokoll für den Zugriff auf Zeichen-und Animationsdaten verwenden, verwenden Sie die [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode, um die Verfügbarkeit der **Bewegungs** Zustands Animationen vor dem Aufrufen dieser Methode sicherzustellen. Auch wenn die Animation nicht geladen ist, verschiebt der Server den Frame noch immer.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: SetPosition**](iagentcharacter--setposition.md)


 

 