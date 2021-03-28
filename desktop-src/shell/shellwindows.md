---
description: Stellt eine Auflistung der geöffneten Fenster dar, die zur Shell gehören. Mit diesen Objekten verknüpfte Methoden können Befehle in der Shell Steuern und ausführen sowie andere shellbezogene Objekte abrufen.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Shellwindows-Objekt (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979809"
---
# <a name="shellwindows-object"></a>Shellwindows-Objekt

Stellt eine Auflistung der geöffneten Fenster dar, die zur Shell gehören. Mit diesen Objekten verknüpfte Methoden können Befehle in der Shell Steuern und ausführen sowie andere shellbezogene Objekte abrufen.

## <a name="members"></a>Member

Das **shellwindows** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **shellwindows** -Objekt verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](shellwindows--newenum-method-7ral.md) | Erstellt ein neues **shellwindows** -Objekt, das eine Kopie dieses **shellwindows** -Objekts ist, und gibt es zurück.<br/>        |
| [**Element**](shellwindows-item.md)                      | Ruft ein [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) -Objekt ab, das das Shellfenster darstellt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **shellwindows** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                       | Zugriffstyp          | BESCHREIBUNG                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Anzahl**](shellwindows-count.md)<br/> | Schreibgeschützt<br/> | Enthält die Anzahl der Elemente in der Auflistung.<br/> |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 
