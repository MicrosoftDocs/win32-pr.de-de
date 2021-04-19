---
description: Das deviceInfo-Objekt ermöglicht den Zugriff auf die Eigenschaften eines Windows-Abbild Erfassungs Hardware Geräts (WIA).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Debug-Objekt
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
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368758"
---
# <a name="deviceinfo-object"></a>Debug-Objekt

Das **deviceInfo** -Objekt ermöglicht den Zugriff auf die Eigenschaften eines Windows-Abbild Erfassungs Hardware Geräts (WIA). Außerdem bietet es mithilfe der [**Create**](-wia-iwiadeviceinfo-create.md) -Methode eine Möglichkeit für die Anwendung oder das Skript, eine Verbindung mit dem Gerät herzustellen und ein [**Element**](-wia-item.md) Objekt abzurufen, das das Gerät darstellt. Verwenden Sie die [**Devices**](-wia-iwia-devices.md) -Methode, um eine Sammlung von **deviceInfo** -Objekten abzurufen.

## <a name="members"></a>Member

Das Objekt " **de viceinfo** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **deviceInfo** -Objekt verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stelle**](-wia-iwiadeviceinfo-create.md)           | Die [**Create**](-wia-iwiadeviceinfo-create.md) -Methode des **deviceInfo** -Objekts stellt eine Verbindung mit dem WIA-Gerät her, das durch das **deviceInfo** -Objekt angegeben wird, und gibt ein [**Element**](-wia-item.md) Objekt zurück, das das Gerät darstellt.<br/> |
| [**Getpropbyid**](-wia-iwiadeviceinfo-getpropbyid.md) | Die [**getpropbyid**](-wia-iwiadeviceinfo-getpropbyid.md) -Methode des **deviceInfo** -Objekts verwendet die ID einer Geräte Eigenschaft, um ihren Wert zurückzugeben.<br/>                                                                                               |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **de viceinfo** " verfügt über diese Eigenschaften.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Eigenschaft</th>
<th style="text-align: left;">Zugriffstyp</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-id.md"><strong>Name</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ruft die ID des WIA-Hardware Geräts ab. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Hersteller</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ruft den Namen des Herstellers dieses Hardware Geräts ab.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Der Name des WIA-Hardware Geräts, wie er in der Benutzeroberfläche angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ruft den Port ab, mit dem das WIA-Hardware Gerät verbunden ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-type.md"><strong>type</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ruft den Typ des WIA-Hardware Geräts ab. Dabei sind folgende Werte möglich: <br/>
<ul>
<li>Digitalcamera</li>
<li>Scanner</li>
<li>Streamingvideo</li>
<li>Standard</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>Uiclsid</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Ruft die Klassen-ID der vom Hersteller bereitgestellten Benutzeroberfläche für dieses WIA-Hardware Gerät ab. Der Wert ist eine Zeichen folgen Darstellung einer GUID. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




