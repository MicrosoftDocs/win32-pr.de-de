---
description: Enthält das Anwendungs Objekt der Auflistung der Ordner Elemente.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: Folderitems. Application-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7f073b81106923f889ca5209c0aa492f4c4bbd60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127840"
---
# <a name="folderitemsapplication-property"></a>Folderitems. Application (Eigenschaft)

Enthält das **Anwendungs** Objekt der Auflistung der Ordner Elemente.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a>Eigenschaftswert

Ein Objekt Verweis auf das Anwendungs Objekt.

## <a name="remarks"></a>Bemerkungen

Die **Application** -Eigenschaft gibt das Automatisierungs Objekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält. Andernfalls gibt diese Eigenschaft das Automatisierungs Objekt des Webbrowser-Steuer Elements zurück.

Verwenden Sie diese Eigenschaft mit den Befehlen SET **und "** **Set** " oder mit dem Befehl " **GetObject** ", um eine Instanz der Windows Internet Explorer-Anwendung zu erstellen und zu bearbeiten.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 




