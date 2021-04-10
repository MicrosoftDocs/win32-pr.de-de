---
description: Eine Symbol Datei kann verschiedene Größen desselben Symbol Bilds enthalten.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Ikonsistze-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042145"
---
# <a name="iconsize-control-attribute"></a>Ikonsistze-Steuerelement Attribut

Eine Symbol Datei kann verschiedene Größen desselben Symbol Bilds enthalten. Diese Bits geben an, welche Größe des Symbol Bilds geladen werden soll. Wenn keines der Bits festgelegt ist, wird das erste Bild geladen. Wenn nur **msidbControlAttributesIconSize16** festgelegt ist, wird das erste 16x16-Bild geladen. Wenn nur **msidbControlAttributesIconSize32** festgelegt ist, wird das erste 32x32-Bild geladen. Wenn **msidbControlAttributesIconSize48** festgelegt ist, wird das erste 48-Bild geladen.

## <a name="valid-controls"></a>Gültige Steuerelemente

[CheckBox](checkbox-control.md)

[Symbol:](icon-control.md)

[PUSHBUTTON](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | BESCHREIBUNG                          |
|---------|-------------|--------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie die ikonsistze-Bits in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Wenn das [FixedSize](fixedsize-control-attribute.md) -Bit nicht festgelegt ist, wird das geladene Bild verkleinert oder gestreckt, um es an das Symbol Steuerelement anzupassen. Wenn das [FixedSize](fixedsize-control-attribute.md) -Bit festgelegt ist und das geladene Bild kleiner als das Symbol Steuerelement ist, wird das Bild im-Steuerelement zentriert angezeigt. Wenn das [FixedSize](fixedsize-control-attribute.md) -Bit festgelegt ist und das geladene Bild größer als das Symbol Steuerelement ist, wird das Bild so reduziert, dass es dem Steuerelement entspricht.

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



