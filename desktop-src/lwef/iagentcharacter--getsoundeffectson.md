---
title: Iagentcharacter getsoundebug
description: Iagentcharacter getsoundebug
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a40f18a4fb8e7778c116c54391a7dc50e5267af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341888"
---
# <a name="iagentcharactergetsoundeffectson"></a><span data-ttu-id="3bf91-103">Iagentcharacter:: getsounentffectson</span><span class="sxs-lookup"><span data-stu-id="3bf91-103">IAgentCharacter::GetSoundEffectsOn</span></span>

<span data-ttu-id="3bf91-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3bf91-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

<span data-ttu-id="3bf91-105">Ruft ab, ob die Einstellung für die Soundeffekte des Zeichens aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3bf91-105">Retrieves whether the character's sound effects setting is enabled.</span></span>

-   <span data-ttu-id="3bf91-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3bf91-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3bf91-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbon*</span><span class="sxs-lookup"><span data-stu-id="3bf91-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="3bf91-108">Die Adresse einer Variablen, die **true** empfängt, wenn die Einstellung für die Soundeffekte des Zeichens aktiviert ist, und **false** , wenn Sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3bf91-108">Address of a variable that receives **True** if the character's sound effects setting is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="3bf91-109">Die Einstellung Soundeffekte des Zeichens bestimmt, ob Soundeffekte, die als Teil des Zeichens kompiliert werden, beim Abspielen einer zugeordneten Animation wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3bf91-109">The character's sound effects setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="3bf91-110">Die Einstellung unterliegt der Einstellung globaler Soundeffekte des Benutzers in [**iagentaudiooutputproperties:: getusingsoundebug**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="3bf91-110">The setting is subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3bf91-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3bf91-111">See Also</span></span>

<span data-ttu-id="3bf91-112">[**Iagentcharacter:: setsounbinffectson**](iagentcharacter--setsoundeffectson.md), [ **iagentaudiooutputproperties:: getusingsoundebug**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="3bf91-112">[**IAgentCharacter::SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




