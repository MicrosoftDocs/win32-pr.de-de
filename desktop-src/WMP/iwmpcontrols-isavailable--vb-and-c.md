---
title: IWMPControls.isAvailable (VB und C )
description: Die isAvailable-Eigenschaft (die get \_ isAvailable-Methode in C\) ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls.isAvailable (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73562fb4f96731216c30ada33db8e13d1468b31fb6fcefe7eedef6dd7892348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054848"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a>IWMPControls.isAvailable (VB und C#)

Die **isAvailable-Eigenschaft** (die **get \_ isAvailable-Methode** in C#) ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Parameter

*bstrItem*

Eine System.String,die einer der folgenden Werte ist.



| Wert           | Beschreibung                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Currentitem     | Ermittelt, ob der Benutzer die **IWMPControls.currentItem-Eigenschaft** festlegen kann.                                                                                     |
| currentMarker   | Ermittelt, ob der Benutzer nach einem bestimmten Marker suchen kann.                                                                                                         |
| currentPosition | Ermittelt, ob der Benutzer eine bestimmte Position in der Datei suchen kann. Einige Dateien unterstützen keine Suche.                                                        |
| Fastforward     | Ermittelt, ob die Datei die schnelle Weiterleitung unterstützt und ob diese Funktionalität aufgerufen werden kann. Viele Dateitypen (und Livestreams) unterstützen fastForward nicht. |
| fastReverse     | Ermittelt, ob die Datei fastReverse unterstützt und ob diese Funktionalität aufgerufen werden kann. Viele Dateitypen (und Livestreams) unterstützen fastReverse nicht.     |
| Weiter            | Ermittelt, ob der Benutzer den nächsten Eintrag in einer Wiedergabeliste suchen kann.                                                                                              |
| pause           | Ermittelt, ob die **IWMPControls.pause-Methode** verfügbar ist.                                                                                                 |
| Spielen            | Ermittelt, ob die **IWMPControls.play-Methode** verfügbar ist.                                                                                                  |
| Vorherige        | Ermittelt, ob der Benutzer den vorherigen Eintrag in einer Wiedergabeliste suchen kann.                                                                                          |
| Schritt            | Ermittelt, ob die **IWMPControls2.step-Methode** während der Wiedergabe verfügbar ist.                                                                                 |
| stop            | Ermittelt, ob die **IWMPControls.stop-Methode** verfügbar ist.                                                                                                  |



 

## <a name="property-value"></a>Eigenschaftswert

**System.Boolean**

Ein **System.Boolean,** der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.

## <a name="remarks"></a>Hinweise

**IWMPControls.isAvailable** ist eine Eigenschaft in Visual Basic, die einen Parameter annimmt. In C# wird dies als **IWMPControls.get \_ isAvailable-Methode** bezeichnet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **isAvailable-Eigenschaft** (die **get \_ isAvailable-Methode** in C#) verwendet, um zu überprüfen, ob das aktuelle Medienelement die **currentPosition-Eigenschaft** unterstützt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPControls-Schnittstelle (VB und C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentItem (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPControls.pause (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls.stop (VB und C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPControls2.step (VB und C#)**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





