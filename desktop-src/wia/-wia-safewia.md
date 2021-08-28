---
description: Das SafeWia-Objekt ist ein &\# 0034;sicher für die Skripterstellung&\# 0034; Einstiegspunkt für alle WIA-Skriptfunktionen (Windows Image Acquisition).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: SafeWia-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: ef324934abee38e2581b6e05c0fdac92145e4f43
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473846"
---
# <a name="safewia-object"></a>SafeWia-Objekt

Das **SafeWia-Objekt** ist ein "sicherer Einstiegspunkt für die Skripterstellung" für alle WIA-Skriptfunktionen (Windows Image Acquisition). Jede Anwendung, die das WIA-Skriptmodell verwendet, muss ein **SafeWia-** oder [**Wia-Objekt**](-wia-wia.md) erstellen. Verwenden Sie dieses Objekt, um Geräte aufzuzählen und zu erstellen und Benachrichtigungen über Hardwareereignisse zu empfangen.

## <a name="members"></a>Member

Das **SafeWia-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SafeWia-Objekt** verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Erstellen**](-wia-iwia-create.md) | Die [**Create-Methode**](-wia-iwia-create.md) des [**Wia-Objekts**](-wia-wia.md) stellt eine Verbindung mit dem angegebenen WIA-Gerät her und gibt ein [**Item-Objekt**](-wia-item.md) zurück, das das Gerät darstellt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **SafeWia-Objekt** verfügt über diese Eigenschaften.




| Eigenschaft | Zugriffstyp | BESCHREIBUNG | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>Geräte</strong></a><br /> | Schreibgeschützt<br /> | Sammlung von <a href="-wia-deviceinfo.md"><strong>DeviceInfo-Objekten,</strong></a> die alle auf dem Computer installierten Geräte darstellen. Schreibgeschützt. <br /><blockquote>[!Note]<br />Diese Auflistung basiert auf 0.</blockquote><br /> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |
| IID<br/>                      | CLSID \_ SafeWia<br/>                                                                                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wia**](-wia-wia.md)
</dt> </dl>

 

 




