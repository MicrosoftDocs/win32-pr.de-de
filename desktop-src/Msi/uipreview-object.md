---
description: Das UIPreview-Objekt wird verwendet, um Während der Erstellung Benutzeroberflächendialogfelder und -fenster anzuzeigen. Dieses Objekt wird von der EnableUIPreview-Methode des Database-Objekts erstellt.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: UIPreview-Objekt
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
ms.openlocfilehash: 82436f21cc3920c2e1f635f8d1612118831e7d29f3fb1202105511f2e61f7a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623499"
---
# <a name="uipreview-object"></a>UIPreview-Objekt

Das **UIPreview-Objekt** wird verwendet, um Während der Erstellung Benutzeroberflächendialogfelder und -fenster anzuzeigen. Dieses Objekt wird von der [**EnableUIPreview-Methode**](database-enableuipreview.md) des [**Database-Objekts**](database-object.md) erstellt.

## <a name="members"></a>Member

Das **UIPreview-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **UIPreview-Objekt** verfügt über diese Methoden.



| Methode                                           | Beschreibung                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ViewBillboard**](uipreview-viewbillboard.md) | Zeigt mithilfe des Hoststeuerfelds im aktuell angezeigten Dialogfeld ein autoriertes -Steuerelement an.<br/> |
| [**ViewDialog**](uipreview-viewdialog.md)       | Zeigt ein in der aktuellen Datenbank gespeichertes Dialogfeld der erstellten Benutzeroberfläche an.<br/>                           |



 

### <a name="properties"></a>Eigenschaften

Das **UIPreview-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                          | Zugriffstyp           | Beschreibung                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eigenschaft**](uipreview-property.md)<br/> | Lesen/Schreiben<br/> | Stellt den Zeichenfolgenwert einer benannten Installereigenschaft oder, wenn ein Prozentzeichen (%) vorangestellt ist, den Wert einer Systemumgebungsvariablen für den aktuellen Prozess dar.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview ist als 000C109A-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows Skriptbeispiele für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




