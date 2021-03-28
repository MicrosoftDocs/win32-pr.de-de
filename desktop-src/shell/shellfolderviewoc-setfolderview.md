---
description: Leitet die Ereignisse des angegebenen shellfolderview-Objekts an den entsprechenden shellfolderviewoc-Ereignishandler weiter.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Shellfolderviewoc. setfolderview-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980424"
---
# <a name="shellfolderviewocsetfolderview-method"></a>Shellfolderviewoc. setfolderview-Methode

Leitet die Ereignisse des angegebenen [**shellfolderview**](shellfolderview.md) -Objekts an den entsprechenden [**shellfolderviewoc**](shellfolderviewoc-object.md) -Ereignishandler weiter.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*oshellfolderview* \[ in\]
</dt> <dd>

Typ: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _

Ein [_ *shellfolderview* *](shellfolderview.md) -Objekt. Die [**enumdone**](shellfolderviewoc-enumdone.md) -und [**SelectionChanged**](shellfolderview-selectionchanged.md) -Ereignisse werden an den entsprechenden [**shellfolderviewoc**](shellfolderviewoc-object.md) -Ereignishandler weitergeleitet.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 
