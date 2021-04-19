---
title: Geschwindigkeit (Eigenschaft)
description: Geschwindigkeit (Eigenschaft)
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342046"
---
# <a name="speed-property"></a><span data-ttu-id="0610c-103">Geschwindigkeit (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0610c-103">Speed Property</span></span>

<span data-ttu-id="0610c-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0610c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0610c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0610c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0610c-106">Gibt einen Long Integer-Wert zurück, der die aktuelle Geschwindigkeit der Sprachausgabe des Zeichens angibt.</span><span class="sxs-lookup"><span data-stu-id="0610c-106">Returns a Long integer that specifies the current speed of the character's speech output.</span></span>

</dd> <dt>

<span data-ttu-id="0610c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0610c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0610c-108">*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Beschleunigt**</span><span class="sxs-lookup"><span data-stu-id="0610c-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speed*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0610c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0610c-109">Remarks</span></span>

<span data-ttu-id="0610c-110">Diese Eigenschaft gibt die aktuelle Sprechgeschwindigkeit der Ausgabegeschwindigkeit für das Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="0610c-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="0610c-111">Für Zeichen, die die TTS-Ausgabe verwenden, gibt die-Eigenschaft die tatsächliche TTS-Ausgabe Einstellung für das Zeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="0610c-111">For characters using TTS output, the property returns the actual TTS output setting for the character.</span></span> <span data-ttu-id="0610c-112">Wenn "TTS" nicht aktiviert ist oder das Zeichen keine TTS-Ausgabe unterstützt, gibt die Einstellung die Benutzereinstellung für die Ausgabegeschwindigkeit wieder.</span><span class="sxs-lookup"><span data-stu-id="0610c-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

<span data-ttu-id="0610c-113">Obwohl Ihre Anwendung diesen Wert nicht schreiben kann, können Sie **SPD** -Tags (Geschwindigkeit) in den Ausgabetext einschließen, um die Ausgabe für eine bestimmte Äußerung vorübergehend zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="0610c-113">Although your application cannot write this value, you can include **Spd** (speed) tags in your output text that will temporarily speed up the output for a particular utterance.</span></span> <span data-ttu-id="0610c-114">Die Verwendung des **SPD** -Tags zum Ändern der gesprochenen Ausgabe des Zeichens wirkt sich jedoch nicht auf die Einstellung für die **Geschwindigkeits** Eigenschaft aus.</span><span class="sxs-lookup"><span data-stu-id="0610c-114">However, using the **Spd** tag to change the character's spoken output does not affect the **Speed** property setting.</span></span> <span data-ttu-id="0610c-115">Weitere Informationen finden Sie unter [Sprachausgabe Tags](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="0610c-115">For further information, see [Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




