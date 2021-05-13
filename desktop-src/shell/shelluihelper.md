---
description: Wird von der Shell implementiert, damit Skripts und Microsoft Visual Basic Entwickler einige der in der Shell verfügbaren Features verwenden können. Das ShellUIHelper-Objekt verfügt nicht über Eigenschaften oder Ereignisse. Es werden Methoden zum Hinzufügen von Elementen zur Shell bereitgestellt.
title: ShellUIHelper-Objekt (Exdisp.h)
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
ms.openlocfilehash: b77d618c4c772859a9009f3cca761c59df83257a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842431"
---
# <a name="shelluihelper-object"></a>ShellUIHelper-Objekt

Wird von der Shell implementiert, um Skripts und Microsoft Visual Basic Entwickler bei der Verwendung einiger der in der Shell verfügbaren Features zu unterstützen. Das **ShellUIHelper-Objekt** verfügt nicht über Eigenschaften oder Ereignisse. Es werden Methoden zum Hinzufügen von Elementen zur Shell bereitgestellt.

## <a name="members"></a>Member

Das **ShellUIHelper-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **ShellUIHelper-Objekt** verfügt über diese Methoden.



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
<td style="text-align: left;"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></td>
<td style="text-align: left;">Fügt der Liste der Kanäle im Menü <strong>"Favoriten"</strong> Internet Explorer und der <strong>Kanalleiste</strong> auf dem Desktop einen neuen Kanal hinzu.<br/>
<blockquote>
[!Note]<br />
Diese Methode wird unter Windows Vista nicht mehr unterstützt. Unter diesem Betriebssystem wird E_NOTIMPL zurückgegeben.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></td>
<td style="text-align: left;">Fügt dem Active Desktop ein Element hinzu.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></td>
<td style="text-align: left;">Zeigt die Standardbenutzerschnittstelle zum Erstellen eines bevorzugten Elements an. Die Benutzeroberfläche wird mit den angegebenen Parametern initialisiert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></td>
<td style="text-align: left;">Gibt an, ob eine angegebene URL abonniert wird.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




