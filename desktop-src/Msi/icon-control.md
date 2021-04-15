---
description: Das Symbol Steuerelement zeigt ein statisches Bild eines Symbols an. Der Hintergrund des Bilds ist transparent.
ms.assetid: a2d19093-73d0-4e1f-bf82-21e7334a3f34
title: Symbol Steuerelement (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a9bf90697ff3a839c1953918179fb8cf41f2809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525169"
---
# <a name="icon-control"></a>Symbol Steuerelement

Das Symbol Steuerelement zeigt ein statisches Bild eines Symbols an. Der Hintergrund des Bilds ist transparent.

## <a name="control-attributes"></a>Steuerelement Attribute

Mit diesem Steuerelement können Sie die folgenden Attribute verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement einem ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md) , und Listen Sie den Bezeichner des Attributs in der Attribut-Spalte auf. Geben Sie den Bezeichner des ControlEvent in der Ereignis Spalte ein.



| Attribut Bezeichner                         | Hexadezimales Bit                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)   |                                                                              | Position des Steuer Elements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der Steuerelemente der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Steuerelement Tabelle](control-table.md)ein. Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [Text](text-control-attribute.md)           |                                                                              | Enthält den Namen eines Symbols, das in der [binären Tabelle](binary-table.md)gespeichert ist. Um ein Symbol anzuzeigen, das in der binären Tabelle gespeichert ist, geben Sie den Namen des Abbilds in der Binär Tabelle in die Text-Spalte des [Steuerelement Tabellen](control-table.md) Datensatzes für dieses Steuerelement ein.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [Visible](visible-control-attribute.md)     | 0x00000000 0x00000001<br/>                                             | Verborgenes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Attributspalte in der [Steuerelement Tabelle](control-table.md) ein, damit das Steuerelement bei der Erstellung sichtbar oder ausgeblendet wird.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" ausblenden oder anzeigen.<br/>                                                                                                                                                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)       | 0x00000000 0x00000004<br/>                                             | Zeigt den visuellen Standardstil an. Zeigt das Steuerelement mit einem abgesenkten 3D-Bild an.<br/> Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [FixedSize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/>                                             | Streckt das Symbolbild so, dass es dem Steuerelement entspricht. Zentriert oder zentriert das Symbolbild im-Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Attribut-Spalte der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [Ikonsistenz](iconsize-control-attribute.md)   | 0x00000000 0x00200000<br/> 0x00400000<br/> 0x00600000<br/> | Lädt das erste Bild. Lädt das erste 16x16-Bild.<br/> Lädt das erste 32x32-Bild.<br/> Lädt das erste 48-Bild.<br/> Eine Symbol Datei kann unterschiedliche Größen Bilder desselben Symbols enthalten. Fügen Sie den Wert des entsprechenden bitworts in die Spalte Attribute der [Steuerelement Tabelle](control-table.md) ein.<br/> Wenn diese Bits nicht festgelegt sind, ignoriert das Installationsprogramm das FixedSize-Attribut, und das Bild wird gestreckt, damit es an das Steuerelement Rechteck passt. Wenn sowohl die ikonsistze-Bits als auch die FixedSize-Bits festgelegt sind, wird ein Bild, das kleiner als das-Steuerelement ist, zentriert und ein Bild größer als das Steuerelement, an das es angepasst wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieses Steuerelement kann mithilfe der Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " aus der statischen Klasse erstellt werden. Es verfügt über die Stile **SS- \_ Symbol**, **SS \_ CenterImage**, **WS \_ Child** und **WS \_ Group** .

 

 
