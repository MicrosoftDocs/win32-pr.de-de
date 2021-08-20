---
description: 'ShellFolderView.Application-Eigenschaft: Enthält das Application-Objekt des Objekts.'
ms.assetid: 305766b1-a19f-4743-a9e3-6837b3f8ffe0
title: ShellFolderView.Application-Eigenschaft (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5acd73f2009894a1e6fef302a0b50937ab0e6892b1b77d3d0c11885871f1da43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047607"
---
# <a name="shellfolderviewapplication-property"></a>ShellFolderView.Application (Eigenschaft)

Enthält das Application-Objekt des -Objekts.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a>Eigenschaftswert

Eine Variable vom Typ [**IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) die das Anwendungsobjekt empfängt.

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



 

 
