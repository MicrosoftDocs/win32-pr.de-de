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
# <a name="iagentcharactergetttsspeed"></a><span data-ttu-id="7cba0-103">Iagentcharacter:: getttspeed</span><span class="sxs-lookup"><span data-stu-id="7cba0-103">IAgentCharacter::GetTTSSpeed</span></span>

<span data-ttu-id="7cba0-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="7cba0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

<span data-ttu-id="7cba0-105">Ruft die Einstellung für die TTS-Ausgabegeschwindigkeit des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="7cba0-105">Retrieves the character's TTS output speed setting.</span></span>

-   <span data-ttu-id="7cba0-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7cba0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7cba0-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwspeed*</span><span class="sxs-lookup"><span data-stu-id="7cba0-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="7cba0-108">Adresse einer Variablen, die die Ausgabegeschwindigkeit des Zeichens in Wörtern pro Minute empfängt.</span><span class="sxs-lookup"><span data-stu-id="7cba0-108">Address of a variable that receives the output speed of the character in words per minute.</span></span>

</dd> </dl>

<span data-ttu-id="7cba0-109">Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie in ihren Ausgabetext Geschwindigkeits Tags einschließen, die die Ausgabe für eine bestimmte Äußerung vorübergehend beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="7cba0-109">Although your application cannot write this value, you can include speed tags in your output text that will temporarily speed up the output for a particular utterance.</span></span>

<span data-ttu-id="7cba0-110">Diese Eigenschaft gibt die aktuelle Sprechgeschwindigkeit der Ausgabegeschwindigkeit für das Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="7cba0-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="7cba0-111">Für Zeichen, die die TTS-Ausgabe verwenden, gibt die-Eigenschaft die tatsächliche TTS-Ausgabe für das Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="7cba0-111">For characters using TTS output, the property returns the actual TTS output for the character.</span></span> <span data-ttu-id="7cba0-112">Wenn "TTS" nicht aktiviert ist oder das Zeichen keine TTS-Ausgabe unterstützt, gibt die Einstellung die Benutzereinstellung für die Ausgabegeschwindigkeit wieder.</span><span class="sxs-lookup"><span data-stu-id="7cba0-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

 

 




