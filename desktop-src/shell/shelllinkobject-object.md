---
description: Verwaltet Shelllinks. Dieses Objekt macht einen Großen Teil der Funktionalität der IShellLink-Schnittstelle für Skriptanwendungen verfügbar.
title: ShellLinkObject-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 9908fa86b79ff230c2c6320685cd605a97c9b0747db31cc395f8f449ae2fbfa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941490"
---
# <a name="shelllinkobject-object"></a>ShellLinkObject-Objekt

Verwaltet Shelllinks. Dieses Objekt macht einen Großen Teil der Funktionalität der [**IShellLink-Schnittstelle**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) für Skriptanwendungen verfügbar.

## <a name="members"></a>Member

Das **ShellLinkObject-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **ShellLinkObject-Objekt** verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetIconLocation**](shelllinkobject-geticonlocation.md) | Ruft die Position des Symbols ab, das dem Link zugewiesen ist.<br/>                                 |
| [**Beheben**](shelllinkobject-resolve.md)                 | Sucht nach dem Ziel eines Shelllinks, auch wenn das Ziel verschoben oder umbenannt wurde.<br/> |
| [**Speichern**](shelllinkobject-save.md)                       | Speichert alle Änderungen am Link.<br/>                                                      |
| [**SetIconLocation**](shelllinkobject-seticonlocation.md) | Legt die Position des Symbols fest, das dem Link zugewiesen ist.<br/>                                 |



 

### <a name="properties"></a>Eigenschaften

Das **ShellLinkObject-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp           | BESCHREIBUNG                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Argumente**](shelllinkobject-arguments.md)<br/>               | Lesen/Schreiben<br/> | Enthält die Argumente eines Links.<br/>                                                                   |
| [**Beschreibung**](shelllinkobject-description.md)<br/>           | Lesen/Schreiben<br/> | Ruft die Beschreibung des Links ab oder legt sie fest.<br/>                                                      |
| [**Hotkey**](shelllinkobject-hotkey.md)<br/>                     | Lesen/Schreiben<br/> | Ruft die Tastenkombination für den Link ab oder legt sie fest.<br/>                                               |
| [**Pfad**](shelllinkobject-path.md)<br/>                         | Lesen/Schreiben<br/> | Ruft den Pfad zum Linkobjekt ab oder legt diesen fest.<br/>                                                      |
| [**ShowCommand**](shelllinkobject-showcommand.md)<br/>           | Lesen/Schreiben<br/> | Ruft den anfänglichen Anzeigezustand (Größe, Minimiert oder Maximierung) des Linkbefehls ab oder legt diesen fest.<br/> |
| [**WorkingDirectory**](shelllinkobject-workingdirectory.md)<br/> | Lesen/Schreiben<br/> | Ruft das im Link angegebene Arbeitsverzeichnis ab oder legt es fest.<br/>                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shelllinks](./links.md)
</dt> </dl>

 

 
