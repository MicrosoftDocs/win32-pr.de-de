---
description: Stellt eine Auflistung der geöffneten Fenster dar, die zur Shell gehören. Methoden, die diesen Objekten zugeordnet sind, können Befehle in der Shell steuern und ausführen und andere Shell-bezogene Objekte abrufen.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: ShellWindows-Objekt (Exdisp.h)
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
ms.openlocfilehash: b558bf4df33e84fabae7e70c1722d78647514a52df8f62d05f8ecba8916c488a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857089"
---
# <a name="shellwindows-object"></a>ShellWindows-Objekt

Stellt eine Auflistung der geöffneten Fenster dar, die zur Shell gehören. Methoden, die diesen Objekten zugeordnet sind, können Befehle in der Shell steuern und ausführen und andere Shell-bezogene Objekte abrufen.

## <a name="members"></a>Member

Das **ShellWindows-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **ShellWindows-Objekt** verfügt über diese Methoden.



| Methode                                                 | Beschreibung                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](shellwindows--newenum-method-7ral.md) | Erstellt ein neues **ShellWindows-Objekt,** das eine Kopie dieses **ShellWindows-Objekts** ist, und gibt es zurück.<br/>        |
| [**Element**](shellwindows-item.md)                      | Ruft ein [**InternetExplorer-Objekt**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) ab, das das Shellfenster darstellt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **ShellWindows-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                       | Zugriffstyp          | Beschreibung                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Anzahl**](shellwindows-count.md)<br/> | Schreibgeschützt<br/> | Enthält die Anzahl der Elemente in der Auflistung.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
