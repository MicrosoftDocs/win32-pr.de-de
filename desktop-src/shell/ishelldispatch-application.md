---
description: Enthält ein -Objekt, das eine Anwendung darstellt.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: IShellDispatch.Application-Eigenschaft (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5fbdbd8b2cc847a1b06a316d6f8caebfe1e2e5e4fc79fc4be2ff2ebdb8ee3912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443320"
---
# <a name="ishelldispatchapplication-property"></a>IShellDispatch.Application-Eigenschaft

Enthält ein -Objekt, das eine Anwendung darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a>Eigenschaftswert

Eine Variable vom Typ [**IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) die das Anwendungsobjekt empfängt.

## <a name="remarks"></a>Hinweise

Auf diese Eigenschaft wird über die [**Shell.EjectPC-Eigenschaft**](shell-ejectpc.md) zugegriffen.

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



 

 
