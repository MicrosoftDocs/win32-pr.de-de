---
title: IWMPControls-Schnittstelle (VB und C) (Wmp.h)
description: Bietet eine Möglichkeit, die Wiedergabe eines Medienelements zu bearbeiten, indem die Transportsteuerelemente von Windows Media Player dargestellt werden, z. B. Wiedergabe, Beenden und Anhalten. Die IWMPControls-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- IWMPControls-Schnittstelle (VB und C) Windows Media Player
- IWMPControls-Schnittstelle (VB und C) Windows Media Player beschrieben
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b96f79b8942935d9722bf38dbd1ae946b03d16496664b4c069552819785c1f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119309"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a>IWMPControls-Schnittstelle (VB und C#)

Bietet eine Möglichkeit, die Wiedergabe eines Medienelements zu bearbeiten, indem die Transportsteuerelemente von Windows Media Player dargestellt werden, z. B. Wiedergabe, Beenden und Anhalten.

Die **IWMPControls-Schnittstelle** macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **IWMPControls-Schnittstelle (VB und C#)** weist diese Typen von Membern auf:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPControls-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                       | Beschreibung                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Fastforward**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | Startet die schnelle Wiedergabe des Medienelements in Vorwärtsrichtung.<br/>                     |
| [**fastReverse**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | Startet die schnelle Wiedergabe des Medienelements in umgekehrter Richtung.<br/>                     |
| [**nächster**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | Legt das nächste Element in der Wiedergabeliste als aktuelles Element fest.<br/>                          |
| [**anhalten**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | Hält die Wiedergabe des Medienelements an.<br/>                                               |
| [**Spielen**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | Beginnt die Wiedergabe des aktuellen Medienelements oder setzt die Wiedergabe eines angehaltenen Elements fort.<br/> |
| [**playItem**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | Gibt das angegebene Medienelement wieder.<br/>                                                  |
| [**Vorherigen**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | Legt das vorherige Element in der Wiedergabeliste als aktuelles Element fest.<br/>                      |
| [**Stoppen**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | Beendet die Wiedergabe des Medienelements.<br/>                                                |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPControls-Schnittstelle (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                    | Zugriffstyp           | Beschreibung                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Currentitem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | Lesen/Schreiben<br/> | Ruft das aktuelle Medienelement in einer Wiedergabeliste ab oder legt es fest.<br/>                                                                                                                    |
| [**currentMarker**](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | Lesen/Schreiben<br/> | Ruft die aktuelle Markernummer ab oder legt sie fest.<br/>                                                                                                                               |
| [**currentPosition**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | Lesen/Schreiben<br/> | Ruft die aktuelle Position im Medienelement in Sekunden vom Anfang ab oder legt diese fest.<br/>                                                                                    |
| [**currentPositionString**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | Schreibgeschützt<br/>  | Ruft die aktuelle Position im Medienelement als **System.String** ab.<br/>                                                                                                   |
| [**Isavailable**](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | Schreibgeschützt<br/>  | Ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann. In C# ist dies die **get \_ isAvailable-Methode.**<br/> |



 

Abrufen einer **IWMPControls-Schnittstelle** mithilfe der folgenden Eigenschaft.



| Object                                                                   | Eigenschaft                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [AxWindowsMediaPlayer-Objekt](axwindowsmediaplayer-object--vb-and-c.md) | [**Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPControls2-Schnittstelle (VB und C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**IWMPControls3-Schnittstelle (VB und C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





