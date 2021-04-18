---
title: "\"Settings. Rate\""
description: Die Rate-Eigenschaft gibt die aktuelle Wiedergabe Rate von Video Medien an oder ruft diese ab.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Einstellungen. Raten Sie Windows Media Player
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357652"
---
# <a name="settingsrate"></a>"Settings. Rate"

Die **Rate** -Eigenschaft gibt die aktuelle Wiedergabe Rate von Video Medien an oder ruft diese ab.

## <a name="syntax"></a>Syntax

Player. Settings. Rate

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/schreibzahl (**Double**) mit einem Standardwert von 1,0. 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft fungiert als Multiplikatorwert, mit dem Sie einen Clip schneller oder langsamer abspielen können. Der Standardwert 1,0 gibt die erstellte Geschwindigkeit an. Beachten Sie, dass eine Audiospur bei Raten, die niedriger als 0,5 oder höher als 1,5 sind, schwer zu verstehen ist. Eine Wiedergabe Rate von 2 entspricht der doppelten normalen Wiedergabegeschwindigkeit.

Windows Media Player versucht, die effektivsten von vier verschiedenen Wiedergabe Modi zu verwenden. Bei diesen Modi handelt es sich um eine reibungslose Videowiedergabe, bei der Audiowiedergabe gewartet wird, eine nahtlose Videowiedergabe mit nicht gebeibehaltung Audiowiedergabe, eine Smooth Videowiedergabe ohne Audiodaten und eine Keyframe-Videowiedergabe ohne Audio Der vom Player gewählte Modus hängt von zahlreichen Faktoren ab, einschließlich Dateityp und-Speicherort, Betriebssystem, Netzwerk und Server.

Es gelten auch weitere Überlegungen, abhängig vom Medientyp:

-   Windows Media-Format (WMV) und ASF-Dateien: optimale Werte für diese Eigenschaft liegen zwischen 1 und 10 oder zwischen 1 und 10 für Reverse-Play. Werte zwischen 0,5 und 1,0 oder von-0,5 bis 1,0 funktionieren möglicherweise auch in Fällen, in denen audiotonhöhe beibehalten werden kann, z. b. bei der Wiedergabe von Dateien auf dem lokalen Computer. Werte mit einer absoluten Größe von mehr als 10 sind zulässig, sind jedoch nicht sehr sinnvoll.
-   Andere Video Medientypen: Diese Eigenschaft kann zwischen 0 und 9 liegen. Negative Werte sind nicht zulässig. Werte kleiner als 1 stellen eine langsame Bewegung dar. Werte oberhalb von 9 sind zulässig, sind jedoch nicht sehr sinnvoll.

Die-Steuer *Elemente*. die **FastForward** -Methode ändert den Wert von Rate in 5,0, während die **Steuer** *Elemente*. die **Rate** der **fastreverse** -Methode wurde in 5,0 geändert.

Die Wiedergabe Rate einiger Medientypen kann nicht geändert werden. Verwenden Sie die *Einstellungen*. **IsAvailable** -Methode, um zu bestimmen, ob diese Eigenschaft für ein bestimmtes Medien Element angegeben werden kann.

**Windows Media Player 10 Mobile**: Diese Eigenschaft akzeptiert nur die Werte von-5,0, 1,0 oder 5,0.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-SELECT-Element erstellt, das es dem Benutzer ermöglicht, die Wiedergabegeschwindigkeit des aktuellen Mediums zu ändern. Die SELECT-Optionen bieten eine normale Geschwindigkeit, eine halbe Geschwindigkeit und eine doppelte Geschwindigkeit der Wiedergabe Raten. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls. FastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. fastreverse**](controls-fastreverse.md)
</dt> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> <dt>

[**Settings. IsAvailable**](settings-isavailable.md)
</dt> </dl>

 

 





