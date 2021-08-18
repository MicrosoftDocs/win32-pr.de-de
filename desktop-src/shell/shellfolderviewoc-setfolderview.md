---
description: Gibt die Ereignisse des angegebenen ShellFolderView-Objekts an den entsprechenden ShellFolderViewOC-Ereignishandler weiter.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: ShellFolderViewOC.SetFolderView-Methode (Shldisp.h)
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
ms.openlocfilehash: 41a37d1b8f9874bdddd5a9593e0eade8bc0b5b92d30f8ada4ee9c6295af1d632
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968399"
---
# <a name="shellfolderviewocsetfolderview-method"></a>ShellFolderViewOC.SetFolderView-Methode

Gibt die Ereignisse des angegebenen [**ShellFolderView-Objekts**](shellfolderview.md) an den entsprechenden [**ShellFolderViewOC-Ereignishandler**](shellfolderviewoc-object.md) weiter.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*oShellFolderView* \[ In\]
</dt> <dd>

Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\***

Ein [**ShellFolderView-Objekt.**](shellfolderview.md) Die [**Ereignisse EnumDone**](shellfolderviewoc-enumdone.md) und [**SelectionChanged**](shellfolderview-selectionchanged.md) werden an den entsprechenden [**ShellFolderViewOC-Ereignishandler**](shellfolderviewoc-object.md) weitergeleitet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
