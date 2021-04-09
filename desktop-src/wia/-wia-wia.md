---
description: Das WIA-Objekt ist der Einstiegspunkt für alle WIA-Skriptfunktionen (Windows Image Acquisition).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: WIA-Objekt
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
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129380"
---
# <a name="wia-object"></a>WIA-Objekt

Das **WIA** -Objekt ist der Einstiegspunkt für alle WIA-Skriptfunktionen (Windows Image Acquisition). Jede Anwendung, die das WIA-Skript Modell verwendet, muss ein [**safewia**](-wia-safewia.md) -oder **WIA** -Objekt erstellen. Verwenden Sie dieses Objekt zum Auflisten und Erstellen von Geräten sowie zum Empfangen von Benachrichtigungen über Hardware Ereignisse.

> [!Note]  
> Dieses Objekt ist für die Skripterstellung nicht sicher. Eine Version dieses Objekts, die für die Skripterstellung sicher ist, finden Sie unter [**safewia**](-wia-safewia.md).

 

## <a name="members"></a>Member

Das **WIA** -Objekt verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **WIA** -Objekt enthält diese Ereignisse.



| Ereignis                                                                 | BESCHREIBUNG                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Onde viceconnected**](-wia--iwiaevents-ondeviceconnected.md)       | Das Ereignis tritt auf, wenn ein neues WIA-Hardware Gerät verbunden ist.<br/>    |
| [**Ondevicegetrennte**](-wia--iwiaevents-ondevicedisconnected.md) | Das Ereignis tritt auf, wenn ein neues WIA-Hardware Gerät getrennt wird.<br/> |
| [**Ontransfercomplete**](-wia--iwiaevents-ontransfercomplete.md)     | Das Ereignis tritt auf, wenn eine Datenübertragung erfolgreich abgeschlossen wurde.<br/> |



 

### <a name="methods"></a>Methoden

Das **WIA** -Objekt verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stelle**](-wia-iwia-create.md) | Die [**Create**](-wia-iwia-create.md) -Methode des **WIA** -Objekts stellt eine Verbindung mit dem angegebenen WIA-Gerät her und gibt ein [**Element**](-wia-item.md) Objekt zurück, das das Gerät darstellt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **WIA** -Objekt verfügt über diese Eigenschaften.



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
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>Geräte</strong></a><br/></td>
<td style="text-align: left;">Schreibgeschützt<br/></td>
<td style="text-align: left;">Sammlung von " <a href="-wia-deviceinfo.md"><strong>de viceinfo</strong></a> "-Objekten, die alle auf dem Computer installierten Geräte darstellen. Schreibgeschützt. <br/>
<blockquote>
[!Note]<br />
Diese Auflistung ist 0-basiert.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |
| IID<br/>                      | CLSID- \_ WIA<br/>                                                                                         |



 

 




