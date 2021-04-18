---
title: Iagentcharacter setsounentffectson
description: Iagentcharacter setsounentffectson
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a454a6ebeecc763cb7e5a964bb1f2897df6c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341667"
---
# <a name="iagentcharactersetsoundeffectson"></a><span data-ttu-id="a9dc3-103">Iagentcharacter:: setsounde ffectson</span><span class="sxs-lookup"><span data-stu-id="a9dc3-103">IAgentCharacter::SetSoundEffectsOn</span></span>

<span data-ttu-id="a9dc3-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a9dc3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

<span data-ttu-id="a9dc3-105">Bestimmt, ob die Soundeffekte des Zeichens wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a9dc3-105">Determines whether the character's sound effects are played.</span></span>

-   <span data-ttu-id="a9dc3-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a9dc3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a9dc3-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Böller*</span><span class="sxs-lookup"><span data-stu-id="a9dc3-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="a9dc3-108">Einstellung für Sound Effekte.</span><span class="sxs-lookup"><span data-stu-id="a9dc3-108">Sound effects setting.</span></span> <span data-ttu-id="a9dc3-109">Wenn dieser Parameter **true** ist, werden die Soundeffekte für Animationen bei der Wiedergabe der Animation wiedergegeben. **false** gibt an, dass keine Soundeffekte wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a9dc3-109">If this parameter is **True**, the sound effects for animations are played when the animation plays; if **False**, sound effects are not played.</span></span>

</dd> </dl>

<span data-ttu-id="a9dc3-110">Diese Einstellung bestimmt, ob Soundeffekte, die als Teil des Zeichens kompiliert werden, wiedergegeben werden, wenn Sie eine zugeordnete Animation wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="a9dc3-110">This setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="a9dc3-111">Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="a9dc3-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="a9dc3-112">Die Einstellung unterliegt auch der Einstellung globaler Soundeffekte des Benutzers in [**iagentaudiooutputproperties:: getusingsoundebug**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="a9dc3-112">The setting is also subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a9dc3-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a9dc3-113">See Also</span></span>

<span data-ttu-id="a9dc3-114">[**Iagentcharacter:: getsounbinffectson**](iagentcharacter--getsoundeffectson.md), [ **iagentaudiooutputproperties:: getusingsoundebug**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="a9dc3-114">[**IAgentCharacter::GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




