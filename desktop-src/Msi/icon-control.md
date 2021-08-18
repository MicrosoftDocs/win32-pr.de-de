---
description: Das Symbol-Steuerelement zeigt ein statisches Bild eines Symbols an. Der Hintergrund des Bilds ist transparent.
ms.assetid: a2d19093-73d0-4e1f-bf82-21e7334a3f34
title: Symbolsteuerelement (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce6d1dca9e6664018a0c7a36c9b44f3b5a0b6310bc8c6d18309b73649fa9240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996710"
---
# <a name="icon-control"></a>Symbolsteuerelement

Das Symbol-Steuerelement zeigt ein statisches Bild eines Symbols an. Der Hintergrund des Bilds ist transparent.

## <a name="control-attributes"></a>Steuerelementattribute

Sie können die folgenden Attribute mit diesem Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement für ein ControlEvent in der [EventMapping-Tabelle,](eventmapping-table.md) und listen Sie den Bezeichner des Attributs in der Spalte Attribute auf. Geben Sie den Bezeichner des ControlEvent in der Spalte Ereignis ein.



| Attributbezeichner                         | Hexadezimalbit                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)   |                                                                              | Position des Steuerelements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der linken Ecke des Steuerelements in die Spalten Width, Height, X und Y der [Control-Tabelle](control-table.md)ein. Verwenden Sie [Installationseinheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [Text](text-control-attribute.md)           |                                                                              | Enthält den Namen eines Symbols, das in der Binärtabelle gespeichert [ist.](binary-table.md) Um ein Symbol anzuzeigen, das in der Binärtabelle gespeichert ist, geben Sie den Namen des Bilddatensatzes ein, der in der Binärtabelle in der Text -Spalte des [Steuerelementtabellendatensatzes](control-table.md) für dieses Steuerelement angezeigt wird.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [Visible](visible-control-attribute.md)     | 0x00000000 0x00000001<br/>                                             | Ausgeblendetes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das Bitwort der Attributes -Spalte in die [Control-Tabelle](control-table.md) ein, um das Steuerelement beim Erstellen sichtbar oder ausgeblendet zu machen.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle](controlcondition-table.md)ausblenden oder anzeigen.<br/>                                                                                                                                                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)       | 0x00000000 0x00000004<br/>                                             | Zeigt den standardmäßigen visuellen Stil an. Zeigt das Steuerelement mit einem eingesenkten 3D-Look an.<br/> Schließen Sie diese Bits in das Bitwort in die Attributes -Spalte der [Control-Tabelle](control-table.md)ein.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [Fixedsize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/>                                             | Streckt das Symbolbild an das Steuerelement. Schneidet das Symbolbild im Steuerelement aus oder zentrt es.<br/> Schließen Sie dieses Bit in das Bitwort der Attributes -Spalte der [Control-Tabelle](control-table.md)ein.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [IconSize](iconsize-control-attribute.md)   | 0x00000000 0x00200000<br/> 0x00400000<br/> 0x00600000<br/> | Lädt das erste Bild. Lädt das erste 16x16-Image.<br/> Lädt das erste 32x32-Image.<br/> Lädt das erste 48 x 48-Bild.<br/> Eine Symboldatei kann Bilder unterschiedlicher Größe desselben Symbols enthalten. Einschließen des Werts des entsprechenden Bitworts in die Attributes-Spalte der [Control-Tabelle](control-table.md)<br/> Wenn diese Bits nicht festgelegt sind, ignoriert das Installationsprogramm das FixedSize-Attribut, und das Bild wird gestreckt, um es an das Steuerelementrechteck anzupassen. Wenn sowohl die IconSize-Bits als auch die FixedSize-Bits festgelegt sind, ist ein Bild, das kleiner als das Steuerelement ist, zentriert, und ein Bild ist größer als das Steuerelement, um es anzupassen.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Steuerelement kann mithilfe der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) aus der STATIC-Klasse erstellt werden. Sie verfügt über die **Stile SS \_ ICON,** **SS \_ CENTERIMAGE,** **WS \_ CHILD** und **WS \_ GROUP.**

 

 
