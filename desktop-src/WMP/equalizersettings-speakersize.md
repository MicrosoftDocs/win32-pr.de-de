---
title: EQUALIZERSETTINGS.speakerSize
description: Das speakerSize-Attribut gibt die Indexnummer der aktuellen Sprechergröße an oder ruft sie ab.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS.speakerSize Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d289a89a22e8c10cf669e9b55fc304826acb3ce0f72468f725e7d5fae0dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748648"
---
# <a name="equalizersettingsspeakersize"></a>EQUALIZERSETTINGS.speakerSize

Das **speakerSize-Attribut** gibt die Indexnummer der aktuellen Sprechergröße an oder ruft sie ab.

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Lese-/Schreibnummer (long), die einen der folgenden Werte enthält.



| Wert | Beschreibung                              |
|-------|------------------------------------------|
| 0     | Die aktuellen Sprecher sind Sprechspeer.     |
| 1     | Die aktuellen Lautsprecher haben eine normale Größe. |
| 2     | Die aktuellen Lautsprecher sind groß.          |



 

## <a name="remarks"></a>Hinweise

Der Anzeigename der Sprechergröße kann mithilfe des **currentSpeakerName-Attributs** abgerufen werden.

Dieses Attribut wird ignoriert, wenn **enhancedAudio** auf FALSE festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EQUALIZERSETTINGS-Element**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.currentSpeakerName**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**EQUALIZERSETTINGS.enhancedAudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





