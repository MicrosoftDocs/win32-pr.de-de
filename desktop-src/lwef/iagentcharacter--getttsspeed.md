---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7fbe4cbba7eaed22f49865e1a0f0994c512867fb6f233ef2bbfa01dcaafcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609870"
---
# <a name="iagentcharactergetttsspeed"></a>IAgentCharacter::GetTTSSpeed

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

Ruft die TTS-Ausgabegeschwindigkeit des Zeichens ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*
</dt> <dd>

Adresse einer Variablen, die die Ausgabegeschwindigkeit des Zeichens in Wörtern pro Minute empfängt.

</dd> </dl>

Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie Geschwindigkeitstags in Ihren Ausgabetext hinzufügen, die die Ausgabe für eine bestimmte Äußerung vorübergehend beschleunigen.

Diese Eigenschaft gibt die aktuelle Einstellung für die Sprechausgabegeschwindigkeit für das Zeichen zurück. Bei Zeichen, die die TTS-Ausgabe verwenden, gibt die -Eigenschaft die tatsächliche TTS-Ausgabe für das Zeichen zurück. Wenn TTS nicht aktiviert ist oder das Zeichen keine TTS-Ausgabe unterstützt, spiegelt die Einstellung die Benutzereinstellung für die Ausgabegeschwindigkeit wider.

 

 




