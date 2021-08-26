---
description: Wird von der Shell implementiert, um Skripts und Microsoft Visual Basic Entwicklern die Verwendung einiger der in der Shell verfügbaren Features zu erleichtern. Das ShellUIHelper-Objekt verfügt nicht über Eigenschaften oder Ereignisse. Es werden Methoden zum Hinzufügen von Elementen zur Shell bereitgestellt.
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
ms.openlocfilehash: f254bd218024b3d1df15a826da701b1f010ae616
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473326"
---
# <a name="shelluihelper-object"></a>ShellUIHelper-Objekt

Wird von der Shell implementiert, um Skripts und Microsoft Visual Basic Entwicklern die Verwendung einiger der in der Shell verfügbaren Features zu erleichtern. Das **ShellUIHelper-Objekt** verfügt nicht über Eigenschaften oder Ereignisse. Es werden Methoden zum Hinzufügen von Elementen zur Shell bereitgestellt.

## <a name="members"></a>Member

Das **ShellUIHelper-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **ShellUIHelper-Objekt** verfügt über diese Methoden.




| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a> | Fügt der Liste der Kanäle im Menü <strong>"Favoriten"</strong> Internet Explorer und der <strong>Kanalleiste</strong> auf dem Desktop einen neuen Kanal hinzu.<br /><blockquote>[!Note]<br />Diese Methode wird unter Windows Vista nicht mehr unterstützt. Unter diesem Betriebssystem wird E_NOTIMPL zurückgegeben.</blockquote><br /> | 
| <a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a> | Fügt dem Active Desktop ein Element hinzu.<br /> | 
| <a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a> | Zeigt die Standardbenutzerschnittstelle zum Erstellen eines bevorzugten Elements an. Die Benutzeroberfläche wird mit den angegebenen Parametern initialisiert.<br /> | 
| <a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a> | Gibt an, ob eine angegebene URL abonniert wird.<br /> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




