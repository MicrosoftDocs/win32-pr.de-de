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
ms.openlocfilehash: 95ef542f91235b3b068e1b1b54768b4dd453d9b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083468"
---
# <a name="shellfolderviewapplication-property"></a>ShellFolderView.Application-Eigenschaft

Enthält das Application-Objekt des Objekts.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a>Eigenschaftswert

Eine Variable vom Typ [**IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) die das Application-Objekt empfängt.

## <a name="remarks"></a>Bemerkungen

Die **Application-Eigenschaft** gibt das Automatisierungsobjekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält, wenn auf dieses Objekt zugegriffen werden kann. Andernfalls gibt diese Eigenschaft das Automatisierungsobjekt des WebBrowser-Steuerelements zurück.

Verwenden Sie diese Eigenschaft mit den Befehlen **Set** und **CreateObject** oder mit dem **Befehl GetObject,** um eine Instanz der Windows Internet Explorer-Anwendung zu erstellen und zu bearbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
