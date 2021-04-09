---
description: Dieses Steuerelement zeigt eine lange Text Zeichenfolge an, die nicht vollständig auf die Seite passt. Das Steuerelement wird häufig verwendet, um den Lizenzvertrag anzuzeigen.
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: Scrollabletext-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ff807f2b0175eb411b3c45eb9d1e3b5eeaea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865192"
---
# <a name="scrollabletext-control"></a>Scrollabletext-Steuerelement

Dieses Steuerelement zeigt eine lange Text Zeichenfolge an, die nicht vollständig auf die Seite passt. Das Steuerelement wird häufig verwendet, um den Lizenzvertrag anzuzeigen.

Beachten Sie, dass die Text Zeichenfolge, die mit diesem Steuerelement verwendet wird, keine eingebettete Eigenschaft enthalten Verwenden Sie stattdessen das [Text-Steuer](text-control.md)Element, um Text mit eingebetteten Eigenschaften anzuzeigen.

## <a name="control-attributes"></a>Steuerelement Attribute

Mit diesem Steuerelement können Sie die folgenden Attribute verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement einem ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md) , und Listen Sie den Bezeichner des Attributs in der Attribut-Spalte auf. Geben Sie den Bezeichner des ControlEvent in der Ereignis Spalte ein.



| Attribut Bezeichner                               | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Position des Steuer Elements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der Steuerelemente der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Steuerelement Tabelle](control-table.md) oder der [Tabelle bbcontrol](bbcontrol-table.md)ein. Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.<br/>                                            |
| [Text](text-control-attribute.md)                 |                                  | Der vom Steuerelement angezeigte Text. Geben Sie die RTF-Text Zeichenfolge in die Text-Spalte der [Steuerelement Tabelle](control-table.md)ein.                                                                                                                                                                                                                                                       |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Verborgenes Steuerelement. Sichtbares Steuerelement.<br/> Um das Steuerelement sichtbar zu machen oder bei seiner Erstellung ausgeblendet zu werden, schließen Sie dieses Bit in das bitwort der Spalte Attribute in der Tabelle [Control Table](control-table.md) oder [bbcontrol](bbcontrol-table.md)ein.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" ausblenden oder anzeigen.<br/> |
| [Aktiviert](enabled-control-attribute.md)           | 0x00000000 0x00000002<br/> | Steuerelement in deaktiviertem Zustand. Steuerelement im aktivierten Zustand.<br/> Fügen Sie dieses Bit in die Spalte Attribute der [Steuer](control-table.md) Element-oder [bbcontrol-Tabellen](bbcontrol-table.md) ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" aktivieren oder deaktivieren.<br/>             |
| [Sunken](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Anzeigen des standardmäßigen visuellen Stils. Zeigen Sie das Steuerelement mit einem abgesenkten 3D-Bild an.<br/> Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                                                                                    |
| [Rtlro](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | Der Text im-Steuerelement wird in einer Lesefolge von links nach rechts angezeigt. Der Text im-Steuerelement wird in der Lesefolge von rechts nach links angezeigt.<br/>                                                                                                                                                                                                                               |
| [Rechtsbündig](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | Der Text im-Steuerelement wird linksbündig ausgerichtet. Der Text im Steuerelement wird rechtsbündig ausgerichtet.<br/>                                                                                                                                                                                                                                                                            |
| [Leftscroll](leftscroll-control-attribute.md)     | 0x00000000 0x00000080<br/> | Die Scrollleiste befindet sich auf der rechten Seite des-Steuer Elements. Die Scrollleiste befindet sich auf der linken Seite des-Steuer Elements.<br/>                                                                                                                                                                                                                                              |
| [Bidi](bidi-control-attribute.md)                 | 0x000000e0                       | Legen Sie diesen Wert für eine Kombination der Attribute [rtlro](rtlro-control-attribute.md), [rightausgerichtete](rightaligned-control-attribute.md)und [leftscroll](leftscroll-control-attribute.md) fest.                                                                                                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Steuerelement kann mithilfe der Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " aus der RichEdit-Klasse erstellt werden. Es verfügt über die Stile **\_ MultiLine**, **WS \_ VScroll**, **es read \_ only**, **WS \_ Tabstopps**, **es \_ autovscroll**, **WS \_ Child**, **WS \_ Group** und **es \_ nooledragdrop** .

 

 
