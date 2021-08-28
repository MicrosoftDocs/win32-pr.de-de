---
title: IAgentCharacter GetSoundEffectsOn
description: IAgentCharacter GetSoundEffectsOn
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f7133e41e4c291200feaf8fdb8ab3919cdb622ca927c155fc0941202fd555a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848640"
---
# <a name="iagentcharactergetsoundeffectson"></a>IAgentCharacter::GetSoundEffectsOn

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

Ruft ab, ob die Einstellung für Soundeffekte des Zeichens aktiviert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Adresse einer Variablen, die **True** empfängt, wenn die Soundeffekteinstellung des Zeichens aktiviert ist, **False,** wenn deaktiviert.

</dd> </dl>

Die Einstellung für Soundeffekte des Zeichens bestimmt, ob als Teil des Zeichens kompilierte Soundeffekte wiedergegeben werden, wenn Sie eine zugeordnete Animation wiedergeben. Die Einstellung unterliegt der Globalen Soundeffekteinstellung des Benutzers in [**IAgentAudioOutputProperties::GetUsingSoundEffects.**](iagentaudiooutputproperties--getusingsoundeffects.md)

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [ **IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




