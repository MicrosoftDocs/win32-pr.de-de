---
title: Iagentcharacter getttspitch
description: Iagentcharacter getttspitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339240"
---
# <a name="iagentcharactergetttspitch"></a><span data-ttu-id="27a7f-103">Iagentcharacter:: getttspitch</span><span class="sxs-lookup"><span data-stu-id="27a7f-103">IAgentCharacter::GetTTSPitch</span></span>

<span data-ttu-id="27a7f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="27a7f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

<span data-ttu-id="27a7f-105">Ruft die Einstellung für die TTS-Ausgabe Tonhöhe des Zeichens ab.</span><span class="sxs-lookup"><span data-stu-id="27a7f-105">Retrieves the character's TTS output pitch setting.</span></span>

-   <span data-ttu-id="27a7f-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="27a7f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="27a7f-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwpitch*</span><span class="sxs-lookup"><span data-stu-id="27a7f-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*</span></span>
</dt> <dd>

<span data-ttu-id="27a7f-108">Adresse einer Variablen, die die aktuelle TTS-Erstellungs Einstellung des Zeichens in Hertz empfängt.</span><span class="sxs-lookup"><span data-stu-id="27a7f-108">Address of a variable that receives the character's current TTS pitch setting in Hertz.</span></span>

</dd> </dl>

<span data-ttu-id="27a7f-109">Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie tagtags in den Ausgabetext einschließen, der die Tonhöhe für eine bestimmte Äußerung temporär vergrößert.</span><span class="sxs-lookup"><span data-stu-id="27a7f-109">Although your application cannot write this value, you can include pitch tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="27a7f-110">Diese Methode gilt nur für Zeichen, die für die TTS-Ausgabe konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="27a7f-110">This method applies only to characters configured for TTS output.</span></span> <span data-ttu-id="27a7f-111">Wenn die Funktion für die Sprachsynthese (TTS) nicht aktiviert (oder installiert) ist oder das Zeichen keine TTS-Ausgabe unterstützt, gibt diese Methode 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="27a7f-111">If the speech synthesis (TTS) engine is not enabled (or installed) or the character does not support TTS output, this method returns zero (0).</span></span>

 

 




