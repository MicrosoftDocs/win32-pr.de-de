---
description: Informationen zu Steuerelementattributen finden Sie unter dem Link zu dem steuerelementspezifischen Steuerelement, das Sie in Steuerelementen erstellen müssen, sowie den Links zu bestimmten Steuerelementattributen in den folgenden Listen.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Steuerelementattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9d7412ce3893b785dccf067287c191f033bdf5a100628577260ff10f74ce1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500720"
---
# <a name="control-attributes"></a>Steuerelementattribute

Informationen zu Steuerelementattributen finden Sie unter dem Link zu dem steuerelementspezifischen Steuerelement, das Sie in [Steuerelementen](controls.md) erstellen müssen, sowie den Links zu bestimmten Steuerelementattributen in den folgenden Listen.

Die folgenden Methoden werden zum Angeben der Attribute eines Steuerelements verwendet:

-   Verwenden Sie die [Tabelle ControlCondition,](controlcondition-table.md) um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder bedingten Anweisung zu deaktivieren, zu aktivieren, auszublenden oder anzuzeigen. Sie können diese Tabelle auch verwenden, um das in der [Dialogtabelle](dialog-table.md)angegebene Standardsteuerelement zu überschreiben.
-   Abonnieren Sie das Steuerelement für ein ControlEvent in der [EventMapping-Tabelle](eventmapping-table.md). Geben Sie den Bezeichner des Attributs in der Spalte Attribute und den Bezeichner von ControlEvent in der Spalte Ereignis dieser Tabelle ein.
-   Legen Sie die Steuerelementattribut-Bitflags für das Steuerelement in der Attributspalte der [Control-Tabelle fest.](control-table.md) Dadurch werden die Attribute bei der Erstellung des Steuerelements festgelegt.

Einige Attribute können nicht für jedes Steuerelement festgelegt oder von allen oben genannten Methoden angegeben werden. Weitere Informationen finden Sie in den Themen zu bestimmten Steuerelementen und Attributen.

Die Anfangswerte einiger Steuerelementattribute können mit Bits in der [Control-Tabelle](control-table.md)festgelegt werden.



| attribute                                          | Decimal | Hexadezimal | Konstante                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [Bidi](bidi-control-attribute.md)                 | 224     | 0x000000E0  | **msidbControlAttributesBiDi**         |
| [Aktiviert](enabled-control-attribute.md)           | 2       | 0x00000002  | **msidbControlAttributesEnabled**      |
| [Indirekt](indirect-control-attribute.md)         | 8       | 0x00000008  | **msidbControlAttributesIndirect**     |
| [Ganzzahliges Steuerelement](integer-control-attribute.md)   | 16      | 0x00000010  | **msidbControlAttributesInteger**      |
| [LeftScroll](leftscroll-control-attribute.md)     | 128     | 0x00000080  | **msidbControlAttributesLeftScroll**   |
| [RightAligned](rightaligned-control-attribute.md) | 64      | 0x00000040  | **msidbControlAttributesRightAligned** |
| [RTLRO](rtlro-control-attribute.md)               | 32      | 0x00000020  | **msidbControlAttributesRTLRO**        |
| [Sunken](sunken-control-attribute.md)             | 4       | 0x00000004  | **msidbControlAttributesSunken**       |
| [Visible](visible-control-attribute.md)           | 1       | 0x00000001  | **msidbControlAttributesVisible**      |



 

Diese Attribute von Textsteuerelementen werden mit Bits festgelegt.



| attribute                                            | Decimal | Hexadezimal | Konstante                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [FormatSize](formatsize-control-attribute.md)       | 524288  | 0x00080000  | **msidbControlAttributesFormatSize**    |
| [NoPrefix](noprefix-control-attribute.md)           | 131072  | 0x00020000  | **msidbControlAttributesNoPrefix**      |
| [Nowrap](nowrap-control-attribute.md)               | 262144  | 0x00040000  | **msidbControlAttributesNoWrap**        |
| [Kennwort](password-control-attribute.md)           | 2097152 | 0x00200000  | **msidbControlAttributesPasswordInput** |
| [Transparent](transparent-control-attribute.md)     | 65536   | 0x00010000  | **msidbControlAttributesTransparent**   |
| [UsersLanguage](userslanguage-control-attribute.md) | 1048576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

Dieses Attribut des ProgressBar-Steuerelements wird mit einem Bit festgelegt.



| attribute                                      | Decimal | Hexadezimal | Konstante                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [Progress95](progress95-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

Diese Attribute von Volume- und Directory SelectCombo-Steuerelementen werden mit Bits festgelegt.



| attribute                                                | Decimal | Hexadezimal | Konstante                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [CORPORAVolume](cdromvolume-control-attribute.md)         | 524288  | 0x00080000  | **msidbControlAttributesCATTRIBUTEVolume**     |
| [FixedVolume](fixedvolume-control-attribute.md)         | 131072  | 0x00020000  | **msidbControlAttributesFixedVolume**     |
| [FloppyVolume](floppyvolume-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesFloppyVolume**    |
| [RAMDiskVolume](ramdiskvolume-control-attribute.md)     | 1048576 | 0x00100000  | **msidbControlAttributesRAMDiskVolume**   |
| [RemoteVolume](remotevolume-control-attribute.md)       | 262144  | 0x00040000  | **msidbControlAttributesRemoteVolume**    |
| [RemovableVolume](removablevolume-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

Diese Attribute von ListBox- und ComboBox-Steuerelementen werden mit Bits festgelegt.



| attribute                                            | Decimal | Hexadezimal | Konstante                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [ComboList-Steuerelement](combolist-control-attribute.md) | 131072  | 0x00020000  | **msidbControlAttributesComboList** |
| [Sortiertes Steuerelement](sorted-control-attribute.md)       | 65536   | 0x00010000  | **msidbControlAttributesSorted**    |



 

Dieses Attribut des Edit-Steuerelements wird mit einem Bit festgelegt.



| attribute                                    | Decimal | Hexadezimal | Konstante                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [Mehrzeiligen](multiline-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

Diese Attribute von PictureButton-Steuerelementen werden mit Bits festgelegt.



| attribute                                          | Decimal | Hexadezimal | Konstante                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [Bitmap](bitmap-control-attribute.md)             | 262144  | 0x00040000  | **msidbControlAttributesBitmap**     |
| [Fixedsize](fixedsize-control-attribute.md)       | 1048576 | 0x00100000  | **msidbControlAttributesFixedSize**  |
| [Symbol:](icon-control-attribute.md)                 | 524288  | 0x00080000  | **msidbControlAttributesIcon**       |
| [IconSize16](iconsize-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| [IconSize32](iconsize-control-attribute.md)       | 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| [IconSize48](iconsize-control-attribute.md)       | 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |
| [PushLike-Steuerelement](pushlike-control-attribute.md) | 131072  | 0x00020000  | **msidbControlAttributesPushLike**   |



 

Dieses Attribut des RadioButton-Steuerelements wird mit einem Bit festgelegt.



| attribute                                    | Decimal  | Hexadezimal | Konstante                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [HasBorder](hasborder-control-attribute.md) | 16777216 | 0x01000000  | **msidbControlAttributesHasBorder** |



 

Dieses Attribut des PushButton-Steuerelements wird mit einem Bit festgelegt.



| attribute                                        | Decimal | Hexadezimal | Konstante                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [ElevationShield](elevationshield-attribute.md) | 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

Dieses Attribut des VolumeCostList-Steuerelements wird mit einem Bit festgelegt.



| attribute                                                                | Decimal | Hexadezimal | Konstante                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [ControlShowRollbackCost](controlshowrollbackcost-control-attribute.md) | 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

Die folgenden Steuerelementattribute werden nicht mit Bits festgelegt. Diese Attribute werden in den Tabellen der Benutzeroberfläche erstellt oder mithilfe von [Steuerungsereignissen](control-events.md)festgelegt.

[Name des Unternamens](billboardname-control-attribute.md)

 

[IndirectPropertyName](indirectpropertyname-control-attribute.md)

 

[Position](position-control-attribute.md)

 

[Statussteuerelement](progress-control-attribute.md)

 

[PropertyName](propertyname-control-attribute.md)

 

[PropertyValue](propertyvalue-control-attribute.md)

 

[Text Control](text-control-attribute.md)

 

[TimeRemaining](timeremaining-control-attribute.md)

Weitere Informationen finden [Sie unter Hinzufügen von Steuerelementen und Text.](adding-controls-and-text.md)

 

 



