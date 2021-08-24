---
title: IAgentCharacter SetSoundEffectsOn
description: IAgentCharacter SetSoundEffectsOn
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71abb6adebf09182d4329202e77355e7dc365899291995e97eca66305a00ab94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725020"
---
# <a name="iagentcharactersetsoundeffectson"></a>IAgentCharacter::SetSoundEffectsOn

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

Bestimmt, ob die Soundeffekte des Zeichens abgespielt werden.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Bon*
</dt> <dd>

Einstellung für Soundeffekte. Wenn dieser Parameter True **ist,** werden die Soundeffekte für Animationen abgespielt, wenn die Animation wiedergibt. False **gibt an,** dass keine Soundeffekte abgespielt werden.

</dd> </dl>

Diese Einstellung bestimmt, ob Soundeffekte, die als Teil des Zeichens kompiliert wurden, beim Wiederspielen einer zugeordneten Animation abgespielt werden. Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens. Die Einstellung unterliegt auch der Einstellung für globale Soundeffekte des Benutzers in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [ **IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




