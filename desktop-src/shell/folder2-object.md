---
description: Erweitert das Ordner Objekt, um Offline Ordner zu unterstützen.
title: Folder2-Objekt (Shldisp. h)
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
ms.openlocfilehash: 8db899fc52cc3511d1af82013fc6c4c87544f1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979673"
---
# <a name="folder2-object"></a>Folder2-Objekt

Erweitert das [**Ordner**](folder.md) Objekt, um Offline Ordner zu unterstützen.

## <a name="members"></a>Member

Das **Folder2** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Folder2** -Objekt verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Dismissedwebviewbarricade**](folder2-dismissedwebviewbarricade.md) | Wird als Antwort auf die webansichtenbarricade aufgerufen, die vom Benutzer verworfen wird.<br/> |
| [**Synchronisieren**](folder2-synchronize.md)                             | Synchronisiert alle Offline Dateien im Ordner.<br/>                             |



 

### <a name="properties"></a>Eigenschaften

Das **Folder2** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                            | Zugriffstyp          | BESCHREIBUNG                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [**Haveum showwebviewbarricade**](folder2-havetoshowwebviewbarricade.md)<br/> | Schreibgeschützt<br/> | Wird derzeit nicht unterstützt.<br/>                                       |
| [**Offlinestatus**](folder2-offlinestatus.md)<br/>                           | Schreibgeschützt<br/> | Enthält den Offline Status des Ordners.<br/>                     |
| [**Selbstbedienungs**](folder2-self.md)<br/>                                             | Schreibgeschützt<br/> | Enthält das [**folderItem**](folderitem.md) -Objekt des Ordners.<br/> |



 

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

[**Ordner**](folder.md)
</dt> </dl>

 

 




