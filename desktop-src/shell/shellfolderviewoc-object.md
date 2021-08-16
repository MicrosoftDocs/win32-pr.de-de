---
description: Weitergeleitet die Ereignisse, die von einem angegebenen ShellFolderView-Objekt ausgelöst werden, an die entsprechenden ShellFolderViewOC-Ereignishandler.
title: ShellFolderViewOC-Objekt (Shldisp.h)
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
ms.openlocfilehash: bc00dc285c1bcca72e998ecb22f75af56dd085542d0f191c484c096e5e511cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857672"
---
# <a name="shellfolderviewoc-object"></a>ShellFolderViewOC-Objekt

Weitergeleitet die Ereignisse, die von einem angegebenen [**ShellFolderView-Objekt**](shellfolderview.md) ausgelöst werden, an die entsprechenden **ShellFolderViewOC-Ereignishandler.**

## <a name="members"></a>Member

Das **ShellFolderViewOC-Objekt** verfügt über die folgenden Membertypen:

-   [Ereignisse](#events)
-   [Methoden](#methods)

### <a name="events"></a>Ereignisse

Das **ShellFolderViewOC-Objekt** verfügt über diese Ereignisse.



| Ereignis                                                          | Beschreibung                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDone**](shellfolderviewoc-enumdone.md)                 | Gibt an, [**dass das ShellFolderView-Objekt**](shellfolderview.md) das Aufzählen des Ordnerinhalts abgeschlossen hat.<br/> |
| [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) | Gibt an, dass sich der Auswahlzustand eines oder mehrere Elemente in der Ansicht geändert hat.<br/>                                     |



 

### <a name="methods"></a>Methoden

Das **ShellFolderViewOC-Objekt** verfügt über diese Methoden.



| Methode                                                   | Beschreibung                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetFolderView**](shellfolderviewoc-setfolderview.md) | Gibt die Ereignisse des angegebenen [**ShellFolderView-Objekts**](shellfolderview.md) an den entsprechenden **ShellFolderViewOC-Ereignishandler** weiter.<br/> |



 

## <a name="remarks"></a>Hinweise

Das [**ShellFolderView-Objekt**](shellfolderview.md) gibt zwei Ereignisse aus, [**EnumDone**](shellfolderviewoc-enumdone.md) und [**SelectionChanged,**](shellfolderviewoc-selectionchanged.md)die in der Regel von Anwendungen verarbeitet werden. Einige Anwendungen müssen jedoch Ereignisse aus einer Reihe von **ShellFolderView-Objekten** verarbeiten. Beispielsweise kann eine Anwendung ein WebBrowser-Steuerelement hosten, mit dem Benutzer durch eine Reihe von Ordnern navigieren können. Jeder Ordner verfügt über ein **eigenes ShellFolderView-Objekt** mit den zugehörigen Ereignissen. Die Behandlung dieser Ereignisse kann schwierig sein.

Das **ShellFolderViewOC-Objekt** vereinfacht die Ereignisbehandlung für solche Szenarien. Dadurch können Anwendungen Ereignisse für alle [**ShellFolderView-Objekte**](shellfolderview.md) mit einem einzelnen Paar von **ShellFolderViewOC-Ereignishandlern** behandeln. Jedes Mal, wenn der Benutzer zu einem neuen Ordner navigiert, übergibt die Anwendung das zugeordnete **ShellFolderView-Objekt** durch Aufrufen von [**SetFolderView**](shellfolderviewoc-setfolderview.md)an das **ShellFolderViewOC-Objekt.** Wenn dann ein [**EnumDone-**](shellfolderviewoc-enumdone.md) oder [**SelectionChanged-Ereignis**](shellfolderviewoc-selectionchanged.md) ausgelöst wird, wird das Ereignis vom **ShellFolderViewOC-Objekt** zur Verarbeitung an seinen eigenen Handler weitergeleitet.

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

[**ShellFolderView**](shellfolderview.md)
</dt> </dl>

 

 




