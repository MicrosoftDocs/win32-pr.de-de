---
description: Enthält ein-Objekt, das eine Anwendung darstellt.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: Ishelldispatch. Application-Eigenschaft (Shldisp. h)
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
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527356"
---
# <a name="ishelldispatchapplication-property"></a>Ishelldispatch. Application (Eigenschaft)

Enthält ein-Objekt, das eine Anwendung darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a>Eigenschaftswert

Eine Variable vom Typ [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die das Anwendungs Objekt empfängt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird implementiert, und der Zugriff erfolgt über die [**Shell. ejectpc**](shell-ejectpc.md) -Eigenschaft.

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



 

 
