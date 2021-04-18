---
description: Das Bitmap-Steuerelement zeigt eine statische Bitmap-oder JPEG-Bilddatei an. Der Windows Installer bestimmt automatisch das Format der Binärdaten und zeigt das Bild an. Das-Steuerelement unterstützt keine Animation.
ms.assetid: 4b511d8a-1819-4a9b-a942-dc32fade75c6
title: Bitmap-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058b67d52266906735719976bf7311b4f562b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351637"
---
# <a name="bitmap-control"></a>Bitmap-Steuerelement

Das Bitmap-Steuerelement zeigt eine statische Bitmap-oder JPEG-Bilddatei an. Der Windows Installer bestimmt automatisch das Format der Binärdaten und zeigt das Bild an. Das-Steuerelement unterstützt keine Animation.

**Windows 8 und Windows Server 2012:** Die Bilddatei kann ein beliebiges Standardformat aufweisen, das von der Windows Imaging Component (WIC) unterstützt wird, einschließlich TIFF, JPEG, PNG, GIF, BMP und HDPhoto. Das-Steuerelement unterstützt keine Animation.

## <a name="control-attributes"></a>Steuerelement Attribute

Mit diesem Steuerelement können Sie die folgenden Attribute verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement einem ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md) , und Listen Sie den Bezeichner des Attributs in der Attribut-Spalte auf. Geben Sie den Bezeichner des ControlEvent in der Ereignis Spalte ein.



| Attribut Bezeichner                                 | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)           |                                  | Position des-Steuer Elements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der Steuerelemente der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Steuerelement Tabelle](control-table.md) oder der [Tabelle bbcontrol](bbcontrol-table.md)ein. Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.<br/>                                         |
| [Text](text-control-attribute.md)                   |                                  | Enthält den Namen einer in der [binären Tabelle](binary-table.md)gespeicherten Bitmap. Gehen Sie folgendermaßen vor, um eine in der binären Tabelle gespeicherte Bitmap anzuzeigen. Geben Sie den Namen des Bitmapbilds, das in der Spalte Name der binären Tabelle angezeigt wird, in die Text-Spalte des [Steuerelement Tabellen](control-table.md) Datensatzes für dieses Steuerelement ein. <br/>                                         |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Verborgenes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Spalte Attribute in der [Tabelle Tabelle oder der](control-table.md) [Tabelle bbcontrol](bbcontrol-table.md)ein. damit das Steuerelement bei der Erstellung sichtbar oder ausgeblendet wird.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" ausblenden oder anzeigen.<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Zeigt den visuellen Standardstil an. Zeigt das Steuerelement mit einem abgesenkten 3D-Bild an.<br/> Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                                                                                   |
| [FixedSize-Steuerelement](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/> | Streckt das Bitmap-Bild so, dass es dem Steuerelement entspricht. Zentriert das Bitmap-Bild im-Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Spalte Attribute der [Tabelle bbcontrol](bbcontrol-table.md) oder der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Dieses Steuerelement kann mithilfe der Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " aus der statischen Klasse erstellt werden. Es verfügt über die Stile **SS \_ Bitmap**, **SS \_ CenterImage**, **WS \_ Child** und **WS \_ Group** .

 

