---
description: Das Steuerelement "Billboard" zeigt häufig verwendete Steuerelemente an, die von ControlEvents hinzugefügt und aus dem Dialogfeld entfernt werden.
ms.assetid: c4c0ed5a-2518-499f-805f-dcbe0b0f9393
title: Billboard-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e056a764ec4a71c3ce6785acf331b4bc1ff95ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864448"
---
# <a name="billboard-control"></a>Billboard-Steuerelement

Das Steuerelement "Billboard" zeigt häufig verwendete Steuerelemente an, die von ControlEvents hinzugefügt und aus dem Dialogfeld entfernt werden. Nur Steuerelemente, die keiner Eigenschaft zugeordnet sind, z. b. [Text](text-control.md), [Bitmap](bitmap-control.md)oder [Symbol](icon-control.md), oder benutzerdefinierte Steuerelemente können in einem Billboard abgelegt werden. In den Steuerelement-Steuerelementen werden normalerweise Statusmeldungen

## <a name="control-attributes"></a>Steuerelement Attribute

Sie können die folgenden Attribute mit dem Billboard-Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement einem ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md) , und Listen Sie den Bezeichner des Attributs in der Attribut-Spalte auf. Geben Sie den Bezeichner des ControlEvent in der Ereignis Spalte ein.



| Attribut Bezeichner                                 | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Billboardname](billboardname-control-attribute.md) |                                  | Der Name des aktuellen Billboard. Geben Sie den Bezeichner für den Billboard in der Spalte Billboard der [Tabelle bbcontrol](bbcontrol-table.md)ein.<br/>                                                                                                                                                                            |
| [Position](position-control-attribute.md)           |                                  | Position des Steuer Elements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten des Steuer Elements der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Tabelle bbcontrol](bbcontrol-table.md)ein. Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.<br/>                                |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Verborgenes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Spalte Attribute in der [Tabelle bbcontrol](bbcontrol-table.md) ein, damit das Steuerelement bei der Erstellung sichtbar oder ausgeblendet wird.<br/> Blenden Sie ein Steuerelement mithilfe der [Tabelle ControlCondition](controlcondition-table.md)aus, oder zeigen Sie es an.<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Zeigt den visuellen Standardstil an. Zeigt das Steuerelement mit einem abgesenkten 3D-Bild an.<br/> Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Steuerelement verfügt über kein eigenes Fenster.

Auf der vollständigen Benutzeroberfläche angezeigte Billboard-Steuerelemente werden in der [Tabelle "Billboard](billboard-table.md)" aufgeführt.

Steuerelemente, die sich auf einem Billboard befinden, müssen in der [Tabelle bbcontrol](bbcontrol-table.md) und nicht in der [Steuerelement Tabelle](control-table.md)aufgeführt werden.

 

 




