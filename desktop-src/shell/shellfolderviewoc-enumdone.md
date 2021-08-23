---
description: Gibt an, dass das ShellFolderView-Objekt das Aufzählen des Ordnerinhalts abgeschlossen hat.
title: ShellFolderViewOC.EnumDone-Ereignis (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: c725a61a6711dab22d50b774cb02556916dae802a66008a48721d7311e163bce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660640"
---
# <a name="shellfolderviewocenumdone-event"></a>ShellFolderViewOC.EnumDone-Ereignis

Gibt an, dass das [**ShellFolderView-Objekt**](shellfolderview.md) das Aufzählen des Ordnerinhalts abgeschlossen hat.

## <a name="syntax"></a>Syntax


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a>Parameter

Dieser Ereignishandler verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Das [**ShellFolderView-Objekt**](shellfolderview.md) muss den Inhalt eines Ordners aufzählen, bevor es ihn anzeigen kann. Bei ordnern, die groß sind oder sich auf einem Remotesystem befinden, kann dieser Vorgang bis zu mehrere Minuten dauern. Während dieser Zeit wird eine animierte Taschenlampengrafik angezeigt, um dem Benutzer anzuzeigen, dass die Verarbeitung läuft. Sobald die Enumeration abgeschlossen ist, wird das **EnumDone-Ereignis** ausgelöst, und die Taschenlampengrafik wird durch den Inhalt des Ordners ersetzt.

Geben Sie wie hier gezeigt Ereignisbehandlungscode für dieses Ereignis an.


```
 
Private Sub object_EnumDone()
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




