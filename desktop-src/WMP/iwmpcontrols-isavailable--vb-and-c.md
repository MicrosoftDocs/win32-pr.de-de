---
title: Iwmpcontrols. IsAvailable (VB und C)
description: Die IsAvailable-Eigenschaft (die get \_ IsAvailable-Methode in C \) Ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- Iwmpcontrols. IsAvailable (VB und C) Windows Media Player
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
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370092"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a>Iwmpcontrols. IsAvailable (VB und c#)

Mit der **IsAvailable** -Eigenschaft (der **get \_ IsAvailable** -Methode in c#) wird ein Wert abgerufen, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.


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

*bstritem*

Ein System. String-Wert, der einem der folgenden Werte entspricht.



| Wert           | BESCHREIBUNG                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | Ermittelt, ob der Benutzer die **iwmpcontrols. accesstitem** -Eigenschaft festlegen kann.                                                                                     |
| currentmarker   | Ermittelt, ob der Benutzer einen bestimmten Marker suchen kann.                                                                                                         |
| CurrentPosition | Ermittelt, ob der Benutzer eine bestimmte Position in der Datei suchen kann. Einige Dateien unterstützen keine Suchvorgänge.                                                        |
| FastForward     | Ermittelt, ob die Datei eine schnelle Weiterleitung unterstützt und ob diese Funktion aufgerufen werden kann. FastForward wird von vielen Dateitypen (und Livestreams) nicht unterstützt. |
| fastreverse     | Ermittelt, ob die Datei fastreverse unterstützt und ob diese Funktion aufgerufen werden kann. Fastreverse wird von vielen Dateitypen (und Livestreams) nicht unterstützt.     |
| Weiter            | Ermittelt, ob der Benutzer den nächsten Eintrag in einer Wiedergabeliste suchen kann.                                                                                              |
| pause           | Ermittelt, ob die **iwmpcontrols. Pause** -Methode verfügbar ist.                                                                                                 |
| Theater            | Ermittelt, ob die **iwmpcontrols. Play** -Methode verfügbar ist.                                                                                                  |
| Vorherige        | Ermittelt, ob der Benutzer den vorherigen Eintrag in einer Wiedergabeliste suchen kann.                                                                                          |
| Schritt            | Ermittelt, ob die **IWMPControls2. Step** -Methode während der Wiedergabe verfügbar ist.                                                                                 |
| stop            | Ermittelt, ob die **iwmpcontrols.** End-Methode verfügbar ist.                                                                                                  |



 

## <a name="property-value"></a>Eigenschaftswert

**System.Boolean**

Ein **System. boolescher** Wert, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.

## <a name="remarks"></a>Bemerkungen

**Iwmpcontrols. IsAvailable** ist eine Eigenschaft in Visual Basic, die einen-Parameter annimmt. In c# wird dies als **iwmpcontrols. get \_ IsAvailable** -Methode bezeichnet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **IsAvailable** -Eigenschaft (die **get \_ IsAvailable** -Methode in c#) verwendet, um zu überprüfen, ob das aktuelle Medien Element die **CurrentPosition** -Eigenschaft unterstützt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Currency Item (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Pause (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Play (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Iwmpcontrols. Stopps (VB und c#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPControls2. Step (VB und c#)**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





