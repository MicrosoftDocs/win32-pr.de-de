---
title: IWMPSettings2-Schnittstelle (VB und C) (Wmp.h)
description: Stellt Eigenschaften und eine Methode bereit, die die IWMPSettings-Schnittstelle ergänzen. Zusätzlich zu den Eigenschaften und Methoden, die von IWMPSettings geerbt wurden, macht die IWMPSettings2-Schnittstelle die folgenden Eigenschaften verfügbar.
ms.assetid: 6bd0f6dd-df49-4c21-b47c-c8c63f85c2c0
keywords:
- IWMPSettings2-Schnittstelle (VB und C) Windows Media Player
- IWMPSettings2-Schnittstelle (VB und C) Windows Media Player beschrieben
topic_type:
- apiref
api_name:
- IWMPSettings2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e227cc255eee625df926031369ef8be0fe270e377b143adff2c3ed2d9ab0aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135353"
---
# <a name="iwmpsettings2-vb-and-c-interface"></a>IWMPSettings2-Schnittstelle (VB und C#)

Stellt Eigenschaften und eine Methode bereit, die die **IWMPSettings-Schnittstelle** ergänzen.

Zusätzlich zu den Eigenschaften und Methoden, die von **IWMPSettings** geerbt wurden, macht die **IWMPSettings2-Schnittstelle** die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **IWMPSettings2-Schnittstelle (VB und C#)** verfügt über folgende Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPSettings2-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                                                   | Beschreibung                                                     |
|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**requestMediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md) | Fordert eine angegebene Zugriffsebene auf die Bibliothek an.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPSettings2-Schnittstelle (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                    | Zugriffstyp          | Beschreibung                                                                               |
|:------------------------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**defaultAudioLanguage**](wmplibiwmpsettings2-iwmpsettings2-defaultaudiolanguage--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft den Gebietsschemabezeichner (LCID) der Standardaudiosprache ab. <br/>              |
| [**mediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)<br/>       | Schreibgeschützt<br/> | Ruft einen Wert ab, der die derzeit für den Bibliothekszugriff gewährten Berechtigungen angibt. <br/> |



 

Abrufen einer **IWMPSettings2-Schnittstelle** durch Umwandeln des werts, der von der **AxWindowsMediaPlayer.settings-Eigenschaft** zurückgegeben wird.



| Object                                                                   | Eigenschaft                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [AxWindowsMediaPlayer-Objekt](axwindowsmediaplayer-object--vb-and-c.md) | [**Einstellungen**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





