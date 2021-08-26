---
title: THEME.playSound
description: Die playSound-Methode gibt die angegebene Sounddatei wieder.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- THEME.playSound Windows Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9e6ac0cb7bdf4f8951bafbc89a0a41bf368afcd1021666eb7875739d1cd912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001750"
---
# <a name="themeplaysound"></a>THEME.playSound

Die **playSound-Methode** gibt die angegebene Sounddatei wieder.

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*
</dt> <dd>

Eine **Zeichenfolge,** die den Namen der wieder zu wiedergibtden Sounddatei angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Mit dieser Methode können Sie einer Skin Soundeffekte hinzufügen, z. B. wenn auf Schaltflächen geklickt wird. Der Sound wird direkt vom Betriebssystem und nicht von Windows Media Player. Dies bedeutet, dass der Sound nicht mit Windows Media Player und Methoden gesteuert werden kann, aber er kann während der Wiedergabe Windows Media Player einer anderen digitalen Mediendatei abgespielt werden.

Diese Methode unterstützt nur WAV-Dateien.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**THEME-Element**](theme-element.md)
</dt> </dl>

 

 





