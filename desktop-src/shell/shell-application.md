---
description: 'Shell.Application-Eigenschaft: Enthält das Application-Objekt des Objekts.'
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Shell.Application-Eigenschaft (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: abab6e19611b927d69746d9b218da73e543f5d592f43baad8362d3406e521f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858131"
---
# <a name="shellapplication-property"></a>Shell.Application-Eigenschaft

Enthält das Application-Objekt des Objekts.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a>Eigenschaftswert

Eine Variable vom Typ [**IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) die das Application-Objekt empfängt.

## <a name="remarks"></a>Hinweise

Die **Application-Eigenschaft** gibt das Automatisierungsobjekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält, wenn auf dieses Objekt zugegriffen werden kann. Andernfalls gibt diese Eigenschaft das Automatisierungsobjekt des WebBrowser-Steuerelements zurück.

Verwenden Sie diese Eigenschaft mit den Befehlen **Set** und **CreateObject** oder mit dem **Befehl GetObject,** um eine Instanz der Windows Internet Explorer Anwendung zu erstellen und zu bearbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
