---
title: Iagentcharacter getttspeed
description: Iagentcharacter getttspeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551074e1647cffc88e0b5f9f530cea931cd21ff9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388810"
---
# <a name="iagentcharactergetttsspeed"></a>Iagentcharacter:: getttspeed

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

Ruft die Einstellung für die TTS-Ausgabegeschwindigkeit des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwspeed*
</dt> <dd>

Adresse einer Variablen, die die Ausgabegeschwindigkeit des Zeichens in Wörtern pro Minute empfängt.

</dd> </dl>

Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie in ihren Ausgabetext Geschwindigkeits Tags einschließen, die die Ausgabe für eine bestimmte Äußerung vorübergehend beschleunigen.

Diese Eigenschaft gibt die aktuelle Sprechgeschwindigkeit der Ausgabegeschwindigkeit für das Zeichen zurück. Für Zeichen, die die TTS-Ausgabe verwenden, gibt die-Eigenschaft die tatsächliche TTS-Ausgabe für das Zeichen zurück. Wenn "TTS" nicht aktiviert ist oder das Zeichen keine TTS-Ausgabe unterstützt, gibt die Einstellung die Benutzereinstellung für die Ausgabegeschwindigkeit wieder.

 

 




