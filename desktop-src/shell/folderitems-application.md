---
description: Enthält das Application-Objekt der Ordnerelementesammlung.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: FolderItems.Application-Eigenschaft (Shldisp.h)
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
ms.openlocfilehash: 3809d76576b69c53f6fc5f8a11ab954242e3a89c9a369ada2f4fa47c460f523f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032608"
---
# <a name="folderitemsapplication-property"></a>FolderItems.Application (Eigenschaft)

Enthält das **Application-Objekt** der Ordnerelementesammlung.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a>Eigenschaftswert

Ein Objektverweis auf das Anwendungsobjekt.

## <a name="remarks"></a>Hinweise

Die **Application-Eigenschaft** gibt das Automatisierungsobjekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält, wenn auf dieses Objekt zugegriffen werden kann. Andernfalls gibt diese Eigenschaft das Automatisierungsobjekt des WebBrowser-Steuerelements zurück.

Verwenden Sie diese Eigenschaft mit den **Befehlen Set** und **CreateObject** oder mit dem **GetObject-Befehl,** um eine Instanz der Windows Internet Explorer zu erstellen und zu bearbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




