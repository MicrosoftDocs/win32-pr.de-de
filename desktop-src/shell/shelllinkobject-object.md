---
description: Verwaltet shelllinks. Dieses Objekt stellt einen Großteil der Funktionen der IShellLink-Schnittstelle für Skript Anwendungen zur Verfügung.
title: Shelllinkobject-Objekt (Shldisp. h)
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
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980729"
---
# <a name="shelllinkobject-object"></a>Shelllinkobject-Objekt

Verwaltet shelllinks. Dieses Objekt stellt einen Großteil der Funktionen der [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) -Schnittstelle für Skript Anwendungen zur Verfügung.

## <a name="members"></a>Member

Das **shelllinkobject** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **shelllinkobject** -Objekt verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Getitirelocation**](shelllinkobject-geticonlocation.md) | Ruft den Speicherort des Symbols ab, das dem Link zugewiesen ist.<br/>                                 |
| [**Beheben**](shelllinkobject-resolve.md)                 | Sucht das Ziel eines shelllinks, auch wenn das Ziel verschoben oder umbenannt wurde.<br/> |
| [**Sicher**](shelllinkobject-save.md)                       | Speichert alle Änderungen am Link.<br/>                                                      |
| [**Standort Standort**](shelllinkobject-seticonlocation.md) | Legt den Speicherort des Symbols fest, das dem Link zugewiesen ist.<br/>                                 |



 

### <a name="properties"></a>Eigenschaften

Das **shelllinkobject** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp           | BESCHREIBUNG                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Argumente**](shelllinkobject-arguments.md)<br/>               | Lesen/Schreiben<br/> | Enthält die Argumente eines Links.<br/>                                                                   |
| [**Beschreibung**](shelllinkobject-description.md)<br/>           | Lesen/Schreiben<br/> | Ruft die Beschreibung des links ab oder legt Sie fest.<br/>                                                      |
| [**Hotkey**](shelllinkobject-hotkey.md)<br/>                     | Lesen/Schreiben<br/> | Ruft die Tastenkombination für den Link ab oder legt Sie fest.<br/>                                               |
| [**`Path`**](shelllinkobject-path.md)<br/>                         | Lesen/Schreiben<br/> | Ruft den Pfad zum Link Objekt ab oder legt diesen fest.<br/>                                                      |
| [**ShowCommand**](shelllinkobject-showcommand.md)<br/>           | Lesen/Schreiben<br/> | Ruft den anfänglichen Anzeige Zustand (Größen, minimiert oder maximiert) des Befehls des links ab oder legt ihn fest.<br/> |
| [**WorkingDirectory**](shelllinkobject-workingdirectory.md)<br/> | Lesen/Schreiben<br/> | Ruft das im Link angegebene Arbeitsverzeichnis ab oder legt es fest.<br/>                                      |



 

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

[Shelllinks](./links.md)
</dt> </dl>

 

 
