---
description: Das Hyperlink-Steuerelement zeigt einen HTML-Link zu einer Adresse an, der im Standardbrowser für den Computer geöffnet wird.
ms.assetid: 06678b10-0915-4649-b917-ec90c40d5160
title: Hyperlink-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce515b64a518012ea187eb2c3a933e653b1ea5cf99b316028f9cfe3b397c5f96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129460"
---
# <a name="hyperlink-control"></a>Hyperlink-Steuerelement

Das Hyperlink-Steuerelement zeigt einen HTML-Link zu einer Adresse an, der im Standardbrowser für den Computer geöffnet wird. Links werden für andere Protokolle als HTML nicht unterstützt.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt. Dieses Steuerelement ist ab Windows Installer 5.0 verfügbar.

Der Text-Wert des HyperLink-Steuerelements verwendet das Ankertag und den HREF-Attributwert, um die URL und den <a> angezeigten Text des Links anzugeben.

``` syntax
[Blue Yonder Airlines](https://www.blueyonderairlines.com)
```

## <a name="control-attributes"></a>Steuerelementattribute

Sie können die folgenden Attribute mit dem Hyperlink-Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement für ein ControlEvent in der [EventMapping-Tabelle,](eventmapping-table.md) und listen Sie den Bezeichner des Attributs in der Spalte Attribut auf. Geben Sie den Bezeichner des ControlEvents in der Spalte Ereignis ein.



| Attributbezeichner                             | Hexadezimales Bit                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)       |                                  | Position des Steuerelements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der linken Ecke des Steuerelements in die Spalten Width, Height, X und Y der [Tabelle Control](control-table.md) oder [BBControl ein.](bbcontrol-table.md) Verwenden [Sie Installationseinheiten](installer-units.md) für Länge und Entfernung.<br/>                                                                                                                                                                       |
| [Text](text-control-attribute.md)               |                                  | Vom Steuerelement angezeigter Text. Stellen Sie der Zeichenfolge der angezeigten Zeichen { style} oder {&style} voran, um die Schriftart und den \\ Schriftschnitt einer Textzeichenfolge zu setzen. Dabei ist style ein Bezeichner, der in der TextStyle -Spalte der [TextStyle-Tabelle aufgeführt ist.](textstyle-table.md) Wenn keines dieser Eigenschaften vorhanden ist, die [**DefaultUIFont-Eigenschaft**](defaultuifont.md) jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet. Der Textwert löst auch \[ Property in die Eigenschaft \] auf, auf die verwiesen wird. <br/> |
| [Visible](visible-control-attribute.md)         | 0x00000000 0x00000001<br/> | Ausgeblendetes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das Bitwort der Attributes -Spalte in die [Control-Tabelle](control-table.md) oder [BBControl-Tabelle](bbcontrol-table.md)ein, um das Steuerelement bei seiner Erstellung sichtbar oder ausgeblendet zu machen.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle ausblenden oder anzeigen.](controlcondition-table.md)<br/>                                                                                                                           |
| [Aktiviert](enabled-control-attribute.md)         | 0x00000000 0x00000002<br/> | Steuerelement in einem deaktivierten Zustand. Steuerelement in einem aktivierten Zustand.<br/> Fügen Sie dieses Bit in das Bitwort in die Spalte Attribute der [Tabellen Control](control-table.md) oder [BBControl](bbcontrol-table.md) ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle aktivieren oder deaktivieren.](controlcondition-table.md)<br/>                                                                                                                        |
| [Sunken](sunken-control-attribute.md)           | 0x00000000 0x00000004<br/> | Zeigt den standardmäßigen visuellen Stil an. Zeigt das Steuerelement mit einem versenkten 3D-Look an.<br/> Schließen Sie diese Bits in das Bitwort in die Spalte Attribute der [Control-Tabelle ein.](control-table.md)<br/>                                                                                                                                                                                                                                                                                            |
| [Transparent](transparent-control-attribute.md) | 0x00000000 0x00010000<br/> | Nicht transparentes Steuerelement. Hintergrund wird über das -Steuerelement gezeigt. Das -Steuerelement hat den WS \_ EX \_ TRANSPARENT-Stil.<br/> Schließen Sie dieses Bit in die Spalte Attribute der [Control- oder](control-table.md) [BBControl-Tabellen ein.](bbcontrol-table.md)<br/>                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Hinweise

Dieses Steuerelement kann mithilfe der CreateWindowEx-Funktion aus der WC \_ [**LINK-Klasse erstellt**](/windows/win32/api/winuser/nf-winuser-createwindowexa) werden. Sie verfügt über die Formate WS \_ CHILD, WS \_ TABSTOP und WS \_ GROUP.

Platzieren Sie transparente [Textsteuerelemente nicht](text-control.md) über farbigen Bitmaps. Der Text ist möglicherweise nicht sichtbar, wenn der Benutzer das Anzeigefarbschema ändert. Beispielsweise kann Text unsichtbar werden, wenn der Benutzer den Parameter für hohen Kontrast aus Gründen der Barrierefreiheit festgibt.

Wenn der Text im Steuerelement länger als die Breite des Steuerelements ist, wird der Text umbrochen oder abgeschnitten, je nachdem, ob die Höhe für den umschlossenen Text ausreicht.

 

 
