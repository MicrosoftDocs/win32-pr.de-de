---
title: Iwmpcontrols (VB und C)-Schnittstelle (WMP. h)
description: Bietet eine Möglichkeit, die Wiedergabe eines Medien Elements zu manipulieren, indem die Transport Steuerelemente von Windows-Media Player dargestellt werden, z. b. wiedergeben, anhalten und anhalten. die iwmpcontrols-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- Iwmpcontrols (VB und C) Interface Windows Media Player
- Iwmpcontrols (VB und C) Interface Windows Media Player, beschrieben
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
ms.openlocfilehash: b544978d801f3a9d5d5cbd9644f1d32ac53791e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373765"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a>Iwmpcontrols (VB und c#)-Schnittstelle

Bietet eine Möglichkeit, die Wiedergabe eines Medien Elements zu manipulieren, indem die Transport Steuerelemente von Windows-Media Player dargestellt werden, z. b. Wiedergabe, anhalten und anhalten.

Die **iwmpcontrols** -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **iwmpcontrols-Schnittstelle (VB und c#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iwmpcontrols-Schnittstelle (VB und c#)** verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**FastForward**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | Startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung.<br/>                     |
| [**fastreverse**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | Startet die schnelle Wiedergabe des Medien Elements in umgekehrter Richtung.<br/>                     |
| [**weiter**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | Legt das nächste Element in der Wiedergabeliste als Aktuelles Element fest.<br/>                          |
| [**Brechung**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | Hält die Wiedergabe des Medien Elements an.<br/>                                               |
| [**Theater**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | Startet die Wiedergabe des aktuellen Medien Elements oder nimmt die Wiedergabe eines angehaltenen Elements wieder auf.<br/> |
| [**PlayItem**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | Gibt das angegebene Medien Element wieder.<br/>                                                  |
| [**vorher**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | Legt das vorherige Element in der Wiedergabeliste als Aktuelles Element fest.<br/>                      |
| [**anzuhalten**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | Beendet die Wiedergabe des Medien Elements.<br/>                                                |



 

### <a name="properties"></a>Eigenschaften

Die **iwmpcontrols-Schnittstelle (VB und c#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                    | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**currentItem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | Lesen/Schreiben<br/> | Ruft das aktuelle Medien Element in einer Wiedergabeliste ab oder legt dieses fest.<br/>                                                                                                                    |
| [**currentmarker**](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | Lesen/Schreiben<br/> | Ruft die aktuelle Markernummer ab oder legt Sie fest.<br/>                                                                                                                               |
| [**CurrentPosition**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | Lesen/Schreiben<br/> | Ruft die aktuelle Position im Medien Element in Sekunden ab oder legt diese fest.<br/>                                                                                    |
| [**currentpositionstring**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | Schreibgeschützt<br/>  | Ruft die aktuelle Position im Medien Element als **System. String** ab.<br/>                                                                                                   |
| [**isAvailable**](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | Schreibgeschützt<br/>  | Ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann. In c# ist dies die **get \_ IsAvailable** -Methode.<br/> |



 

Verwenden Sie die folgende Eigenschaft, um eine **iwmpcontrols** -Schnittstelle zu erhalten.



| Object                                                                   | Eigenschaft                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [AxWindowsMediaPlayer-Objekt](axwindowsmediaplayer-object--vb-and-c.md) | [**CTL-Steuerelemente**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPControls2-Schnittstelle (VB und c#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**IWMPControls3-Schnittstelle (VB und c#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





