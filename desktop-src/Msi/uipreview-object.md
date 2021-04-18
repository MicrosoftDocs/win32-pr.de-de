---
description: Das uipreview-Objekt wird verwendet, um Benutzeroberflächen-Dialogfelder und-Plakate während der Erstellung anzuzeigen. Dieses Objekt wird von der enableuipreview-Methode des Database-Objekts erstellt.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Uipreview-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368421"
---
# <a name="uipreview-object"></a>Uipreview-Objekt

Das **uipreview** -Objekt wird verwendet, um Benutzeroberflächen-Dialogfelder und-Plakate während der Erstellung anzuzeigen. Dieses Objekt wird von der [**enableuipreview**](database-enableuipreview.md) -Methode des [**Database**](database-object.md) -Objekts erstellt.

## <a name="members"></a>Member

Das **uipreview** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **uipreview** -Objekt verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Viewbillboard**](uipreview-viewbillboard.md) | Zeigt ein erstelltes Billboard mithilfe des Host Steuer Elements im momentan angezeigten Dialogfeld an.<br/> |
| [**Viewdialog**](uipreview-viewdialog.md)       | Zeigt das in der aktuellen Datenbank gespeicherte Dialogfeld "erstellte Benutzeroberfläche" an.<br/>                           |



 

### <a name="properties"></a>Eigenschaften

Das **uipreview** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                          | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eigenschaft**](uipreview-property.md)<br/> | Lesen/Schreiben<br/> | Stellt den Zeichen folgen Wert einer benannten installereigenschaft oder, wenn ein Prozentzeichen (%) als Präfix vorangestellt ist, den Wert einer System Umgebungsvariablen für den aktuellen Prozess dar.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iuipreview ist definiert als 000c109a-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




