---
title: Equalizersettings. nextvoreinstellung
description: Die nextvoreinstellung-Methode wendet die nächste Voreinstellung für den equaliausgleich an.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- Fenster "equalizersettings. nextvoreinstellung" Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372727"
---
# <a name="equalizersettingsnextpreset"></a>Equalizersettings. nextvoreinstellung

Die **nextvoreinstellung** -Methode wendet die nächste Voreinstellung für den equaliausgleich an.

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn es sich bei der aktuellen Voreinstellung um die letzte verfügbare Voreinstellung handelt, wird die erste Voreinstellung als aktuell festgestellt.

## <a name="examples"></a>Beispiele


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Equalizersettings-Element**](equalizersettings-element.md)
</dt> <dt>

[**Equalizersettings. previouationsset**](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





