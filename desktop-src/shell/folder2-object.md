---
description: Erweitert das Folder-Objekt zur Unterstützung von Offlineordnern.
title: Folder2-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: c2c630ef36f6e4b2b58f3902c3d5728a31ad1f0d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842061"
---
# <a name="folder2-object"></a>Folder2-Objekt

Erweitert das [**Folder-Objekt**](folder.md) zur Unterstützung von Offlineordnern.

## <a name="members"></a>Member

Das **Folder2-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Folder2-Objekt** verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**DismissedWebViewBar llcde**](folder2-dismissedwebviewbarricade.md) | Wird als Reaktion darauf aufgerufen, dass die Webansichtsleiste vom Benutzer verworfen wird.<br/> |
| [**Synchronisieren**](folder2-synchronize.md)                             | Synchronisiert alle Offlinedateien im Ordner.<br/>                             |



 

### <a name="properties"></a>Eigenschaften

Das **Folder2-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                            | Zugriffstyp          | BESCHREIBUNG                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [**HaveToShowWebViewBar llcde**](folder2-havetoshowwebviewbarricade.md)<br/> | Schreibgeschützt<br/> | Wird derzeit nicht unterstützt.<br/>                                       |
| [**OfflineStatus**](folder2-offlinestatus.md)<br/>                           | Schreibgeschützt<br/> | Enthält den Offlinestatus des Ordners.<br/>                     |
| [**Selbst**](folder2-self.md)<br/>                                             | Schreibgeschützt<br/> | Enthält das [**FolderItem-Objekt**](folderitem.md) des Ordners.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ordner**](folder.md)
</dt> </dl>

 

 




