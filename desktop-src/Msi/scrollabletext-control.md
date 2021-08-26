---
description: Dieses Steuerelement zeigt eine lange Textzeichenfolge an, die nicht vollständig auf die Seite passt. Eine häufige Verwendung dieses Steuerelements ist die Anzeige des Lizenzvertrags.
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: ScrollableText-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f4d5ac48f6b89b779960126e62c204d1d09e1f9a7bc832b0e3477635df35ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041300"
---
# <a name="scrollabletext-control"></a>ScrollableText-Steuerelement

Dieses Steuerelement zeigt eine lange Textzeichenfolge an, die nicht vollständig auf die Seite passt. Eine häufige Verwendung dieses Steuerelements ist die Anzeige des Lizenzvertrags.

Beachten Sie, dass die mit diesem Steuerelement verwendete Textzeichenfolge keine eingebettete Eigenschaft enthalten kann. Um Text mit eingebetteten Eigenschaften anzuzeigen, verwenden Sie stattdessen das [Textsteuerelement](text-control.md).

## <a name="control-attributes"></a>Steuerelementattribute

Sie können die folgenden Attribute mit diesem Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement für ein ControlEvent in der [EventMapping-Tabelle,](eventmapping-table.md) und listen Sie den Bezeichner des Attributs in der Spalte Attribute auf. Geben Sie den Bezeichner des ControlEvent in der Spalte Ereignis ein.



| Attributbezeichner                               | Hexadezimalbit                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Position des Steuerelements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der linken Ecke des Steuerelements in die Spalten Width, Height, X und Y der [Control-Tabelle](control-table.md) oder der [BBControl-Tabelle](bbcontrol-table.md)ein. Verwenden Sie [Installationseinheiten](installer-units.md) für Länge und Entfernung.<br/>                                            |
| [Text](text-control-attribute.md)                 |                                  | Vom Steuerelement angezeigter Text. Geben Sie die RTF-Textzeichenfolge in die Text -Spalte der [Control-Tabelle](control-table.md)ein.                                                                                                                                                                                                                                                       |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Ausgeblendetes Steuerelement. Sichtbares Steuerelement.<br/> Um das Steuerelement bei seiner Erstellung sichtbar oder ausgeblendet zu machen, fügen Sie dieses Bit in das Bitwort der Attributes -Spalte in die [Control-Tabelle](control-table.md) oder [die BBControl-Tabelle](bbcontrol-table.md)ein.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle](controlcondition-table.md)ausblenden oder anzeigen.<br/> |
| [Aktiviert](enabled-control-attribute.md)           | 0x00000000 0x00000002<br/> | Steuerelement in einem deaktivierten Zustand. Steuerelement im aktivierten Zustand.<br/> Schließen Sie dieses Bit in die Spalte Attribute der [Control-](control-table.md) oder [BBControl-Tabellen](bbcontrol-table.md) ein, um das Steuerelement bei der Erstellung zu aktivieren.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle](controlcondition-table.md)aktivieren oder deaktivieren.<br/>             |
| [Sunken](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Zeigt den standardmäßigen visuellen Stil an. Zeigen Sie das Steuerelement mit einem eingesenkten 3D-Look an.<br/> Schließen Sie diese Bits in das Bitwort in die Attributes -Spalte der [Control-Tabelle](control-table.md)ein.<br/>                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | Text im Steuerelement wird in einer Lesereihenfolge von links nach rechts angezeigt. Text im -Steuerelement wird in einer Lesereihenfolge von rechts nach links angezeigt.<br/>                                                                                                                                                                                                                               |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | Der Text im -Steuerelement wird links ausgerichtet. Der Text im Steuerelement wird auf der rechten Seite ausgerichtet.<br/>                                                                                                                                                                                                                                                                            |
| [LeftScroll](leftscroll-control-attribute.md)     | 0x00000000 0x00000080<br/> | Die Bildlaufleiste befindet sich auf der rechten Seite des Steuerelements. Die Bildlaufleiste befindet sich auf der linken Seite des Steuerelements.<br/>                                                                                                                                                                                                                                              |
| [Bidi](bidi-control-attribute.md)                 | 0x000000E0                       | Legen Sie diesen Wert für eine Kombination der Attribute [RTLRO,](rtlro-control-attribute.md) [RightAligned](rightaligned-control-attribute.md)und [LeftScroll](leftscroll-control-attribute.md) fest.                                                                                                                                                                               |



 

## <a name="remarks"></a>Hinweise

Dieses Steuerelement kann mithilfe der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) aus der RICHEDIT-Klasse erstellt werden. Sie verfügt über die Stile **ES \_ MULTILINE,** **WS \_ VSCROLL,** **ES \_ READONLY,** **\_ WS TABSTOP,** **ES \_ AUTOVSCROLL,** **WS \_ CHILD,** **WS \_ GROUP** und **ES \_ NOOLEDRAGDROP.**

 

 
