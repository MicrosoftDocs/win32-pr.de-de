---
description: Das Wia-Objekt ist der Einstiegspunkt für alle WIA-Skriptfunktionen (Windows Image Acquisition).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: Wia-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 38dc5f7ac4440320827e009a7fd38dd6554ceb70
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469617"
---
# <a name="wia-object"></a>Wia-Objekt

Das **Wia-Objekt** ist der Einstiegspunkt für alle WIA-Skriptfunktionen (Windows Image Acquisition). Jede Anwendung, die das WIA-Skriptmodell verwendet, muss ein [**SafeWia-**](-wia-safewia.md) oder **Wia-Objekt** erstellen. Verwenden Sie dieses Objekt, um Geräte aufzuzählen und zu erstellen und Benachrichtigungen über Hardwareereignisse zu empfangen.

> [!Note]  
> Dieses Objekt ist für Skripts nicht sicher. Eine Version dieses Objekts, die für Skripts sicher ist, finden Sie unter [**SafeWia.**](-wia-safewia.md)

 

## <a name="members"></a>Member

Das **Wia-Objekt** verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **Wia-Objekt** verfügt über diese Ereignisse.



| Ereignis                                                                 | BESCHREIBUNG                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)       | Das Ereignis tritt auf, wenn ein neues WIA-Hardwaregerät verbunden ist.<br/>    |
| [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md) | Das Ereignis tritt auf, wenn ein neues WIA-Hardwaregerät getrennt wird.<br/> |
| [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)     | Das Ereignis tritt auf, wenn eine Datenübertragung erfolgreich abgeschlossen wurde.<br/> |



 

### <a name="methods"></a>Methoden

Das **Wia-Objekt** verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Erstellen**](-wia-iwia-create.md) | Die [**Create-Methode**](-wia-iwia-create.md) des **Wia-Objekts** stellt eine Verbindung mit dem angegebenen WIA-Gerät her und gibt ein [**Item-Objekt**](-wia-item.md) zurück, das das Gerät darstellt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Wia-Objekt** verfügt über diese Eigenschaften.




| Eigenschaft | Zugriffstyp | BESCHREIBUNG | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>Geräte</strong></a><br /> | Schreibgeschützt<br /> | Sammlung von <a href="-wia-deviceinfo.md"><strong>DeviceInfo-Objekten,</strong></a> die alle auf dem Computer installierten Geräte darstellen. Schreibgeschützt. <br /><blockquote>[!Note]<br />Diese Auflistung basiert auf 0.</blockquote><br /> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |
| IID<br/>                      | CLSID \_ Wia<br/>                                                                                         |



 

 




