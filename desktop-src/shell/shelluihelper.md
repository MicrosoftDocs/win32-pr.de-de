---
description: Wird von der Shell implementiert, damit Skripts und Microsoft Visual Basic-Entwicklern einige der in der Shell verfügbaren Features verwenden können. Das shelluihelper-Objekt hat keine Eigenschaften oder Ereignisse. Es werden Methoden bereitgestellt, um der Shell Elemente hinzuzufügen.
title: Shelluihelper-Objekt (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980720"
---
# <a name="shelluihelper-object"></a>Shelluihelper-Objekt

Wird von der Shell implementiert, damit Skripts und Microsoft Visual Basic-Entwicklern einige der in der Shell verfügbaren Features verwenden können. Das **shelluihelper** -Objekt hat keine Eigenschaften oder Ereignisse. Es werden Methoden bereitgestellt, um der Shell Elemente hinzuzufügen.

## <a name="members"></a>Member

Das **shelluihelper** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **shelluihelper** -Objekt verfügt über diese Methoden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Methode</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addchannel.md"><strong>Addchannel</strong></a></td>
<td style="text-align: left;">Fügt der Liste der Channels im Internet Explorer-Menü " <strong>Favoriten</strong> " und der <strong>Kanal</strong> Leiste auf dem Desktop einen neuen Kanal hinzu.<br/>
<blockquote>
[!Note]<br />
Diese Methode wird unter Windows Vista nicht mehr unterstützt. Unter diesem Betriebssystem wird E_NOTIMPL zurückgegeben.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-adddesktopcomponent.md"><strong>Adddesktopcomponent</strong></a></td>
<td style="text-align: left;">Fügt dem aktiven Desktop ein Element hinzu.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addfavorite.md"><strong>Addfavorit</strong></a></td>
<td style="text-align: left;">Zeigt die Standardbenutzer Oberfläche zum Erstellen eines bevorzugten Elements an. Die Benutzeroberfläche wird mit den angegebenen Parametern initialisiert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></td>
<td style="text-align: left;">Gibt an, ob eine angegebene URL abonniert ist.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 




