---
description: Gibt an, dass sich der Auswahlzustand eines oder mehrerer Elemente in der Ansicht geändert hat.
title: ShellFolderViewOC.SelectionChanged-Ereignis (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 264631c43dd9ac20bd0ae47632738c2a37a0a85168b487e17ff86a8a2b71c8ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660630"
---
# <a name="shellfolderviewocselectionchanged-event"></a>ShellFolderViewOC.SelectionChanged-Ereignis

Gibt an, dass sich der Auswahlzustand eines oder mehrerer Elemente in der Ansicht geändert hat.

## <a name="syntax"></a>Syntax


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a>Parameter

Dieser Ereignishandler verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Geben Sie wie hier gezeigt Ereignisbehandlungscode für dieses Ereignis an.


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




