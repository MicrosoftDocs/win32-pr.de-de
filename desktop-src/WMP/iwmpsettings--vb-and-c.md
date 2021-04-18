---
title: Iwmpsettings (VB und C)-Schnittstelle (WMP. h)
description: Stellt Eigenschaften und Methoden bereit, mit denen die Werte von Windows Media Player-Einstellungen angezeigt oder festgelegt werden. Die iwmpsettings-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: fb37b455-221e-4cee-a219-cacf2938a92a
keywords:
- Windows Media Player der iwmpsettings-Schnittstelle (VB und C)
- Iwmpsettings (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPSettings (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db911cc6d18ba40777e77a803480c7fcab4ff8ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358040"
---
# <a name="iwmpsettings-vb-and-c-interface"></a>Iwmpsettings-Schnittstelle (VB und c#)

Stellt Eigenschaften und Methoden bereit, mit denen die Werte von Windows Media Player-Einstellungen angezeigt oder festgelegt werden.

Die **iwmpsettings** -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **iwmpsettings (VB und c#)** -Schnittstelle verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iwmpsettings (VB und c#)** -Schnittstelle verfügt über diese Methoden.



| Methode                                                               | BESCHREIBUNG                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**getMode**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md) | Gibt einen Wert zurück, der angibt, ob der Schleifen Modus oder der Shuffle-Modus aktiv ist<br/> |
| [**setMode**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md) | Legt den Schleifen Modus oder den Shuffle-Modus auf aktiv oder inaktiv fest.<br/>               |



 

### <a name="properties"></a>Eigenschaften

Die **iwmpsettings (VB und c#)** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                              | Zugriffstyp           | BESCHREIBUNG                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autostart**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)<br/>                   | Lesen/Schreiben<br/> | Dient zum Abrufen oder Festlegen eines Werts, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird. <br/>                                     |
| [**Schwebe**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)<br/>                       | Lesen/Schreiben<br/> | Ruft den aktuellen Stereo Saldo ab oder legt ihn fest.<br/>                                                                                          |
| [**Basis**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)<br/>                       | Lesen/Schreiben<br/> | Ruft die Basis-URL ab, die für die relative Pfad Auflösung mit URL-Skript Befehlen verwendet wird, die in Inhalte digitaler Medien eingebettet sind, oder legt diese <br/> |
| [**defaultframe**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)<br/>             | Lesen/Schreiben<br/> | Ruft den Namen des Frames ab, der zum Anzeigen einer URL verwendet wird, die in einem **ScriptCommand** -Ereignis empfangen wird, oder legt diesen fest. <br/>                          |
| [**enableerrordialogfelder**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)<br/> | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob automatisch Fehler Dialogfelder angezeigt werden<br/>                                           |
| [**invokeurls**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)<br/>                 | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder legt diesen fest. <br/>                                                  |
| [**isAvailable**](iwmpsettings-isavailable--vb-and-c.md)<br/>                                  | Schreibgeschützt<br/>  | Ruft einen Wert ab, der angibt, ob eine angegebene Aktion ausgeführt werden kann. In c# ist dies die **get \_ IsAvailable** -Methode.<br/>             |
| [**verstum**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)<br/>                             | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob Audiodaten stumm geschaltet werden. <br/>                                                                          |
| [**playcount**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)<br/>                   | Lesen/Schreiben<br/> | Ruft ab oder legt fest, wie oft ein Medien Element wiedergegeben wird. <br/>                                                                         |
| [**zinss**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)<br/>                             | Lesen/Schreiben<br/> | Ruft die aktuelle Wiedergabe Rate für Video ab oder legt Sie fest. <br/>                                                                                |
| [**Handels**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)<br/>                         | Lesen/Schreiben<br/> | Ruft das aktuelle Wiedergabe Volume ab oder legt es fest. <br/>                                                                                        |



 

Verwenden Sie die folgende Eigenschaft, um eine **iwmpsettings** -Schnittstelle zu erhalten.



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

[**IWMPSettings2-Schnittstelle (VB und c#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





