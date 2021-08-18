---
description: Das Bitmap-Steuerelement zeigt eine bitmap- oder JPEG-statische Bilddatei an. Der Windows Installer bestimmt automatisch das Format der Binärdaten und zeigt das Bild an. Das -Steuerelement unterstützt keine Animation.
ms.assetid: 4b511d8a-1819-4a9b-a942-dc32fade75c6
title: Bitmap-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677a7745d3920d5fee44cd64489f9f2c69f8cdb1fb697a0020046a92583e569
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045230"
---
# <a name="bitmap-control"></a>Bitmap-Steuerelement

Das Bitmap-Steuerelement zeigt eine bitmap- oder JPEG-statische Bilddatei an. Der Windows Installer bestimmt automatisch das Format der Binärdaten und zeigt das Bild an. Das -Steuerelement unterstützt keine Animation.

**Windows 8 und Windows Server 2012:** Die Bilddatei kann in einem beliebigen Standardformat vorliegen, das von der Windows Imaging Component (WIC) unterstützt wird, einschließlich TIFF, JPEG, PNG, GIF, BMP und HDPhoto. Das -Steuerelement unterstützt keine Animation.

## <a name="control-attributes"></a>Steuerelementattribute

Sie können die folgenden Attribute mit diesem Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement für ein ControlEvent in der [EventMapping-Tabelle,](eventmapping-table.md) und listen Sie den Bezeichner des Attributs in der Spalte Attribut auf. Geben Sie den Bezeichner des ControlEvents in der Spalte Ereignis ein.



| Attributbezeichner                                 | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)           |                                  | Position des Steuerelements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der linken Ecke des Steuerelements in die Spalten Width, Height, X und Y der [Tabelle Control](control-table.md) oder [BBControl ein.](bbcontrol-table.md) Verwenden [Sie Installationseinheiten](installer-units.md) für Länge und Entfernung.<br/>                                         |
| [Text](text-control-attribute.md)                   |                                  | Enthält den Namen einer Bitmap, die in der [Binärtabelle gespeichert ist.](binary-table.md) Gehen Sie wie folgt vor, um eine in der Binärtabelle gespeicherte Bitmap anzuzeigen. Geben Sie den Namen des Bitmapbilds, das in der Spalte Name der Binärtabelle angezeigt wird, in die Spalte Text des Datensatzes Control [table](control-table.md) für dieses Steuerelement ein. <br/>                                         |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Ausgeblendetes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das Bitwort der Attributes -Spalte in die [Control-Tabelle](control-table.md) oder [BBControl-Tabelle](bbcontrol-table.md)ein, um das Steuerelement bei seiner Erstellung sichtbar oder ausgeblendet zu machen.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle ausblenden oder anzeigen.](controlcondition-table.md)<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Zeigt den standardmäßigen visuellen Stil an. Zeigt das Steuerelement mit einem versenkten 3D-Look an.<br/> Schließen Sie diese Bits in das Bitwort in die Spalte Attribute der [Control-Tabelle ein.](control-table.md)<br/>                                                                                                                                                                   |
| [FixedSize-Steuerelement](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/> | Streckt das Bitmapbild so, dass es an das Steuerelement passt. Das Bitmapbild im Steuerelement wird bzw. centert es.<br/> Schließen Sie dieses Bit in das Bitwort der Attributes -Spalte der [BBControl-Tabelle](bbcontrol-table.md) oder der [Control-Tabelle ein.](control-table.md)<br/>                                                                                                       |



 

## <a name="remarks"></a>Hinweise

Dieses Steuerelement kann mithilfe der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) aus der STATIC-Klasse erstellt werden. Sie verfügt über **die Stile SS \_ BITMAP,** **SS \_ CENTERIMAGE,** **WS \_ CHILD** und **WS \_ GROUP.**

 

