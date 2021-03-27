---
description: Gibt an, dass das shellfolderview-Objekt das Auflisten des Ordner Inhalts abgeschlossen hat.
title: Shellfolderviewoc. enumdone-Ereignis (Shldisp. h)
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
ms.openlocfilehash: 3ce02fd418a93ec5914c438fcad39d8dc73c5c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994990"
---
# <a name="shellfolderviewocenumdone-event"></a>Shellfolderviewoc. enumdone-Ereignis

Gibt an, dass das [**shellfolderview**](shellfolderview.md) -Objekt das Auflisten des Ordner Inhalts abgeschlossen hat.

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

## <a name="remarks"></a>Bemerkungen

Das [**shellfolderview**](shellfolderview.md) -Objekt muss den Inhalt eines Ordners auflisten, bevor es angezeigt werden kann. Bei Ordnern, die groß sind oder sich auf einem Remote System befinden, kann dieser Vorgang einige Minuten in Anspruch nehmen. Während dieser Zeit wird eine animierte Taschen Taschen Grafik angezeigt, um dem Benutzer mitzuteilen, dass die Verarbeitung unter dem Weg ist. Sobald die Enumeration abgeschlossen ist, wird das Ereignis **enumdone** ausgelöst, und die Taschenlampen Grafik wird durch den Inhalt des Ordners ersetzt.

Geben Sie den Ereignis Behandlungs Code für dieses Ereignis an, wie hier gezeigt.


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Shellfolderviewoc**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




