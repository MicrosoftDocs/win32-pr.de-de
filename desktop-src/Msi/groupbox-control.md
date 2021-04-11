---
description: Das GroupBox-Steuerelement zeigt ein Rechteck an, ggf. mit Beschriftungs Text, das zum Gruppieren anderer Steuerelemente im Dialogfeld dient.
ms.assetid: e1cdcf71-876f-4115-96a4-95d8a0f61a9b
title: GroupBox-Steuerelement (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5182284055d95719299b1fecb7dc3f7825176c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215120"
---
# <a name="groupbox-control"></a>GroupBox-Steuerelement

Das GroupBox-Steuerelement zeigt ein Rechteck an, ggf. mit Beschriftungs Text, das zum Gruppieren anderer Steuerelemente im Dialogfeld dient.

## <a name="control-attributes"></a>Steuerelement Attribute

Sie können die folgenden Attribute mit dem GroupBox-Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement einem ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md) , und Listen Sie den Bezeichner des Attributs in der Attribut-Spalte auf. Geben Sie den Bezeichner des ControlEvent in der Ereignis Spalte ein.



| Attribut Bezeichner                               | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Position des Steuer Elements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der Steuerelemente der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Steuerelement Tabelle](control-table.md) oder der [Tabelle bbcontrol](bbcontrol-table.md)ein. Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                                                                         |
| [Text](text-control-attribute.md)                 |                                  | Zeigt eine Beschriftung in der linken oberen Ecke des-Steuer Elements an. Um die Schriftart und den Schrift Schnitt einer Text Zeichenfolge festzulegen, stellen Sie die Zeichenfolge der angezeigten Zeichen mit "{ \\ Style}" oder "{&Style}" vor. Dabei ist Style ein Bezeichner, der in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist. Wenn keines dieser beiden vorhanden ist, die [**defaultuifont**](defaultuifont.md) -Eigenschaft jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet.<br/> |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Verborgenes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Spalte Attribute [der Tabelle "Attribute" oder der](control-table.md) Tabelle " [bbcontrol](bbcontrol-table.md) " ein, damit das Steuerelement bei der Erstellung sichtbar oder ausgeblendet wird.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" ausblenden oder anzeigen.<br/>                                                                             |
| [Sunken](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Zeigt den visuellen Standardstil an. Zeigt das Steuerelement mit einem abgesenkten 3D-Bild an.<br/> Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                                                                                                                                                               |
| [Rtlro](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | Der Text im Steuerelement wird in der Lesefolge von links nach rechts angezeigt. Der Text im Steuerelement wird in der Lesefolge von rechts nach links angezeigt.<br/>                                                                                                                                                                                                                                                                                                                |
| [Rechtsbündig](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | Der Text im-Steuerelement wird linksbündig ausgerichtet. Der Text im-Steuerelement wird rechtsbündig ausgerichtet.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Bemerkungen

Dieses Steuerelement kann mithilfe der Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " aus der Schaltflächen Klasse erstellt werden. Es verfügt über die Stile "Name **\_ GroupBox**", " **WS \_ Child**" und " **WS \_ Group** ".

Zwischen dem oberen Rand des Steuer Elements und dem sichtbaren Frame besteht immer eine Lücke, auch wenn keine Beschriftung vorhanden ist.

 

 
