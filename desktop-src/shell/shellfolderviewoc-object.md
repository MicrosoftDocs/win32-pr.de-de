---
description: Leitet die von einem angegebenen shellfolderview-Objekt ausgelösten Ereignisse an entsprechende shellfolderviewoc-Ereignishandler weiter.
title: Shellfolderviewoc-Objekt (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: b9a2b76f48731bf4c7b515779122503fa2cb02f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960509"
---
# <a name="shellfolderviewoc-object"></a>Shellfolderviewoc-Objekt

Leitet die von einem angegebenen [**shellfolderview**](shellfolderview.md) -Objekt ausgelösten Ereignisse an entsprechende **shellfolderviewoc** -Ereignishandler weiter.

## <a name="members"></a>Member

Das **shellfolderviewoc** -Objekt verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)

### <a name="events"></a>Ereignisse

Das **shellfolderviewoc** -Objekt enthält diese Ereignisse.



| Ereignis                                                          | BESCHREIBUNG                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Enumdone**](shellfolderviewoc-enumdone.md)                 | Gibt an, dass das [**shellfolderview**](shellfolderview.md) -Objekt das Auflisten des Ordner Inhalts abgeschlossen hat.<br/> |
| [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) | Gibt an, dass sich der Auswahl Zustand eines oder mehrerer Elemente in der Ansicht geändert hat.<br/>                                     |



 

### <a name="methods"></a>Methoden

Das **shellfolderviewoc** -Objekt verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Setfolderview**](shellfolderviewoc-setfolderview.md) | Leitet die Ereignisse des angegebenen [**shellfolderview**](shellfolderview.md) -Objekts an den entsprechenden **shellfolderviewoc** -Ereignishandler weiter.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das [**shellfolderview**](shellfolderview.md) -Objekt löst zwei Ereignisse (" [**enumdone**](shellfolderviewoc-enumdone.md) " und " [**SelectionChanged**](shellfolderviewoc-selectionchanged.md)") aus, die in der Regel von Anwendungen verarbeitet werden. Einige Anwendungen müssen jedoch Ereignisse aus einer Reihe von **shellfolderview** -Objekten verarbeiten. Beispielsweise kann eine Anwendung ein Webbrowser-Steuerelement hosten, mit dem Benutzer durch eine Reihe von Ordnern navigieren können. Jeder Ordner verfügt über ein eigenes **shellfolderview** -Objekt mit den zugehörigen Ereignissen. Die Behandlung dieser Ereignisse kann schwierig sein.

Das **shellfolderviewoc** -Objekt vereinfacht die Ereignis Behandlung in solchen Szenarien. Sie ermöglicht Anwendungen das Behandeln von Ereignissen für alle [**shellfolderview**](shellfolderview.md) -Objekte mit einem einzigen Paar von **shellfolderviewoc** -Ereignis Handlern. Jedes Mal, wenn der Benutzer zu einem neuen Ordner navigiert, übergibt die Anwendung das zugehörige **shellfolderview** -Objekt an das **shellfolderviewoc** -Objekt, indem [**setfolderview**](shellfolderviewoc-setfolderview.md)aufgerufen wird. Wenn dann ein [**enumdone**](shellfolderviewoc-enumdone.md) -oder [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) -Ereignis ausgelöst wird, leitet das **shellfolderviewoc** -Objekt das Ereignis zur Verarbeitung an den eigenen Handler weiter.

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

[**Shellfolderview**](shellfolderview.md)
</dt> </dl>

 

 




