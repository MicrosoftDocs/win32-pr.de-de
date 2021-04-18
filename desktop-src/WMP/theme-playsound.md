---
title: Theme. PlaySound
description: Die PlaySound-Methode gibt die angegebene Audiodatei wieder.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- Design. PlaySound-Fenster Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372404"
---
# <a name="themeplaysound"></a>Theme. PlaySound

Die **PlaySound** -Methode gibt die angegebene Audiodatei wieder.

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*
</dt> <dd>

Eine **Zeichenfolge** , die den Namen der zu Wiedergabe enden Audiodatei angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ermöglicht das Hinzufügen von Soundeffekten zu einer Skin, wenn beispielsweise auf Schaltflächen geklickt wird. Der Sound wird vom Betriebssystem direkt und nicht von Windows Media Player abgespielt. Dies bedeutet, dass der Sound nicht mit Windows Media Player-Einstellungen und-Methoden gesteuert werden kann. er kann jedoch abgespielt werden, während Windows Media Player eine andere digitale Mediendatei wieder gibt.

Diese Methode unterstützt nur WAV-Dateien.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Design-Element**](theme-element.md)
</dt> </dl>

 

 





