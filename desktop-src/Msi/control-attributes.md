---
description: Informationen zu Steuerelement Attributen finden Sie unter dem Link zu einem bestimmten Steuerelement, das Sie in-Steuerelementen erstellen müssen, sowie Links zu bestimmten Steuerelement Attributen in den folgenden Listen.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Steuerelement Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d026e84dadefa67ce9d6e00146c6e1c2017cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347789"
---
# <a name="control-attributes"></a>Steuerelement Attribute

Informationen zu Steuerelement Attributen finden Sie unter dem Link zu einem bestimmten Steuerelement, das Sie in-Steuer [Elementen](controls.md) erstellen müssen, sowie Links zu bestimmten Steuerelement Attributen in den folgenden Listen.

Die folgenden Methoden werden zum Angeben der Attribute eines-Steuer Elements verwendet:

-   Verwenden Sie die [Tabelle "ControlCondition](controlcondition-table.md) ", um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder Bedingungs Anweisung zu deaktivieren, zu aktivieren, auszublenden oder anzuzeigen. Sie können diese Tabelle auch verwenden, um das in der [Dialog Feld Tabelle](dialog-table.md)angegebene Standard Steuerelement zu überschreiben.
-   Abonnieren Sie das Steuerelement für ein ControlEvent in der [Tabelle EventMapping](eventmapping-table.md). Geben Sie den Bezeichner des Attributs in der Spalte Attribut und den Bezeichner ControlEvent in der Spalte Ereignis dieser Tabelle ein.
-   Legen Sie die Steuerelement-Attributflags für das-Steuerelement in der Attribut-Spalte der [Steuerelement Tabelle](control-table.md)fest. Dadurch werden die Attribute bei der Erstellung des Steuer Elements festgelegt.

Einige Attribute können nicht für jedes Steuerelement festgelegt werden oder von allen oben genannten Methoden angegeben werden. Weitere Informationen finden Sie in den jeweiligen Themen zu Steuerelementen und Attributen.

Die Anfangswerte einiger Steuerelement Attribute können mit Bits in der Steuerelement [Tabelle](control-table.md)festgelegt werden.



| Attribut                                          | Decimal | Hexadezimal | Konstante                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [Bidi](bidi-control-attribute.md)                 | 224     | 0x000000e0  | **msidbcontrolattributesbidi**         |
| [Aktiviert](enabled-control-attribute.md)           | 2       | 0x00000002  | **msidbcontrolattributesaktivierte**      |
| [Indirekt](indirect-control-attribute.md)         | 8       | 0x00000008  | **msidbcontrolattributesindirekte**     |
| [Integer-Steuerelement](integer-control-attribute.md)   | 16      | 0x00000010  | **msidbcontrolattributesinteger**      |
| [Leftscroll](leftscroll-control-attribute.md)     | 128     | 0x00000080  | **msidbcontrolattributesleftscroll**   |
| [Rechtsbündig](rightaligned-control-attribute.md) | 64      | 0x00000040  | **msidbcontrolattributesrightausgerichteten** |
| [Rtlro](rtlro-control-attribute.md)               | 32      | 0x00000020  | **msidbcontrolattributesrtlro**        |
| [Sunken](sunken-control-attribute.md)             | 4       | 0x00000004  | **msidbcontrolattributess Unken**       |
| [Visible](visible-control-attribute.md)           | 1       | 0x00000001  | **msidbcontrolattributesvisible**      |



 

Diese Attribute von Text Steuerelementen werden mit Bits festgelegt.



| Attribut                                            | Decimal | Hexadezimal | Konstante                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [Formatsize](formatsize-control-attribute.md)       | 524288  | 0x00080000  | **msidbcontrolattributesformatsize**    |
| [NoPrefix](noprefix-control-attribute.md)           | 131072  | 0x00020000  | **msidbcontrolattributesnoprefix**      |
| [NoWrap](nowrap-control-attribute.md)               | 262144  | 0x00040000  | **msidbcontrolattributesnowrap**        |
| [Kennwort](password-control-attribute.md)           | 2097152 | 0x00200000  | **msidbcontrolattributespasswordinput** |
| [Transparent](transparent-control-attribute.md)     | 65536   | 0x00010000  | **msidbcontrolattributestransparent**   |
| [Userslanguage](userslanguage-control-attribute.md) | 1048576 | 0x00100000  | **msidbcontrolattributesuserslanguage** |



 

Dieses Attribut des ProgressBar-Steuer Elements wird mit einem Bit festgelegt.



| Attribut                                      | Decimal | Hexadezimal | Konstante                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [Progress95](progress95-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

Diese Attribute der Steuerelemente Volume und Verzeichnis selectcombo werden mit Bits festgelegt.



| Attribut                                                | Decimal | Hexadezimal | Konstante                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [Cdromvolume](cdromvolume-control-attribute.md)         | 524288  | 0x00080000  | **msidbcontrolattributescdromvolume**     |
| [Fixedvolume](fixedvolume-control-attribute.md)         | 131072  | 0x00020000  | **msidbcontrolattributesfixedvolume**     |
| [Floppyvolume](floppyvolume-control-attribute.md)       | 2097152 | 0x00200000  | **msidbcontrolattributesfloppyvolume**    |
| [Ramdiskvolume](ramdiskvolume-control-attribute.md)     | 1048576 | 0x00100000  | **msidbcontrolattributesramdiskvolume**   |
| [Remotevolume](remotevolume-control-attribute.md)       | 262144  | 0x00040000  | **msidbcontrolattributesremotevolume**    |
| [Removablevolume](removablevolume-control-attribute.md) | 65536   | 0x00010000  | **msidbcontrolattributesremovablevolume** |



 

Diese Attribute von ListBox-und ComboBox-Steuerelementen werden mit Bits festgelegt.



| Attribut                                            | Decimal | Hexadezimal | Konstante                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [Combolist-Steuerelement](combolist-control-attribute.md) | 131072  | 0x00020000  | **msidbcontrolattributescombolist** |
| [Sortiertes Steuerelement](sorted-control-attribute.md)       | 65536   | 0x00010000  | **msidbcontrolattributess orted**    |



 

Dieses Attribut des Bearbeitungs Steuer Elements wird mit einem Bit festgelegt.



| Attribut                                    | Decimal | Hexadezimal | Konstante                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [Mehrzeiligen](multiline-control-attribute.md) | 65536   | 0x00010000  | **msidbcontrolattributesmultiline** |



 

Diese Attribute der PictureButton-Steuerelemente werden mit Bits festgelegt.



| Attribut                                          | Decimal | Hexadezimal | Konstante                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [Bitmap](bitmap-control-attribute.md)             | 262144  | 0x00040000  | **msidbcontrolattributesbitmap**     |
| [FixedSize](fixedsize-control-attribute.md)       | 1048576 | 0x00100000  | **msidbcontrolattributesfixedsize**  |
| [Symbol:](icon-control-attribute.md)                 | 524288  | 0x00080000  | **msidbcontrolattributesicon**       |
| [IconSize16](iconsize-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| [IconSize32](iconsize-control-attribute.md)       | 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| [IconSize48](iconsize-control-attribute.md)       | 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |
| [Pushlike-Steuerelement](pushlike-control-attribute.md) | 131072  | 0x00020000  | **msidbcontrolattributespushlike**   |



 

Dieses Attribut des RadioButton-Steuer Elements wird mit einem Bit festgelegt.



| Attribut                                    | Decimal  | Hexadezimal | Konstante                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [HasBorder](hasborder-control-attribute.md) | 16777216 | 0x01000000  | **msidbcontrolattributeshasborder** |



 

Dieses Attribut des PUSHBUTTON-Steuer Elements wird mit einem Bit festgelegt.



| Attribut                                        | Decimal | Hexadezimal | Konstante                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [Elevationshield](elevationshield-attribute.md) | 8388608 | 0x00800000  | **msidbcontrolattributeselevationshield** |



 

Dieses Attribut des volumecostlist-Steuer Elements wird mit einem Bit festgelegt.



| Attribut                                                                | Decimal | Hexadezimal | Konstante                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [Controlshowrollbackcost](controlshowrollbackcost-control-attribute.md) | 4194304 | 0x00400000  | **msidbcontrolshowrollbackcost** |



 

Die folgenden Steuerelement Attribute sind nicht mit Bits festgelegt. Diese Attribute werden in den Benutzeroberflächen Tabellen erstellt oder mithilfe von [Steuerelement Ereignissen](control-events.md)festgelegt.

[Billboardname](billboardname-control-attribute.md)

 

[Derekpropertyname](indirectpropertyname-control-attribute.md)

 

[Position](position-control-attribute.md)

 

[Fortschrittskontrolle](progress-control-attribute.md)

 

[PropertyName](propertyname-control-attribute.md)

 

[PropertyValue](propertyvalue-control-attribute.md)

 

[Text Control](text-control-attribute.md)

 

[TimeRemaining](timeremaining-control-attribute.md)

Siehe [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md).

 

 



