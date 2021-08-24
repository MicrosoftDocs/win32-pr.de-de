---
description: Eine Symboldatei kann mehrere verschiedene Größen desselben Symbolbilds enthalten.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: IconSize-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7323d9c3d8dc9bef1bfd4cd275a20dfcadaa3be946bc78fd358a2d6484db53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894200"
---
# <a name="iconsize-control-attribute"></a>IconSize-Steuerelementattribut

Eine Symboldatei kann mehrere verschiedene Größen desselben Symbolbilds enthalten. Diese Bits geben an, welche Größe des Symbolbilds geladen werden soll. Wenn keines der Bits festgelegt ist, wird das erste Bild geladen. Wenn nur **msidbControlAttributesIconSize16** festgelegt ist, wird das erste 16x16-Image geladen. Wenn nur **msidbControlAttributesIconSize32** festgelegt ist, wird das erste 32x32-Image geladen. Wenn **msidbControlAttributesIconSize48** festgelegt ist, wird das erste 48x48-Image geladen.

## <a name="valid-controls"></a>Gültige Steuerelemente

[CheckBox](checkbox-control.md)

[Symbol:](icon-control.md)

[Pushbutton](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | BESCHREIBUNG                          |
|---------|-------------|--------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie die IconSize-Bits in die Spalte Attribute des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Wenn das [FixedSize-Bit](fixedsize-control-attribute.md) nicht festgelegt ist, wird das geladene Bild verkleinern oder gestreckt, um es an das Symbolsteuerelement anzupassen. Wenn das [FixedSize-Bit](fixedsize-control-attribute.md) festgelegt ist und das geladene Bild kleiner als das Symbolsteuerelement ist, wird das Bild im Steuerelement zentriert angezeigt. Wenn das [FixedSize-Bit](fixedsize-control-attribute.md) festgelegt ist und das geladene Bild größer als das Symbolsteuerelement ist, wird das Bild auf das Steuerelement reduziert.

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter [Steuerelemente](controls.md)erstellen müssen.

 

 



