---
description: Das safewia-Objekt ist ein &\# 0034; Safe for Scripting&\# 0034; der Einstiegspunkt für alle Funktionen zur WIA-Skripterstellung (Windows Image Acquisition).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Safewia-Objekt
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
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345075"
---
# <a name="safewia-object"></a>Safewia-Objekt

Das **safewia** -Objekt ist der Einstiegspunkt "sicher für Skripting" für alle Skriptfunktionen für die Windows-Abbild Erfassung (WIA). Jede Anwendung, die das WIA-Skript Modell verwendet, muss ein **safewia** -oder [**WIA**](-wia-wia.md) -Objekt erstellen. Verwenden Sie dieses Objekt zum Auflisten und Erstellen von Geräten sowie zum Empfangen von Benachrichtigungen über Hardware Ereignisse.

## <a name="members"></a>Member

Das **safewia** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **safewia** -Objekt verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stelle**](-wia-iwia-create.md) | Die [**Create**](-wia-iwia-create.md) -Methode des [**WIA**](-wia-wia.md) -Objekts stellt eine Verbindung mit dem angegebenen WIA-Gerät her und gibt ein [**Element**](-wia-item.md) Objekt zurück, das das Gerät darstellt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **safewia** -Objekt verfügt über diese Eigenschaften.



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
| IID<br/>                      | CLSID \_ safewia<br/>                                                                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WIA**](-wia-wia.md)
</dt> </dl>

 

 




