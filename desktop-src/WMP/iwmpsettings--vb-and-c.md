---
title: IWMPSettings-Schnittstelle (VB und C) (Wmp.h)
description: Stellt Eigenschaften und Methoden bereit, die die Werte Windows Media Player Einstellungen abrufen oder festlegen. Die IWMPSettings-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: fb37b455-221e-4cee-a219-cacf2938a92a
keywords:
- IWMPSettings-Schnittstelle (VB und C) Windows Media Player
- IWMPSettings-Schnittstelle (VB und C) Windows Media Player beschrieben
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
ms.openlocfilehash: 6a537efcd9b39f993705244020e579b9d667164180fd5cd70ab05fc692bed8fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996470"
---
# <a name="iwmpsettings-vb-and-c-interface"></a>IWMPSettings-Schnittstelle (VB und C#)

Stellt Eigenschaften und Methoden bereit, die die Werte Windows Media Player Einstellungen abrufen oder festlegen.

Die **IWMPSettings-Schnittstelle** macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **IWMPSettings-Schnittstelle (VB und C#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPSettings-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                               | Beschreibung                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**getMode**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md) | Gibt einen Wert zurück, der angibt, ob der Schleifenmodus oder der Shufflemodus aktiv ist.<br/> |
| [**setMode**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md) | Legt den Schleifenmodus oder Shufflemodus auf aktiv oder inaktiv fest.<br/>               |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPSettings-Schnittstelle (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                              | Zugriffstyp           | Beschreibung                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**autoStart**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)<br/>                   | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob das aktuelle Medienelement automatisch wiedergegeben wird, oder legt diesen fest. <br/>                                     |
| [**Gleichgewicht**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)<br/>                       | Lesen/Schreiben<br/> | Ruft die aktuelle Stereo-Ausgewogenheit ab oder legt sie fest.<br/>                                                                                          |
| [**baseURL**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)<br/>                       | Lesen/Schreiben<br/> | Ruft die Basis-URL ab, die für die relative Pfadauflösung mit URL-Skriptbefehlen verwendet wird, die in digitale Medieninhalte eingebettet sind, oder legt diese fest. <br/> |
| [**defaultFrame**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)<br/>             | Lesen/Schreiben<br/> | Ruft den Namen des Frames ab, der zum Anzeigen einer URL verwendet wird, die in einem **scriptCommand-Ereignis** empfangen wird, oder legt diesen fest. <br/>                          |
| [**enableErrorDialogs**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)<br/> | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob Fehlerdialogfelder automatisch angezeigt werden, oder legt einen Wert fest.<br/>                                           |
| [**invokeURLs**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)<br/>                 | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder legt den Wert fest. <br/>                                                  |
| [**Isavailable**](iwmpsettings-isavailable--vb-and-c.md)<br/>                                  | Schreibgeschützt<br/>  | Ruft einen Wert ab, der angibt, ob eine angegebene Aktion ausgeführt werden kann. In C# ist dies die **get \_ isAvailable-Methode.**<br/>             |
| [**Stumm**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)<br/>                             | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, ob audio stummgeschaltet ist, oder legt einen Wert fest. <br/>                                                                          |
| [**playCount**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)<br/>                   | Lesen/Schreiben<br/> | Ruft ab oder legt fest, wie oft ein Medienelement wiedergegeben wird. <br/>                                                                         |
| [**Rate**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)<br/>                             | Lesen/Schreiben<br/> | Ruft die aktuelle Wiedergaberate für Video ab oder legt sie fest. <br/>                                                                                |
| [**Volumen**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)<br/>                         | Lesen/Schreiben<br/> | Ruft das aktuelle Wiedergabevolume ab oder legt dieses fest. <br/>                                                                                        |



 

Abrufen einer **IWMPSettings-Schnittstelle** mithilfe der folgenden Eigenschaft.



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

[**IWMPSettings2-Schnittstelle (VB und C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





