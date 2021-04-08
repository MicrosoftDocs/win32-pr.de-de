---
description: Das Hyperlink-Steuerelement zeigt einen HTML-Link zu einer Adresse an, die im Standardbrowser für den Computer geöffnet wird.
ms.assetid: 06678b10-0915-4649-b917-ec90c40d5160
title: Hyperlink-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d074efa00fcf51fec979d9df07f1854631279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866308"
---
# <a name="hyperlink-control"></a>Hyperlink-Steuerelement

Das Hyperlink-Steuerelement zeigt einen HTML-Link zu einer Adresse an, die im Standardbrowser für den Computer geöffnet wird. Links werden für andere Protokolle als HTML nicht unterstützt.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Dieses Steuerelement ist ab Windows Installer 5,0 verfügbar.

Der Textwert des Hyperlink-Steuer Elements verwendet das Anchor- <a> Tag und den href-Attribut Wert, um die URL und den angezeigten Text des Links anzugeben.

``` syntax
[Blue Yonder Airlines](https://www.blueyonderairlines.com)
```

## <a name="control-attributes"></a>Steuerelement Attribute

Sie können die folgenden Attribute mit dem Hyperlink-Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement einem ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md) , und Listen Sie den Bezeichner des Attributs in der Attribut-Spalte auf. Geben Sie den Bezeichner des ControlEvent in der Ereignis Spalte ein.



| Attribut Bezeichner                             | Hexadezimales Bit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)       |                                  | Position des Steuer Elements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der Steuerelemente der linken Ecke des Steuer Elements in die Spalten Width, Height, X und Y der [Steuerelement Tabelle](control-table.md) oder der [Tabelle bbcontrol](bbcontrol-table.md)ein. Verwenden Sie die [Installer-Einheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                                                                                                                       |
| [Text](text-control-attribute.md)               |                                  | Der vom Steuerelement angezeigte Text. Um die Schriftart und den Schrift Schnitt einer Text Zeichenfolge festzulegen, stellen Sie die Zeichenfolge der angezeigten Zeichen mit "{ \\ Style}" oder "{&Style}" vor. Dabei ist Style ein Bezeichner, der in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist. Wenn keines dieser beiden vorhanden ist, die [**defaultuifont**](defaultuifont.md) -Eigenschaft jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet. Der Textwert löst auch \[ die Eigenschaft \] für die Eigenschaft auf, auf die verwiesen wird. <br/> |
| [Visible](visible-control-attribute.md)         | 0x00000000 0x00000001<br/> | Verborgenes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das bitwort der Spalte Attribute in der [Tabelle Tabelle oder der](control-table.md) [Tabelle bbcontrol](bbcontrol-table.md)ein. damit das Steuerelement bei der Erstellung sichtbar oder ausgeblendet wird.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" ausblenden oder anzeigen.<br/>                                                                                                                           |
| [Aktiviert](enabled-control-attribute.md)         | 0x00000000 0x00000002<br/> | Steuerelement in deaktiviertem Zustand. Steuerelement im aktivierten Zustand.<br/> Fügen Sie dieses Bit in das bitwort in die Spalte Attribute der [Steuer](control-table.md) Element-oder [bbcontrol-Tabellen](bbcontrol-table.md) ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [Tabelle "ControlCondition](controlcondition-table.md)" aktivieren oder deaktivieren.<br/>                                                                                                                        |
| [Sunken](sunken-control-attribute.md)           | 0x00000000 0x00000004<br/> | Zeigt den visuellen Standardstil an. Zeigt das Steuerelement mit einem abgesenkten 3D-Bild an.<br/> Fügen Sie diese Bits in das bitwort in die Spalte Attribute der [Steuerelement Tabelle](control-table.md)ein.<br/>                                                                                                                                                                                                                                                                                            |
| [Transparent](transparent-control-attribute.md) | 0x00000000 0x00010000 bis<br/> | Undurchsichtiges Steuerelement. Hintergrund zeigt durch das Steuerelement. Das Steuerelement verfügt über den transparenten WS- \_ Ex- \_ Stil.<br/> Fügen Sie dieses Bit in die Spalte Attribute der [Steuer](control-table.md) Element-oder [bbcontrol-Tabellen](bbcontrol-table.md)ein.<br/>                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Dieses Steuerelement kann \_ mithilfe der Funktion " [**linatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " aus der WC-Link Klasse erstellt werden. Es verfügt über die \_ Stile WS Child, WS \_ Tabstopps und WS \_ Group.

Platzieren Sie keine transparenten [Text Steuerelemente](text-control.md) oberhalb von farbigen Bitmaps. Der Text ist möglicherweise nicht sichtbar, wenn der Benutzer das Anzeige Farbschema ändert. Beispielsweise kann Text unsichtbar werden, wenn der Benutzer den Parameter für hohe Kontraste aus Barrierefreiheits Gründen festlegt.

Wenn der Text im-Steuerelement länger als die Steuerelement Breite ist, wird der Text umschlossen oder abgeschnitten, je nachdem, ob die Höhe für den umschachtelten Text ausreichend ist.

 

 
