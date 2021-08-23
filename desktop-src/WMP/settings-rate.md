---
title: Einstellungen.rate
description: Die eigenschaft rate gibt die aktuelle Wiedergaberate von Videomedien an oder ruft sie ab.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Einstellungen.rate Windows Media Player
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
ms.openlocfilehash: 01936462593b8b27a8d45f2e3e4090b9cf242d79e1d9b1c2cda00c152bd41182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646400"
---
# <a name="settingsrate"></a>Einstellungen.rate

Die **eigenschaft rate** gibt die aktuelle Wiedergaberate von Videomedien an oder ruft sie ab.

## <a name="syntax"></a>Syntax

player.settings.rate

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/Schreibnummer (**double**) mit dem Standardwert 1.0. 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft fungiert als Multiplikatorwert, mit dem Sie einen Clip schneller oder langsamer wiederverspielen können. Der Standardwert 1,0 gibt die erstellungsgeschwindigkeit an. Beachten Sie, dass eine Audiospur mit Raten unter 0,5 oder höher als 1,5 schwer zu verstehen ist. Eine Wiedergaberate von 2 entspricht der doppelten normalen Wiedergabegeschwindigkeit.

Windows Media Player versucht, die effektivste von vier verschiedenen Wiedergabemodi zu verwenden. Diese Modi sind eine reibungslose Videowiedergabe mit beibehaltener Audiowiedergabe, eine reibungslose Videowiedergabe mit nicht verwalteter Audiowiedergabe, eine reibungslose Videowiedergabe ohne Audio und eine Keyframe-Videowiedergabe ohne Audio. Der vom Player gewählte Modus hängt von zahlreichen Faktoren ab, einschließlich Dateityp und Speicherort, Betriebssystem, Netzwerk und Server.

Je nach Medientyp gelten auch andere Überlegungen:

-   Windows Medienformatdateien (WMV) und ASF-Dateien: Optimale Werte für diese Eigenschaft liegen zwischen 1 und 10 oder von 1 bis 10 für reverse play. Werte von 0,5 bis 1,0 oder von -0,5 bis -1,0 funktionieren möglicherweise auch gut in Fällen, in denen audio pitch beibehalten werden kann, z. B. bei der Wiedergabe von Dateien auf dem lokalen Computer. Werte mit einer absoluten Größe größer als 10 sind zulässig, sind jedoch nicht sehr aussagekräftig.
-   Andere Videomedientypen: Diese Eigenschaft kann zwischen 0 und 9 liegen. Negative Werte sind nicht zulässig. Werte kleiner als 1 stellen langsame Bewegung dar. Werte über 9 sind zulässig, aber nicht sehr aussagekräftig.

Das *-Steuerelement*. **Die fastForward-Methode** ändert den Wert der **Rate** in 5,0, während die *Controls -Methode .* **Die fastReverse-Methode** **ändert die Rate** in 5.0.

Die Wiedergaberate einiger Medientypen kann nicht geändert werden. Verwenden Sie *Einstellungen*. **isAvailable-Methode,** um zu bestimmen, ob diese Eigenschaft für ein bestimmtes Medienelement angegeben werden kann.

**Windows Media Player 10 Mobile:** Diese Eigenschaft akzeptiert oder gibt nur Werte von -5.0, 1.0 oder 5.0 zurück.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML SELECT-Element erstellt, mit dem der Benutzer die Wiedergabegeschwindigkeit des aktuellen Mediums ändern kann. Die SELECT-Optionen bieten normale Geschwindigkeit, halbe Geschwindigkeit und Doppelte Geschwindigkeit bei der Wiedergabe. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls.fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls.fastReverse**](controls-fastreverse.md)
</dt> <dt>

[**Einstellungen Objekt**](settings-object.md)
</dt> <dt>

[**Einstellungen.isAvailable**](settings-isavailable.md)
</dt> </dl>

 

 





