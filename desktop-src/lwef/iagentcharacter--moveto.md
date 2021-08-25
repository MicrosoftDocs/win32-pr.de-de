---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ea5a0e288e4b7d9782f1b463fdbcccf01b0da9314894be1a60c556392e25e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848540"
---
# <a name="iagentcharactermoveto"></a>IAgentCharacter::MoveTo

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

Gibt die zugeordnete Animation **zum Bewegen** des Zustands wieder und verschiebt den Zeichenrahmen an die angegebene Position.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgegeben wird, enthält diese Variable die ID der Anforderung.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Die x-Koordinate der neuen Position in Pixel relativ zum Bildschirmursprung (oben links). Die Position eines Zeichens basiert auf der oberen linken Ecke des Animationsrahmens.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Die y-Koordinate der neuen Position in Pixel relativ zum Bildschirmursprung (oben links). Die Position eines Zeichens basiert auf der oberen linken Ecke des Animationsrahmens.

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*
</dt> <dd>

Ein Parameter, der in Millisekunden angibt, wie schnell sich der Rahmen des Zeichens bewegt. Der empfohlene Wert ist 1000. Wenn Null (0) angegeben wird, wird der Frame ohne Wiedergabe einer Animation verschoben.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse einer Variablen, die die MoveTo-Anforderungs-ID empfängt. [](https://www.bing.com/search?q=**MoveTo**)

</dd> </dl>

Wenn Sie das HTTP-Protokoll verwenden, um auf Zeichen- und Animationsdaten zuzugreifen, verwenden Sie die [**Prepare-Methode,**](/windows/desktop/lwef/iagentcharacter--prepare) um die Verfügbarkeit der **Moving** State-Animationen sicherzustellen, bevor Sie diese Methode aufrufen. Auch wenn die Animation nicht geladen ist, verschiebt der Server den Frame trotzdem.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md)


 

 