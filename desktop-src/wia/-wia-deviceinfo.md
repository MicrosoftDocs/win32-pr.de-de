---
description: Das DeviceInfo-Objekt bietet Zugriff auf die Eigenschaften eines WIA-Hardwaregeräts (Windows Image Acquisition).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: DeviceInfo-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 69b34a97483a8a6ce231890454148c7948f63e4e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467177"
---
# <a name="deviceinfo-object"></a>DeviceInfo-Objekt

Das **DeviceInfo-Objekt** ermöglicht den Zugriff auf die Eigenschaften eines Windows WIA-Hardwaregeräts (Image Acquisition). Darüber hinaus bietet er über die [**Create-Methode**](-wia-iwiadeviceinfo-create.md) eine Möglichkeit für die Anwendung oder das Skript, eine Verbindung mit dem Gerät herzustellen und ein [**Item-Objekt**](-wia-item.md) zu erhalten, das das Gerät darstellt. Verwenden [](-wia-iwia-devices.md) Sie die Devices-Methode, um eine Sammlung von **DeviceInfo-Objekten zu** erhalten.

## <a name="members"></a>Member

Das **DeviceInfo-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **DeviceInfo-Objekt** verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Erstellen**](-wia-iwiadeviceinfo-create.md)           | Die [**Create-Methode**](-wia-iwiadeviceinfo-create.md) des **DeviceInfo-Objekts** stellt eine Verbindung mit dem vom **DeviceInfo-Objekt** angegebenen WIA-Gerät und gibt ein [**Item-Objekt**](-wia-item.md) zurück, das das Gerät darstellt.<br/> |
| [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) | Die [**GetPropById-Methode**](-wia-iwiadeviceinfo-getpropbyid.md) des **DeviceInfo-Objekts** verwendet die ID einer Geräteeigenschaft, um ihren Wert zurück zu geben.<br/>                                                                                               |



 

### <a name="properties"></a>Eigenschaften

Das **DeviceInfo-Objekt** verfügt über diese Eigenschaften.




| Eigenschaft | Zugriffstyp | BESCHREIBUNG | 
|----------|-------------|-------------|
| <a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a><br /> | Schreibgeschützt<br /> | Ruft die ID des WIA-Hardwaregeräts ab. <br /> | 
| <a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Hersteller</strong></a><br /> | Schreibgeschützt<br /> | Ruft den Namen des Herstellers dieses Hardwaregeräts ab.<br /> | 
| <a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a><br /> | Schreibgeschützt<br /> | Der Name des WIA-Hardwaregeräts, wie er auf der Benutzeroberfläche angezeigt wird.<br /> | 
| <a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a><br /> | Schreibgeschützt<br /> | Ruft den Port ab, mit dem das WIA-Hardwaregerät verbunden ist.<br /> | 
| <a href="-wia-iwiadeviceinfo-type.md"><strong>type</strong></a><br /> | Schreibgeschützt<br /> | Ruft den Typ des WIA-Hardwaregeräts ab. Mögliche Werte: <br /><ul><li>DigitalCamera</li><li>Scanner</li><li>StreamingVideo</li><li>Standard</li></ul> | 
| <a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a><br /> | Schreibgeschützt<br /> | Ruft die Klassen-ID der vom Hersteller bereitgestellten Benutzeroberfläche für dieses WIA-Hardwaregerät ab. Der Wert ist eine Zeichenfolgendarstellung einer GUID. <br /> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




