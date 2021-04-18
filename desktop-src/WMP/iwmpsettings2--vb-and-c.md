---
title: IWMPSettings2-Schnittstelle (VB und C) (WMP. h)
description: Stellt Eigenschaften und eine Methode bereit, die die iwmpsettings-Schnittstelle ergänzen. Zusätzlich zu den Eigenschaften und Methoden, die von iwmpsettings geerbt werden, macht die IWMPSettings2-Schnittstelle die folgenden Eigenschaften verfügbar.
ms.assetid: 6bd0f6dd-df49-4c21-b47c-c8c63f85c2c0
keywords:
- IWMPSettings2 (VB und C) Interface Windows Media Player
- IWMPSettings2 (VB und C) Interface Windows Media Player, beschrieben
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
ms.openlocfilehash: eb782433085544a94db0eab6b9314f1e4df488e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352116"
---
# <a name="iwmpsettings2-vb-and-c-interface"></a>IWMPSettings2-Schnittstelle (VB und c#)

Stellt Eigenschaften und eine Methode bereit, die die **iwmpsettings** -Schnittstelle ergänzen.

Zusätzlich zu den Eigenschaften und Methoden, die von **iwmpsettings** geerbt werden, macht die **IWMPSettings2** -Schnittstelle die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die IWMPSettings2-Schnittstelle **(VB und c#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die IWMPSettings2-Schnittstelle **(VB und c#)** verfügt über diese Methoden.



| Methode                                                                                                   | BESCHREIBUNG                                                     |
|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**requestmediaaccessrights**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md) | Fordert eine angegebene Zugriffsebene für die Bibliothek an.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die IWMPSettings2-Schnittstelle **(VB und c#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                    | Zugriffstyp          | BESCHREIBUNG                                                                               |
|:------------------------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**defaultaudiolanguage**](wmplibiwmpsettings2-iwmpsettings2-defaultaudiolanguage--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) der standardmäßigen Audiosprache ab. <br/>              |
| [**mediaaccessrights**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)<br/>       | Schreibgeschützt<br/> | Ruft einen Wert ab, der die Berechtigungen angibt, die derzeit für den Bibliotheks Zugriff erteilt werden <br/> |



 

Sie erhalten eine **IWMPSettings2** -Schnittstelle durch Umwandeln des Werts, der von der **AxWindowsMediaPlayer. Settings** -Eigenschaft zurückgegeben wird.



| Object                                                                   | Eigenschaft                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [AxWindowsMediaPlayer-Objekt](axwindowsmediaplayer-object--vb-and-c.md) | [**Einstellungen**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





