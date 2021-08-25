---
description: Die UOPValid-Methode ruft einen Wert ab, der angibt, ob der angegebene Benutzervorgang (UOP) derzeit gültig ist.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: UOPValid-Methode (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eee8f11fbcc51c982b2a619f35fdd56b0f0eebe86945e84f18d6ce62afa783b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078670"
---
# <a name="uopvalid-method"></a>UOPValid-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die -Methode ruft einen Wert ab, der angibt, ob der angegebene Benutzervorgang `UOPValid` (UOP) derzeit gültig ist.

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*
</dt> <dd>

Gibt den Benutzervorgang (UOP) als ganze Zahl an.



| Wert | BESCHREIBUNG                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | [**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)                                                                                      |
| 1     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 2     | [**PlayTitle**](playtitle-method.md)                                                                                                                                                                                    |
| 3     | [**Stoppen**](stop-method.md)                                                                                                                                                                                              |
| 4     | [**ReturnFromSubmenu**](returnfromsubmenu-method.md)                                                                                                                                                                    |
| 5     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 6     | [**PlayPrevChapter**](playprevchapter-method.md), [ **ReplayChapter**](replaychapter-method.md)                                                                                                                         |
| 7     | [**PlayNextChapter**](playnextchapter-method.md)                                                                                                                                                                        |
| 8     | [**PlayForwards**](playforwards-method.md)                                                                                                                                                                              |
| 9     | [**PlayBackwards**](playbackwards-method.md)                                                                                                                                                                            |
| 10    | [**ShowMenu mit**](showmenu-method.md) dem Parameterwert 2 \_ (DVD-MENÜtitel) \_                                                                                                                                       |
| 11    | [**ShowMenu mit**](showmenu-method.md) dem Parameterwert 3 (DVD \_ MENU \_ Root)                                                                                                                                        |
| 12    | [**ShowMenu**](showmenu-method.md) mit einem Parameterwert von 4 (DVD \_ MENU \_ Subpicture)                                                                                                                                  |
| 13    | [**ShowMenu mit**](showmenu-method.md) einem Parameterwert von 5 (DVD \_ MENU \_ Audio)                                                                                                                                       |
| 14    | [**ShowMenu mit**](showmenu-method.md) einem Parameterwert von 6 (DVD \_ MENU \_ Angle)                                                                                                                                       |
| 15    | [**ShowMenu mit**](showmenu-method.md) einem Parameterwert von 7 (DVD \_ MENU \_ Chapter)                                                                                                                                     |
| 16    | [**Fortsetzen**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md) |
| 18    | [**StillOff**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**Anhalten**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**CurrentAudioStream**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**CurrentSubpictureStream**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**SollaudioPresentationMode**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | Wählen Sie die Einstellung video mode (Videomoduseinstellung) aus.                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob der angegebene Vorgang vom UOP-Steuerelement zugelassen wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment.h</dt> </dl> |



 

 




